---
title:  "Recommendation Systems on AWS: 0.0 - Introduction"
date:   2020-06-01 23:37:00
categories: ai
---

[Google Rec Systems](https://developers.google.com/machine-learning/recommendation)

### Table Of Contents:
> 1. [Introduction](#introduction)
> 2. [Architecture](#architecture)
> 3. [Technology Stack](#technology-stack)
> 4. [Bonus Resources](#bonus-resources)


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

## Architecture



## Technology Stack


## Bonus Tutorials
1. [Tensorflow Serving on Sagemaker]()
2. [Query CSV or JSON file stored in S3 using Glue and Athena]()


