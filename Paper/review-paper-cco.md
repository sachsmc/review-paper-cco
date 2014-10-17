---
title: Statistical Principles for Omics-based Clinical Trials
author:
- name: Michael C Sachs
  affiliation: National Cancer Institute
  email: michael.sachs@nih.gov
date: October 2014
abstract: 'High-throughput technologies enable the measurement of a large number of molecular characteristics from a small tissue sample. High-dimensional molecular information (referred to as omics data) offers the possibility of predicting the future outcome of a patient (prognosis) and predicting the likely response to a specific treatment (prediction). Embedded in the vast amount of data is the hope that there exists some signal that will enable practitioners to deliver therapy personalized to the molecular profile of a tumor, thereby improving health outcomes. The challenges are to determine that the omics assays are valid and reproducible in a clinical setting, to develop a valid and optimal omics-based test that algorithmically determines the optimal treatment regime, to evaluate that test in a powerful and unbiased manner, and finally to demonstrate clinical utility: that the test under study improves clinical outcome as compared to not using the test. We review the statistical considerations involved in each of these stages, specifically dealing with the challenges of high-dimensional, omics data.'
keywords: genomics; personalized medicine; predictive biomarker; statistics
...

Introduction
==============
Omics technologies that generate a large amount of molecular data about a cancerous tumor have the potential to provide accurate predictions of a patient's prognosis and predictions of their response to a specific treatment regime. The idea of omics-based biomarkers is that distinct tumor types can be identified using the multi-dimensional molecular data leading to treatment decisions personalized to that tumor type. An omics-based test can guide the decisions to treat or not to treat and help identify the particular therapy most likely to work. The challenge is to identify and demonstrate definitively that the use of an omics-based test improves clinical outcomes in a patient population.

An omics-based test can be used to predict a patient's prognosis, which is their expected clinical outcome. A test that provides accurate predictions of prognosis, regardless of treatment, is referred to as a prognostic biomarker. A predictive omics test is one that accurately predicts disease outcomes with the application of specific interventions. Predictive markers are therefore useful for the selection among two or more treatment options. Statistically, a prognostic test is strongly associated with clinical outcome and a predictive test modifies the association between treatment and clinical outcome (interaction). High dimensional omics data can be used to identify specific molecular targets as potential mechanisms for drug development, however the use of omics technologies for drug development is beyond the scope of this review.

The path from development to definitively evaluating an omics-based test for prognosis or prediction of treatment response is long and arduous. Often, the end goal is to develop a test suitable for use in a clinical trial for guiding treatment. The oncology literature is full of reports that develop and/or evaluate omics-based tools for prognosis and prediction. Developing a simple test based on high-dimensional omics data can be complex and often uses novel statistical methods. Definitive evaluation of a prognostic or predictive test is costly and rife with methodological pitfalls. We aim to review such issues, giving you the resources to ask the right questions when critically weighing the evidence presented in a report of an omics-based study. Ultimately, as a practicing oncologist the question is: "Is this omics-based test something I want to use to improve patient care?".

The long road to implementing a test in a practice starts with analytical validation, that is, demonstrating that the omics-based assay accurately and reproducibly measures the molecular quantities. After the assay performance is established comes the test development and preliminary evaluation. This involves reducing the high-dimensional data into a one-dimensional quantity that will be used to make a decision. This one-dimensional quantity is often a risk score: an estimate of the probability of a specific clinical outcome. It is necessary to establish the clinical validity of this risk score, that is, demonstrate that the risk score is independently associated with clinical outcome. Care must be taken to completely separate the development of the risk score from the evaluation, otherwise estimates can be optimistically biased. Finally, the risk score must be translated into a binary decision, often using a threshold. It remains to demonstrate that the use of the test to make this decision improves patient outcomes. 

The following sections specify questions you should ask while reading a report of an omics-based clinical study. We review the importance of such questions, and common pitfalls to watch for. If you are reporting on an omics-based trial, answers to these questions should be made clear to the reader. Formal efforts to guide reporting have been developed, such as the REMARK checklist [@altman2012reporting], the GRIPS statement [@janssens2011strengthening], and a third guideline article that lacks an acronym [@mcshane2013criteria]. Our review reflects these efforts through the readers' lens. 

