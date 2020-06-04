---
title:  "Finance: Sentiment Analysis of Tesla Stock"
date:   2020-09-01 05:37:00
categories: finance
---


## Text Processing
I will be following a chapter([Determining The Vocabulary Of Terms](https://nlp.stanford.edu/IR-book/html/htmledition/determining-the-vocabulary-of-terms-1.html)) from Christopher Manning's book [Introduction to Information Retrieval](https://nlp.stanford.edu/IR-book/html/htmledition/irbook.html) 

### **Getting Text Data**
From API, CSV file, Plain Text

### **Cleaning**
Parse text from the data. HTML: BeautifulSoup

### **Normalization**
* Lowercase
* Remove Special Characters (spaces, punctuations)

### **Tokenization**
Split sentences into words or tokens.
NLTK does a better job than simple `re` split, most of the times.

### **Remove Stop Words**
* Reduces the size of the text
* Removes unimportant words

There might be applications where the stop words might end up being useful, so be careful.

### **Stemming & Lemmatization**
* Porter, Snowball stemmers etc
* Wordnet
    Lemmatization: Reduce to its root form am, are, is -> be
    
Lemmatization needs a dictionary but Stemming doesn't need one. This makes Stemming a lot more memory efficient, but slightly less correct.

> 1. Stemming and Lemmatization both generate the root form of the inflected words. The difference is that stem might not be an actual word
> whereas, lemma is an actual language word.
>
> 1. Stemming follows an algorithm with steps to perform on the words which makes it faster. Whereas, in lemmatization, you used WordNet
> corpus and a corpus for stop words as well to produce lemma which makes it slower than stemming. You also had to define a parts-of-speech to obtain the correct lemma.
> \- [datacamp.com](https://www.datacamp.com/community/tutorials/stemming-lemmatization-python)
 

### **Parts of Speech Tagging**

### **Named Entity Recognition**
word_tokenize -> pos_tag -> ne_chunk

## Feature Extraction


### BOW (Bag of Words)

### TF-IDF

### One-Hot Encoding

### Word Embeddings

### Word2Vec

### Glove

### Embeddings for Deep Learning

### Dimensionality Reduction: t-SNE vs PCA
t-SNE is better as it keeps the relative information.

## Analyzing 10-k document

### Readability
Here is an IEEE paper you might want to read on [Readability Equation Consistencies](http://umich.edu/~driving/publications/ZhouHeejinGreenHowConsistReadability.pdf). 

1. Flesch-Kincaid Grade Index
1. Gunning-Fog Grade Index

### Sentiment


### Similarity




