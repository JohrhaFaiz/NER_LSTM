

This project demonstrates how to build a Named Entity Recognition (NER) model using LSTM (Long Short-Term Memory) networks with PyTorch and TorchText.

NER is the process of identifying and classifying words in a sentence into predefined categories such as:
- Person names
- Locations
- Organizations
- Dates

## Project Goal
Train a deep learning model to recognize entities in text — such as people's names, locations, and other important keywords — based on labeled data.

## Technologies Used
- Python 3.x
- PyTorch 1.7.0
- TorchText 0.8.0
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Google Colab (for training)

## Dataset
We use a public NER dataset (`ner_dataset.csv`) which contains:
- Sentence # : ID of the sentence
- Word       : Each word in the sentence
- Tag        : The label/category of the word (e.g. B-PER, I-LOC, O)

## Steps in the Notebook

### 1. Setup
- Install required libraries
- Mount Google Drive (for dataset access)

### 2. Load and Clean Data
- Read CSV using pandas
- Drop unused columns and fill missing values
- Group words into sentences

### 3. Explore the Data
- Analyze sentence lengths
- Count number of unique words and tags

### 4. Prepare Data
- Split dataset into training and testing sets
- Convert words and tags into numerical format
- Create batches for training

### 5. Build the LSTM Model
- Use an embedding layer, LSTM layer, and linear output layer
- Input: Sequence of word indices
- Output: Predicted tag for each word

### 6. Train the Model
- Use cross-entropy loss and Adam optimizer
- Train for several epochs and monitor loss

### 7. Evaluate the Model
- Test on unseen data
- Calculate accuracy and F1-score