Terminology
==============
An omics-based test, or simple an **omics test**, is a mapping from the set of features on the omics assay to a single number. This number can be a binary value, such as good or poor prognosis, or it can provide a continuous scale, such as a risk score. It must be feasible to perform the test on an individual patient basis, by measuring the omics assay on the individual's tissue. The assay generates lots of measurements, which we will refer to as **features**, and then fixed mathematical calculations are done to transform the many features into the single test value. Examples of such features are gene expression values, protein expression measurements, or genomic mutations. 

Investigators determine the way that the mathematical calculations are done in the **development phase**. Often, there is a complete sample which is randomly allocated into **development** and **validation** samples. These are also sometimes referred to as **training** and **test** sets of samples. A report may cover only one of the two steps. At the end of the development phase, the model for the mathematical calculations is fixed and locked down.

That model is evaluated definitively in the **validation** phase in a completely independent sample. In order for the validation to be unbiased and definitive, it is imperative that no information from the validation sample leaks into the development phase. The validation should mimic realistic clinical use as much as possible, and that means that no further refinement to the test is allowed based on the observed results. 


What is the intended clinical use?
============

As with all clinical studies, the end goal is to improve patient care. Omics studies are no different, and a clear statement of the intended clinical use of the omics-test should be prominent. Carefully describing the context for the use of the assay determines the type of study needed to develop and validate it. The intended use of the assay also provides an overarching context in which to interpret the population under study, the assay measurements, and the statistical methods. 

Omics-based tests in oncology generally are used for one of two clinical purposes: prognostic or predictive. A **prognostic** test is used to predict the likely clinical outcome of a patient. What is the clinical use of such a prediction? Often a prognosis is used to guide management of the disease. Patients with a very good prognosis may opt not to receive any treatment, while patients with a poor prognosis may opt for more aggressive treatment. An omics-based  prognostic test that is currently used in practice is EndoPredict, which is used to predict recurrence in ER-positive, HER2-negative breast cancer [@filipits2011new]. For patients with a low risk of recurrence, it has been demonstrated that the risks of chemotherapy do not outweigh the benefits. Prognostic tests are clinically useful for guiding general disease management. 

**Predictive** tests are most useful for selecting patient populations for treatment with specific targeted therapies. This presumes the existence of a particular molecular targeted therapy. The predictive test is used to identify patients who will benefit from the targeted therapy. Predictive tests are generally based on only one or a few molecular characteristics that the therapy may target. For example, HER-2 is a gene that predicts a more aggressive form of breast cancer. Trastuzumab is a drug that specifically targets HER-2 and has been shown to be effective in HER-2 positive breast cancer [@fleeman2013pertuzumab]. While targeted therapies generally target only one molecular characteristic, omics assays can be used to identify molecular targets for less well-understood drugs. However, most successful targeted therapies have associated predictive tests that were developed based on the underlying biology rather than a broad search over a large number of molecular features [@sawyers2008cancer].



What is the patient population of interest?
===========
Along with the intended clinical use, a report should have a clear statement of the intended population in which the test is being evaluated. This could be broad or quite specific. For the omics test to be useful, it must provide sufficient information above and beyond the standard of care in the target patient population. The distribution of the omics test and the expected benefit in the population should be clearly specified in advance. 

The expected benefit of a new omics-based test could differ greatly by patient population. For instance, a prognostic test has more potential for benefit in stage 2 breast cancer than it does in stage 1 breast cancer, as the prognosis for stage 1 is already very good. Evaluating an omics-based test in a broad populations that encompasses multiple stages or multiple disease types can be difficult, as the test must provide more information beyond that provided by standard clinical and pathological factors. 


Is the omics assay valid?
===========
Analytical validation of an assay involves evaluating the performance of the measurement in terms of accuracy, bias, and precision under a variety of conditions. Conditions are things like pre-analytic factors such as specimen quality, specimen collection, storage, and processing procedures, and technical aspects such as laboratory technician and batch effects from reagent lots or other assay materials. The high-dimensional nature of omics data makes it very difficult to assess each of the hundreds or thousands of outputs from a single assay. In developing a omics-based signature that only uses a subset of the components of a high-dimensional assay, one can analytically validate the final signature alone. However, prior to developing the signature, one must develop detailed standard operating procedures for specimen handling and processing to ensure a baseline level of validity. 

