# Next Word Predictor Using LSTM

This project demonstrates a text prediction model built with Long Short-Term Memory (LSTM) neural networks. It predicts the next word based on the given text input.

## Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Dataset](#dataset)
- [Installation](#installation)
- [Usage](#usage)
- [Model Architecture](#model-architecture)
- [Results](#results)
- [License](#license)

## Introduction
The **Next Word Predictor** is a deep learning project that uses LSTM to predict the next word based on a sequence of input text. The model is trained on a sample FAQ text about C++ programming, which serves as the vocabulary source.

## Features
- Tokenization of input text.
- Preprocessing using padded sequences.
- LSTM-based architecture for sequence prediction.
- Text generation based on user input.

## Dataset
The model is trained using sample FAQ text about C++ programming. The data is tokenized and converted into sequences for training.

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/Aishjahan/Next-Word-Predictor-using-LSTM.git
   cd next-word-predictor
   ```

2. Install dependencies 
  ```bash
    pip install tensorflow
  ```

## Usage
### Train the model:
Run the Python code to preprocess the text, create the LSTM model, and train it.
```bash
python next_word_predictor.py
```

### Generate predictions:
Enter a starting phrase (e.g., `c++ is a`), and the model will predict the next words.

## Model Architecture
The model consists of:
- **Embedding Layer**: Converts words to dense vector representations.
- **LSTM Layer**: Captures sequential dependencies.
- **Dense Layer**: Outputs predictions with `softmax` activation.

### Model summary:
```text
Layer (type)                 Output Shape              Param #
=================================================================
embedding (Embedding)        (None, 63, 100)           44900
lstm (LSTM)                  (None, 150)              150600
dense (Dense)                (None, 449)              67799
=================================================================
Total params: 263,299
Trainable params: 263,299
```

## Results
The model predicts the next words based on the given input text.

### Example:
- **Input**: `c++ is a`
- **Output**: `c++ is a powerful programming language`

## License
This project is licensed under the [MIT License](LICENSE).

