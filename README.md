# BoolQ-T5: Fine-Tuned T5 Model for Boolean Question Answering

**BoolQ-T5**, a project that fine-tunes the T5 (Text-To-Text Transfer Transformer) model on the [BoolQ dataset](https://github.com/google-research-datasets/boolean-questions) to predict Yes/No answers for Boolean questions. This repository contains the implementation, preprocessing pipeline, hyperparameter analysis, and evaluation of the fine-tuned model.

## Project Overview

This project modifies and fine-tunes the T5 model to perform binary classification (Yes/No) on the BoolQ dataset. The pipeline includes data preprocessing, model training, hyperparameter tuning, and output post-processing to ensure accurate and interpretable results.

### Key Features
- **Model**: Fine-tuned T5 (small/base, depending on configuration) for Boolean question answering.
- **Dataset**: BoolQ training dataset, consisting of question-passage pairs with Yes/No labels.
- **Preprocessing**: Custom preprocessing of inputs and outputs to fit the T5 architecture and produce clear Yes/No predictions.
- **Hyperparameter Tuning**: Extensive analysis of key parameters to optimize model performance.

## Methodology

### Data Preprocessing
- Inputs are formatted as `"question: {question} context: {passage}"` to leverage T5's text-to-text framework.
- Outputs are preprocessed to extract and map model predictions to "Yes" or "No".

### Training
- The T5 model is fine-tuned on the BoolQ training set using a supervised learning approach.
- Key hyperparameters analyzed include:
  - **Batch Size**: Tested values like 8, 16, 32 to balance memory usage and training speed.
  - **Learning Rate**: Explored rates such as 1e-5, 3e-5, 5e-4 for optimal convergence.
  - **Sequence Length**: Adjusted max input/output lengths (e.g., 128, 256, 512) to handle varying question-passage sizes.

### Evaluation
- Model performance is evaluated on validation accuracy and loss.
- Hyperparameter configurations are compared to identify the best-performing setup.

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/shahJenil/BoolQ-T5.git
   cd BoolQ-T5
