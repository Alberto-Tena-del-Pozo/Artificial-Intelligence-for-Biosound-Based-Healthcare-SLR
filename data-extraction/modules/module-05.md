# Module 05

This module was used in a dedicated ChatGPT conversation.
The headings below organise the original extraction instructions.

## Field: Clinical Setting

### Objective

Characterise the healthcare context, care pathway, or clinical environment in which the proposed system is evaluated or intended to operate.
This field answers:
In which healthcare context is the system intended or evaluated to be used?
It describes the healthcare setting, not the technology, disease, population, or computational architecture.

### General principles

Rule 1 — Report the healthcare context, not the technology
Clinical Setting must describe where and how healthcare is delivered.
Include:
•	care environment;
•	healthcare pathway;
•	monitoring model;
•	screening context.
Do not include:
•	smartphone;
•	wearable;
•	IoT;
•	edge/cloud infrastructure;
•	ML deployment.
Examples:
Correct:
•	Home monitoring.
•	Remote patient monitoring.
•	Hospital-based screening.
Incorrect:
•	Smartphone application.
•	Cloud-based platform.
•	Edge deployment.

### Rule 2 — Do not infer from disease or modality

Never assign a setting only because of the disorder studied.
Examples:
Incorrect:
•	Parkinson's disease → Neurology clinic ❌
•	COPD → Respiratory clinic ❌
•	Depression → Mental health clinic ❌
Only assign specialist settings when explicitly reported.

### Rule 3 — Prioritise explicit evaluation context

If the system was evaluated in a real healthcare environment, report that setting.
Examples:
"Patients were assessed in a hospital outpatient service."
→ Hospital outpatient care
"Patients used the system at home and clinicians followed their evolution remotely."
→ Home monitoring; Remote patient monitoring

### Rule 4 — Future intended applications

Do not encode "intended" in the output.
The maturity/status of the application belongs to Deployment maturity.
Examples:
"Intended for home remote monitoring."
Output:
Home monitoring
NOT:
Home monitoring (intended application)

### Rule 5 — Multiple settings

Multiple categories are allowed only when they represent independent healthcare contexts explicitly described.
Example:
"Patients recorded data at home and physicians monitored disease progression remotely."
Output:
Home monitoring; Remote patient monitoring
Do not add categories only because they are related.

### Final Clinical Setting taxonomy

Hospital-based care
Hospital inpatient care
Use for:
•	hospital wards;
•	bedside monitoring;
•	inpatient monitoring;
•	ICU.
Examples:
•	Hospital wards.
•	Bedside respiratory monitoring.

### Hospital outpatient care

Use for:
•	outpatient assessments;
•	specialist consultations;
•	ambulatory hospital evaluations.
Examples:
•	Outpatient neurological assessment.
•	Hospital outpatient assessment.

### Hospital-based screening

Use for:
•	hospital screening;
•	hospital triage;
•	diagnostic screening performed in hospitals.
Examples:
•	Hospital-based respiratory screening.
•	Hospital COVID-19 screening.

### Primary and specialist healthcare

Primary care
Use for:
•	general practitioners;
•	primary healthcare services.
Examples:
•	Primary care screening.

### Specialist clinic

Use when a specialised outpatient clinical service is explicitly reported.
Includes:
•	neurology clinic;
•	memory clinic;
•	respiratory clinic;
•	sleep clinic;
•	mental health clinic.
Output:
Specialist clinic
Do not preserve medical specialty names.
Examples:
"Neurology clinic assessment"
→ Specialist clinic
"Memory clinic evaluation"
→ Specialist clinic

### Remote healthcare

Remote patient monitoring
Use when the system enables remote follow-up, monitoring, or management of patients.
Includes:
•	telemonitoring;
•	longitudinal remote follow-up;
•	post-hospitalisation follow-up.
Examples:
"Remote monitoring of COPD patients after discharge."
→ Remote patient monitoring

### Telemedicine

Use when remote healthcare delivery or clinical interaction is explicitly described.
Includes:
•	telehealth;
•	remote clinical interaction;
•	remote healthcare delivery.
Examples:
"Telemedicine platform connecting patients and clinicians."
→ Telemedicine
Do not assign only because data are transmitted remotely.

### Remote screening

Use when screening is performed remotely.
Includes:
•	remote screening;
•	remote self-screening;
•	remote pre-screening.
Examples:
"Remote self-screening using a mobile application."
→ Remote screening

### Home-based healthcare

