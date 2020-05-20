---
title:  "Recommendation Systems on AWS: 1.0 - Item Similarity - Introduction"
date:   2020-06-02 23:37:00
categories: ai
---

<img src="https://source.unsplash.com/uENjpJ0sCb0/1600x900"/>

## Introduction
Ever wondered how Search engines such as Google or Bing find results that matches best your search term? 

What goes behind the scenes when
 you search for a movie on Netflix and the results that you get back? Sometimes you don't find a TV show that you are looking for  Most of
  the websites with any
  kind corpus
  has some
  sort of search
  functionality to help users find what they are looking for. TBT, if it was easy to build search engines, there would be tons
   of Googles around us but there is a lot more goes into building search engines of that scale. We will leave data mining for some other
    tutorial but for this one, we will cover modern search techniques using lucene based search tool .... [Elasticsearch](https://www
    .elastic.co/what-is/elasticsearch.)
    The more I learn about Elasticsearch, the more I realize how little I know about its capabilities.
    
Obviously there are times when Netflix disappoints you with it's results and not return what you want(sucks when it doesn't have it in it's corpus). Like the below ```Mandalorian``` search.

<p align="center">
  <img src="./../../../../../assets/images/netflix-mandalorian.png"/>
</p>
 
### How does search work?
I don't think anyone does it better than Google, so I will let them explain it to you.
 * [Google Search Text](https://www.google.com/search/howsearchworks/)
 * [Google Search Video](https://www.youtube.com/watch?v=cxWo4ttPgAc#t=04m38s)
 * [Google Rankings](https://ahrefs.com/blog/how-do-search-engines-work/)
 
Since our use case is a lot simpler, we will look at how Elasticsearch works.

Elasticsearch runs Lucene under the hood so by default it uses Lucene's Practical Scoring Function. 
This is a similarity model based on Term Frequency (tf) and Inverse Document Frequency (idf) aka TF/IDF. In recent versions of
 Elasticsearch it moved towards more optimized implementation of [similarity](https://www.elastic.co/guide/en/elasticsearch/reference/current/similarity.html) algorithm such as [Okapi BM25](https://en.wikipedia.org
 /wiki/Okapi_BM25). This makes Elasticsearch a really powerful tool to search items. The problem occurs when a we would like to recommend
  items based on their contextual meaning.
  
Let's say user searched for:
 * "Can puppy eat apricots?"

Our search engine should be able to recommend answer for:
 * "Can dogs eat apricots?"
 * "Are dogs allergic to apricots?"

TBH Elasticsearch does a great job at simple searches but we can modify it to use contextual meaning of the query terms to make our
 search 2x better if not more. 

### **Lexical Search**
Lexical search is a search implementation where the results are totally based on the occurrence of the search keywords. It is implemented
 using algorithms such as TF/IDF.

### **Semantic Search**
Semantic search uses contextual meaning of the documents. We can enhance it further by using Deeplearning to find best possible embedding
 that represents the whole sentence and even a complete article.

## What's next? 
In our next two tutorials, we will dive deeper into each technique and build a solution using Elasticsearch.
