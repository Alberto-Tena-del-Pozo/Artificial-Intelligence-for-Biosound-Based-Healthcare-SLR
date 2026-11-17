# Module 04

This module was used in a dedicated ChatGPT conversation.
The headings below organise the original extraction instructions.

## Computational workflow architecture field — Final extraction rules

### Purpose

Describe the computational workflow implemented at each architectural layer, specifying what computational operations are performed at each layer of the system.
This field must represent the functional computational pipeline, not implementation details, software platforms, hardware specifications, or user-facing functionalities.
The objective is to enable comparison across studies by identifying where computational operations occur and which type of operations are executed.

### General extraction principles

1. Report computational operations only
Include only operations related to data processing, machine learning execution, or computational workflow.
Report:
•	biosignal acquisition
•	data acquisition (for non-biosignal inputs)
•	signal preprocessing
•	signal processing
•	feature extraction
•	feature transformation
•	feature selection
•	data augmentation
•	data integration
•	model training
•	model pretraining
•	model inference
•	classification
•	regression
•	prediction
•	decision making
•	decision fusion
•	multimodal fusion
•	severity assessment
•	risk assessment
•	event detection
•	alert generation
•	result generation
•	data storage
•	model aggregation
•	model updating
•	model synchronisation
•	model optimisation
•	model compression
•	performance evaluation
•	explainability analysis
•	visualisation (only when explicitly part of the computational system)

### 2. Remove implementation-specific details

Do not report:
•	software platforms:
o	Google Colab
o	MATLAB
o	TensorFlow
o	PyTorch
o	Flask
•	cloud providers:
o	AWS
o	Azure
o	Google Cloud
o	Oracle Cloud
•	programming frameworks
•	programming languages
•	specific algorithms or model names
Examples:
Replace:
Random Forest inference
with:
model inference
Replace:
CNN-based cough detection
with:
model inference
Replace:
FedAvg aggregation
with:
model aggregation
Replace:
MFCC extraction
with:
feature extraction
Replace:
Mel-spectrogram generation
with:
feature transformation

### 3. Remove user interaction elements

Exclude:
•	user interaction
•	questionnaire completion
•	symptom entry
•	participant recruitment
•	informed consent
•	clinician access
•	caregiver notification
•	dashboard access
•	application navigation
unless they directly represent a computational operation.
Example:
Original:
On-device: questionnaire completion; voice acquisition
Output:
On-device: biosignal acquisition

### 4. Remove communication operations by default

Do not report:
•	secure transmission
•	wireless transmission
•	Bluetooth communication
•	data upload
unless transmission is an essential computational operation of the architecture.
Exceptions:
Keep when explicitly related to:
•	federated learning:
o	model exchange
o	parameter transmission
•	distributed systems:
o	model synchronisation
•	edge-cloud computational pipelines where transmission defines the processing distribution.

### 5. Normalise operation terminology

Use the following mappings:
Original description	Normalised output
voice/speech/cough/breathing recording	biosignal acquisition
audio acquisition	biosignal acquisition
respiratory sound acquisition	biosignal acquisition
sensor acquisition	biosignal acquisition
FFT/MFCC/eGeMAPS extraction	feature extraction
Mel-spectrogram generation	feature transformation
spectrogram generation	feature transformation
signal denoising/filtering/enhancement	signal preprocessing
segmentation	signal preprocessing
normalisation/standardisation	signal preprocessing
PCA/LASSO/RFE/PSO/BALO feature selection	feature selection
GAN synthetic data generation	data augmentation
multimodal feature combination	multimodal fusion
late fusion/score fusion/probability fusion	decision fusion
classifier prediction	model inference
disease identification	classification
severity prediction	severity assessment
risk prediction	risk assessment
UPDRS prediction	severity assessment
retraining/fine-tuning/update	model updating
FedAvg/FedDyn aggregation	model aggregation
global model distribution	model synchronisation
complexity/runtime analysis	performance evaluation

### 6. Layer naming rules

Maintain the architectural layer explicitly reported by the article.
Allowed layers:
•	On-device
•	Edge
•	Cloud
•	Local workstation
•	Federated nodes
•	Federated server
•	Central server
•	IoT sensor nodes
•	Backend server
Do not reinterpret layers.
Examples:
Wearable device
→ keep as:
Wearable
if explicitly reported.
Edge (wearable patch)
→ keep:
Edge
Do not convert automatically to On-device.

