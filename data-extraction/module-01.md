# Module 01

This module was used in a dedicated ChatGPT conversation.
The headings below organise the original extraction instructions.

## Study aim

### Purpose

The Study aim field must concisely summarise the principal objective of the study.
The extracted value should capture what the authors intended to develop, propose, investigate, evaluate or validate, together with the targeted healthcare application and, when explicitly stated, the intended computational or deployment context.
This field provides a standardised description of the primary research objective while preserving the scientific meaning reported by the authors.

### General principles

Extract only the principal study objective explicitly stated by the authors.
Summarise the objective into one concise sentence beginning with:
•	To develop...
•	To propose...
•	To investigate...
•	To evaluate...
•	To validate...
•	To assess...
•	To compare...
•	To implement...
using the verb that best reflects the authors' stated objective.
Never infer objectives that are not explicitly reported.

### Reporting format

Use the following structure whenever applicable:
To <primary action> <main contribution> for <targeted healthcare application> using <biosound modality>, with <computational or deployment objective (if explicitly part of the study aim)>.
Not every component is mandatory.
Include only information explicitly forming part of the study objective.

### Information to preserve

Whenever explicitly stated, preserve:
•	the principal methodological contribution;
•	the targeted disorder or healthcare application;
•	the intended clinical purpose;
•	the biosound modality;
•	the intended deployment environment (mobile, wearable, edge, cloud, IoT, AIoT, telemedicine, etc.) when it constitutes part of the stated objective;
•	validation or feasibility objectives when they represent one of the primary aims.

### Information to omit

Do not include:
•	detailed methodology;
•	model architecture;
•	network topology;
•	feature extraction techniques;
•	optimisation algorithms;
•	dataset names;
•	participant numbers;
•	performance results;
•	validation protocols;
•	hardware specifications.
These belong to other extraction fields.

### Multiple study objectives

When several objectives are presented, report only the principal objective.
Secondary objectives should only be incorporated when they form an integral part of the overall research aim.
Avoid producing long lists of independent objectives.

### Wording harmonisation

Standardise the opening verb according to the principal contribution.
Examples:
Authors state:
We present...
Extract as:
To develop...
Authors state:
We introduce...
Extract as:
To propose...
Authors state:
We investigate...
Extract as:
To investigate...
Authors state:
We evaluate the feasibility...
Extract as:
To evaluate the feasibility...
Authors state:
We clinically validate...
Extract as:
To clinically validate...

### Deployment objective

Include the deployment or computational environment only when it is explicitly part of the study aim, for example:
•	smartphone-based screening;
•	mobile health;
•	wearable monitoring;
•	IoT;
•	AIoT;
•	cloud-based diagnosis;
•	edge computing;
•	telemedicine;
•	remote monitoring.
Do not add deployment information merely because the implementation uses these technologies.

### Preferred style

The extracted objective should:
•	consist of a single sentence;
•	begin with To;
•	use concise academic English;
•	preserve the principal contribution of the study;
•	avoid unnecessary methodological detail;
•	remain approximately one sentence in length.

### Examples

Correct
To develop an AI-powered smartphone-based screening tool for preliminary COVID-19 diagnosis from cough sounds, deployable anytime and anywhere through a cloud-connected mobile application.
To investigate the feasibility of fully automated speech-based screening for Alzheimer's disease and mild cognitive impairment using a self-administered mobile application and automatic speech analysis.
To develop and validate a lightweight Parkinson's disease speech-classification framework based on isolated-word analysis and novel articulation-related biomarkers, with potential deployment for smartphone-based home monitoring.
To develop and implement an energy-efficient FPGA-based machine learning system for real-time Parkinson's disease detection from voice signals, enabling portable and low-power diagnostic devices.

### Missing information

If the manuscript does not explicitly state the study objective:
Not reported.

### Final quality check

Before finalising, verify that:
•	the extracted sentence reflects the principal study objective;
•	it begins with To followed by the appropriate action verb;
•	only one concise objective is reported;
•	unnecessary methodological detail has been removed;
•	deployment information is included only when explicitly forming part of the study aim;
•	no results or conclusions are included;
•	the extracted objective faithfully represents the authors' stated aim without introducing additional interpretation.

## Targeted disorder / application domain

### Purpose

This field identifies the clinical disorder, health condition, functional impairment, or health-related application domain directly investigated in the study.
It answers only:
What disorder, condition, impairment, or health-related domain is targeted?
It must not describe:
•	the clinical purpose;
•	the machine-learning task;
•	the deployment setting;
•	the computational environment;
•	the type of monitoring;
•	the predicted clinical scale;
•	the study outcome.

### 1. General extraction rule

Report only the disorder, condition, impairment, or health-related application domain explicitly evaluated in the study.
Use the following structure:
Primary targeted condition; Additional explicitly evaluated condition(s)
Examples:
•	Parkinson’s disease
•	COVID-19
•	Alzheimer’s disease; Mild Cognitive Impairment
•	Depression; Anxiety; Suicide risk
•	Obstructive Sleep Apnoea; Central Sleep Apnoea
•	Amyotrophic Lateral Sclerosis; Dysarthria
•	Respiratory disease
•	Sleep quality
•	Emotion recognition
Do not append the clinical purpose.
Incorrect:
•	Parkinson’s disease; Severity assessment
•	COVID-19; Screening and monitoring
•	Depression; Risk assessment
•	Pneumonia; Diagnosis
•	Alzheimer’s disease; Cognitive screening
Correct:
•	Parkinson’s disease
•	COVID-19
•	Depression
•	Pneumonia
•	Alzheimer’s disease

### 2. Include only explicitly evaluated targets

Include a disorder or application domain only when it is directly addressed by:
•	the model;
•	the classification or regression task;
•	the study population;
•	the reported evaluation;
•	the principal study objective.
Do not include conditions mentioned only in:
•	the introduction;
•	the clinical motivation;
•	examples of possible use;
•	future work;
•	broader disease lists;
•	general discussion.
Example:
If a respiratory activity system is described as potentially applicable to COVID-19, asthma, and pertussis, but the study only classifies breathing, cough, and speech activities, extract:
Respiratory activity monitoring
Do not extract:
COVID-19; Asthma; Pertussis

