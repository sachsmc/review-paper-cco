---
title: Statistical Principles for Omics-based Clinical Trials
author:
- name: Michael C Sachs
  affiliation: National Cancer Institute
  email: michael.sachs@nih.gov
- name: Lisa M McShane
  affiliation: National Cancer Institute
  email: McShaneL@CTEP.NCI.NIH.gov
date: September 2014
abstract: 'High-throughput techologies enable the measurement of a large number of molecular characteristics from a small tissue sample. High-dimensional molecular information (referred to as omics data) offers the possibility of predicting the future outcome of a patient (prognosis) and predicting the likely response to a specific treatment (prediction). Embedded in the vast amount of data is the hope that there exists some signal that will enable practicioners to deliver therapy personalized to the molecular profile of a tumor, thereby improving health outcomes. The challenges are to determine that the omics assays are valid and reproducible in a clinical setting, to develop a valid and optimal omics-based test that algorithmically determines the optimal treatment regime, to evaluate that test in a powerful and unbiased manner, and finally to demonstrate clinical utility: that the test under study improves clinical outcome as compared to not using the test. We review the statistical considerations involved in each of these stages, specifically dealing with the challenges of high-dimensional, omics data.'
keywords: genomics; personalized medidcine; predictive biomarker; statistics
...

Introduction
==============
Omics technolgies that generate a large amount of molecular data about a cancerous tumor have the potential to provide accurate predictions of a patient's prognosis and their response to a specific treatment regime. The idea of omics-based biomarkers is that distinct tumor types can be identified using the multi-dimensional molecular data leading to treatment decisions personalized to that tumor type. An omics-based test can guide the decisions to treat or not to treat and help identify the particular therapy most likely to work. The challenge is to identify and demonstrate definitively that the use of an omics-based decision rule improves clinical outcomes in a patient population.

The prognosis of a patient is their expected clinical outcome.  An omics-based test can be used to predict a patient's prognosis. A test that provides accurate predictions of prognosis, regardless of treatment, is referred to as a prognostic biomarker. A predictive omics-test is one that accurately predicts disease outcomes with the application of specific interventions. Predictive markers are therefore useful for the selection among two or more treatment options. Statistically, a prognostic test is strongly associated with clinical outcome and a predictive test modifies the association between treatment and clinical outcome (interaction). The two are not mutually exclusive, however. It is uncommon for a test to be purely predictive [@mcshane2013development], and prognostic tests can be used to inform treatment decisions. 

A patient's prognosis can be used to determine the type and intensity of medical treatment, or whether to treat at all. Endopredict [@filipits2011new] is an omics-based test test that is used to determine the likelihood of distant recurrence in ER-positive, HER2-negative breast cancer. The test has been shown to accurately predict prognosis, and is therefore useful for guiding treatment decisions, determining eligibility for trials, and making disease-management decisions. Endopredict as a prognostic test has been rigorously evaluated and shown to be clinically valid, even thought it does not predict response to any specific therapy. 

The goal of this paper is to review the path to definitively evaluating an omics-based test for prognosis or prediction of treatment response. We assume that the patient population is well-defined, and that there may exist targeted therapies for a subset of that population. High dimensional omics data can be used to identify specific molecular targets as potential mechnisms for drug development, however the use of omics technologies for drug development is beyond the scope of this review. 

The long road to implementing a test in a clinical trial starts with analytical validation, that is, demonstrating that the omics-based assay accurately and reproducibly measures the molecular quantities. After the assay performance is established comes the test development and preliminary evaluation. This involves reducing the high-dimensional data into a one-dimensional quantity that will be used to make a decision. This one-dimensional quantity is often a risk score: an estimate of the probability of a speicific clinical outcome. It is necessary to establish the clinical validity of this risk score, that is, demonstrate that the risk score is independently associated with clinical outcome. Care must be taken to completely separate the development of the risk score from the evaluation, otherwise estimates can be optimistically biased. Finally, the risk score must be translated into a binary decision, often using a threshold. It remains to demonstrate that the use of the test to make this decision improves patient outcomes. 


Analytical validation
============
Analytical validation of an assay involves evaluating the performance of the measurement in terms of accuracy, bias, and precision under a variety of conditions. Conditions are things like preanalytic factors such as specimen quality, specimen collection, storage, and processing procedures, and technical aspects such as laboratory technician and batch effects from reagent lots or other assay materials. The high-dimensional nature of omics data makes it very difficult to assess each of the hundreds or thousands of outputs from a single assay. In developing a omics-based signature that only uses a subset of the components of a high-dimensional assay, one can analytically validate the final signature alone. However, prior to developing the signature, one must develop detailed standard operating procedures for specimen handling and processing to ensure a baseline level of validity. 

Do: develop criteria for the rejection of poor-quality specimens. Percent tumor, necrosis, etc. 

Do: filter features based on QC prior to development

Do: assess the impact of sample and specimen handling. [@werner2000effect; @srinivasan2002effect; @van2008effects; @specht2001quantitative; @iwamoto1996feasibility]

Do: assess the impact of lots and batch effects. Bias, accuracy. [@pennello2013analytical; @isler2007analytical] 

Do: minimize the impact of technical aspects to greatest extent possible by developing detailed SOP. 

Test development and preliminary evaluation
============
Study design: consider retrospective [@simon2009use]

Don't: confound technical factors with clinical outcomes. [@leek2010tackling; @soneson2014batch]

Do: maintain strict separation between development and evaluation. 

Do: cross validation if you have a data-sparse setting. [@mcshane2013development; @moons2012riskI; @moons2012riskII; @polley2013statistical]

Don't: use convoluted methods leading to overfitting. 

Don't: do partial resubstitution

Compare: feature filtering based on association with outcome, regularization. [@bair2004semi; @hastie2009elements]

Do: consider all available methods, model averaging. Hard to determine best method in advance. 

Don't: rely on clustering to yield good predictions of outcome. 


Demonstrating clinical utility
===============
Do: define the clinical use [@mandrekar2010predictive]

Do: use a valid and interpretable statistical method appropriate to that use [@janes2014approach; @pepe2011problems; @hilden2013note]

Do: Design your study appropriately to answer the clinical question definitively [@freidlin2014biomarker; @baker2010designing; @baker2012biomarkers; @brannath2009confirmatory; @denne2014identifying; @eng2014randomized; @freidlin2010cross; @freidlin2012randomized; @freidlin2013marker; @jiang2007biomarker; @mandrekar2009clinical; @morita2014biomarker]

Do: Power your trial appropriately [@mackey2013sample; @peterson1993sample]

Don't: make these mistakes [@lee2008mistakes; @sargent2013statistical; @simon2003pitfalls]



Concluding remarks
===============
Do: follow reporting criteria [@bouwmeester2012reporting; @janssens2011strengthening; @mcshane2013criteria]



References
============
\setlength{\parindent}{0pt}