### 7. Operation ordering

Within each layer, follow the computational workflow:
1.	Data/biosignal acquisition
2.	Signal preprocessing
3.	Feature extraction
4.	Feature transformation
5.	Feature selection
6.	Data augmentation
7.	Model training
8.	Model inference
9.	Classification/regression/prediction
10.	Decision making/fusion
11.	Assessment
12.	Alert generation
13.	Data storage
14.	Model updating/synchronisation
15.	Evaluation/visualisation
Only include explicitly reported operations.

### 8. Output format

Always provide a single line.
Format:
Layer: operation, operation, operation; Layer: operation, operation, operation.
Example:
Input:
Cloud (Google Colab): MFCC feature extraction; model training; model inference/testing; Random Forest late-fusion decision making; Random Forest retraining.
Output:
Cloud: feature extraction, model training, model inference, decision fusion, model updating.

### 9. Main distinction with related fields

Computational infrastructure
Answers:
What computational operations are performed at each layer?
Example:
Edge: biosignal acquisition, feature extraction, model inference.
Cloud: model aggregation, visualisation.
Architectural deployment strategy
Answers:
How are the layers distributed?
Example:
Edge-Cloud
Computing paradigm
Answers:
What computational model is used?
Example:
Cloud computing
Federated computing
Edge computing
This separation avoids redundancy between fields.

## Computational infrastructure — Final extraction rule

### Definition

Computational infrastructure describes the physical or virtual computational resources explicitly used to acquire, process, train, infer, store, or deploy the ML-based biosound system.
The field reports where the computation takes place and the type of computational resource involved, but does not describe the computational organisation or architecture (e.g., centralised, federated, edge–cloud), which is captured separately in Computing paradigm.

### General extraction principles

1. Report only explicitly mentioned infrastructures
•	Do not infer computational resources from:
o	ML algorithms;
o	software frameworks;
o	programming languages;
o	datasets;
o	deployment claims;
o	generic terms such as "server", "device", or "platform".
Examples:
✅ "NVIDIA RTX 3090 GPU" → Desktop workstation (GPU-accelerated)
❌ "Deep learning model implemented in Python" → no infrastructure inference.

### 2. Remove unnecessary hardware specifications

Do **not report:
•	CPU model;
•	GPU model;
•	RAM capacity;
•	storage capacity;
•	operating system;
•	software versions.
Keep only information relevant for infrastructure characterisation.
Example:
Original:
Intel Xeon Silver 4214 CPU; 230 GB RAM; NVIDIA RTX 2080 GPU
Extract:
✅ Desktop workstation (GPU-accelerated)

### 3. Preserve computational capability when relevant

The following modifiers should be included when explicitly reported:
Resource	Normalised output
GPU available	(GPU-accelerated)
CPU-only execution explicitly reported	(CPU-based)
NPU available	(NPU-accelerated)
Embedded microcontroller	(Embedded MCU)
FPGA hardware	FPGA
Examples:
•	NVIDIA RTX 4090 workstation
→ Desktop workstation (GPU-accelerated)
•	Raspberry Pi + Coral TPU
→ Edge device (NPU-accelerated)
•	STM32 Cortex-M7 wearable board
→ Wearable device (Embedded MCU)

### Taxonomy

1. User and mobile devices
Smartphone
Includes:
•	Android/iOS smartphones;
•	mobile applications executed on smartphones;
•	smartphone-based acquisition or inference.
Output:
Smartphone

### Tablet

Includes:
•	iPad;
•	Android tablets.
Output:
Tablet

### Laptop

Includes portable computers used for:
•	training;
•	inference;
•	processing.
Output:
Laptop
If acceleration is reported:
Laptop (GPU-accelerated)

### 2. Wearable and sensing devices

Wearable device
Includes:
•	smart bands;
•	wearable patches;
•	smart masks;
•	wearable sensing platforms;
•	wearable embedded systems.
Output:
Wearable device
With embedded processing:
Wearable device (Embedded MCU)

### Smartwatch

Includes:
•	Wear OS watches;
•	Apple Watch;
•	commercial smartwatches.
Output:
Smartwatch

### Smart sensor/device