### 3. Use the most specific supported diagnosis

Use the most specific condition explicitly supported by the study.
Preferred:
•	Parkinson’s disease
•	Idiopathic Pulmonary Fibrosis
•	Major Depressive Disorder
•	Obstructive Sleep Apnoea
•	Alzheimer’s disease
Avoid broader labels when a specific diagnosis is available.
Incorrect:
Neurological disorder
when the study evaluates only Parkinson’s disease.
Correct:
Parkinson’s disease
Use an umbrella category only when:
1.	multiple heterogeneous disorders are genuinely evaluated;
2.	the authors report only a broad diagnostic group; or
3.	the study target is the broader clinical domain rather than an individual disorder.
Examples:
•	Respiratory disease
•	Neurocognitive disorders
•	Chronic respiratory disease
•	Speech impairment
•	Mental health disorders

### 4. Do not include healthy controls

Healthy participants, healthy controls, normal recordings, or non-pathological classes are comparator groups, not targeted disorders.
Incorrect:
•	Asthma; Healthy controls
•	COPD; Pneumonia; Healthy subjects
•	Parkinson’s disease; Healthy controls
•	Normal; Crackles; Wheezes
Correct:
•	Asthma
•	COPD; Pneumonia
•	Parkinson’s disease
•	Adventitious respiratory sounds
Healthy or normal classes must be reported in the sample-composition or quantitative-results fields.

### 5. Distinguish disorders from acoustic event classes

Cough, snoring, crackles, wheezes, throat clearing, respiratory cycles, pauses, and speech segments are not automatically clinical disorders.
When the study targets a disease, report the disease.
Example:
A model classifying cough from COVID-19-positive and negative participants:
COVID-19
A model classifying crackles and wheezes without disease-level labels:
Adventitious respiratory sounds
A model recognising cough, breathing, and speech for general respiratory monitoring:
Respiratory activity monitoring
A model detecting Velcro crackles in patients with IPF:
Idiopathic Pulmonary Fibrosis; Velcro crackles

### 6. Separate disorders from application domains

Use a recognised clinical condition whenever the study directly evaluates one.
Use a broader application-domain label only when no specific disorder is the direct target.
Valid disorder examples:
•	COVID-19
•	Parkinson’s disease
•	Alzheimer’s disease
•	Major Depressive Disorder
•	Asthma
•	Chronic Obstructive Pulmonary Disease
•	Pneumonia
•	Obstructive Sleep Apnoea
Valid application-domain examples:
•	Stress
•	Emotion recognition
•	Sleep quality
•	Respiratory activity monitoring
•	Speech impairment
•	Voice pathology
•	Assistive communication
•	Cognitive impairment
•	Chronic cough
•	Sleep staging
Do not add general domains when a specific disorder already fully represents the target.
Incorrect:
Parkinson’s disease; Neurological disorder
Correct:
Parkinson’s disease

### 7. Multiple conditions

List multiple conditions only when each one is explicitly evaluated.
Use semicolons.
Examples:
•	Alzheimer’s disease; Mild Cognitive Impairment
•	Depression; Anxiety
•	Obstructive Sleep Apnoea; Central Sleep Apnoea
•	COVID-19; Influenza A; Influenza B; Respiratory Syncytial Virus infection
•	COPD; Pneumonia; Bronchiectasis; Upper Respiratory Tract Infection
Do not include conditions merely because they occur in the dataset unless the study evaluates them separately or includes them in the target classification.

### 8. Broad disease families

When a study includes many related conditions and the analytical target is the broader family, use an umbrella label.
Examples:
•	Respiratory disease
•	Chronic respiratory disease
•	Neurocognitive disorders
•	Mental health disorders
•	Sleep-related disorders
However, retain individual diseases when they correspond to explicit output classes or separate analyses.
Example:
If the model distinguishes COPD, pneumonia, bronchiectasis, and URTI, use:
Chronic Obstructive Pulmonary Disease; Pneumonia; Bronchiectasis; Upper Respiratory Tract Infection
If the model performs only general abnormal-versus-normal respiratory classification, use:
Respiratory disease

### 9. Functional impairments and symptoms

Include a symptom or functional impairment when it is itself the direct target of the study.
Examples:
•	Dysarthria
•	Freezing of Gait
•	Chronic cough
•	Snoring
•	Speech impairment
•	Cognitive impairment
•	Respiratory activity
•	Sleep quality
•	Stress
•	Emotion recognition
When both a disease and an associated impairment are directly evaluated, both may be included.
Examples:
•	Amyotrophic Lateral Sclerosis; Dysarthria
•	Parkinson’s disease; Freezing of Gait
•	Idiopathic Pulmonary Fibrosis; Velcro crackles
•	Parkinson’s disease; Dysarthria
Do not include associated symptoms that are merely input features or background manifestations.

### 10. Exclude clinical purpose and setting

Do not include:
•	Diagnosis
•	Detection
•	Screening
•	Monitoring
•	Severity assessment
•	Progression monitoring
•	Prognosis
•	Risk assessment
•	Remission assessment
•	Telemonitoring
•	Remote diagnosis
•	Home monitoring
•	Clinical decision support
•	Point-of-care screening
•	Post-hospitalisation follow-up
•	Vulnerable-population monitoring
These concepts belong in other extraction fields.
Example:
Original:
Parkinson’s disease; remote diagnosis; disease progression monitoring
Harmonised:
Parkinson’s disease
Original:
COVID-19; pandemic infection detection; remote respiratory disease screening
Harmonised:
COVID-19
Original:
Pneumonia risk detection and monitoring
Harmonised:
Pneumonia

### 11. Exclude clinical scales and outcome variables