Home monitoring
Use when healthcare monitoring occurs in the patient's home environment.
Includes:
•	home remote monitoring;
•	home respiratory monitoring;
•	home sleep monitoring.
Examples:
"Patients collected respiratory sounds at home."
→ Home monitoring

### Home self-assessment

Use when users perform self-administered evaluations at home.
Includes:
•	home neurological self-assessment;
•	home cognitive self-assessment.
Examples:
"Users performed cognitive tasks at home."
→ Home self-assessment

### Community and point-of-care healthcare

Community screening
Use for population/community-based screening.
Includes:
•	community screening;
•	underserved community screening.
Examples:
"Screening campaign in rural communities."
→ Community screening

### Point-of-care screening

Use for screening close to the patient outside conventional laboratory settings.
Includes:
•	early screening;
•	near-patient screening.
Examples:
"Early point-of-care respiratory screening."
→ Point-of-care screening

### Specialised / research environments

Sleep laboratory
Use for dedicated sleep assessment environments.
Examples:
•	Sleep laboratory.
•	Polysomnography laboratory.

### Clinical research environment

Use when the study occurs in a supervised clinical research context without a clearer healthcare pathway.
Examples:
•	Clinical research laboratory.
•	Multicentre clinical study.

### Consumer and preventive healthcare

Consumer digital health
Use when explicitly positioned as a consumer healthcare application.
Examples:
•	Consumer digital health application.

### Preventive healthcare

Use when the application is explicitly preventive.
Examples:
•	Preventive mental health monitoring.
•	Early preventive assessment.

### Assistive applications

Assistive communication
Use for systems supporting communication abilities.
Examples:
•	Communication support systems.

### Missing information

Not reported
Use when:
•	only disease/application is described;
•	only computational architecture is described;
•	only the objective is reported without healthcare context.
Examples:
"Respiratory health monitoring and screening."
→ Not reported
"Clinical Decision Support System for respiratory diagnosis."
→ Not reported

### Final normalisation rules

Original term	Normalised output
Home remote monitoring	Home monitoring
Home respiratory monitoring	Home monitoring
Home-based neurological self-assessment	Home self-assessment
Remote cognitive screening	Remote screening
Remote self-screening	Remote screening
Telehealth	Telemedicine
Post-hospitalisation follow-up	Remote patient monitoring
Sleep laboratory screening	Sleep laboratory
Hospital respiratory screening	Hospital-based screening
Hospital wards	Hospital inpatient care
Bedside monitoring	Hospital inpatient care
Neurology clinic	Specialist clinic
Memory clinic	Specialist clinic
Mental health clinic	Specialist clinic
Preventive mental health monitoring in educational environments	Consumer digital health; Preventive healthcare

## Real-time capability field

### Purpose

The Real-time capability field must assess whether the study explicitly demonstrates, claims, or does not address real-time operation of the proposed system.
This field aims to evaluate the translational maturity of biosound-based digital health systems by distinguishing between:
1.	Computational real-time capability: whether the machine learning inference process satisfies temporal constraints based on experimentally measured computational metrics.
2.	Operational real-time capability: whether the complete end-to-end system has been experimentally validated under continuous, streaming, or real-world operational conditions.
The classification must be performed conservatively.
Never infer real-time capability.

### Allowed categories

Use only one of the following categories:
•	Operational real-time demonstrated
•	Computational real-time demonstrated
•	Claimed, not demonstrated
•	Not reported

### Category definitions

Operational real-time demonstrated
Use this category only if the study experimentally validates the complete end-to-end system under operational conditions.
Evidence must include:
Quantitative temporal measurements
At least one of:
•	inference latency;
•	end-to-end latency;
•	throughput;
•	response time;
•	FPS;
•	communication latency;
•	processing time per sample/window.
The reported temporal metric must be explicitly defined by the authors as representing a machine learning or complete system performance metric. Ambiguous or undefined temporal measurements must not be considered sufficient evidence.
AND
Experimental validation in a realistic operational environment.
Examples include:
•	continuous streaming;
•	online monitoring;
•	smartphone applications running continuously;
•	wearable systems performing online inference;
•	embedded/IoT systems processing incoming biosignals in real time;
•	hospital or home deployments with live data acquisition;
•	real-time FPGA/microcontroller implementations validated experimentally.
Examples:
Operational real-time demonstrated. A smartwatch continuously processed respiratory windows online with an average latency of 24 ms.
Operational real-time demonstrated. The smartphone application performed continuous cough detection with an end-to-end latency of 52 ms.

### Computational real-time demonstrated

