# Multilingual Language Identification

A Natural Language Processing project for identifying the language of a given text across **20 languages** using traditional machine learning techniques and an optional large language model experiment.

The project compares multiple feature extraction methods and classifiers. The best-performing traditional approach achieved approximately **99.39% accuracy** using **Linear SVM with Character-Level TF-IDF**.

## Overview

Language identification is an important preprocessing task in multilingual NLP systems such as machine translation, search engines, chatbots, sentiment analysis, and virtual assistants.

This project explores how different text representations and machine learning models affect multilingual language classification performance.

## Key Features

* Language identification across 20 languages
* Text cleaning and preprocessing
* Bag of Words representation
* Word-Level TF-IDF
* Character-Level TF-IDF
* Naive Bayes classifier
* Logistic Regression classifier
* Support Vector Machine (SVM)
* Model comparison and evaluation
* Confusion matrix visualization
* Optional ALLAM large language model experiment
* Optional Gradio interface for interactive prediction

## Best Result

The strongest traditional machine learning configuration was:

**Character-Level TF-IDF + Linear SVM**

with an accuracy of approximately:

**99.39%**

Character-level features performed especially well because they capture language-specific character patterns, spelling structures, and writing systems.

## Dataset

The project uses the **Language Identification Dataset | 20 Languages** available on Kaggle.

Dataset:
https://www.kaggle.com/datasets/mabubakrsiddiq/language-identification-dataset-20-languages

Download the dataset and place `train.csv` in the same directory as the notebook before running it.

## Project Structure

```text
multilingual-language-identification/
│
├── language\\\\\\\\\\\\\\\_identification.ipynb
├── README.md
├── requirements.txt
└── .gitignore
```

## Technologies

* Python
* Pandas
* NumPy
* NLTK
* Scikit-learn
* Matplotlib
* Hugging Face Transformers
* Gradio
* PyTorch

## Installation:

Clone the repository:o

```bash
git clone https://github.com/ReemAhmadi/multilingual-language-identification.git
cd multilingual-language-identification
```

Install the required packages:

```bash
pip install -r requirements.txt
```

Then download `train.csv` from the Kaggle dataset linked above.

## Running the Project

Open:

```text
language\\\\\\\\\\\\\\\_identification.ipynb
```

using Jupyter Notebook, JupyterLab, VS Code, or Google Colab and run the cells in order.

## Experiments

The notebook compares:

|Feature Representation|Models|
|-|-|
|Bag of Words|Naive Bayes, Logistic Regression, SVM|
|Word-Level TF-IDF|Naive Bayes, Logistic Regression, SVM|
|Character-Level TF-IDF|Naive Bayes, Logistic Regression, SVM|

Additional preprocessing experiments include:

* Stop-word removal
* Stemming
* Lemmatization

## Optional ALLAM Experiment

The notebook also contains an optional experiment using the `ALLaM-AI/ALLaM-7B-Instruct-preview` model for prompt-based language identification.

To run this section in Google Colab:

1. Use a compatible GPU runtime.
2. Add your Hugging Face token to **Colab Secrets**.
3. Save the secret using the name `HF\\\\\\\\\\\\\\\_TOKEN`.
4. Never place access tokens directly inside the notebook.

## Interactive Demo

An optional Gradio interface is included in the notebook for entering text and receiving a predicted language.

> Gradio public share links generated from Colab are temporary and are therefore not included as permanent project links.

## Notes

* The dataset itself is not included in this repository.
* Hugging Face access tokens and other secrets should never be committed to GitHub.
* The ALLAM section is optional and is not required to reproduce the traditional machine learning results.

## Future Improvements

Potential extensions include:

* Testing performance on very short or noisy text
* Evaluating code-switched and mixed-language inputs
* Comparing additional multilingual transformer models
* Deploying the best model as a permanent web application
* Adding automated tests and a lightweight inference API