Do not include clinical scores, scales, or predicted variables.
Remove:
•	UPDRS
•	Motor-UPDRS
•	Total-UPDRS
•	AHI
•	PHQ-9
•	DASS-21
•	MMSE
•	cognitive scores
•	symptom severity scores
•	remission status
•	pulmonary function values
Examples:
Original:
Parkinson’s disease; Motor-UPDRS and Total-UPDRS prediction
Harmonised:
Parkinson’s disease
Original:
Obstructive Sleep Apnoea severity assessment; AHI estimation
Harmonised:
Obstructive Sleep Apnoea

### 12. Harmonised terminology

Use British English and consistent disease naming.
Preferred terminology:
Respiratory and infectious conditions
•	COVID-19
•	Influenza-like illness
•	Influenza A
•	Influenza B
•	Respiratory Syncytial Virus infection
•	Asthma
•	Chronic Obstructive Pulmonary Disease
•	Pneumonia
•	Bronchiectasis
•	Bronchiolitis
•	Pulmonary fibrosis
•	Idiopathic Pulmonary Fibrosis
•	Cystic fibrosis
•	Pertussis
•	Croup
•	Upper Respiratory Tract Infection
•	Lower Respiratory Tract Infection
•	Chronic respiratory disease
•	Respiratory disease
•	Chronic cough
•	Respiratory activity monitoring
•	Adventitious respiratory sounds
•	Velcro crackles
Neurological and neurocognitive conditions
•	Parkinson’s disease
•	Alzheimer’s disease
•	Mild Cognitive Impairment
•	Subjective Cognitive Decline
•	Dementia
•	Cognitive impairment
•	Amyotrophic Lateral Sclerosis
•	Huntington’s disease
•	Cerebral palsy
•	Stroke-related impairment
•	Traumatic Brain Injury
•	Dysarthria
•	Apraxia of speech
•	Neurogenic speech impairment
•	Voice pathology
Mental-health and affective conditions
•	Major Depressive Disorder
•	Depression
•	Anxiety
•	Generalised Anxiety Disorder
•	Suicide risk
•	Attention-Deficit/Hyperactivity Disorder
•	Stress
•	Emotion recognition
•	Mental health disorders
Sleep-related conditions and domains
•	Obstructive Sleep Apnoea
•	Central Sleep Apnoea
•	Sleep-disordered breathing
•	Insomnia
•	Sleep quality
•	Sleep staging
•	Snoring
•	Nocturnal sleep sounds
Functional and assistive domains
•	Assistive communication
•	Speech impairment
•	Respiratory activity monitoring
•	Cognitive impairment
•	Voice pathology
•	Human–robot interaction

### 13. Capitalisation and abbreviations

Use consistent capitalisation.
Preferred:
•	Parkinson’s disease
•	Alzheimer’s disease
•	Major Depressive Disorder
•	Mild Cognitive Impairment
•	Chronic Obstructive Pulmonary Disease
Use abbreviations only when necessary for clarity or dataset consistency.
Preferred:
Chronic Obstructive Pulmonary Disease (COPD)
or simply:
Chronic Obstructive Pulmonary Disease
Do not alternate between:
•	Parkinson’s Disease
•	Parkinson’s disease
•	PD
Use one harmonised form throughout the dataset.
Use:
•	Obstructive Sleep Apnoea, not Obstructive Sleep Apnea
•	Central Sleep Apnoea, not Central Sleep Apnea
•	Generalised Anxiety Disorder, not Generalized Anxiety Disorder

### 14. Formatting rules

1.	Use semicolons to separate distinct targeted conditions.
2.	Do not use full stops.
3.	Do not include long explanatory clauses.
4.	Do not include classification labels in parentheses.
5.	Do not include healthy controls.
6.	Do not include datasets, devices, algorithms, settings, or deployment terms.
7.	Do not include the clinical purpose.
8.	Prefer one to three concepts whenever possible.
9.	Use more than three conditions only when each is an explicit analytical target.
10.	Do not infer a diagnosis that is not explicitly reported.

### 15. Decision procedure

For each study:
1.	Identify the disease, impairment, or health domain directly evaluated.
2.	Remove healthy and normal comparator groups.
3.	Remove diagnosis, screening, monitoring, prognosis, severity, and risk terminology.
4.	Remove devices, clinical settings, computational environments, and deployment descriptions.
5.	Remove clinical scales and predicted scores.
6.	Remove diseases mentioned only as examples or future applications.
7.	Retain multiple diseases only when each is explicitly modelled or evaluated.
8.	Replace unnecessarily broad categories with specific diagnoses when supported.
9.	Use an umbrella category when the study genuinely targets a broad family of conditions.
10.	Return a concise semicolon-separated value.

### 16. Harmonisation examples

