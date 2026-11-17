# Module 02

This module was used in a dedicated ChatGPT conversation.
The headings below organise the original extraction instructions.

## Origin of data

### Purpose

The Origin of data field identifies the provenance of the dataset(s) used to develop and evaluate the proposed machine learning system.
The field distinguishes whether the study relies exclusively on publicly available datasets, exclusively on privately collected datasets, or a combination of both.
This field characterises the accessibility and origin of the data rather than the data acquisition process.

### Allowed categories

Use only one of the following categories:
•	Public
•	Private
•	Mixed
No other values are permitted.

### Category definitions

Public
Use this category when all datasets used for model development and/or evaluation are publicly available.
Public datasets include:
•	publicly accessible repositories;
•	benchmark datasets;
•	open research datasets;
•	publicly downloadable datasets;
•	datasets explicitly described by the authors as public or open-access.
Examples include:
•	UCI Parkinson's Disease Dataset
•	ICBHI Respiratory Sound Database
•	Coswara
•	COUGHVID
•	DAIC-WOZ
•	PhysioNet datasets
Examples:
•	Public

### Private

Use this category when all datasets used for model development and/or evaluation were collected by the authors or obtained from institutions without public availability.
Examples include:
•	hospital datasets;
•	prospectively collected cohorts;
•	institutional databases;
•	proprietary datasets;
•	clinical studies recruiting participants;
•	datasets explicitly described as unavailable to the public.
Examples:
•	Private

### Mixed

Use this category when the study uses both public and private datasets within the same work.
This includes situations where:
•	public datasets are combined with newly collected clinical data;
•	public benchmark datasets are supplemented with institutional cohorts;
•	private data are used for external validation of publicly trained models;
•	different stages of the study use public and private datasets.
Examples:
•	Mixed

### General principles

Determine the category considering all datasets used in the study, including:
•	training;
•	validation;
•	testing;
•	external validation;
•	independent cohorts.
The classification refers to the overall origin of the data used by the study.

### Important rules

### Rule 1 — Public datasets

If every dataset used in the study is publicly available:
Public

### Rule 2 — Private datasets

If every dataset was privately collected or institutionally owned:
Private

### Rule 3 — Mixed datasets

If at least one public dataset and at least one private dataset are both used anywhere in the study:
Mixed
This rule applies regardless of:
•	which dataset is larger;
•	which dataset is used for training;
•	which dataset is used for testing;
•	whether the public or private dataset is the primary dataset.

### Rule 4 — Dataset availability determines the classification

Classify the origin according to the availability of the dataset, not according to where the recordings were acquired.
For example:
•	a hospital dataset that has been publicly released → Public
•	a hospital dataset available only to the authors → Private

### Rule 5 — Do not infer public availability

Never assume that a dataset is public simply because it has a name or has been cited previously.
The manuscript must explicitly indicate that the dataset is publicly available, or the dataset must correspond to a well-established public repository.
Otherwise:
•	classify it as Private, if clearly institution-specific;
•	if availability cannot be determined, use Private only when the manuscript clearly indicates institutional collection; otherwise classify as Unclear during extraction and resolve during reviewer consensus if your protocol allows uncertainty.
(Si en tu extracción nunca utilizaste "Unclear", eliminaría esta última frase para mantener únicamente las tres categorías.)

### Rule 6 — Data collected through public applications

Data collected through mobile applications, web platforms or wearable devices developed by the authors are Private unless the resulting dataset is explicitly released as a public dataset.

### Rule 7 — External validation

The use of an external validation cohort does not change the classification unless its origin differs from the primary dataset.
Examples:
•	Public training + Public external validation → Public
•	Private training + Private external validation → Private
•	Public training + Private external validation → Mixed
•	Private training + Public external validation → Mixed

### Missing information

If the origin of the dataset cannot be determined from the manuscript:
Not reported

### Final quality check

Before finalising, verify that:
•	only one category has been assigned;
•	the classification considers all datasets used in the study;
•	Mixed is assigned whenever both public and private datasets are used;
•	the classification reflects dataset availability rather than acquisition location;
•	no assumptions about public availability have been made;
•	the assigned category is one of Public, Private, or Mixed.

## Sample size field

### Purpose

The Sample size field must quantify exclusively the biosound cohort used in the study.
This field represents the amount of biosound evidence available for model development and evaluation.
Always prioritise the population from which biosound recordings were obtained.

### Reporting rules

Whenever possible, report:
1.	Number of participants/subjects.
2.	Number of biosound recordings.
3.	Number of biosound segments, cycles, or windows, if explicitly reported.
Preferred formats:
248 participants; 4,732 respiratory sound recordings.
126 participants; 920 respiratory recordings segmented into 6,481 respiratory cycles.

### Prioritisation hierarchy

When multiple descriptors are available, prioritise:
1.	Participants.
2.	Biosound recordings.
3.	Biosound segments/windows.

### Multimodal studies

