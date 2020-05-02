---
title:  "Recommendation Systems on AWS: 1.1 - Item Similarity - Lexical"
date:   2020-06-02 23:37:00
categories: ai
---

### Table Of Contents:
> 1. [Introduction](#introduction)
> 2. [Architecture](#architecture)
> 3. [Technology Stack](#technology-stack)
> 4. [Bonus Resources](#bonus-resources)

{% gist 596747c81ef295aaa5618cfc3367dc22 app.py %}


## Introduction
Benefits of recommendations (Two examples):
 * Quickly find related content : Recommend based on your history (like or dislike)
 * Explore New Content: Recommend some new things (Expanding the scope)
 
### Targets (Goal)
Recommend Articles User might be interested in.

### Features For Common Types Of Recommendations:
> 1. Content-Based
>  * Metadata of the User (Cluster Similar Users)
>  * Metadata of the Article (Cluster Similar Articles)
> 2. Collaborative Filtering
>  * History of Articles read by the User
>  * History of Users who viewed an Article
> 3. Knowledge-Based



## Architecture

{% gist 596747c81ef295aaa5618cfc3367dc22 text2vec.py %}

## Technology Stack

{% gist 596747c81ef295aaa5618cfc3367dc22 index-elasticsearch.py %}

<script src="https://gist.github.com/dhruvpratapsingh/596747c81ef295aaa5618cfc3367dc22.js?file=text2vec.py"></script>

## Bonus Resources