Original value	Harmonised value
COVID-19 diagnosis	COVID-19
COVID-19 screening and monitoring; acoustic cough profile classification	COVID-19
Bulbar-onset Amyotrophic Lateral Sclerosis; dysarthria monitoring	Amyotrophic Lateral Sclerosis; Dysarthria
Student stress monitoring	Stress
Parkinson’s Disease	Parkinson’s disease
Alzheimer’s Disease and Mild Cognitive Impairment	Alzheimer’s disease; Mild Cognitive Impairment
Depression; Anxiety; Suicide risk	Depression; Anxiety; Suicide risk
Obstructive Sleep Apnoea / Snoring monitoring and suppression	Obstructive Sleep Apnoea; Snoring
Chronic cough monitoring; respiratory disease monitoring	Chronic cough; Respiratory disease
COVID-19 prognosis; hospital patient monitoring	COVID-19
Pneumonia; COPD; respiratory disease screening	Pneumonia; Chronic Obstructive Pulmonary Disease
Asthma detection using lung sound recordings	Asthma
Cough classification; COVID-19-related cough; wet cough; dry cough	COVID-19
Depression detection in adolescents	Depression
Influenza-like illnesses, including COVID-19	Influenza-like illness; COVID-19
Sleep quality monitoring; sleep disorders; OSA	Sleep quality; Sleep-related disorders; Obstructive Sleep Apnoea
Parkinson’s disease; Freezing of Gait	Parkinson’s disease; Freezing of Gait
Parkinson’s disease progression monitoring	Parkinson’s disease
Depression risk assessment; depression screening	Depression
Child stress-state identification	Stress
Major Depressive Disorder; remission/non-remission detection	Major Depressive Disorder
Sleep-disordered breathing; OSA severity assessment; sleep staging	Sleep-disordered breathing; Obstructive Sleep Apnoea; Sleep staging
Human–Robot Interaction; emotion recognition; stress management; mental health support	Emotion recognition; Stress; Human–robot interaction
Parkinson’s disease; severity assessment; telemonitoring; UPDRS prediction	Parkinson’s disease
Respiratory diseases including healthy controls	Respiratory disease
COVID-19; respiratory infections; remote symptom monitoring	COVID-19; Respiratory infection
Neurocognitive disorders; SCD; MCI; Dementia; Alzheimer’s disease	Subjective Cognitive Decline; Mild Cognitive Impairment; Dementia; Alzheimer’s disease
Childhood mental health disorders; Anxiety; Depression; ADHD	Anxiety; Depression; Attention-Deficit/Hyperactivity Disorder
Respiratory disease screening; Normal, Crackles, Wheezes	Adventitious respiratory sounds
Alzheimer’s disease; MCI; cognitive impairment screening	Alzheimer’s disease; Mild Cognitive Impairment
Respiratory activity monitoring; potential COVID-19, asthma and pertussis screening	Respiratory activity monitoring
Idiopathic Pulmonary Fibrosis; Velcro crackle detection	Idiopathic Pulmonary Fibrosis; Velcro crackles
Emotion recognition; driver stress detection; human–robot interaction	Emotion recognition; Stress; Human–robot interaction
Pneumonia risk detection and monitoring	Pneumonia
Assistive communication; dysarthria, apraxia, neurogenic speech disorders	Assistive communication; Speech impairment
Traumatic Brain Injury; Depression	Traumatic Brain Injury; Depression

## Clinical or functional purpose

### Purpose

This field describes the exact clinical or health-related function performed by the proposed machine-learning system.
It must allow the reader to understand:
1.	what the system detects, distinguishes, estimates, predicts, or monitors;
2.	which clinical groups, event classes, severity levels, or outcomes are involved;
3.	how the reported Primary ML task and Quantitative ML result(s) relate to the healthcare objective.
This field answers:
What is the machine-learning system intended to determine, and between which clinical states, groups, events, or outcome levels?

### Relationship with other fields

Field	Question answered
Targeted disorder / application domain	What disorder, impairment, or health-related domain is studied?
Clinical or functional purpose	What exactly does the system determine within that domain?
Primary ML task	What formal machine-learning task is performed?
Quantitative ML result(s)	How well does the system perform that task?
Example
Targeted disorder / application domain
COVID-19
Clinical or functional purpose
Detection of COVID-19 by distinguishing participants with confirmed COVID-19 from non-COVID-19 controls
Primary ML task
Binary classification
Quantitative ML result(s)
COVID-19 positive vs non-COVID-19: Accuracy = 92%; Sensitivity = 90%; Specificity = 94%

### 1. General extraction rule

Report the specific clinical or functional objective of the machine-learning system, including the evaluated groups, classes, events, severity levels, or outcome variable whenever these are explicitly reported.
Use the following general structure:
Action + clinical or functional target + evaluated classes or outcome
Examples:
•	Detection of COVID-19 by distinguishing COVID-19-positive participants from non-COVID-19 controls
•	Detection of Parkinson’s disease by distinguishing participants with Parkinson’s disease from healthy controls
•	Classification of respiratory cycles as normal, crackles, wheezes, or combined crackles and wheezes
•	Differentiation of obstructive from central respiratory events during sleep
•	Estimation of Parkinson’s disease severity from voice recordings using Motor-UPDRS and Total-UPDRS scores
•	Detection and severity classification of depression from speech
•	Recognition of cough, breathing, speech, and other nocturnal sound events
•	Isolation of the target speaker from overlapping or interfering speech
•	Prediction of pneumonia risk from cough, physiological, and clinical data

### 2. The field must be clinically or functionally explicit

Avoid generic descriptions such as:
•	Disease detection
•	Respiratory classification
•	Speech analysis
•	Health monitoring
•	Screening
•	Diagnosis
•	Event recognition
These are insufficient because they do not indicate what is being distinguished or estimated.
Preferred:
•	Detection of asthma by distinguishing participants with asthma from healthy controls
•	Classification of respiratory sounds as normal, crackles, wheezes, or combined adventitious sounds
•	Detection of depression by distinguishing depressed from non-depressed participants
•	Classification of sleep stages as wake, NREM, or REM
•	Detection of nocturnal cough and snoring events

### 3. Include the comparison groups or output classes

For classification studies, state the evaluated classes whenever explicitly reported.
Binary classification
Use:
Detection or differentiation of X by distinguishing A from B
Examples:
•	Detection of COVID-19 by distinguishing COVID-19-positive from COVID-19-negative participants
•	Detection of Parkinson’s disease by distinguishing participants with Parkinson’s disease from healthy controls
•	Differentiation of Subjective Cognitive Decline from Mild Cognitive Impairment or dementia
•	Differentiation of obstructive from central respiratory events
•	Detection of dysarthric speech by distinguishing dysarthric from healthy speech
•	Detection of pneumonia by distinguishing pneumonia from non-pneumonia cases
Do not write only:
•	COVID-19 detection
•	Parkinson’s disease detection
•	Dysarthria classification
when the class comparison is known.

### Multiclass classification

List the clinically meaningful output classes.
Examples:
•	Classification of respiratory sounds as normal, crackles, wheezes, or combined crackles and wheezes
•	Classification of respiratory disease as COPD, pneumonia, bronchiectasis, URTI, or healthy
•	Classification of cognitive status as Alzheimer’s disease, Mild Cognitive Impairment, or cognitively healthy
•	Classification of depression severity as healthy, mild, moderate, moderately severe, or severe
•	Recognition of cough, breathing, speech, sneezing, snoring, sniffing, laughter, or other nocturnal sounds
Avoid reproducing an excessively long class list when the classes can be represented by a clear umbrella expression.
Example:
Classification of nine cough phenotypes
may be used if all individual classes are already reported in the quantitative-results field and the complete list would make this field unnecessarily long.