Use this category when the study reports explicitly defined quantitative timing metrics demonstrating computational efficiency, but evaluation is performed offline or on pre-segmented data.
Typical scenarios:
•	inference latency measured on a workstation;
•	prediction time;
•	processing time;
•	communication latency;
•	throughput;
•	benchmarking on GPU/CPU hardware;
•	offline inference profiling;
•	latency measured on static benchmark datasets;
•	no continuous acquisition or streaming evaluation.
The reported temporal metric must be explicitly identified by the authors as representing a machine learning computational process (e.g., inference, prediction, processing, communication, throughput, or end-to-end execution). Ambiguous or undefined temporal measurements must not be considered sufficient evidence of computational real-time capability.
Examples:
Computational real-time demonstrated. Inference latency of 7.3 ms per sample was measured on an RTX 3090 GPU using offline benchmark datasets.
Computational real-time demonstrated. The proposed model achieved 150 ms inference latency on CPU, although evaluation was performed on pre-recorded data.
This category indicates that:
The computational core may be compatible with real-time deployment, but operational real-time behaviour has not been experimentally validated.

### Claimed, not demonstrated

Use this category when the study:
•	claims real-time operation;
•	targets continuous monitoring;
•	presents a functional prototype;
•	implements a mobile, wearable, or IoT application;
•	discusses real-time deployment feasibility;
but provides neither quantitative timing measurements nor experimental operational validation.
Examples:
Claimed, not demonstrated. The study proposes continuous respiratory monitoring but does not report latency measurements.
Claimed, not demonstrated. The wearable system acquires biosignals continuously, but no temporal performance evaluation is provided.
Typical phrases leading to this category:
•	"real-time monitoring";
•	"continuous monitoring";
•	"online diagnosis";
•	"instant screening";
•	"edge deployment";
without supporting experimental evidence.

### Not reported

Use this category when the manuscript does not discuss, evaluate, or claim real-time operation.
Examples:
Not reported.
Typical characteristics:
•	retrospective offline analyses;
•	benchmark studies;
•	no mention of latency, throughput, online processing, or continuous monitoring.

### Important rules

Rule 1 — Hardware alone is insufficient
The mere use of:
•	smartphones;
•	wearables;
•	Jetson devices;
•	FPGAs;
•	microcontrollers;
•	IoT hardware;
does not imply real-time capability.
Example:
Incorrect:
Operational real-time demonstrated because a smartphone was used.
Correct:
Claimed, not demonstrated
unless timing metrics and operational validation are reported.

### Rule 2 — Latency alone does not imply operational real-time capability

Studies reporting:
•	inference latency;
•	FPS;
•	throughput;
on offline datasets should be classified as:
Computational real-time demonstrated
rather than:
Operational real-time demonstrated
unless live end-to-end operation is experimentally validated.

### Rule 3 — Temporal metrics must be explicitly interpretable

Only temporal measurements whose meaning is explicitly defined by the authors may be used as evidence of computational or operational real-time capability.
Sensor-level metrics such as:
•	response time;
•	recovery time;
•	sampling frequency;
do not demonstrate machine learning real-time capability.
Likewise, ambiguous temporal measurements (e.g., an undefined response time or execution time) must not be interpreted as evidence of real-time capability unless the manuscript clearly specifies that they correspond to inference, prediction, processing, communication, throughput, or end-to-end execution.
Example:
Incorrect:
Computational real-time demonstrated because response time = 95 s, without specifying what the response time represents.
Correct:
Claimed, not demonstrated (if real-time operation is claimed) or Not reported (if no real-time capability is discussed).

### Rule 4 — Edge deployment does not imply operational real-time

On-device inference without temporal measurements should be classified as:
Claimed, not demonstrated
unless timing metrics and operational evaluation are available.

### Rule 5 — Federated learning studies

Federated learning systems should be classified as:
Computational real-time demonstrated
if they report:
•	communication latency;
•	convergence time;
•	round duration;
•	inference latency.
Operational real-time demonstrated
only if the federated system is experimentally validated under live distributed operation.

### Examples

Example 1
Real-time capability:
Operational real-time demonstrated.
Evidence:
Continuous smartphone cough monitoring with end-to-end latency = 35 ms.
Example 2
Real-time capability:
Computational real-time demonstrated.
Evidence:
Inference latency = 7.3 ms/sample measured on an RTX 3090 GPU using offline benchmark datasets.
Example 3
Real-time capability:
Claimed, not demonstrated.
Evidence:
The wearable prototype targets continuous monitoring, but no latency metrics were reported.
Example 4
Real-time capability:
Not reported.