Report only the biosound cohort.
Do not include sample sizes corresponding to:
•	imaging datasets;
•	physiological datasets;
•	wearable sensor datasets;
•	electronic health records;
•	textual datasets;
•	other non-biosound modalities.
These should not be quantified in this field.
Example:
Sample size:
81 participants (40 Parkinson's disease, 41 healthy controls); 81 sustained vowel (/a/) recordings.

### Longitudinal studies

Whenever available, explicitly report:
•	number of participants;
•	number of recording sessions;
•	total biosound recordings.
Example:
45 ALS patients; 312 longitudinal recording sessions; 2,154 voice recordings.

### Exclusion rules

Do not report:
•	synthetic samples generated by augmentation;
•	GAN-generated recordings;
•	oversampled instances;
•	duplicated samples;
•	synthetic multimodal tuples;
unless they constitute the principal study dataset.
Synthetic data should instead be described under:
Additional methodological comments

### Missing information

If participant or recording counts are unavailable:
Sample size:
Not reported.
Never estimate sample sizes.

### Final quality check

Before finalising, verify that:
•	only biosound participants and recordings are reported;
•	no non-biosound cohorts are quantified;
•	participant counts are prioritised over recording counts;
•	longitudinal information is included whenever available;
•	synthetic or augmented samples are excluded.

### Homogenisation rules

### Objective

To report the quantitative size of the data used in each study without duplicating information already available in other fields.

### General format

Use:
Participants: ...
Recordings: ...
Additional samples: ...
External validation: ...
Longitudinal follow-up: ...
Only include sections that apply.

### Rule 1 — Participants

Report:
•	total number of participants;
•	clinical distribution when available.
Format:
Participants: N (class distribution).
Examples:
Participants: 31 (23 PD, 8 HC).

Participants: 310 (70 COVID-19 positive, 120 recovered COVID-19, 120 HC).

### Standard abbreviations

Use:
Original	Standard
Parkinson's disease	PD
Healthy controls	HC
Mild cognitive impairment	MCI
Alzheimer's disease	AD
Alzheimer's disease dementia	ADD
Subjective cognitive decline	SCD
Major depressive disorder	MDD

### Rule 2 — Do not mention datasets inside Sample Size

Dataset names belong exclusively to Database.
Avoid:
Participants: UCI dataset: 31 participants.
Use:
Participants: Cohort 1: 31.

### Rule 3 — Multiple datasets/cohorts

When several independent datasets are used, report them as cohorts.
Use:
Participants: Cohort 1: ...; Cohort 2: ...
Example:
Participants: Cohort 1: 65; Cohort 2: 181.
Do not mention dataset names.

### Rule 4 — Development/validation cohorts

When the study explicitly defines functional roles, preserve them.
Use:
Participants: Development cohort: ...; External validation cohort: ...
Examples:
Participants: Development cohort: 392 (282 PD, 110 HC); External validation cohort: 178.

### Rule 5 — Recordings

Report only the number of acquired recordings.
If there is one modality:
Recordings: 195.
Do not repeat:
•	voice;
•	cough;
•	breathing;
•	sustained vowel;
•	read speech.
These belong to Biosound modality.

### Rule 6 — Multiple modalities

If several biosound modalities exist, indicate the number per modality.
Format:
Recordings: Voice: 310; Speech: 310; Cough: 930.
Examples:
Recordings: Snoring: 40; Breathing: 40.

### Rule 7 — Derived units

Do not classify derived units as recordings.
Use:
Additional samples:
For:
•	segments;
•	cycles;
•	events;
•	observations;
•	samples;
•	windows;
•	trials.
Examples:
Additional samples: 6,898 respiratory cycles.

Additional samples: 1,310 speech segments.

Additional samples: 4,441 respiratory events.

### Rule 8 — Preserve original quantitative units

Do not transform:
•	cycles → recordings;
•	events → recordings;
•	sessions → recordings.
Examples:
Recordings: 73 speech interview sessions.
not
Recordings: 73 recordings.

### Rule 9 — Duration-based datasets

If only duration is reported:
Use:
Recordings: X hours/minutes/seconds of recordings.
Examples:
Recordings: 4 hours of cough recordings.

Recordings: 1,557 seconds of cough recordings.

### Rule 10 — Longitudinal studies

Separate temporal information.
Use:
Longitudinal follow-up: X months.
or
Longitudinal follow-up: X assessment visits.
Do not include it in recordings.

### Rule 11 — Federated learning datasets

Clients are computational partitions, not cohorts.
Do not write:
Cohort 1: Client 1.
Use:
Recordings: 195 (distributed across two federated clients: 98 and 97).

### Rule 12 — Missing information

Use:
NR
Examples:
Participants: NR.

Recordings: NR.
Never add qualitative information when quantitative information is missing.

### Rule 13 — Dataset size versus used subset

If an article reports:
•	original dataset size;
•	subset actually used;
report the subset used in the experiment.
Example:
Original:
Database contains 707 recordings; experiments used 195.
Final:
Recordings: 195.

## Biosound modality field

### Purpose

The Biosound modality field must identify both:
1.	The biosound modality acquired or analysed.
2.	The specific recording task, elicitation protocol, or acoustic event associated with that modality.
This field aims to characterise not only what biosound was recorded, but also how it was produced or elicited, as recording tasks strongly influence acoustic biomarkers, model generalisability, and clinical applicability.
Reporting format
Use the following structure whenever possible:
<Modality> (<recording task / elicitation protocol / acoustic event>)
Examples:
Voice (sustained phonation of vowel /a/)
Speech (read speech)
Cough (voluntary cough)
Breathing sounds (deep oral breathing)
Respiratory sounds (thoracic auscultation during spontaneous breathing)
If multiple biosound tasks are analysed:
Voice (sustained phonation of vowels /a/, /i/, /u/); Speech (sentence reading); Cough (voluntary cough)
Biosound modalities
Possible modalities include, but are not limited to:
•	Voice
•	Speech
•	Cough
•	Breathing sounds
•	Lung sounds
•	Respiratory sounds
•	Tracheal sounds
•	Swallowing sounds
•	Snoring sounds
•	Wheeze sounds
•	Crackle sounds
•	Mixed respiratory sounds
Recording task examples
Voice
Examples:
Voice (sustained phonation of vowel /a/)
Voice (sustained phonation of vowels /a/, /i/, /u/)
Voice (maximum phonation task)
Voice (DDK task /pa-ta-ka/)
Voice (vowel repetition task)
Voice (pitch glides)
Speech
Examples:
Speech (read speech)
Speech (spontaneous speech)
Speech (picture description task)
Speech (sentence repetition)
Speech (text reading)
Speech (telephone conversation)
Speech (free speech)
Cough
Examples:
Cough (voluntary cough)
Cough (spontaneous cough)
Cough (forced cough)
Cough (continuous ambulatory cough monitoring)
Breathing / respiratory sounds
Examples:
Breathing sounds (deep oral breathing)
Breathing sounds (tidal breathing)
Breathing sounds (forced breathing)
Respiratory sounds (electronic stethoscope auscultation)
Respiratory sounds (thoracic auscultation at multiple chest locations)
Lung sounds (posterior chest auscultation)
Swallowing
Examples:
Swallowing sounds (water swallowing task)
Swallowing sounds (saliva swallowing)
Swallowing sounds (videofluoroscopic swallowing assessment)
Sleep-related sounds
Examples:
Snoring sounds (overnight sleep monitoring)
Breathing sounds (overnight polysomnography)
Event-specific respiratory studies
When the study targets specific pathological acoustic events, explicitly indicate them.
Examples:
Respiratory sounds (Velcro crackles)
Respiratory sounds (wheeze detection)
Respiratory sounds (crackle detection)
Respiratory sounds (adventitious sound classification)
Multimodal biosound studies
Report all biosound modalities analysed.
Example:
Voice (sustained phonation of vowel /a/); Cough (voluntary cough); Breathing sounds (deep breathing)
Missing information
If the manuscript specifies the biosound modality but not the recording task:
Voice (task not reported)
If neither the modality nor the recording protocol is explicitly described:
Not reported

### General principles

•	Always prioritise the terminology used by the authors.
•	Preserve clinically meaningful recording tasks.
•	Be sufficiently specific to distinguish studies using different elicitation protocols.
•	Never infer recording tasks that are not explicitly reported in the manuscript.

### Homogenisation rules

### Objective

To standardise the description of biosound modalities by reporting:
1.	the primary biosound modality;
2.	the acquisition task/protocol when relevant.
The field should describe what type of biosound signal was collected and how it was elicited, while avoiding excessive methodological details already captured in other fields.

### General formatting rule

Use the following format:
Modality (task)
For studies using multiple modalities, separate entries using semicolons:
Voice (sustained phonation); Speech (read speech); Cough (voluntary cough).

### Rule 1 — Standardised biosound modality taxonomy

Use only the following primary categories:
Voice
Use for:
•	sustained phonation;
•	sustained vowel production;
•	vowel phonation;
•	vocal prolongation tasks.
Examples:
Original:
Voice (sustained phonation of vowel /a/)
Standardised:
Voice (sustained phonation /a/)
Original:
Speech (sustained phonation of five long vowels)
Corrected:
Voice (sustained phonation of vowels)

### Speech

Use for:
•	read speech;
•	spontaneous speech;
•	conversational speech;
•	interviews;
•	articulation tasks;
•	diadochokinetic tasks;
•	verbal fluency tasks;
•	sentence production;
•	linguistic tasks.
Examples:
Original:
Speech (reading predefined poems)
Standardised:
Speech (read speech)
Original:
Speech (natural telephone conversations)
Standardised:
Speech (conversational speech)
Original:
Speech (clinical depression assessment interviews)
Standardised:
Speech (clinical interview)

### Cough

Use for cough-related recordings.
Examples:
Cough (voluntary cough)
Cough (continuous monitoring)
Cough (spontaneous cough)

### Breathing sounds

Use for non-auscultatory breathing recordings.
Examples:
Breathing sounds (deep breathing)
Breathing sounds (overnight monitoring)

### Respiratory sounds

Use for clinical respiratory sounds acquired through auscultation or lung sound monitoring.
Includes:
•	lung sounds;
•	chest-wall respiratory sounds;
•	wheezes;
•	crackles;
•	respiratory cycles.
Examples:
Original:
Lung sounds (electronic stethoscope auscultation at multiple chest-wall locations)
Standardised:
Respiratory sounds (lung auscultation)

### Snoring sounds

Use for:
•	snoring recordings;
•	overnight snoring monitoring.
Example:
Snoring sounds (overnight monitoring)

### Non-speech sounds

Use for non-linguistic vocalisations or environmental acoustic signals.
Includes:
•	crying;
•	laughing;
•	screaming;
•	daily activity sounds.
Example:
Non-speech sounds (children vocalisations)

### Rule 2 — Task simplification

Do not include excessive acquisition details.
Remove:
•	device information;
•	sensor type;
•	hospital/location;
•	experimental conditions;
•	participant instructions;
•	language details unless clinically relevant.
Example:
Original:
Speech (emotion-elicited sentence reading in English and Mandarin under multilingual, mask-wearing, and multi-speaker conditions)
Standardised:
Speech (emotional speech)

Original:
Respiratory sounds (thoracic auscultation during spontaneous breathing, including wheezes, crackles, and normal respiratory cycles)
Standardised:
Respiratory sounds (lung auscultation)

### Rule 3 — Avoid modality-task confusion

The modality must represent the physiological signal, not the task name.
Examples:
Incorrect:
Speech (sustained phonation of vowel /a/)
Correct:
Voice (sustained phonation /a/)

Incorrect:
Speech (sustained vocalisation recordings)
Correct:
Voice (sustained phonation)

### Rule 4 — Multiple modalities

When a study includes several biosound modalities, report each separately.
Example:
Original:
Voice (sustained phonation of vowel /a/); Speech (read sentence); Cough (voluntary cough)
Standardised:
Voice (sustained phonation /a/); Speech (read speech); Cough (voluntary cough)

### Rule 5 — Task not reported

When the biosound modality is known but the acquisition task is not described:
Use:
Cough (task not reported)
Voice (task not reported)
Breathing sounds (task not reported)
Do not infer the task from the dataset or application.

### Rule 6 — Preserve clinically meaningful distinctions

Maintain task information when it changes the interpretation of the signal acquisition.
Examples:
Keep:
Speech (clinical interview)
because it differs from:
Speech (read speech)
Keep:
Cough (continuous monitoring)
because it differs from:
Cough (voluntary cough)
Keep:
Breathing sounds (overnight monitoring)
because it differs from:
Breathing sounds (deep breathing)

### Rule 7 — Do not include dataset information

Do not include:
•	database names;
•	hospitals;
•	repositories;
•	cohorts.
These belong to:
•	Database
•	Origin of data
•	Clinical setting
Example:
Incorrect:
Respiratory sounds (ICBHI lung sounds)
Correct:
Respiratory sounds (lung auscultation)

### Rule 8 — Recommended final vocabulary

The final dataset should mainly contain:
Modalities
•	Voice
•	Speech
•	Cough
•	Breathing sounds
•	Respiratory sounds
•	Snoring sounds
•	Non-speech sounds
•	Respiratory airflow signals
Tasks
•	sustained phonation
•	read speech
•	conversational speech
•	clinical interview
•	oral diadochokinesis
•	verbal fluency task
•	emotional speech
•	voluntary cough
•	spontaneous cough
•	continuous monitoring
•	deep breathing
•	shallow breathing
•	overnight monitoring
•	lung auscultation
•	task not reported

### Final principle

Preserve clinically and methodologically relevant acquisition tasks and specific stimuli (e.g., vowels, phonemes, words, sentences, validated tasks). Remove only non-essential acquisition details such as devices, locations, repositories, and experimental conditions.

## Feature sets field

### Purpose

The Feature sets field must report exclusively the biosound-derived input features or representations used by the machine learning models.
This field aims to characterise how biosound signals are represented computationally prior to model training and inference.
Whenever possible, both the number and name of the extracted features must be reported.

### General principles

•	Report only features extracted from biosound recordings.
•	Always prioritise the exact terminology used by the authors.
•	Explicitly state the biosound origin when necessary.
•	Quantify the number of features whenever this information is available.
•	Include both handcrafted features and deep learning input representations.
•	Never infer feature dimensionality if not explicitly reported.
Include
Examples include:
Handcrafted acoustic features
•	MFCCs
•	GFCCs
•	BFCCs
•	LPC
•	PLP
•	Jitter
•	Shimmer
•	HNR
•	Spectral centroid
•	Spectral roll-off
•	Zero-crossing rate
•	Spectral flux
•	Chroma features
•	Formants
•	Prosodic features
•	Temporal features
Deep learning representations
•	Raw waveforms
•	Spectrograms
•	STFT representations
•	Mel-spectrograms
•	Log-Mel spectrograms
•	Scalograms
•	Wavelet representations
•	Embeddings extracted from pretrained audio models
Exclude
Do not include:
•	Age
•	Sex
•	BMI
•	Symptoms
•	Clinical variables
•	Physiological measurements
•	Demographic variables
•	Chest X-ray features
•	PSG variables
•	Accelerometer features
•	Environmental variables
These variables must be reported under:
Additional data
Reporting format
Whenever possible, use the following structure:
<number> <feature family> extracted from <biosound modality>
Examples:
39 acoustic features extracted from respiratory sounds, including MFCCs, spectral centroid, spectral bandwidth, zero-crossing rate, and spectral roll-off.
13 MFCCs extracted from sustained vowel /a/ recordings, including first- and second-order derivatives (39 coefficients in total).
88 eGeMAPS acoustic features extracted from read speech recordings.
Deep learning representations
For end-to-end systems, explicitly report the input representation.
Examples:
Raw cough waveforms sampled at 16 kHz.
Log-Mel spectrograms generated from respiratory sounds using a 25-ms window, 10-ms overlap, and 128 Mel filter banks.
224 × 224 RGB spectrogram images generated from breathing sound recordings.
Multimodal biosound studies
Report all biosound feature sets.
Example:
Voice: 88 eGeMAPS features extracted from sustained vowels; Cough: 128-band Log-Mel spectrograms generated from voluntary cough recordings.
Novel biomarkers
Do not describe novel biomarkers or custom feature engineering in this field.
Novel representations should instead be reported under:
The proposed features
Example:
Feature sets:
88 eGeMAPS features extracted from speech recordings.

The proposed features:
Ranked-Dominant Pitch Intensity (RDPI) biomarker.
Level of detail
Prefer:
53 acoustic features spanning temporal, spectral, and cepstral domains, including HNR, PSD descriptors, MFCCs, and spectral energy, extracted from breathing, cough, and speech recordings.
instead of:
MFCCs; HNR; PSD.
Missing information
If the study states that acoustic features were extracted but does not specify them:
Acoustic feature extraction was reported, but the specific feature set was not described.
If the manuscript does not describe any biosound features:
Not reported.
Examples
Correct:
88 eGeMAPS features extracted from sustained phonation recordings.
128-band Log-Mel spectrograms generated from respiratory sounds.
Raw respiratory waveforms together with 39 MFCC-derived cepstral features extracted from lung sound recordings.
Incorrect:
Age; sex; MFCCs.
Correct alternative:
Feature sets:
39 MFCC-derived acoustic features extracted from lung sounds.

Additional data:
Age; sex.
Final quality check
Before finalising, verify that:
•	all reported features originate from biosound signals;
•	no demographic or clinical variables are included;
•	feature dimensionality is reported whenever available;
•	deep learning input representations are explicitly described;
•	the biosound source is clearly identified.

### Harmonisation rules

### Objective

The Feature sets field describes the computational representation(s) extracted from biosound signals and used as input to machine learning models.
The field must characterise how biosound recordings are transformed into numerical representations for ML analysis.
Included biosound modalities:
•	voice;
•	speech;
•	cough;
•	breathing sounds;
•	respiratory sounds;
•	lung sounds;
•	snoring;
•	swallowing sounds;
•	other human-generated biomedical acoustic signals.

### Fundamental rule 1 — Biosound-only restriction

Feature sets must include only features extracted directly from biosound signals.
A feature or representation can be included only if it is computed from:
•	acoustic recordings;
•	derived acoustic signals;
•	acoustic representations generated from biosound.
Examples included:
✅ MFCCs extracted from cough recordings
✅ Mel-spectrograms generated from speech
✅ Jitter/shimmer extracted from sustained phonation
✅ Wavelet coefficients extracted from respiratory sounds
✅ COVAREP extracted from voice recordings

### Excluded from Feature sets

Features from other modalities must not be included, even if they are fused with biosound representations.
Examples:
Medical imaging
•	MRI volume;
•	cortical thickness;
•	MRI texture descriptors.
Report as:
Additional data: MRI-derived structural features

### Physiological signals

•	ECG;
•	accelerometer;
•	oxygen saturation;
•	heart-rate features.
Report as:
Additional data: Physiological features

### Clinical/demographic information

•	age;
•	sex;
•	clinical scores;
•	disease severity scales.
Report as:
Additional data: Clinical/demographic variables

### Fundamental rule 2 — Standardised acoustic feature extraction frameworks

When a study uses a recognised acoustic feature extraction framework, the framework name must be preserved.
Do not decompose the framework into individual feature families unless the study explicitly analyses only a subset.
Rationale
Standardised toolkits represent a methodological choice and should remain identifiable for quantitative synthesis.
Examples:
Correct:
ComParE feature set (6,373 features)
eGeMAPSv2 feature set (88 features)
COVAREP feature set (74 features)
Incorrect:
MFCCs; Spectral features; Phonatory features
when these are all components of COVAREP/eGeMAPSv2/ComParE.

### Rule 3 — Handcrafted acoustic features

When features are manually extracted and no standardised toolkit is used, classify them according to acoustic family.

#### 3.1 Cepstral features

Includes:
•	MFCCs;
•	ΔMFCC;
•	ΔΔMFCC;
•	GTCC;
•	LPC-derived cepstral coefficients;
•	Mel-cepstral coefficients when explicitly reported outside a toolkit.
Standardisation:
MFCCs
Examples:
MFCCs (13-dimensional)
MFCCs with delta and delta-delta coefficients

#### 3.2 Spectral features

Frequency-domain descriptors:
•	spectral centroid;
•	spectral bandwidth;
•	spectral roll-off;
•	spectral flux;
•	spectral slope;
•	spectral spread;
•	spectral entropy;
•	spectral flatness;
•	spectral skewness;
•	spectral kurtosis;
•	power spectral density.
Standardisation:
Spectral features

#### 3.3 Temporal features

Time-domain descriptors:
•	RMS energy;
•	short-time energy;
•	zero-crossing rate;
•	duration;
•	pause-related measures;
•	temporal envelope descriptors;
•	amplitude statistics.
Standardisation:
Temporal features

#### 3.4 Prosodic features

Speech rhythm and intonation descriptors:
•	F0;
•	pitch;
•	pitch range;
•	pitch variability;
•	speaking rate;
•	articulation rate;
•	pause patterns.
Standardisation:
Prosodic features

#### 3.5 Phonatory features

Features related to vocal fold vibration and phonation.
Includes:
•	jitter;
•	shimmer;
•	HNR;
•	NHR;
•	CPP;
•	glottal parameters;
•	MDVP perturbation measures.
Standardisation:
Phonatory features

#### 3.6 Nonlinear acoustic features

Complexity and nonlinear dynamics:
•	RPDE;
•	DFA;
•	PPE;
•	correlation dimension;
•	Lempel–Ziv complexity;
•	entropy-based nonlinear descriptors.
Standardisation:
Nonlinear acoustic features

#### 3.7 Dysphonia-related biomarkers

Disease-oriented vocal biomarkers.
Includes:
•	Spread1;
•	Spread2;
•	MDVP disease-related parameters.
Standardisation:
Dysphonia-related biomarkers

#### 3.8 Linguistic features

Features derived from speech content.
Includes:
•	vocabulary richness;
•	lexical diversity;
•	information units;
•	verbal fluency measures;
•	semantic descriptors.
Standardisation:
Linguistic features
Only include when derived from recorded speech.

### Rule 4 — Time-frequency representations

Representations preserving spectral and temporal information.

### Mel-spectrograms

Standardise:
Mel-spectrograms
Examples:
Mel-spectrograms (128-band)

### Spectrograms

Includes:
•	STFT spectrograms;
•	FFT spectrograms.
Standardise:
Spectrograms

### Wavelet representations

Includes:
•	DWT coefficients;
•	Wavelet Scattering Transform;
•	other wavelet-derived acoustic representations.
Standardise:
Wavelet representations

### Rule 5 — Learned acoustic representations

Representations obtained from pretrained or learned audio models.
Examples:
•	YAMNet embeddings;
•	Wav2Vec embeddings;
•	VGGish embeddings.
Standardisation:
YAMNet embeddings (1024-dimensional)
Acoustic embeddings

### Rule 6 — Raw biosound representations

When the ML model directly processes the signal.
Use:
Raw waveforms
Examples:
Raw cough waveforms
Raw respiratory waveforms

### Rule 7 — Dimensionality reporting

Include dimensionality only when explicitly reported.
Examples:
Correct:
MFCCs (40-dimensional)
ComParE feature set (6,373 features)
COVAREP feature set (74 features)
Do not report:
•	extraction window;
•	sampling frequency;
•	FFT size;
•	overlap.

### Rule 8 — Avoid extraction parameters

Remove:
•	window length;
•	hop size;
•	filtering;
•	preprocessing parameters.
Example:
Original:
MFCCs extracted using 25 ms windows at 16 kHz
Final:
MFCCs

### Rule 9 — Avoid ML information

Do not include:
•	CNN;
•	LSTM;
•	Transformer;
•	classifier.
Incorrect:
Mel-spectrograms for CNN classification
Correct:
Mel-spectrograms

### Rule 10 — Unknown feature descriptions

If the paper only states:
Acoustic features were extracted
without details:
Use:
Acoustic features (not further specified)
Do not infer MFCCs or spectral features.

### Rule 11 — Multiple feature families

Separate families using semicolons.
Example:
MFCCs (13-dimensional); Spectral features; Temporal features

## Additional data field

### Purpose

The Additional data field must contain all non-biosound information used as model input or integrated within the analytical framework.
Only report additional modalities or variables that were explicitly used by the machine learning model.
This field complements the Database and Feature sets fields by documenting every non-acoustic source of information incorporated into the predictive pipeline.

Include
Examples include:
•	demographic variables;
•	age;
•	sex;
•	BMI;
•	symptoms;
•	questionnaires;
•	clinical variables;
•	pulmonary function variables;
•	physiological measurements;
•	ECG;
•	heart rate;
•	respiratory rate;
•	SpO₂;
•	body temperature;
•	accelerometer signals;
•	gyroscope signals;
•	wearable sensor signals;
•	chest X-ray images;
•	CT images;
•	MRI images;
•	PSG variables;
•	environmental measurements;
•	electronic health records;
•	textual reports.

Exclude
Do not include variables that were merely reported descriptively but were not used by the model.
Example:
If age and sex are only described in the cohort characteristics:
Additional data:
None reported.

### Multimodal studies

Report all non-biosound modalities incorporated into the model.
Whenever possible, report:
1.	the source dataset;
2.	the corresponding modality or variable.
Preferred format:
Additional data:
PPMI clinical records and MRI images; NLM India CT images and medical reports; Smart Pen accelerometer and gyroscope signals; demographic variables.
This preserves traceability while keeping the description concise.

### Level of detail

Avoid excessive detail.
Prefer:
Pulmonary function variables.
instead of:
FEV1; FVC; FEV1/FVC ratio; TLC; RV; DLCO.
Likewise, prefer:
Smart Pen accelerometer and gyroscope signals.
instead of enumerating every derived inertial feature.

### Auxiliary datasets

If a non-biosound dataset is used exclusively for:
•	benchmarking;
•	pre-training;
•	methodological validation;
•	simulation;
•	federated convergence analysis;
report it here.
Example:
Additional data:
MNIST benchmark dataset used exclusively for federated convergence analysis.

### Missing information

If no additional information is incorporated by the model:
Additional data:
None reported.
Never infer the use of demographic, clinical, physiological, imaging, textual, or environmental variables unless their incorporation into the predictive model is explicitly stated.

### Final quality check

Before finalising, verify that:
•	only non-biosound information is reported;
•	every modality was explicitly used by the model;
•	descriptive variables not used for prediction are excluded;
•	multimodal studies identify both the additional modality and, whenever possible, its source dataset;
•	no biosound datasets or acoustic features appear in this field;
•	no sample sizes are reported.

### Harmonisation rules

### Objective

The Additional data field reports all non-biosound information explicitly incorporated into the machine learning pipeline as:
•	model input;
•	multimodal information;
•	auxiliary data source;
•	complementary information used by the predictive framework.
This field complements:
•	Database → origin and characteristics of the data source.
•	Feature sets → representations extracted from biosound signals.
The purpose is to identify all non-acoustic information sources contributing to the predictive model.

### Fundamental rule 1 — Non-biosound restriction

The Additional data field must include only information not directly derived from biosound signals.
Included
Demographic information
Examples:
•	age;
•	sex;
•	BMI;
•	education;
•	socioeconomic variables.
Standardisation:
Demographic variables

### Clinical information

Examples:
•	symptoms;
•	clinical scores;
•	disease severity measures;
•	clinician assessments;
•	diagnosis-related variables;
•	questionnaires.
Standardisation:
Clinical variables
Specific clinically meaningful tools or assessments should be retained when explicitly reported.
Examples:
UPDRS scores
Hoehn & Yahr stage
PHQ-9
GAD-7
C-SSRS assessments
Questionnaires
Clinical symptoms
Do not reduce these to Clinical variables when the specific assessment provides meaningful methodological information.

### Physiological measurements

Examples:
•	ECG;
•	heart rate;
•	respiratory rate;
•	SpO₂;
•	blood pressure;
•	body temperature;
•	blood glucose.
Keep clinically relevant measurements explicit.
Examples:
SpO₂
ECG
Blood pressure
Heart rate
Body temperature
Blood glucose
Avoid replacing specific measurements with:
Physiological measurements
when the exact modality is available.

### Medical imaging

Examples:
•	MRI images;
•	CT images;
•	chest X-ray images;
•	ultrasound images.
Standardisation:
MRI images
CT images
Chest X-ray images
Ultrasound images

### Wearable and inertial sensing

Examples:
•	accelerometer signals;
•	gyroscope signals;
•	smartwatch sensor signals;
•	inertial measurement unit signals.
Preferred standardisation:
Accelerometer and gyroscope signals
or:
Wearable sensor signals
when the exact sensor type is not specified.
If the sensing technology is explicitly reported, preserve it:
MEMS accelerometer signals
Triaxial MEMS accelerometer signals

### Environmental/contextual information

Examples:
•	temperature;
•	humidity;
•	pollution measurements;
•	GPS location data.
Maintain explicit modalities when relevant:
GPS location data
Environmental measurements

### Digital health information

Examples:
•	electronic health records;
•	clinical reports;
•	textual medical information;
•	interview transcripts.

### Fundamental rule 2 — Explicit model utilisation

Only report additional information that was explicitly incorporated into the machine learning model or analytical pipeline.
Do not include variables only reported as participant characteristics.
Example:
The paper reports:
Participants were characterised by age, sex, BMI and disease duration.
but only audio is used for prediction.
Correct:
None reported.
Incorrect:
Age; sex; BMI; disease duration

### Fundamental rule 3 — Additional data must not duplicate Feature sets

Do not include information derived from biosound recordings.
Examples excluded:
•	MFCCs;
•	Mel-spectrograms;
•	acoustic embeddings;
•	voice quality features;
•	cough descriptors;
•	respiratory sound features.
These belong exclusively to:
Feature sets

### Rule 4 — Multimodal studies

When multiple non-biosound modalities are incorporated, report all relevant sources separated by semicolons.
Preferred format:
MRI images; Clinical variables; Demographic variables
If the dataset source is relevant and explicitly reported:
PPMI clinical records and MRI images; Smart Pen accelerometer and gyroscope signals
Do not include:
•	sample size;
•	acquisition protocol;
•	preprocessing steps;
•	ML architecture;
•	derived feature extraction details.

### Rule 5 — Derived information from non-biosound modalities

When derived representations or measurements from a non-biosound modality are used, report the source modality category rather than the specific extracted descriptors.
Purpose:
Maintain comparability between studies using the same non-biosound source.
Examples:
Incorrect:
MRI-derived medial temporal lobe atrophy measures
Correct:
MRI-derived features

Incorrect:
CT texture descriptors extracted using GLCM
Correct:
CT-derived features

Incorrect:
HRV indices extracted from ECG
Correct:
ECG-derived features

### Rule 6 — Categories and level of detail

The field must maintain a balance between:
•	excessive granularity;
•	excessive abstraction.
Preserve individual modalities when they have methodological relevance.
Correct:
SpO₂; ECG; Blood pressure; GPS location data
because these represent different sensing modalities.
Incorrect:
Physiological measurements; Environmental measurements
when the original modalities are explicitly available.

Aggregate only highly related variables.
Examples:
Pulmonary function variables
Incorrect:
FEV1; FVC; FEV1/FVC ratio; TLC; RV
Correct:
Pulmonary function variables

### Questionnaire-based assessments

Correct:
Questionnaires
when multiple questionnaire-derived variables are used.

### Derived inertial measurements

Incorrect:
Acceleration magnitude; orientation angles; movement entropy
Correct:
Accelerometer and gyroscope signals
unless the derived representation itself is the explicitly used modality.

### Rule 7 — Auxiliary datasets

Do not include auxiliary datasets used exclusively for:
•	benchmarking;
•	pre-training unrelated to the target biosound model;
•	simulation;
•	methodological validation;
•	federated learning convergence analysis.
These datasets should not be reported in Additional data.
Only include non-biosound datasets when they provide information directly used as model input for the target predictive task.

### Rule 8 — Missing information

If no additional non-biosound information is incorporated:
Use:
None reported.
Never infer:
•	demographic variables;
•	clinical information;
•	imaging;
•	physiological measurements;
•	environmental variables.

### Rule 9 — Avoid excessive technical detail

Do not report:
•	preprocessing;
•	acquisition parameters;
•	feature extraction methods;
•	dimensionality reduction;
•	derived statistics.
Examples:
Incorrect:
Accelerometer variance, entropy and frequency-domain features
Correct:
Accelerometer signals

Incorrect:
MRI texture descriptors extracted using GLCM
Correct:
MRI-derived features

Incorrect:
Yaw, Pitch and Roll; acceleration magnitude
Correct:
Accelerometer signals

### Final quality checklist

Before finalising the field, verify:
✅ Only non-biosound information is included.
✅ Every modality was explicitly used by the predictive model.
✅ Descriptive-only cohort variables were excluded.
✅ Biosound-derived information is not duplicated.
✅ Multimodal studies report all additional modalities.
✅ Relevant sensing modalities remain identifiable.
✅ Clinically meaningful assessments are not unnecessarily generalised.
✅ Derived features from non-biosound sources are harmonised by modality.
✅ Excessive feature-level detail is avoided.
✅ No sample sizes are reported.
✅ No preprocessing or ML information is included.

## Field: Feature engineering strategy

### Objective

The Feature engineering strategy field describes the methodological operations applied to transform, reduce, select, weight, or learn the final biosound-derived input representation before its use by the machine learning model.
This field captures:
•	feature selection;
•	feature weighting;
•	dimensionality reduction;
•	representation transformation;
•	learned representation extraction.
This field does not describe:
•	the acoustic representations themselves;
•	the final representation name;
•	the novelty of the representation;
•	multimodal fusion strategies;
•	classifier architectures;
•	model training strategies.
The purpose of this field is to identify methodological operations performed between biosound acquisition and the final model input representation.

### Fundamental rule 1 — Do not duplicate Feature sets

Feature engineering strategy must not repeat acoustic representations already reported in Feature sets.
Incorrect:
MFCC-based feature selection.
Correct:
Feature selection.
Feature sets describe what representations are used.
Feature engineering strategy describes what operation was applied to those representations.

### Fundamental rule 2 — Conventional feature extraction is not feature engineering

Do not report standard extraction procedures already represented in Feature sets.
Exclude:
•	MFCC extraction;
•	Mel-spectrogram generation;
•	eGeMAPS extraction;
•	COVAREP extraction;
•	ComParE extraction;
•	standard acoustic descriptor computation;
•	handcrafted feature calculation.
Examples:
Feature sets:
MFCCs
Feature engineering strategy:
None reported.

### Fundamental rule 3 — Feature selection

Include explicit strategies that select subsets of the original representation.
Use the standardised format:
<method>-based feature selection.
Examples:
RFECV-based feature selection.
LASSO-based feature selection.
PSO-based feature selection.
Correlation-based feature selection.
mRMR-based feature selection.
ANOVA-based feature selection.
Wrapper-based feature selection.
Important:
Feature selection is not novelty by itself.
Incorrect:
Novel feature engineering strategy based on RFECV.
Correct:
RFECV-based feature selection.

### Fundamental rule 4 — Feature weighting

Include strategies where features are explicitly assigned different weights before prediction.
Use:
<method>-based feature weighting.
Examples:
PSO-based feature weighting.
Entropy-based feature weighting.
Exclude:
•	attention mechanisms inside neural networks;
•	classifier weighting;
•	ensemble weights;
•	client aggregation weights in federated learning.
These belong to Applied ML techniques.

### Fundamental rule 5 — Dimensionality reduction

Include methods that reduce or project the feature representation into a lower-dimensional space.
Use:
<method>-based dimensionality reduction.
Examples:
PCA-based dimensionality reduction.
Autoencoder-based dimensionality reduction.
Latent-space dimensionality reduction.
Include:
•	PCA;
•	LDA;
•	autoencoder compression;
•	latent-space projection.
Exclude:
•	embeddings generated directly by pretrained models unless additional reduction is applied.
Example:
Feature sets:
Wav2Vec2 embeddings
Feature engineering strategy:
None reported.
unless:
PCA-based dimensionality reduction.

### Fundamental rule 6 — Representation transformation

Include operations that transform one representation into another before model input.
The field must describe the transformation process, not the final representation name.
Use:
<method>-based representation transformation.
Examples:
Spectrogram-to-image transformation.
Wavelet-based representation transformation.
Fourier-based representation transformation.
Covariance transformation.
Tangent-space projection.
VMD-based representation transformation.
Examples:
Incorrect:
Novel acoustic representation.
Correct:
Spectrogram-to-image transformation.
Incorrect:
Novel wavelet representation.
Correct:
Wavelet-based representation transformation.

### Fundamental rule 7 — Learned representation extraction

Include deep learning models when they are used to generate intermediate representations, embeddings, or latent features that are subsequently used for prediction.
Use:
<model>-based representation learning.
or
<model>-based embedding extraction.
Examples:
CNN-based embedding extraction.
CNN-based feature extraction.
Transformer-based representation learning.
BiLSTM-based representation learning.
Include when:
•	CNN extracts embeddings from spectrograms;
•	Transformer generates latent representations;
•	recurrent models generate feature embeddings.
Exclude when the model is only the final classifier.
Incorrect:
CNN-based feature extraction.
if:
"The CNN directly classified the input."
Correct:
None reported.

### Fundamental rule 8 — Multimodal studies

Do not report multimodal fusion as feature engineering.
Exclude:
•	multimodal feature fusion;
•	feature-level fusion;
•	early fusion;
•	late fusion;
•	cross-modal fusion;
•	attention-based fusion.
These describe how multiple modalities are combined and frequently correspond to model architecture decisions.
They must be reported in:
•	Applied ML techniques;
•	Computational architecture fields;
•	Multimodal analysis fields if applicable.
Example:
Feature sets:
MFCCs; MRI images
Applied ML techniques:
Feature fusion; CNN.
Feature engineering strategy:
None reported.

### Fundamental rule 9 — No strategy reported

Use:
None reported.
when:
•	conventional features are directly used;
•	no selection is applied;
•	no weighting is applied;
•	no dimensionality reduction is applied;
•	no representation transformation is applied;
•	no learned representation extraction is performed.
Examples:
Feature sets:
MFCCs
Feature engineering strategy:
None reported.

### Fundamental rule 10 — Separate from Applied ML techniques

Do not include:
•	CNN;
•	LSTM;
•	Transformer;
•	SVM;
•	Random Forest;
•	XGBoost;
•	classifier names;
•	hyperparameter optimisation;
•	data augmentation;
•	federated aggregation;
•	attention mechanisms;
•	voting strategies;
•	decision fusion;
•	probability averaging.
These belong to Applied ML techniques.

### Standardised vocabulary

Strategy	Standardised term
Feature selection	<method>-based feature selection
Feature weighting	<method>-based feature weighting
PCA	PCA-based dimensionality reduction
Autoencoder	Autoencoder-based dimensionality reduction
Spectrogram conversion	Spectrogram-to-image transformation
Wavelet transformation	Wavelet-based representation transformation
Fourier transformation	Fourier-based representation transformation
Covariance mapping	Covariance transformation
Tangent projection	Tangent-space projection
Deep embeddings	<model>-based embedding extraction
Deep representations	<model>-based representation learning

### Final quality checklist

Before finalising verify:
✅ The field does not duplicate Feature sets.
✅ The field does not describe novelty.
✅ Conventional feature extraction is excluded.
✅ Feature selection methods are included.
✅ Feature weighting is included only when explicitly applied.
✅ Dimensionality reduction is included only when reducing/projecting representations.
✅ Representation transformations describe the actual operation.
✅ Learned representations are included only when intermediate embeddings/features are generated.
✅ Multimodal fusion is excluded.
✅ Classifier architectures are excluded.
✅ Training strategies are excluded.
✅ The strategy corresponds to the final model input representation.
✅ Use "None reported" when no operation is explicitly described.

### Harmonisation rules

### Objective

The Feature engineering strategy field describes the methodological operation applied to obtain or modify the final model input representation from biosound-derived data.
This field captures:
•	feature selection;
•	feature weighting;
•	dimensionality reduction;
•	representation transformation;
•	feature fusion;
•	learned representation extraction.
This field does not describe:
•	the acoustic features themselves;
•	the final representation name;
•	the novelty of the representation.

### Fundamental rule 1 — Do not duplicate Feature sets

Do not include acoustic representations already reported in Feature sets.
Incorrect:
MFCC-based feature selection.
Correct:
Feature selection.

### Fundamental rule 2 — Feature selection

Include explicit selection strategies.
Standardised format:
<method>-based feature selection.
Examples:
RFECV-based feature selection.
LASSO-based feature selection.
PSO-based feature selection.
Correlation-based feature selection.

### Fundamental rule 3 — Feature weighting

Include when features are explicitly weighted.
Format:
<method>-based feature weighting.
Examples:
PSO-based feature weighting.

### Fundamental rule 4 — Dimensionality reduction

Include representation reduction methods.
Examples:
PCA-based dimensionality reduction.
Autoencoder-based dimensionality reduction.

### Fundamental rule 5 — Representation transformation

Include operations that transform one representation into another.
Examples:
Wavelet-based representation transformation.
Spectrogram-to-image transformation.
Covariance transformation.

### Fundamental rule 6 — Feature fusion

Include only fusion occurring before prediction.
Examples:
Feature-level fusion.
Multimodal feature fusion.
Exclude:
•	majority voting;
•	probability averaging;
•	decision fusion.

### Fundamental rule 7 — Learned representation extraction

Include deep models when they are used to generate representations or embeddings.
Examples:
CNN-based feature extraction.
CNN-based embedding extraction.
Transformer-based representation learning.
Exclude:
CNN classifier.

### Fundamental rule 8 — No engineering strategy

Use:
None reported.
when:
•	conventional features are directly used;
•	no selection;
•	no weighting;
•	no reduction;
•	no transformation;
•	no fusion;
•	no learned representation extraction.
