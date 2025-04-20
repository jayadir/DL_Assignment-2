# DL_Assignment-2
# README for Machine Learning Projects

## 1. Latin to Devanagari Transliteration Model

### Overview
This project implements a sequence-to-sequence (seq2seq) model to transliterate Latin script words into Devanagari script (Hindi). The model is trained on the Dakshina dataset, which contains parallel Latin-Devanagari word pairs.

### Key Features
- Implements both SimpleRNN and LSTM-based seq2seq models
- Character-level translation approach
- Evaluation metrics for model comparison
- Sample translation demonstration

### Dataset
The model uses the Dakshina dataset (`hi.translit.sampled.*.tsv` files) containing:
- Training set: 48,524 word pairs
- Dev set: 500 word pairs
- Test set: 2,500 word pairs

### Model Architecture
1. **Encoder-Decoder Structure**:
   - Encoder: Processes input Latin characters
   - Decoder: Generates output Devanagari characters
2. **Embedding Layer**: 64-dimensional character embeddings
3. **Recurrent Layers**: 128-unit LSTM/RNN cells
4. **Dense Layer**: Softmax output over Devanagari vocabulary

### Performance
- LSTM model achieves 15.62% character-level accuracy
- SimpleRNN model achieves 13.36% character-level accuracy
![Screenshot 2025-04-20 123330](https://github.com/user-attachments/assets/25efc38b-47ca-4a7e-bc66-543b7f31ffa7)
![Screenshot 2025-04-20 123304](https://github.com/user-attachments/assets/f2bf66ce-e279-49fc-bd4c-dc11b5f21fc0)

### Usage
1. Run the notebook `translation-of-latin-to-dakshina.ipynb`
2. The complete pipeline includes:
   - Data loading and preprocessing
   - Model training
   - Evaluation
   - Sample translations

## 2. GPT-2 Fine-Tuning for Poetry Generation

### Overview
This project fine-tunes a GPT-2 model on Justin Bieber song lyrics to generate new poetic text in a similar style.

### Key Features
- Fine-tuning of pre-trained GPT-2 model
- Text generation with temperature sampling
- Custom tokenization and dataset preparation
- Model saving and reloading capability

### Dataset
- Justin Bieber lyrics dataset (`bieber.txt`)
- Contains 3,715 lines of song lyrics

### Model Specifications
- Base model: GPT-2 (124M parameters)
- Training:
  - Batch size: 4
  - Epochs: 5
  - Learning rate: 5e-5
- Generation parameters:
  - Temperature: 1.0
  - Top-k: 50-500
  - Max length: 256 tokens

### Usage
1. Run the notebook `Fine_tuning_gpt_2.ipynb`
2. The workflow includes:
   - Dataset loading
   - Tokenization
   - Model fine-tuning
   - Text generation
   - Model saving

### Example Output
```
First you wanna go to the left, then you wanna turn right
```
![Screenshot 2025-04-20 123712](https://github.com/user-attachments/assets/5bd8fc35-3e4a-4083-917b-cdf840d8f86c)

## Requirements
For both projects:
- Python 3.7+
- TensorFlow 2.x
- NumPy
- Pandas
- Transformers library (for GPT-2 project)

## Installation
```bash
pip install tensorflow numpy pandas transformers datasets
```