### Final quality check

Before finalising, verify that:
•	real-time capability is never inferred;
•	hardware usage alone does not imply real-time operation;
•	latency measurements alone do not imply operational real-time capability;
•	only explicitly defined machine learning temporal metrics are accepted as evidence of real-time capability;
•	ambiguous or undefined temporal measurements are not interpreted as evidence of real-time capability;
•	offline benchmarking studies are distinguished from live operational systems;
•	sensor-level timings are not confused with machine learning execution times;
•	operational and computational real-time capabilities are clearly differentiated.

## Privacy/confidential mechanisms field

### Purpose

The Privacy/confidential mechanisms field must describe the specific technical mechanisms explicitly implemented to protect the confidentiality, integrity, or privacy of user data within the proposed system.
This field focuses on engineering mechanisms rather than general privacy claims or regulatory statements.
It answers the question:
Which technical privacy-preserving mechanisms are implemented?

### General principles

Report only mechanisms explicitly described in the manuscript.
Never infer privacy protection simply because:
•	medical data are used;
•	federated learning is employed;
•	data are anonymised;
•	ethical approval was obtained.
Only include mechanisms that are actually implemented.

### Include

Examples include:
Data minimisation
•	Local inference
•	On-device processing
•	Edge inference
•	Local feature extraction
•	Local decision making
•	Feature-only transmission
•	Compressed embedding transmission

### Federated learning mechanisms

•	Federated Averaging (FedAvg)
•	Secure aggregation
•	Peer-to-peer federated learning
•	Split learning
•	Model parameter exchange
•	Gradient exchange
•	Zero raw-data sharing

### Cryptographic mechanisms

•	Encryption
•	End-to-end encryption
•	Homomorphic encryption
•	Secure Multi-Party Computation (SMPC)
•	Differential Privacy
•	Trusted Execution Environment (TEE)

### Identity protection

•	De-identification
•	Pseudonymisation
•	Local identifier management
•	Isolated user databases

### Communication mechanisms

•	Secure communication channels
•	TLS/SSL
•	Encrypted wireless communication

### Access control

•	Authentication
•	Authorization
•	Secure credential management

### Exclude

Do not report:
•	GDPR compliance
•	HIPAA compliance
•	ethics approval
•	informed consent
•	IRB approval
•	regulatory approval
These are ethical or legal aspects rather than technical privacy mechanisms.
Do not report vague statements such as:
Privacy is preserved.
unless accompanied by explicit mechanisms.

### Preferred reporting style

Examples:
•	Local feature extraction; compressed embedding transmission; zero raw-audio sharing.
•	Federated Averaging with local model updates and parameter exchange only.
•	On-device inference; encrypted communication.
•	Differential Privacy with secure aggregation.
•	De-identified local databases with encrypted cloud synchronization.

### Missing information

If no technical privacy mechanisms are explicitly implemented:
None reported.

### Final quality check

Before finalising, verify that:
•	every reported item is a concrete technical mechanism;
•	ethical or regulatory statements are excluded;
•	privacy claims without implementation are not reported.

### Taxonomy

1. Data minimisation and local processing
Local processing
Incluye:
•	On-device processing
•	Edge processing
•	Local computation
Output:
Local processing

### Local inference

Incluye:
•	On-device inference
•	Edge inference
•	Local decision making
Output:
Local inference

### Local feature extraction

Incluye:
•	Feature extraction performed locally
•	Local preprocessing before transmission
Output:
Local feature extraction

### Feature/embedding transmission instead of raw data

Incluye:
•	Feature-only transmission
•	Compressed embedding transmission
•	Compressed representation transmission
Output:
Feature/embedding transmission

### Raw data avoidance

Incluye:
•	No raw audio transmission
•	No raw video transmission
•	Zero raw-data sharing
Output:
Raw data avoidance

### Data minimisation

Incluye:
•	Short audio snippets
•	Reduced data collection
•	Limited data acquisition
Output:
Data minimisation

### Local data deletion

Incluye:
•	Automatic deletion after inference
•	Local disposal of temporary data
Output:
Local data deletion

### 2. Federated and distributed privacy mechanisms

Federated learning
Incluye:
•	Federated Averaging (FedAvg)
•	FedDyn
•	Federated aggregation
Output:
Federated aggregation

### Local model training

Incluye:
•	Training performed locally
•	Local updates
Output:
Local model training

### Model parameter exchange