### 4. Regression and continuous-outcome studies

For regression studies, identify the exact estimated variable.
Examples:
•	Estimation of Parkinson’s disease severity using Motor-UPDRS and Total-UPDRS scores
•	Estimation of Apnoea–Hypopnoea Index from overnight breathing sounds
•	Prediction of cognitive assessment scores from spontaneous speech
•	Estimation of depression severity from acoustic and lexical speech features
•	Prediction of pulmonary function from respiratory sounds
•	Estimation of sleep quality level from nocturnal sounds
Do not write only:
•	Severity assessment
•	Score prediction
•	Regression analysis

### 5. Detection and monitoring must be distinguished

Use detection when the system determines whether a condition, event, or state is present.
Examples:
•	Detection of COVID-19 from cough recordings
•	Detection of Velcro crackles in respiratory sounds
•	Detection of nocturnal snoring events
Use monitoring only when repeated, continuous, longitudinal, or ongoing assessment is actually part of the system objective.
Examples:
•	Longitudinal monitoring of Parkinson’s disease progression through repeated voice recordings
•	Continuous monitoring of cough and respiratory events
•	Monitoring of sleep quality across overnight recordings
Do not use monitoring merely because the paper mentions potential future home or remote use.

### 6. Event-level and signal-level purposes

Some studies do not diagnose a disease directly but identify clinically relevant sound or speech events.
These must be reported as functional purposes.
Examples:
•	Detection of cough events in continuous audio
•	Classification of respiratory cycles as normal or adventitious
•	Recognition of cough, throat-clearing, and breathing events
•	Detection of apnoea and hypopnoea events
•	Classification of sleep stages
•	Detection of pause events in spontaneous speech
•	Target-speaker isolation from speech containing crosstalk
•	Recognition of dysarthric speech utterances
•	Classification of emotional states from speech
Do not force these studies into disease-detection wording when the model does not actually diagnose a disorder.

### 7. Disease detection versus sound-event classification

The field must reflect the actual prediction target.
Example A — Disease detection
The model uses cough recordings labelled by COVID-19 status.
Use:
Detection of COVID-19 by distinguishing COVID-19-positive from COVID-19-negative participants
Example B — Cough-type classification
The model classifies dry cough, wet cough, pertussis cough, or croup cough without predicting patient diagnosis.
Use:
Classification of cough sounds by cough type
Example C — Respiratory sound classification
The model classifies normal, crackles, and wheezes.
Use:
Classification of respiratory cycles as normal, crackles, wheezes, or combined adventitious sounds
Do not report:
Respiratory disease diagnosis
unless a disease-level label is actually predicted.

### 8. Screening, diagnosis, and risk prediction

Use terminology conservatively.
Detection
Use when the model distinguishes presence versus absence of a condition.
Detection of Parkinson’s disease by distinguishing affected participants from healthy controls
Screening
Use when the authors explicitly frame the system as identifying individuals who may require further clinical assessment.
Screening for clinically significant Obstructive Sleep Apnoea using an AHI threshold of ≥15 events/hour
Diagnosis
Use only when the paper explicitly presents the model as a diagnostic system and evaluates disease-level diagnosis.
Diagnosis of COPD by distinguishing COPD from asthma and other respiratory conditions
Risk prediction
Use when the model estimates future risk or probability rather than current disease status.
Prediction of pneumonia risk from cough and physiological measurements
Do not automatically replace “classification” with “diagnosis”.

### 9. Severity, progression, prognosis, and treatment response

Report these as distinct clinical purposes when explicitly evaluated.
Examples:
•	Assessment of Parkinson’s disease severity from voice
•	Prediction of Motor-UPDRS and Total-UPDRS scores
•	Classification of depression severity into five clinical levels
•	Monitoring of Parkinson’s disease progression
•	Prediction of COVID-19 prognosis in hospitalised patients
•	Prediction of depression remission status
•	Differentiation of Parkinson’s disease patients with and without Freezing of Gait
•	Assessment of dysarthria severity
•	Classification of sleep apnoea severity
Do not merge these purposes into generic disease detection.

### 10. Multiple clinical purposes

When a study performs more than one clinically distinct task, report each purpose separated by a semicolon.
Examples:
•	Detection of Obstructive Sleep Apnoea using AHI ≥15 events/hour; Estimation of Apnoea–Hypopnoea Index
•	Detection of Parkinson’s disease; Estimation of disease severity using UPDRS scores
•	Classification of cognitive status; Prediction of cognitive assessment scores
•	Detection of depression; Classification of depression severity
•	Recognition of respiratory activities; Detection of asthma
•	Target-speaker isolation; Improvement of downstream traumatic brain injury and depression assessment
Only include purposes that were actually evaluated.

### 11. Do not include technical implementation details

Do not include:
•	algorithm names;
•	feature sets;
•	model architectures;
•	datasets;
•	devices;
•	cloud, edge, fog, or federated terminology;
•	validation schemes;
•	performance metrics.
Incorrect:
COVID-19 detection using ResNet on Mel-spectrograms collected with smartphones
Correct:
Detection of COVID-19 by distinguishing COVID-19-positive from COVID-19-negative participants
The technical details belong in:
•	Feature sets
•	Applied ML techniques
•	Proposed ML algorithm
•	Computational infrastructure
•	Architectural deployment strategy

### 12. Do not include the general application setting

Do not include:
•	home monitoring;
•	telemedicine;
•	point-of-care;
•	hospital screening;
•	remote diagnosis;
•	mobile health;
•	sleep laboratory;
•	primary care.
These belong in Clinical setting.
Incorrect:
Remote home detection of Parkinson’s disease
Correct:
Detection of Parkinson’s disease by distinguishing affected participants from healthy controls

