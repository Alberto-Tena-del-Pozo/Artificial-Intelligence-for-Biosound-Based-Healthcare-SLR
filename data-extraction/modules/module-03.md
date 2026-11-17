# Module 03

This module was used in a dedicated ChatGPT conversation.
The headings below organise the original extraction instructions.

## ML paradigm field

### Purpose

Describe the machine learning paradigm(s) explicitly implemented by the final proposed model or framework.
This field characterises how the proposed system learns, not which algorithms, architectures, optimisation methods, or feature engineering techniques are used.
Only report paradigms that are explicitly implemented as part of the final proposed methodology.

### Allowed taxonomy

Use only one or more of the following categories:
•	Traditional Machine Learning
•	Deep Learning
•	Ensemble Learning
•	Transfer Learning
•	Federated Learning
•	Split Learning
•	Self-supervised Learning
•	Reinforcement Learning
•	Generative AI
Do not introduce additional categories or alternative terminology.

### Definitions

### Traditional Machine Learning

Models based on manually engineered features combined with conventional machine learning algorithms.
Examples:
•	Support Vector Machine (SVM)
•	Random Forest
•	Logistic Regression
•	Decision Tree
•	K-Nearest Neighbours (KNN)
•	Naïve Bayes
•	Linear Discriminant Analysis (LDA)
•	Quadratic Discriminant Analysis (QDA)
•	Gradient Boosting
•	XGBoost
•	CatBoost
•	LightGBM

### Deep Learning

Models based on neural networks that automatically learn hierarchical feature representations.
Examples:
•	CNN
•	MLP
•	RNN
•	LSTM
•	BiLSTM
•	GRU
•	Transformer
•	Autoencoder (non-generative use)

### Ensemble Learning

Learning strategies that combine multiple predictive models into a single final prediction.
Examples:
•	Majority voting
•	Soft voting
•	Hard voting
•	Stacking
•	Bagging
•	Boosting
•	Random Forest
•	Gradient Boosting
•	AdaBoost
•	XGBoost (ensemble implementation)
Do not classify a study as Ensemble Learning simply because several classifiers are compared experimentally.
The ensemble itself must constitute the final proposed predictive model.

### Transfer Learning

Reuse or fine-tuning of pretrained models for the target task.
Examples:
•	VGG
•	ResNet
•	EfficientNet
•	MobileNet
•	wav2vec
•	HuBERT
•	Whisper
•	OPERA

### Federated Learning

Collaborative distributed learning through parameter exchange without sharing raw data.

### Split Learning

Distributed learning where different parts of a neural network are executed on different computational nodes.

### Self-supervised Learning

Representation learning using automatically generated supervisory signals.

### Reinforcement Learning

Learning through interaction with an environment using reward signals.

### Generative AI

Models explicitly designed to generate new data.
Examples:
•	GAN
•	Diffusion models
•	Variational Autoencoders (when used generatively)
•	Large Language Models used for generation
Do not classify standard autoencoders as Generative AI unless their generative capability is explicitly exploited.

### Classification rules

### 1. Report only implemented paradigms

Only report paradigms that are explicitly implemented in the proposed methodology.
Do not classify paradigms that are:
•	mentioned in the Introduction
•	discussed as future work
•	described as potential applications
•	shown only in conceptual diagrams
•	cited from previous studies

### 2. Multiple paradigms

Report multiple paradigms only when they are simultaneously implemented in the final proposed framework.
Examples:
CNN + Federated Learning
→
Deep Learning; Federated Learning
CNN + Transfer Learning
→
Deep Learning; Transfer Learning
CNN ensemble
→
Deep Learning; Ensemble Learning
Random Forest majority-voting ensemble
→
Traditional Machine Learning; Ensemble Learning
GAN + CNN classifier
→
Generative AI; Deep Learning
CNN + Random Forest late-fusion framework
→
Deep Learning; Traditional Machine Learning; Ensemble Learning

### 3. Do not confuse paradigms with techniques

The following belong to Applied ML techniques, not to ML paradigm:
•	Attention mechanisms
•	Multi-head attention
•	Feature selection
•	RFECV
•	PSO
•	Genetic algorithms
•	PCA
•	LDA (when used only for dimensionality reduction)
•	Optimisers
•	Loss functions
•	Data augmentation
•	Early fusion
•	Late fusion
•	Feature fusion
•	Hyperparameter optimisation
•	Bayesian optimisation
•	Grid Search
•	SHAP
•	LIME
•	Grad-CAM
•	Saliency maps
•	Knowledge distillation

### 4. Comparative studies

If the study only compares several algorithms and does not propose an integrated framework, classify the paradigm according to the best-performing final model only.
Example:
Compared models:
•	SVM
•	Random Forest
•	Logistic Regression
•	KNN
Best model:
Random Forest
→