Use when the device itself is relevant but does not fit wearable/mobile categories.
Examples:
•	smart stethoscope;
•	electronic stethoscope;
•	specialised biosensing device.
Outputs:
Electronic stethoscope
or
Smart sensor device

### 3. Edge and embedded infrastructure

Edge device
Includes:
•	Raspberry Pi;
•	NVIDIA Jetson;
•	embedded AI boards;
•	IoT gateways performing local computation.
Output:
Edge device
Add acceleration if explicitly reported:
•	Jetson GPU → Edge device (GPU-accelerated)
•	Edge NPU → Edge device (NPU-accelerated)
•	Raspberry Pi only → Edge device (Embedded board)

### Microcontroller

Use only when the microcontroller itself is the computational unit and not part of a larger wearable/IoT category.
Output:
Microcontroller
With embedded processing:
Microcontroller (Embedded MCU)

### FPGA

Includes:
•	FPGA boards;
•	FPGA-based accelerators.
Output:
FPGA
Do not add "FPGA-accelerated" because it is redundant.

### 4. Local computational infrastructure

Desktop workstation
Includes:
•	desktop PCs;
•	local machines used for training/evaluation.
Outputs:
Desktop workstation
Modifiers:
•	GPU → Desktop workstation (GPU-accelerated)
•	CPU only → Desktop workstation (CPU-based)
•	NPU → Desktop workstation (NPU-accelerated)

### Local server

Use only when a server infrastructure is explicitly mentioned without cloud characteristics.
Examples:
"backend server deployed locally"
→
Local server
Do not classify generic "server" as cloud.

### 5. Cloud infrastructure

Cloud resources must be classified according to the role of the cloud service, not the provider name alone.

### Cloud server (Public Cloud)

Use for public cloud computing providers:
Examples:
•	Amazon Web Services;
•	Microsoft Azure;
•	Google Cloud;
•	Alibaba Cloud;
•	Oracle Cloud.
Output:
Cloud server (Public Cloud)

### Cloud server (Private Cloud)

Use when authors explicitly mention:
•	private cloud;
•	institutional cloud infrastructure;
•	proprietary cloud infrastructure.
Output:
Cloud server (Private Cloud)

### Cloud server (Cloud computing platform)

Use when the cloud environment is a computational platform but no specific deployment role is reported.
Examples:
•	Google Colab;
•	cloud notebooks;
•	generic cloud computing environment.
Output:
Cloud server (Cloud computing platform)
If acceleration is explicitly reported:
Cloud server (Cloud computing platform; GPU-accelerated)

### Cloud server (Cloud storage service)

Use when the cloud is only used for storage/database purposes.
Examples:
•	Azure Storage;
•	cloud database.
Output:
Cloud server (Cloud storage service)

### Cloud server (Cloud inference platform)

Use when the cloud specifically provides inference services.
Examples:
•	ONNX Runtime inference server;
•	cloud AI inference API.
Output:
Cloud server (Cloud inference platform)

### Multiple infrastructures

When multiple computational infrastructures are reported:
•	Separate using +.
•	Preserve all relevant components.
•	Avoid excessive detail.
Example:
Original:
Android smartphone + Raspberry Pi 4 + NVIDIA RTX 3090 workstation + AWS
Output:
Smartphone + Edge device (Embedded board) + Desktop workstation (GPU-accelerated) + Cloud server (Public Cloud)

### Missing information rule

If computational infrastructure is not reported:
Output:
Not reported
Do not infer from:
•	federated learning terminology;
•	client/server terminology;
•	"local device";
•	"global model";
•	"cloud-based framework" unless a cloud infrastructure is explicitly described.
Example:
"Federated learning with local clients and central server"
Output:
Not reported

### Final quality-control checklist

Before assigning a value:
1.	Is the infrastructure explicitly reported?
→ If no: Not reported.
2.	Is it hardware, computational infrastructure, or only software?
→ Keep only hardware/infrastructure.
3.	Have unnecessary specifications been removed?
→ Keep only computationally relevant characteristics.
4.	Have GPU/CPU/NPU/MCU accelerators been preserved when explicitly reported?
→ Yes.
5.	Has no inference been made from architecture terms?
→ Yes.
6.	Is the output compatible with quantitative synthesis and comparison across studies?
→ Yes.

## Architectural deployment strategy

### Purpose