### 13. Do not infer unreported classes

Use only the classes, groups, events, or outcomes explicitly reported.
If the article states only that it performs “respiratory disease classification” and the disease classes are not given, use:
Classification of respiratory disease
Do not infer:
Classification of COPD, asthma, pneumonia, and bronchiectasis
If the negative or comparator class is unclear, use:
Detection of COVID-19 from cough recordings
rather than inventing:
COVID-19-positive versus healthy controls

### 14. Harmonised action vocabulary

Use one or more of the following terms:
•	Detection of
•	Differentiation of
•	Classification of
•	Recognition of
•	Estimation of
•	Prediction of
•	Assessment of
•	Monitoring of
•	Screening for
•	Isolation of
•	Segmentation of
•	Identification of
Avoid inconsistent synonyms such as:
•	spotting;
•	discovery;
•	diagnosis prediction;
•	health identification;
•	patient recognition.

### 15. Relationship with Primary ML task

The field must be semantically consistent with Primary ML task.
Clinical or functional purpose	Primary ML task
Detection of COVID-19-positive versus negative participants	Binary classification
Classification of normal, crackles, wheezes, and combined sounds	Multiclass classification
Estimation of AHI	Regression
Classification of depression severity into five levels	Ordinal or multiclass classification
Prediction of UPDRS score	Regression
Detection of cough events in continuous audio	Event detection
Isolation of target speech from crosstalk	Source separation
Classification of sleep stages	Multiclass classification
Recognition of spoken commands	Speech recognition
If these fields do not align, the extraction must be reviewed.

### 16. Relationship with Quantitative ML result(s)

The clinical or functional purpose must provide the context required to interpret the reported metrics.
Example:
Clinical or functional purpose
Detection of Parkinson’s disease by distinguishing participants with Parkinson’s disease from healthy controls
Quantitative ML result(s)
Parkinson’s disease vs healthy controls: Accuracy = 94%; Sensitivity = 92%; Specificity = 95%
The wording of the result must use the same clinical classes whenever possible.
For regression:
Clinical or functional purpose
Estimation of Motor-UPDRS and Total-UPDRS scores
Quantitative ML result(s)
Motor-UPDRS: RMSE = 2.39, R² = 0.91; Total-UPDRS: RMSE = 8.33, R² = 0.90

### 17. Final formatting rules

1.	Begin with a harmonised action term.
2.	Identify the clinical or functional target.
3.	Include comparison groups, classes, events, or outcome variables when reported.
4.	Use semicolons for multiple purposes.
5.	Do not end with a full stop.
6.	Do not include algorithms, datasets, devices, settings, validation methods, or metrics.
7.	Do not use vague phrases such as health assessment or disease monitoring.
8.	Do not infer unreported clinical labels.
9.	Keep the value concise but sufficiently explicit to interpret the ML task and results.
10.	Use British English.

### 18. Examples based on the review dataset

Targeted disorder / application domain	Clinical or functional purpose	Primary ML task
COVID-19	Detection of COVID-19 by distinguishing COVID-19-positive from COVID-19-negative participants	Binary classification
Parkinson’s disease	Detection of Parkinson’s disease by distinguishing affected participants from healthy controls	Binary classification
Parkinson’s disease	Estimation of Motor-UPDRS and Total-UPDRS scores from voice recordings	Regression
Alzheimer’s disease; Mild Cognitive Impairment	Classification of cognitive status as Alzheimer’s disease, Mild Cognitive Impairment, or cognitively healthy	Multiclass classification
Subjective Cognitive Decline; Mild Cognitive Impairment; Dementia	Differentiation of Subjective Cognitive Decline from Mild Cognitive Impairment or dementia	Binary classification
Obstructive Sleep Apnoea	Screening for clinically significant Obstructive Sleep Apnoea using AHI ≥15 events/hour; Estimation of AHI	Binary classification; Regression
Obstructive Sleep Apnoea; Central Sleep Apnoea	Differentiation of obstructive from central respiratory events	Binary classification
Respiratory disease	Classification of respiratory cycles as normal, crackles, wheezes, or combined crackles and wheezes	Multiclass classification
Idiopathic Pulmonary Fibrosis; Velcro crackles	Detection of Velcro crackles; Classification of respiratory sounds as normal, Velcro crackles, or other abnormalities	Binary classification; Multiclass classification
Depression	Detection of depression by distinguishing depressed from non-depressed participants	Binary classification
Depression	Classification of depression severity as healthy, mild, moderate, moderately severe, or severe	Multiclass classification
Anxiety; Depression; ADHD	Independent detection of anxiety, depression, and ADHD	Multiple binary classification tasks
Sleep quality	Classification of sleep quality into five ordered categories	Multiclass classification
Sleep staging	Classification of sleep epochs as wake, NREM, or REM	Multiclass classification
Respiratory activity monitoring	Recognition of breathing, cough, and speech activities	Multiclass classification
Nocturnal sleep sounds	Recognition of cough, laughter, screaming, sneezing, snoring, sniffing, and flatulence sounds	Multiclass classification
Dysarthria	Detection of dysarthric speech by distinguishing dysarthric from healthy speech	Binary classification
Traumatic Brain Injury; Depression	Isolation of target speech from crosstalk to improve downstream traumatic brain injury and depression assessment	Source separation
Assistive communication; Speech impairment	Recognition of an 11-class spoken vocabulary from acoustic speech and EEG signals	Multiclass recognition
Emotion recognition	Classification of emotional states from speech and mmWave signals	Multiclass classification

## Study type

### Purpose

This field describes the scientific study design used to generate, collect, analyse, or validate the evidence reported in the article.
It answers:
How was the scientific evidence generated?
It must not describe:
•	the algorithm, model, framework, platform, application or hardware developed;
•	the computational or deployment architecture;
•	the machine-learning task;
•	the technological maturity of the implementation;
•	the deployment readiness of the system.
These aspects are captured by other extraction fields (e.g., Deployment maturity, Deployment level, Computing paradigm).