### Traditional Machine Learning

Do not report all evaluated paradigms.

### 5. Hybrid frameworks

If the proposed methodology genuinely integrates multiple learning paradigms into a single predictive framework, report all implemented paradigms.
Example:
CNN feature extractor + Random Forest classifier + majority voting
→
Deep Learning; Traditional Machine Learning; Ensemble Learning

### 6. Proposed methodology takes precedence

The ML paradigm must always describe the final proposed methodology, never the complete list of evaluated algorithms.
Baseline models, comparison classifiers, ablation experiments, and alternative models must not influence the assigned paradigm unless they are explicitly integrated into the final proposed framework.

### Cross-field consistency

Before returning the extraction, verify that:
•	Every reported paradigm is explicitly implemented in the final proposed methodology.
•	Every reported paradigm is supported by the Proposed ML algorithm field.
•	Every reported paradigm is consistent with the Applied ML techniques field.
•	Comparative baseline models do not influence the assigned paradigm.
•	Feature engineering methods, optimisation procedures, explainability methods, and training strategies are not incorrectly classified as learning paradigms.
•	The ML paradigm is the highest-level conceptual description of how the proposed system learns, rather than a list of algorithms.

## Proposed ML algorithm field

### Purpose

The Proposed ML algorithm field must identify and describe the final machine learning algorithm, architecture, or framework proposed by the study.
This field aims to capture the main methodological contribution of the article from an algorithmic perspective.
The emphasis should be placed on the novel or final model introduced by the authors, rather than on baseline or comparative models.

### General principles

•	Report only the proposed/final model.
•	Prioritise the architecture that constitutes the principal contribution of the paper.
•	Use the official name provided by the authors whenever available.
•	If the study proposes a novel architecture, explicitly describe its main components.
•	If no novel algorithm is proposed, explicitly state this.
•	Do not list all baseline or comparison models.

### Reporting format

Use the following structure whenever possible:
<Official model name> (<acronym>) integrating <main architectural components>.
Examples:
CMF-Former-D (Contextual Multimodal Federated Transformer with Dual-Level Distillation) integrating Conformer-based audio encoding, MobileViT-Tiny image encoding, cross-modal attention, and dual-level knowledge distillation.
Dual-Stream Signal Processing Framework integrating SEResNet50, Squeeze-and-Excitation Mamba Modules (SEMBM), Gated Attention Fusion Modules (GAFM), and DeiT-based classification.
Federated CNN framework based on FedAvg aggregation for decentralized respiratory disease classification.

### Novel algorithms

When the authors propose a novel algorithm or architecture, explicitly describe:
•	official algorithm name;
•	acronym;
•	principal modules/components;
•	architectural paradigm if relevant.
Example:
SEMBM-Net, a novel respiratory sound classification architecture combining residual CNN blocks, Mamba state-space modules, and gated attention fusion.

### Non-novel studies

If the article does not propose a new algorithm and merely evaluates existing methods:
No novel machine learning algorithm was proposed. The study evaluated conventional SVM, Random Forest, and CNN classifiers.
Examples:
No novel machine learning algorithm was proposed. The study compared ResNet-50, MobileNet-V2, and VGG-16 architectures, with VGG-16 achieving the best performance.
No novel machine learning algorithm was proposed. The study evaluated conventional machine learning classifiers including SVM and Random Forest.

### Include

Examples include:
•	novel neural architectures;
•	novel fusion frameworks;
•	custom federated learning algorithms;
•	custom aggregation strategies;
•	newly designed hybrid pipelines;
•	custom ensemble architectures.

### Exclude

Do not include:
•	feature extraction methods;
•	preprocessing steps;
•	data augmentation techniques;
•	optimization algorithms;
•	training hyperparameters;
•	baseline models not constituting the main contribution.
Examples of incorrect entries:
MFCC extraction followed by data augmentation.
Adam optimizer with learning rate 0.001.

### Ensemble and hybrid systems

For ensemble or hybrid approaches, explicitly describe all principal components.
Example:
Hybrid ensemble framework combining CNN-based feature extraction, LSTM temporal modelling, and majority-voting classification.

### Federated learning studies

Describe both:
•	the learning framework;
•	the aggregation strategy if it represents a methodological contribution.
Example:
Decentralized federated learning framework using FairWeight-Gossip aggregation and dual-level knowledge distillation.

### Missing information

If the manuscript does not clearly identify the proposed model:
The proposed machine learning algorithm was not explicitly specified.
If no algorithmic contribution is proposed:
No novel machine learning algorithm was proposed.

### Examples