Incluye:
•	Model parameter exchange
•	Gradient exchange
•	Soft-logit exchange
Output:
Model parameter exchange

### Zero raw-data sharing

Incluye:
•	No raw data transfer
•	Raw data remain local
Output:
Zero raw-data sharing

### Secure aggregation

Incluye:
•	Secure aggregation protocols
Output:
Secure aggregation

### Peer-to-peer federated learning

Output:
Peer-to-peer federated learning

### 3. Cryptographic mechanisms

Encryption
Incluye:
•	Encryption
•	Encrypted storage
•	Encrypted transmission
Output:
Encryption

### TLS/SSL secure communication

Output:
TLS/SSL

### Homomorphic encryption

Output:
Homomorphic encryption

### Secure Multi-Party Computation

Output:
Secure Multi-Party Computation

### Differential privacy

Incluye:
•	Noise injection
•	Differential privacy
Output:
Differential Privacy

### Trusted Execution Environment

Output:
Trusted Execution Environment

### 4. Identity and data protection

De-identification
Incluye:
•	De-identification
•	Anonymisation
•	Anonymous identifiers
Output:
De-identification

### Pseudonymisation

Output:
Pseudonymisation

### Sensitive attribute protection

Incluye:
•	Sensitive attribute anonymisation
•	Privacy-sensitive content removal
Output:
Sensitive attribute protection

### Isolated user data management

Incluye:
•	Isolated databases
•	User-specific databases
•	Local identifier management
Output:
Isolated data management

### 5. Access and authentication mechanisms

Authentication
Incluye:
•	User authentication
•	Password protection
•	Credential management
Output:
Authentication

### Authorization and access control

Incluye:
•	Role-based access control
•	Restricted dataset access
•	Controlled database access
Output:
Access control

### 6. Secure communication mechanisms

Secure communication
Incluye:
•	Secure communication channels
•	Encrypted wireless communication
Output:
Secure communication

### Secure wireless communication

Incluye:
•	Bluetooth Low Energy secure communication
Output:
Secure wireless communication

### 7. Storage protection

Secure storage
Incluye:
•	Secure cloud storage
•	Secure local storage
•	Encrypted databases
Output:
Secure storage

### Data retention management

Incluye:
•	Selective retention
•	Data deletion policies
Output:
Data retention management

### 8. Content privacy protection

Content filtering
Incluye:
•	On-device speech filtering
•	Removal of privacy-sensitive speech
•	Target speaker isolation
Output:
Content filtering

### Privacy-preserving signal processing

Incluye:
•	Content-free speech analysis
•	Removal of irrelevant signal components
Output:
Privacy-preserving signal processing

### 9. Blockchain / distributed ledger mechanisms

Blockchain-based security
Incluye:
•	Blockchain ledger
•	Public/private key encryption
•	Consensus mechanisms
•	Hashing
Output:
Blockchain-based security

### 10. Missing information

Output:
None reported

### Reglas de normalización principales

Original	Normalizado
On-device processing	Local processing
On-device inference	Local inference
Local feature extraction	Local feature extraction
No raw-data sharing	Zero raw-data sharing
Zero raw-audio sharing	Zero raw-data sharing
FedAvg	Federated aggregation
Federated aggregation	Federated aggregation
Model parameter exchange only	Model parameter exchange
Anonymisation	De-identification
Data anonymisation	De-identification
TLS/SSL secure communication	TLS/SSL
Secure cloud storage	Secure storage
Role-based access control	Access control
User authentication	Authentication
Password-protected authentication	Authentication
Local data retention	Data retention management
Data deletion policies	Data retention management
Encrypted storage	Encryption + Secure storage
Encrypted transmission	Encryption

### Decisiones metodológicas importantes

No incluir:
•	GDPR
•	HIPAA
•	consent
•	ethics approval
•	IRB

### No convertir en mecanismo:

❌ Federated learning por sí solo
Debe descomponerse:
•	FedAvg → Federated aggregation
•	local training → Local model training
•	parameter exchange → Model parameter exchange
•	no raw data sharing → Zero raw-data sharing

### No incluir claims:

❌ Privacy preserving system
❌ Secure platform
❌ Confidential framework
si no hay mecanismo explícito.

### Formato final del campo

Ejemplo:
Local processing; Local inference; Zero raw-data sharing; Federated aggregation; Model parameter exchange
o:
De-identification; Encryption; Authentication; Access control; Secure storage

### Creo que esta taxonomía encaja mejor con tu SLR porque después podrás responder preguntas como:

•	¿Cuántos sistemas usan privacidad por descentralización?
•	¿Cuántos usan criptografía?
•	¿Cuántos usan federated learning real?
•	¿Cuántos solo aplican anonimización?
•	¿Cuántos no implementan ningún mecanismo técnico?

## Explainability field

### Purpose

The Explainability field must assess whether the study incorporates mechanisms that improve the interpretability, transparency, or explainability of the machine learning system.
This field aims to determine whether the study provides insights into:
•	model decision-making;
•	relevant acoustic biomarkers;
•	feature contributions;
•	clinically meaningful patterns.
The classification must be performed conservatively.
Never infer explainability.

### Allowed categories

Use only one of the following categories:
•	Dedicated XAI methods
•	Intrinsic interpretability mechanisms
•	No explainability

### Category definitions

Dedicated XAI methods
Use this category when the study explicitly implements dedicated explainable AI (XAI) techniques designed to interpret model predictions.
Examples include:
•	SHAP
•	LIME
•	Grad-CAM
•	Grad-CAM++
•	Score-CAM
•	Layer-wise Relevance Propagation (LRP)
•	Integrated Gradients
•	Saliency maps
•	Occlusion analysis
•	Counterfactual explanations
•	Feature attribution methods
•	Attention heatmaps explicitly generated for interpretation
Examples:
Dedicated XAI methods. SHAP analysis was used to quantify the contribution of acoustic biomarkers to Parkinson's disease detection.
Dedicated XAI methods. Grad-CAM heatmaps were generated to identify discriminative spectro-temporal regions associated with pathological cough events.
Dedicated XAI methods. Saliency maps and Integrated Gradients were employed to interpret model predictions.

### Intrinsic interpretability mechanisms

Use this category when the study provides some level of interpretability through model structure or auxiliary analyses, but does not employ dedicated post-hoc XAI techniques.
Examples include:
Feature importance analyses
•	feature importance ranking;
•	permutation importance;
•	biomarker ranking;
•	variable importance analysis.
Interpretable models
•	decision trees;
•	rule-based systems;
•	sparse linear models;
•	prototype learning.
Attention-based interpretation
Only if attention mechanisms are explicitly analysed or visualised for interpretation.
Representation analyses
•	t-SNE visualisation;
•	UMAP visualisation;
•	latent-space visualisation;
•	embedding analysis.
Examples:
Intrinsic interpretability mechanisms. Random Forest feature importance analysis was used to identify clinically relevant respiratory biomarkers.
Intrinsic interpretability mechanisms. Attention entropy analysis and cross-modal mutual information analysis were used to interpret multimodal interactions.
Intrinsic interpretability mechanisms. Latent-space visualisation using t-SNE was employed to assess class separability.
Intrinsic interpretability mechanisms. Prototype learning was used to provide case-based explanations.

### No explainability

Use this category when the study does not include any explicit interpretability or explainability strategy.
Examples:
No explainability. The study did not incorporate dedicated explainable AI methods or model interpretation techniques.

### Important rules

Rule 1 — Attention layers alone are insufficient
The mere presence of attention modules does not constitute explainability.
Incorrect:
Dedicated XAI methods because the model contains an attention layer.
Correct:
No explainability
unless the attention weights or maps are explicitly analysed for interpretation.

### Rule 2 — Ablation studies are not explainability

Do not classify the following as explainability:
•	ablation studies;
•	benchmark comparisons;
•	statistical significance analyses;
•	robustness analyses;
•	confusion matrices;
•	ROC curves.
Incorrect:
Intrinsic interpretability mechanisms because ablation studies were performed.

### Rule 3 — Feature extraction is not explainability

The use of MFCCs, spectrograms, or handcrafted features does not imply interpretability.
Feature importance or biomarker analyses must be explicitly reported.

### Reporting format

Use the following structure:
<Explainability category>. <Brief description>.
Examples:
Dedicated XAI methods. SHAP analysis was used to quantify the contribution of speech biomarkers.
Intrinsic interpretability mechanisms. Feature importance ranking and attention entropy analyses were performed.
No explainability. The study did not incorporate dedicated explainable AI methods or model interpretation techniques.

### Final quality check

Before finalising, verify that:
•	explainability is never inferred;
•	dedicated XAI methods are clearly distinguished from intrinsic interpretability mechanisms;
•	attention layers alone are not considered explainability;
•	ablation studies are not classified as explainability;
•	only explicitly reported interpretation mechanisms are included.
