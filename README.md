# PAPER PEEK
---

## Introduction:
Paper Peek is project based on Natural Language Processing which can help the medical professionals to read large paragraphs of abstracts of randomized controlled trials from papers and other articles. Automatically classifying each sentence in an abstract would help researchers read abstracts more efficiently, especially in fields where abstracts may be long, such as the medical field.

## PubMed 200k RCT dataset:
The PubMed 200k RCT dataset is described in Franck Dernoncourt, Ji Young Lee. [PubMed 200k RCT: a Dataset for Sequential Sentence Classification in Medical Abstracts](https://arxiv.org/abs/1710.06071). International Joint Conference on Natural Language Processing (IJCNLP). 2017.

**Abstract:**

> PubMed 200k RCT is new dataset based on PubMed for sequential sentence classification. The dataset consists of approximately 200,000 abstracts of randomized controlled trials, totaling 2.3 million sentences. Each sentence of each abstract is labeled with their role in the abstract using one of the following classes: background, objective, method, result, or conclusion. The purpose of releasing this dataset is twofold. First, the majority of datasets for sequential short-text classification (i.e., classification of short texts that appear in sequences) are small: we hope that releasing a new large dataset will help develop more accurate algorithms for this task. Second, from an application perspective, researchers need better tools to efficiently skim through the literature.

The Dataset is available here: [pubmed-rct](https://github.com/Franck-Dernoncourt/pubmed-rct)

## Different Modelling Experiments:
Paper Peek have different models implemented which are as follows:

| EXPERIMENTS | MODEL |
| ---- | ---- |
| Model 0 | Naive Bayes with TF-IDF encoder (baseline) |
| Model 1 | Conv1D with token embeddings |
| Model 2 | TensorFlow Hub Pretrained Feature Extractor |
| Model 3 | Conv1D with character embeddings |
| Model 4 | Pretrained token embeddings + character embeddings |
| Model 5 | Pretrained token embeddings + character embeddings + positional embeddings |

Above all the models, the **Model 5** is the best performing model.

## Features of Paper Peek:
* TF-IDF Vectorizer
* Token Embeddings
* Character Embeddings
* Positional Embeddings
* Find Most Wrong Predictions


## Model Visualizations:
* **Comparing Results:**
  ![](https://i.imgur.com/QIWwzyf.png)

* **Finding Most Wrong Predictions:**
  ![](https://i.imgur.com/EUQC4jU.png) 

* **Making predictions on example abstracts:**
  ![](https://i.imgur.com/uhhLxLl.png)
  

## Conclusion: 
The Model 5 is able to perform the best among all other models achieving the accuracy of about **83.67%.***
