# AI-Powered Autism Screening and Personalized Therapy

## Published Research

This repository contains the implementation associated with our published research paper:

**AI-Powered Personalized Therapy for Children with Autism: A Reinforcement Learning Approach**

**Published in the proceedings of the 2025 International Conference on Advances in Machine Intelligence and Cybersecurity Technologies (AMICT), IEEE.**

The study explores AI-based autism screening and investigates architectures that could support future personalized and adaptive therapy systems.

---

## Research Objective

Autism Spectrum Disorder (ASD) presents challenges in both early screening and individualized therapy because symptoms, behavioral characteristics, and developmental trajectories can vary significantly between individuals.

This research aimed to:

- develop robust AI models for ASD-related screening,
- investigate a reinforcement-learning-inspired approach for future adaptive therapy recommendations,
- compare deep learning architectures for prediction performance and stability,
- examine important behavioral and demographic features related to ASD screening.

---

## Dataset

The study uses the **Autistic Spectrum Disorder Screening Data for Adults** dataset containing **704 records**.

The dataset includes:

- AQ-10 behavioral screening responses,
- demographic variables,
- background information,
- ASD screening labels.

The class distribution contains approximately:

- **515 non-ASD records**
- **189 ASD records**

The original study preserved this class imbalance rather than applying synthetic oversampling.

---

## Models Implemented

Two main neural architectures were investigated.

### 1. Regularized DQN-Inspired Neural Network

The first model is inspired by **Deep Q-Network (DQN)** architectures.

The model includes:

- fully connected neural layers,
- Layer Normalization,
- dropout regularization,
- Gaussian input noise,
- L1/L2 regularization,
- early stopping,
- adaptive learning-rate scheduling.

Because the available dataset is static rather than longitudinal therapy-session data, the model is used as a **DQN-inspired classification architecture rather than a complete reinforcement learning environment**.

### 2. Transformer-Based Neural Network

The second model applies a transformer architecture adapted for tabular data.

It includes:

- feature embeddings,
- positional encodings,
- multi-head attention,
- transformer encoder layers,
- Layer Normalization,
- dropout,
- global mean pooling,
- label smoothing.

The transformer architecture was designed with the possibility of future extension toward longitudinal and session-based therapy personalization.

---

## Key Results

Both models achieved very high predictive performance in the experiments reported in the paper.

| Model | Accuracy | Precision | Recall | F1-Score | AUC-ROC |
|---|---:|---:|---:|---:|---:|
| Regularized DQN | 99.53% | 99.54% | 99.53% | 99.53% | 1.0000 |
| Regularized Transformer | 99.81% | 99.67% | 99.41% | 98.57% | 0.9954 |

The transformer achieved the highest reported accuracy, while the DQN-inspired model achieved the highest reported AUC-ROC.

---

## Research Significance

This project explores how advanced neural architectures can support ASD screening while also providing a foundation for future adaptive therapy systems.

The published work positions the current models as a starting point for more advanced systems using:

- longitudinal therapy-session data,
- sequential patient feedback,
- adaptive intervention strategies,
- reinforcement-learning environments,
- larger and more diverse clinical datasets.

---

## My Contribution

As the first author of this research, my contributions included:

- Contributing to the formulation of the research problem and overall study methodology.
- Preparing and preprocessing the autism screening dataset for model development.
- Implementing the regularized DQN-inspired neural network and transformer-based model in Python.
- Training and evaluating the models using accuracy, precision, recall, F1-score, and AUC-ROC.
- Performing model performance analysis, including confusion-matrix and training/validation analysis.
- Conducting feature-importance analysis to investigate influential behavioral and demographic predictors.
- Interpreting the experimental results and identifying limitations and directions for future longitudinal reinforcement-learning research.
- Contributing to the literature review, manuscript preparation, technical writing, and revision of the published paper.

## Repository Structure

```text
AI-Powered-Autism-Screening-and-Personalized-Therapy/
│
├── README.md
│
├── data/
│   └── autism_screening.csv
│
├── notebooks/
│   └── autism_screening_dqn_transformer.ipynb
│
└── figures/
