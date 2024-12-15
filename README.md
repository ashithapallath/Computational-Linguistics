# Computational-Linguistics
This repository applies computational techniques to process and analyze natural language. It includes functions for tokenization, spelling correction, and bigram probability calculation to improve text accuracy and meaning. The program identifies misspelled words, suggests corrections, and evaluates sentence structure based on language models.

# Computational Linguistics Lab

## Overview
This repository contains implementations for various computational linguistics tasks. The goal is to explore and implement key concepts of text processing, language modeling, and machine learning for linguistic analysis.

## Lab Cycles

### Lab Cycle 1


- **Text Tokenizer**: Implement a rule-based text tokenizer for the English language using regular expressions. This tokenizer handles punctuation, special symbols, contractions (e.g., "isn't" → "is" and "n't"), abbreviations (e.g., "U.S.A"), and internal hyphenation (e.g., "ice-cream").

- **Finite State Automata (FSA)**: Design and implement an FSA that accepts English plural nouns ending with the character 'y' (e.g., "boys", "ponies", "puppies") but not incorrectly formed plurals (e.g., "boies", "ponys").

- **Finite State Transducer (FST)**: Implement an FST that generates plural forms of English words based on the e-insertion rule (e.g., "fox^s#" → "foxes", "boy^s#" → "boys").

- **Minimum Edit Distance Algorithm**: Implement the Minimum Edit Distance algorithm to compute the edit distance between two strings, including the edit operations.

---

### Lab Cycle 2


- **Statistical Spell Checker**:
    - Tokenize the corpus and create a vocabulary of unique words.
    - Create a bigram frequency table for all possible bigrams.
    - Detect non-word spelling errors in the input text.
    - Generate candidate corrections using 1 edit distance from misspelled words.
    - Suggest the best candidate by calculating the probability of the sentence using the bigram language model.

- **Sentiment Analysis with Naive Bayes**:
    - Implement a text classifier for sentiment analysis using the Naive Bayes theorem.
    - Use Add-k smoothing to handle zero probabilities.
    - Compare classifier performance for different values of k (0.25, 0.75, and 1).

---

### Lab Cycle 3


- **Viterbi Algorithm**: Implement the Viterbi algorithm to find the most probable Part-of-Speech (POS) tag sequence for a given sentence, using given probabilities.

- **Bigram Probability Calculation**: Write a Python program to calculate bigrams from a given corpus and compute the probability of any sentence.

- **TF-IDF Matrix**: Compute the TF-IDF matrix for a set of training documents. Also, calculate cosine similarity between any two given documents or words.

- **PPMI Matrix**: Compute the PPMI matrix for a set of training documents. Also, calculate cosine similarity between any two given documents or words.

- **Naive Bayes with Add-1 Smoothing**: Implement a Naive Bayes classifier with Add-1 smoothing and use it to disambiguate words in a given test sentence using the Bag-of-Words model.

  **Sample Input**:
  1. Sentence: "I love fish. The smoked bass fish was delicious." | Sense: fish
  2. Sentence: "The bass fish swam along the line." | Sense: fish
  3. Sentence: "He hauled in a big catch of smoked bass fish." | Sense: fish
  4. Sentence: "The bass guitar player played a smooth jazz line." | Sense: guitar

  **Test Sentence**: "He loves jazz. The bass line provided the foundation for the guitar solo in the jazz piece."
  **Test Word**: bass

  **Output**: guitar

---

## Requirements

- Python 3.x
- Libraries: `re`, `nltk`, `sklearn`, `numpy`, `pandas` (install using `pip`)

## Installation

Clone the repository and install the necessary dependencies:

```bash
git clone https://github.com/ashithapallath/computational-linguistics-lab.git
cd computational-linguistics-lab
pip install -r requirements.txt
```
## Usage
To run the implementations in Google Colab, follow these steps:

1.Upload the Python scripts to your Colab environment.

2.Run each script cell to test the implementations. Each script includes sample inputs and expected outputs for validation.
## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