Did the authors of the report state what type of specimens were used in the study? Can the test be applied to formalin-fixed paraffin embedded (FFPE) tissue, or only fresh-frozen? Most omics-based assays require a minimum percentage of tumor to be successful. A report should clearly state what criteria were used to screen tissue samples prior to running the assay. Generally this involves a criteria for the rejection of poor-quality specimens on the basis of percent tumor, percent necrosis, or some other marker of tissue quality. 

Molecular assays can successfully be run on decades old FFPE tissue [@iwamoto1996feasibility]. However, factors involved in the tissue processing and storage can impact the results [@srinivasan2002effect; @van2008effects; @specht2001quantitative]. Due to the high dimensionality of omics assays, a small amount of bias on each feature can translate into large errors when incorporating data from hundreds or thousands of features into a single continuous measurement. Therefore it is important to assess the impact of processing on the individual features in addition to the overall test. 

In addition to processing and storage, technical aspects of an assay can impact the final results in a predictable way [@pennello2013analytical; @isler2007analytical]. There could be technical effects, differences due to reagent lots, and other batch effects. Such batch effects are commonly recognized yet often ignored in high-dimensional assays [@leek2010tackling]. Efforts should be made to measure the impact of these technical aspects and minimize them to the greatest extent possible. The way in which samples are assayed should be randomized to prevent confounding batch effects with the clinical outcome. Development and validation samples are sometimes run in the same batch or with the same lot of technical aspects. This does minimize batch effects, however, it can provide an overly optimistic assessment of the test, because in clinical use, running things in the same batch is not an option. 

On what samples was the test developed?
============

Similar to developing criteria for rejection of tissue samples, in omics settings, criteria should be developed for the rejection of individual features (e.g. genes, proteins) prior to the development of the test. Features that do not pass the pre-specified quality metrics should be removed from consideration from the final test. Note that this feature processing step does not involve any clinical outcome measurements. As a concrete example, in the development of a gene expression based test, investigators may choose to exclude probe locations that have a dynamic range under some threshold, or probes for which only a small proportion of the samples had calls, or probes that have absolute expression levels below some threshold. Quality control steps like this can ensure a more robust a reproducible development of the test. 


Don't: confound technical factors with clinical outcomes. [@leek2010tackling; @soneson2014batch]

Do: maintain strict separation between development and evaluation. 

Do: cross validation if you have a data-sparse setting. [@mcshane2013development; @moons2012riskI; @moons2012riskII; @polley2013statistical]

Don't: use convoluted methods leading to overfitting. 


What does the omics-test do?
==============
Once the analytical validity of the omics assay is established, the features are translated into a binary classification, a multi-category classification, or a continuous risk score. Carefully evaluate the methods used to perform this translation and ask how are the features of the omics assay translated into a clinically meaningful quantity? 

Unfortunately, a common approach to developing prediction models is to use cluster analysis of omics features, ignoring the clinical outcome among the development samples. Cluster analysis is a class of methods that is used to partition samples into groups based on the similarities or differences among the omics features [@hastie2009elements]. The meaning and number groups are not known in advance, but rather they are data dependent. Clustering is unsupervised in the sense that the groups discovery is done ignoring the true groups defined by the clinical outcome. The resulting clusters are not designed to provide valid information regarding a prognosis or prediction of response to therapy [@simon2003pitfalls]. A common argument in favor of clustering is that it identifies biologically distinct groups. However, the groups are identified using a statistical algorithm and the biological relevance is only considered *post hoc*. For developing omics-based prognostic or predictive tests, it is better to use statistical methods which are designed to address those aims. 

Often, there are more features measured than there are patients in the sample. In such high-dimensional settings, it is required to identify a subset of the features that will be used in the final multivariate mathematical model. There are two broad statistical approaches to this problem: **filtering** and **regularization**. 