Correct:
CMF-Former-D integrating cross-modal attention and dual-level knowledge distillation.
No novel machine learning algorithm was proposed. The study evaluated VGG-16 and MobileNet-V2 architectures.
Incorrect:
MFCCs; spectrograms; Adam optimizer.

### Final quality check

Before finalising, verify that:
•	only the proposed/final model is described;
•	baseline models are excluded unless no novel model exists;
•	the official model name is preserved whenever available;
•	architectural novelty is clearly described;
•	preprocessing and training details are not included.

### Taxonomy

### Objective

Characterise the algorithmic family and architectural design of the proposed ML model.

### General rules

•	Describe the model family, not the application.
•	Include architectural families only when explicitly reported.
•	Multiple labels can be assigned separated by semicolons.
•	Avoid generic labels such as "AI model", "hybrid model", or "deep architecture".
•	Do not duplicate deployment information (edge/cloud/federated) here.
•	Do not include optimisation techniques unless they define the algorithm structure.
•	Feature selection methods alone do not define an algorithm taxonomy.
Format:
Category 1; Category 2; Category 3

### Base architecture categories

### CNN-based architecture

Use for convolutional neural network models.
Examples:
•	CNN
•	1D-CNN
•	2D-CNN
•	ResNet
•	MobileNet
•	DenseNet
•	ShuffleNet
•	EfficientNet
Output:

### CNN-based architecture

### RNN-based architecture

Use for recurrent neural network models.
Examples:
•	LSTM
•	GRU
•	BiLSTM
Output:
RNN-based architecture

### Transformer-based architecture

Use when Transformer models are central.
Examples:
•	Transformer encoder
•	Vision Transformer
•	Conformer
•	GPT/BERT-based models
•	Multimodal Transformer
Output:
Transformer-based architecture

### MLP-based architecture

Use for fully connected neural networks.
Examples:
•	ANN
•	DNN
•	FCNN
•	Multi-layer perceptron
Output:
MLP-based architecture

### Tree-based architecture

Use for tree-based classifiers/regressors.
Examples:
•	Random Forest
•	XGBoost
•	LightGBM
•	CatBoost
•	Extra Trees
Output:
Tree-based architecture

### Tree-based ensemble architecture

Use when multiple tree models are combined.
Examples:
•	RF + XGBoost + LightGBM voting
•	Multiple tree classifiers with ensemble fusion
Output:
Tree-based ensemble architecture

### Kernel-based architecture

Use for kernel learning approaches.
Examples:
•	SVM with RBF kernel
•	Polynomial SVM
•	Linear SVM
Output:
Kernel-based architecture

### Instance-based architecture

Use for similarity/distance-based methods.
Examples:
•	kNN
•	Nearest neighbour classification
Output:
Instance-based architecture

### Probabilistic architecture

Use for probabilistic classifiers.
Examples:
•	Naïve Bayes
•	Bayesian classifiers
•	Probabilistic graphical models
Output:
Probabilistic architecture

### Similarity-based architecture

Use when prediction is based on similarity matching rather than learned classification.
Examples:
•	Pearson correlation similarity
•	Template matching
•	Spectral similarity
Output:
Similarity-based architecture

### Hybrid architecture rules

Use when multiple model families are integrated.
Format:
Hybrid Family1-Family2 architecture
Examples:
CNN + LSTM:
Hybrid CNN-RNN architecture
CNN + Transformer:
Hybrid CNN-Transformer architecture
CNN + Random Forest:
Hybrid CNN-tree architecture
RNN + Decision Tree:
Hybrid RNN-tree architecture
CNN + LSTM + GNN:
Hybrid CNN-RNN-GNN architecture
Rules:
•	Capture model families, not modalities.
•	Do not use "Hybrid multimodal architecture".
•	Multimodal is an independent attribute.

### Additional architectural attributes

Multimodal
Use when multiple data modalities are jointly modelled.
Examples:
•	Voice + image
•	Speech + EEG
•	Audio + text
Output:
Multimodal

### Fusion-based

Use when combining modalities/models is an explicit architectural component.
Examples:
•	Early fusion
•	Feature fusion
•	Decision fusion
•	Score fusion
•	Late fusion
Output:
Fusion-based

### Attention-based architecture

Use when attention mechanisms are explicitly incorporated.
Examples:
•	Self-attention
•	Cross-attention
•	Multi-head attention
•	Attention blocks
Output:
Attention-based architecture

### Residual architecture

Use when residual connections define the architecture.
Examples:
•	ResNet
•	Residual CNN
Output:
Residual architecture

### Generative architecture

Use when generative networks define part of the model.
Examples:
•	GAN
•	Diffusion model
Output:
Generative architecture

### Knowledge distillation architecture

Use when teacher-student optimisation defines the architecture.
Output:
Knowledge distillation architecture
