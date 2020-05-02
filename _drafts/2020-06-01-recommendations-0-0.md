---
title:  "Recommendation Systems on AWS: 0.0 - Introduction"
date:   2020-06-01 23:37:00
categories: ai
---

### Table Of Contents:
> 1. [Introduction](#introduction)
> 2. [Terminology](#terminology)
> 3. [Technology Stack](#technology-stack)
> 4. [Bonus Tutorials](#bonus-tutorials)


## Introduction
A good recommendation system helps user to find useful item from a large collection. Two common use cases can be:
 * Quickly find related content : Recommend based on the item the user is currently looking at. When you are looking at an item to buy, Amazon.com might recommend similar items for the user to buy or compare.[**Content Based**]
 * Suggest items based on other users history: Recommed other items based on similar purchages in the past from other users. [**Collaborative**]

### Features For Common Types Of Recommendations:
> 1. Content-Based
>  * Metadata of the User (Cluster Similar Users)
>  * Metadata of the Article (Cluster Similar Articles)
> 2. Collaborative Filtering
>  * History of Articles read by the User
>  * History of Users who viewed an Article
> 3. Knowledge-Based
>  * Explicitly ask for User preferences
> 4. Deep Neural Network
>  * Recommend based on (User's history of Articles (LSTM) + Article's metadata)[RNN]

<p align="center">
  <img src="./../../../../../assets/images/recs-venn-hybrid.png"/>
</p>

## Terminology

1. **Items**: *Products from Amazon.com, Videos from Youtube, Apps on App Store, Articles on Reuters.com*
1. **Item Metadata**: *Information about the products such as Genre, Ratings, Price etc.*
1. **User Metadata**: *User information such as Age, Experience, Preferences etc.(We will implement some guards for our system to not
 discriminate based on Age and Gender etc.)*
1. **User/Item interactions**: *User logs and their actions such as Google analytics etc.*
1. **Embeddings**: *Converting variable features into a comparable dimension. It can be Text to Vectors or Features to Vectors.*

## Technology Stack
1. [Python](https://www.python.org/)
    - [Google Python Style Guide](http://google.github.io/styleguide/pyguide.html)
1. [Tensorflow](https://www.tensorflow.org/)
    - Serving
    - JS
    - Dashboard
1. [Spark](https://spark.apache.org/)
1. AWS
    - [S3](https://aws.amazon.com/s3/)
    - [Glue](https://aws.amazon.com/glue/)
    - [Athena](https://aws.amazon.com/athena/)
    - [Sagemaker](https://aws.amazon.com/sagemaker/)
        - Notebooks: Jupyter Lab
        - Tensoflow Serving
        - Github Version Control
    - [Personalize](https://aws.amazon.com/personalize/)
1. [Elasticsearch](https://aws.amazon.com/elasticsearch-service/)
1. [Benchmarking Nearest Neighbor Indexes](https://erikbern.com/2018/06/17/new-approximate-nearest-neighbor-benchmarks.html)
    - [Annoy](https://github.com/spotify/annoy) (Spotify)
    - [FAISS](https://github.com/facebookresearch/faiss) (Facebook)
    - [NMSLIB](https://github.com/nmslib/nmslib)
1. Algorithms
    - Matrix Factorization with (SGD & WALS)
    - Text Embedding (Universal Sentence Encoder, BERT Sentence Transformer etc...)


## Bonus Tutorials
1. [Tensorflow Serving on Sagemaker](../../../../2020/06/02/recommendations-1-2)
2. [Query CSV or JSON file stored in S3 using Glue and Athena](../../../../2020/06/02/recommendations-2-3)

<hr/>
# Recommendation Tutorial References:

### Tutorials
1. [Recommendation Systems on GCP](https://app.pluralsight.com/courses/2fdadde7-6d35-420f-94c9-65464d279321/table-of-contents)
1. [Onebar Semantic Search](https://blog.onebar.io/building-a-semantic-search-engine-using-open-source-components-e15af5ed7885)

### Papers
1. [Weighted Alternating Least Squares](http://cs229.stanford.edu/proj2017/final-posters/5147271.pdf)

### References
1. [Recommendation Systems Guide - Google](https://developers.google.com/machine-learning/recommendation)

### Good to Know
1. [Machine Learning Glossary](https://developers.google.com/machine-learning/glossary#top_of_page)
2. [A-Z AI Flashcards](https://atozofai.withgoogle.com/intl/en-GB/)