Architectural deployment strategy describes the computational architecture intentionally proposed by the authors as the target deployment model of the system, regardless of whether that architecture was fully implemented or only partially validated.
The objective of this field is not to assess implementation maturity, deployment readiness or experimental validation. These aspects are evaluated independently by Deployment maturity and Deployment level.
Instead, this field answers the following question:
According to the authors, where is computation intended to take place in the final system architecture?
The classification should therefore reflect the intended computational organisation of the proposed system rather than the experimental implementation used for validation.

### Relationship with other computational fields

Field	Purpose
Computational infrastructure	Describes which computational operations are executed at each layer.
Computational platform	Describes the physical hardware.
Architectural deployment strategy	Describes the intended computational architecture proposed by the authors.
Deployment maturity	Indicates whether that architecture has actually been implemented.

### Allowed taxonomy

Use exactly one value.
•	Local
•	Cloud
•	Edge
•	Edge–Cloud
•	Edge–Fog–Cloud
•	Federated Edge

### Definitions

Local
The proposed system is intended to execute on a single local computer or workstation.
No distributed computational architecture is proposed.
Examples
•	MATLAB implementation
•	Python desktop application
•	Google Colab experiment
•	Standalone workstation

### Cloud

The proposed architecture is centred on cloud computing.
Client devices may perform only:
•	data acquisition
•	user interaction
•	data transmission
without performing meaningful computational processing.
The cloud performs the computational intelligence of the system.
Typical examples
•	smartphone uploads audio
•	cloud performs preprocessing
•	cloud extracts features
•	cloud performs inference
•	cloud stores results
Uploading data does not constitute Edge computing.

### Edge

The proposed system performs the computational processing entirely on edge devices.
Typical edge computation includes
•	signal preprocessing
•	feature extraction
•	inference
•	local decision making
•	embedded ML
No cloud computing is involved.

### Edge–Cloud

The proposed architecture intentionally distributes meaningful computational processing between edge devices and cloud services.
The edge performs at least one computational stage beyond simple acquisition or transmission, such as
•	signal preprocessing
•	feature extraction
•	compression
•	quality assessment
•	local inference
•	partial inference
•	privacy-preserving processing
•	model adaptation
The cloud performs complementary processing such as
•	advanced inference
•	model aggregation
•	storage
•	longitudinal analysis
•	clinician dashboard
•	remote monitoring
Simply recording audio and uploading it to the cloud does not qualify as Edge–Cloud.

### Edge–Fog–Cloud

The proposed architecture explicitly defines three computational layers
•	Edge
•	Fog
•	Cloud
with computational processing occurring at each layer.

### Federated Edge

The proposed architecture is based on federated learning across distributed edge nodes.
This category takes precedence over all others.

### Classification rules

Rule 1
Classify the architecture intentionally proposed by the authors, not the experimental implementation.
Implementation maturity is captured separately.

### Rule 2

Ignore whether the architecture has been fully implemented.
If the paper explicitly proposes an intended deployment architecture, classify that architecture.

### Rule 3

Do not classify generic future work or speculative applications that are not presented as part of the proposed system.
Examples
•	Smart Healthcare
•	IoT
•	5G
•	6G
•	Telemedicine
•	Digital Twins
mentioned only as future possibilities.

### Rule 4

A client device performing only
•	recording
•	sensing
•	user interaction
•	data transmission
is not considered an Edge computing node.
Such systems are classified as Cloud.

### Rule 5

Edge computing requires meaningful computation to occur locally.
Examples include
•	preprocessing
•	denoising
•	feature extraction
•	compression
•	local AI inference
•	embedded ML
•	privacy-preserving local processing

### Rule 6

If meaningful computation occurs both locally and in the cloud
→ Edge–Cloud

### Rule 7

If all meaningful computation occurs locally
→ Edge

### Rule 8

If all meaningful computation occurs in the cloud
→ Cloud

### Rule 9

If no distributed architecture is proposed
→ Local

### Rule 10

If federated learning across distributed edge devices is proposed
→ Federated Edge
This rule overrides all others.

### Decision examples

Example 1
Smartphone records cough.
Uploads WAV.
Cloud extracts MFCC.
Cloud performs CNN.
Cloud stores results.
→ Cloud

### Example 2

Smartphone records cough.
Smartphone removes silence.
Smartphone extracts MFCC.
Cloud performs diagnosis.
→ Edge–Cloud