### Allowed taxonomy

Use one primary study design and, when explicitly supported, one or more complementary study-design qualifiers.
Primary study design
•	Experimental study
•	Observational study
•	Diagnostic accuracy study
•	Clinical validation study
•	Benchmarking study
Complementary study-design qualifiers
•	Case-control
•	Cross-sectional
•	Longitudinal
•	Prospective
•	Retrospective
•	Multi-centre
•	Comparative

### Output format

Use
Primary study design; Complementary qualifier(s)
Examples
Experimental study

Experimental study; Comparative

Clinical validation study; Prospective

Clinical validation study; Multi-centre

Observational study; Longitudinal

Diagnostic accuracy study; Case-control

Benchmarking study; Comparative

Observational study; Prospective; Longitudinal
Use no more than three elements unless the study design genuinely requires additional clarification.

### Classification rules

#### Rule 1 — Describe the scientific design

This field must describe how scientific evidence was generated, not how the technology was implemented.
Incorrect
•	Framework development
•	System development
•	Platform development
•	Prototype development
•	Hardware implementation
•	Mobile application
•	Wearable implementation
Correct
•	Experimental study
•	Clinical validation study
•	Observational study
•	Benchmarking study

#### Rule 2 — Experimental study

Use Experimental study when the authors develop, train, validate or compare machine-learning methods under controlled analytical conditions.
This is the default category for most papers.
Typical examples include
•	developing a CNN;
•	comparing classifiers;
•	evaluating feature representations;
•	testing ensemble models;
•	validating a new architecture using public or private datasets.
Do not include
•	algorithm development;
•	model development;
•	framework development.

#### Rule 3 — Benchmarking study

Use Benchmarking study only when systematic comparison is itself the principal objective.
Typical examples
•	comparison of several ML algorithms;
•	comparison of multiple datasets;
•	comparison of feature representations;
•	comparison of computational platforms;
•	comparison of validation strategies.
Do not use Benchmarking merely because the proposed method is compared against several baselines.

#### Rule 4 — Diagnostic accuracy study

Use Diagnostic accuracy study only when the paper explicitly evaluates diagnostic performance against an accepted clinical reference standard.
Typical reference standards include
•	polysomnography;
•	RT-PCR;
•	neurologist diagnosis;
•	psychiatrist diagnosis;
•	radiologist assessment;
•	validated clinical questionnaires;
•	biomarker-confirmed diagnosis.
Do not classify every disease-classification paper as a diagnostic accuracy study.

#### Rule 5 — Clinical validation study

Use Clinical validation study when the model is evaluated using clinically recruited participants, prospectively collected patient data, or real clinical workflows.
Typical examples
•	memory clinics;
•	hospital recruitment;
•	sleep laboratories;
•	outpatient clinics;
•	clinical telemonitoring programmes.
Clinical validation is stronger than simple algorithm evaluation using public datasets.

#### Rule 6 — Observational study

Use Observational study when researchers analyse naturally occurring clinical or behavioural data without introducing an experimental intervention.
Typical qualifiers include
•	Cross-sectional
•	Longitudinal
•	Prospective
•	Retrospective
Examples
•	passive smartphone monitoring;
•	smartwatch monitoring during daily life;
•	repeated home recordings;
•	routinely collected clinical speech.

#### Rule 7 — Case-control

Use Case-control only when participants are explicitly recruited as clinically defined cases and controls.
Do not assign this qualifier simply because a dataset contains positive and negative labels.

#### Rule 8 — Cross-sectional

Use Cross-sectional when each participant contributes data from a single assessment time point.
Multiple recordings acquired during the same session do not constitute longitudinal follow-up.

#### Rule 9 — Longitudinal

Use Longitudinal only when repeated measurements from the same participants are collected over time to analyse progression, monitoring, follow-up or temporal evolution.
Do not infer longitudinal design merely because participants contribute multiple recordings.

#### Rule 10 — Prospective

Use Prospective only when participant recruitment and data collection follow a predefined forward-looking protocol.
Do not infer prospective design simply because the data were newly collected.

#### Rule 11 — Retrospective

Use Retrospective only when the study explicitly analyses previously collected clinical records or archived datasets.
Public datasets should not automatically be labelled retrospective.

#### Rule 12 — Multi-centre

Use Multi-centre only when participants are recruited or clinically evaluated across two or more independent healthcare institutions.
Using multiple public datasets alone does not constitute a multi-centre study.

#### Rule 13 — Comparative

Use Comparative only when comparison itself represents one of the principal scientific objectives.
Typical examples
•	unimodal versus multimodal models;
•	controlled versus uncontrolled recordings;
•	local versus cloud inference;
•	different sensing modalities;
•	different acquisition protocols.
Do not assign Comparative simply because baseline models are reported.

### Explicit exclusions

The following terms must never appear in this field because they describe technological maturity rather than scientific study design:
•	Feasibility study
•	Pilot study
•	Simulation study
•	Prototype development
•	Framework development
•	Platform development
•	Algorithm development
•	System development
•	Hardware implementation
•	Real-wordl
These concepts are already captured by:
•	Deployment maturity
•	Deployment level
and therefore must not be duplicated.

### Conservative classification

When the study design cannot be classified more specifically, use
Experimental study
rather than inferring additional design labels.

### Final decision hierarchy

1.	Identify the scientific study design.
2.	Add only explicitly supported study-design qualifiers.
3.	Ignore implementation details, deployment architecture and hardware.
4.	Do not encode technological maturity in this field.
5.	When uncertain, classify as:
Experimental study

## Database field

### Purpose

The Database field must report exclusively the biosound datasets used for training, validation, or testing the machine learning models.
This field represents the biosound evidence base underpinning the study.

### Inclusion criteria

