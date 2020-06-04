---
title:  "Recommendation Systems on AWS: 1.1 - Item Similarity - Lexical"
date:   2020-06-02 23:37:00
categories: ai
---

<div align="center">
    <span>
        <a target="_blank" href="https://www.kaggle.com/dataset/4b34e8bfef6e12a3b3115ca2ac3f84451f5dd2b805d49ebb3b9a24d345045af9">Data
        </a><span> | </span><a
         href="https://github.com/dhruvpratapsingh/recommendation-systems" target="_blank">Code</a>
    </span>
</div>

### Table Of Contents:
> 1. [Install Elasticsearch: Local & AWS](#install-elasticsearch)
> 1. [Create Index and Mappings](#create-index-and-mappings)
> 1. [Use Elastichead](#elastichead)
> 1. [Insert single log to elasticsearch](#insert-document)
> 1. [Use JQ to do bulk insert](#bulk-insert-using-jq)
> 1. [Use MLT query perform Lexical Recommendations](#More-Like-This-Search)
> 1. [Next Steps](#next-steps)

# Install Elasticsearch

### Install on Local: Docker
If you would like to install Elasticsearch locally you can follow these instructions [Install: Docker + Elasticsearch](https://www.elastic.co/guide/en/elasticsearch/reference/current/docker.html)
For this tutorial I will be using local instance of ES cluster with a single node, it saves us money as ES cluster on AWS is slightly
 expensive.

### Create ES Instance on AWS
If you would like to create an ES(Elasticsearch) cluster on AWS you should be able to follow below steps.

#### Search ES service on AWS.
<p align="center">
  <img src="./../../../../../assets/images/create-es1.png"/>
</p>

#### Click on `Create a new domain`
<p align="center">
  <img src="./../../../../../assets/images/create-es2.png"/>
</p>

#### Choose deployment type
<p align="center">
  <img src="./../../../../../assets/images/create-es3.png"/>
</p>

#### Configure domain
<p align="center">
  <img src="./../../../../../assets/images/create-es4.png"/>
</p>

#### Configure access and security
<p align="center">
  <img src="./../../../../../assets/images/create-es5.png"/>
</p>

#### Review all of the settings. (Screenshot is cut-off)
<p align="center">
  <img src="./../../../../../assets/images/create-es6.png"/>
</p>

#### VPC endpoint below is the domain that we can use to perform ES actions. It is comparable to localhost:9200, when we run ES on localhost.
<p align="center">
  <img src="./../../../../../assets/images/create-es7.png"/>
</p>

### Get the status of our ES index.
If your cluster is deployed on AWS you will see different build types compare to below which says `docker`.
<p align="center">
  <img src="./../../../../../assets/images/es-index.png"/>
</p>

### Create Index and Mappings

#### We can create new index named analytics using below command.

Here is the Put request body:
{% highlight json %}

{
  "mappings": {
    "properties": {
      "visitor_id": {
        "type": "keyword"
      },
      "content_id": {
        "type": "keyword"
      },
      "category": {
        "type": "keyword"
      },
      "title": {
        "type": "text"
      },
      "author": {
        "type": "text"
      }
    }
  }
}

{% endhighlight %}

If the command is successful, you should see response similar to below.
<p align="center">
  <img src="./../../../../../assets/images/create-index-mappings.png"/>
</p>

#### List all the indexes.
<p align="center">
  <img src="./../../../../../assets/images/index-list.png"/>
</p>

# Use Elastichead
There are several plugins or apps you can use to explore Elasticsearch Data including Kibana and Elastichead etch. For the purpose of
 this tutorial we will use Elastichead as it's a simple [Chrome Plugin.](https://chrome.google.com/webstore/detail/elasticsearch-head/ffmkiejjmecolpfloofpjologoblkegm?hl=en-US)

We can see our newly created `analytics` index show below. We will go through a lot more tips & tricks to search documents and do
 aggregations etc.
<p align="center">
  <img src="./../../../../../assets/images/elastichead.png"/>
</p>

# Insert single item to Elasticsearch


# Use JQ to do bulk insert
[JQ](https://stedolan.github.io/jq/) is one of the most useful tools if you ever want to modify JSON objects. I stumbled upon a blog post
 from [Kevin Marsh](https://kevinmarsh.com/2014/10/23/using-jq-to-import-json-into-elasticsearch.html). We will use JQ to bulk upload the
  data to Elasticsearch.

# Use MLT query perform Lexical Recommendations


# Next Steps
In the next tutorial we will extend our similarity search to use Semantics to find similar documents in addition to just using Lexical
 strategy.