### Example 3

Smartphone records cough.
Smartphone performs TinyML inference.
No cloud.
→ Edge

### Example 4

Wearable computes features.
Fog gateway aggregates.
Cloud performs longitudinal analytics.
→ Edge–Fog–Cloud

### Example 5

Desktop MATLAB experiment.
Authors mention that the model could eventually be deployed on smartphones.
→ Local

## Deployment maturity field

### Purpose

The Deployment maturity field must describe the technological maturity of the proposed system, reflecting how close it is to practical implementation.
Unlike the Computing paradigm, this field evaluates the maturity of the solution, not where computation occurs.

### Allowed categories

Use only one of the following categories:
•	Pilot deployment
•	Functional Prototype
•	Concept validation

### Category definitions

Pilot deployment
The complete system has been deployed and evaluated in its intended environment with real users or clinical workflows.
Examples include:
•	hospitals;
•	homes;
•	community settings;
•	routine clinical practice;
•	real patients using smartphones or wearables.

### Functional Prototype

A functional hardware–software prototype has been implemented and experimentally validated on the intended computational platform.
Typical examples include:
•	smartphone applications;
•	smartwatch applications;
•	wearable systems;
•	FPGA implementations;
•	Jetson deployments;
•	IoT devices;
•	embedded systems.
Validation may still occur under controlled laboratory conditions.

### Concept validation

The study demonstrates methodological feasibility only.
Typical situations include:
•	offline benchmarking;
•	workstation-only evaluation;
•	simulations;
•	public datasets;
•	algorithmic validation;
•	conceptual deployment discussions;
•	computational complexity analyses.
This category also includes studies explicitly designed for future mobile, wearable or IoT deployment but without implementation on the target platform.

### Important rules

Rule 1
A deployment discussion does not increase maturity.
If the study merely proposes future deployment, classify it as:
Concept validation

### Rule 2

Running experiments on a workstation always corresponds to Concept validation unless a functional prototype is experimentally implemented on the target hardware.

### Rule 3

Hardware implementation takes precedence.
If inference is experimentally executed on smartphones, wearables, Jetson, FPGA or similar devices, classify as:
Functional Prototype
even if evaluation is limited to laboratory conditions.

### Rule 4

Real clinical use takes precedence over all other categories.
Studies evaluated in routine practice or with real end users should be classified as:
Pilot deployment

## Deployment level field

### Purpose

The Deployment level field must describe the degree to which the proposed system has progressed towards real-world implementation, independently of its computational environment.

### Allowed categories

•	Level A – Real-world deployment
•	Level B – Functional prototype
•	Level C – Concept validation

### Category definitions

Level A – Real-world deployment
The system has been implemented and evaluated within its intended operational environment.
Examples include:
•	hospitals;
•	homes;
•	community healthcare;
•	smartphones used by participants;
•	wearable devices used by participants;
•	clinical workflows;
•	telemedicine programmes.

### Level B – Functional prototype

A working system has been implemented on the intended deployment hardware but evaluated under controlled experimental conditions.
Examples include:
•	smartphone prototype;
•	smartwatch prototype;
•	wearable prototype;
•	FPGA implementation;
•	Jetson implementation;
•	IoT prototype;
•	embedded edge implementation.

### Level C – Concept validation

The study validates only the underlying methodology.
Typical characteristics include:
•	offline algorithm evaluation;
•	workstation-based experiments;
•	simulated architectures;
•	public benchmark datasets;
•	computational complexity analysis;
•	conceptual deployment discussions.
This category also includes studies whose intended deployment platform is explicitly stated but has not yet been implemented.

### Relationship with Computing paradigm

Examples:
Computing paradigm	Deployment level
Local workstation	Level C
Local workstation (consumer-device deployment discussed conceptually only)	Level C
Edge	Level B
On-device only	Level B
Hybrid (Wearable Edge + Cloud)	Level B
Smartphone evaluated in hospital	Level A
Wearable evaluated with patients	Level A

### Important rules

•	Computing paradigm and Deployment level evaluate different aspects and should not be confused.
•	Conceptual deployment proposals remain Level C, regardless of how detailed the deployment discussion is.
•	Real hardware implementation is required to achieve Level B.
•	Evaluation with end users or within real clinical workflows is required to achieve Level A.