Include only datasets containing one or more biosound modalities, such as:
•	Voice
•	Speech
•	Cough
•	Breathing sounds
•	Lung sounds
•	Respiratory sounds
•	Snoring
•	Swallowing sounds
•	Tracheal sounds
•	Other clinically relevant biosound recordings
Examples:
•	ICBHI Respiratory Sound Database
•	Coswara
•	COUGHVID
•	UCI Parkinson Telemonitoring
•	TORGO
•	Voiceome
•	Self-collected respiratory sound dataset
•	Private voice dataset
If multiple biosound datasets are used, list all of them separated by semicolons.
Example:
Database:
ICBHI Respiratory Sound Database; Coswara

### Exclusion criteria

Do not include:
•	MNIST
•	ImageNet
•	CIFAR
•	generic physiological repositories
•	chest X-ray datasets
•	MRI datasets
•	CT datasets
•	Smart Pen datasets
•	PSG repositories without biosound recordings
•	benchmark datasets unrelated to biosound signals
unless those datasets themselves contain biosound recordings.

### Multimodal studies

For multimodal studies, report only the biosound datasets.
Example:
Database:
Coswara
Additional data:
ChestX6 chest X-ray images; pulmonary function variables.

### Auxiliary datasets

Datasets used exclusively for:
•	benchmarking,
•	pre-training,
•	methodological validation,
•	federated convergence analysis,
•	simulation,
must not appear in this field.
If they contain non-biosound information relevant to the model, report them under:
Additional data
Example:
Database:
ICBHI Respiratory Sound Database
Additional data:
MNIST benchmark dataset used exclusively for federated convergence analysis.

### Missing information

If no biosound dataset is explicitly reported:
Database:
Not reported.
Never infer dataset provenance or composition.

### Final quality check

Before finalising, verify that:
•	every reported dataset contains biosound recordings;
•	no imaging or physiological datasets appear in this field;
•	multimodal studies include only the biosound datasets;
•	auxiliary benchmark datasets are excluded.

### Homogenisation rules

#### Objective

To standardise dataset names while preserving the canonical identification of the data resources used in each study.

#### General rule

Use the canonical name of the dataset/resource as reported in the literature. Do not include additional descriptive information that does not form part of the dataset name.

#### Rule 1 — Preserve official dataset names

If the dataset has an established name, use that name without additional explanations.
Examples
Original:
COUGHVID Crowdsourcing Dataset
Final:
COUGHVID
Original:
D-MOMO (Digital-Multimodal Monitoring) speech dataset
Final:
D-MOMO
Original:
MDVR-KCL (Mobile Device Voice Recordings – King's College London)
Final:
MDVR-KCL

#### Rule 2 — Remove acronym expansions when the acronym is the canonical identifier

Do not include the expanded form of well-established datasets.
Examples
DAIC-WOZ (Distress Analysis Interview Corpus – Wizard-of-Oz)
→
DAIC-WOZ
TORGO (Toronto Dysarthria Corpus)
→
TORGO
RAVDESS (Ryerson Audio-Visual Database of Emotional Speech and Song)
→
RAVDESS

#### Rule 3 — Remove repository/platform information

Repositories are not dataset names.
Remove:
•	Kaggle
•	UCI Machine Learning Repository
•	GitHub
•	Zenodo
•	repository URLs
unless the repository itself is the official dataset name.
Examples
Kaggle Parkinson's Disease Voice Dataset derived from the Kay Elemetrics Voice Disorders Database
↓
Kay Elemetrics Voice Disorders Database
Parkinson's Disease Dataset (UCI Machine Learning Repository)
↓
UCI Parkinson's Disease Dataset

#### Rule 4 — Preserve named private datasets

If a private dataset has a specific name, keep it.
Examples
BreathSet (private respiratory sound dataset)
↓
BreathSet
Private Firefly sleep dataset
↓
Firefly Sleep Dataset
Project Achoo application dataset
↓
Project Achoo Dataset

#### Rule 5 — Standardise unnamed private datasets

If no official name exists, create a descriptive canonical name.
Format:
Private + modality/application + dataset
Examples:
Private clinical speech dataset

Private respiratory sound dataset

Private hospital cough dataset

Private smartwatch voice dataset

Private child speech dataset

Private tracheal breathing sound dataset

#### Rule 6 — Do not include acquisition details

Remove information describing:
•	location;
•	hospital;
•	recruitment process;
•	sensor/device;
•	acquisition protocol;
•	study conditions.
Examples:
Private respiratory airflow dataset collected at Upgraded Government Primary Health Centre using a custom sensor
↓
Private respiratory airflow dataset

#### Rule 7 — Separate multiple datasets with semicolon

Example:
ICBHI 2017 Respiratory Sound Database; JUT Respiratory Sound Dataset

Original	Homogeneizado
Coswara Dataset	Coswara
Coswara	Coswara
Virufy Open Dataset; Virufy Clinical 1	Virufy Open Dataset; Virufy Clinical 1
UCI Parkinson Disease Classification Dataset	UCI Parkinson's Disease Dataset
Parkinson's Disease Dataset (UCI Machine Learning Repository)	UCI Parkinson's Disease Dataset
UCI Parkinson Telemonitoring Voice Dataset	UCI Parkinson's Telemonitoring Dataset
UCI Parkinson's Telemonitoring Dataset	UCI Parkinson's Telemonitoring Dataset
Respiratory Sound Database	ICBHI 2017 Respiratory Sound Database (si realmente corresponde a ICBHI)
Corona Hack Respiratory Sound Dataset	CoronaHack Respiratory Sound Dataset
Cambridge COVID-19 Sounds Dataset	Cambridge COVID-19 Sounds
COUGHVID Crowdsourcing Dataset	COUGHVID
PC-GITA speech corpus	PC-GITA Parkinson's Speech Corpus
Saarbruecken Voice Database (SVD)	Saarbruecken Voice Database (SVD)
Distress Analysis Interview Corpus-Wizard of Oz (DAIC-WOZ)	DAIC-WOZ
EATD-Corpus (E-therapy Assessment and Treatment for Depression Corpus)	EATD-Corpus
VoiceWise Dataset	VoiceWise
MDVR-KCL (Mobile Device Voice Recordings – King's College London)	MDVR-KCL