Filtering is a statistical approach where univariate methods are applied to each of the many omics features in turn. Typically, the univariate method involves estimating the association of the feature with the clinical outcome. Then, some criterion, which is chosen in advance or selected using cross-validation, is applied to the statistic to select a subset of features. For example, I am interested in developing a gene expression based test to predict clinical response to a new therapy. For each of the 1000 gene expression features that I have, I can compute a t-statistic comparing the expression levels for responders versus non-responders. I then filter out the genes with t-test p-values greater than 0.0001, and use the remaining ones in a multivariable logistic regression model to predict response. [@bair2004semi] describes a novel approach to filtering that is applied successfully to predict B-cell lymphoma subtypes using gene expression microarrays. 

Regularization is an approach where all of the features in consideration are entered into a special multivariable statistical model for prediction of the clinical outcome, even if there are more features than samples. The special model includes a penalty component which encourages the model to throw out or downplay the impact of features that are not relevant. There are various types of penalty functions each with different properties, such as the LASSO [@tibshirani1996regression], the ridge penalty [@hoerl1970ridge], the elastic net [@zou2005regularization], and others [@hastie2009elements]. Each type of penalty term contains at least one tuning parameter, which may be pre-specified or selected using cross-validation. 

Each type of approach has its merits, and within each class there are a variety of specific models to choose from. In real applications, it is hard to determine what method will work best in advance. Instead of selecting a single model to use, multiple models can be averaged to improve prediction [@hoeting1999bayesian]. This approach, called Bayesian model averaging has proven successful in different applications, including prediction of cancer subtypes [@yeung2005bayesian]. It is more common, however, to try out various different methods then select the one with the best performance. This is fine as long as the model selection is done entirely separated from the final validation sample. Leaking of information from the validation data into the model selection process can cause bias in insidious ways. Verify that the model selection and estimation process was done completely independently and locked down. 


On what samples is the test being evaluated?
===============
Do: define the clinical use [@mandrekar2010predictive]

Study design: consider retrospective [@simon2009use]

Do: Design your study appropriately to answer the clinical question definitively [@freidlin2014biomarker; @baker2010designing; @baker2012biomarkers; @brannath2009confirmatory; @denne2014identifying; @eng2014randomized; @freidlin2010cross; @freidlin2012randomized; @freidlin2013marker; @jiang2007biomarker; @mandrekar2009clinical; @morita2014biomarker]

Do: Power your trial appropriately [@mackey2013sample; @peterson1993sample]

Don't: do partial resubstitution

Are valid methods being used to evaluate the test?
===============
Bad: IDI or net reclassification [@hilden2013note; @pepe2011problems]

Bad: Comparing AUCs for regression models [@seshan2013comparing]

Good: comprehensive and pre-specified approach [@janes2014approach]

Are the development and evaluation samples strictly separated?
================
This issue has come up in previous sections, yet this error occurs so frequently that it needs to be highlighted in its own section. The evaluation sample for the assessment of a prognostic or predictive test needs to be completely independent from the development sample. This is especially true for omics-based tests, whose development is often complex and convoluted. Any information from the evaluation sample that leaks into the development sample can bias the results, making tests appear better than they truly are. 

Leaking information between samples can happen in subtle ways. Sometimes, part of the model development process is done on the validation data again. This is called partial resubstitution [@simon2003pitfalls]. For example, a common model development approach is to first filter a subset of 50 genes from a larger set of 450,000 based on their observed association with the outcome. Then, the 50 genes are put into a regression model to develop a single risk score. Occasionally, investigators will perform the filtering on the development sample and then re-estimate the regression model using the combined development and validation samples. This gives overly optimistic estimates of the performance of the algorithm. Partial resubstitution can be difficult to detect when the model development is more complex, and if cross-validation is used to estimate the performance. 

In settings where relatively few samples are available, cross-validation is an efficient and valid approach to estimating performance [@lee2008mistakes]. The key point whether using the split sample approach or cross validation is that the entire model building process must be validated. Even informal checks of the model on the validation sample, such as viewing survival curve plots, prior to locking down the model can unknowingly cause bias. Therefore, once again we highlight the imperative that the validation sample be strictly separated from the **entire** model development process. 



Concluding remarks
===============
Do: follow reporting criteria [@bouwmeester2012reporting; @janssens2011strengthening; @mcshane2013criteria; @altman2012reporting]



References
============
\setlength{\parindent}{0pt}