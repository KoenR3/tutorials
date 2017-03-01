---
layout: tutorial
title: A Hands-On Tour of Apache Spark in 5 Minutes
tutorial-id: 360
tutorial-series: Spark
tutorial-version: hdp-2.6.0
intro-page: true
components: [ spark, zeppelin ]
---

![](https://raw.github.com/hortonworks/tutorials/hdp-2.6/assets/a-tour-of-spark-in-5-minutes/spark-logo.png)

Apache Spark is a fast, in-memory data processing engine with elegant and expressive development APIs in Scala, Java, Python, and R that allow developers to execute a variety of data intensive workloads.

In this tutorial, we will use an [Apache Zeppelin](https://zeppelin.apache.org/) notebook for our development environment to keep things simple and elegant. Zeppelin will allow us to run in a pre-configured environment and execute code written for Spark in Scala and SQL, a few basic Shell commands, pre-written Markdown directions, and an HTML formatted table.

### The Dataset

![](https://raw.githubusercontent.com/roberthryniewicz/images/master/silicon_valley_corporation.jpg)

To make things fun and interesting, we will introduce a film series dataset from the [Silicon Valley Comedy TV show](http://www.imdb.com/title/tt2575988/) and perform some basic operations with Spark in Zeppelin.

### Prerequisites

This tutorial is a part of series of hands-on tutorials to get you started with Hortonworks Data Platform (HDP) using either the [Hortonworks Data Cloud (HDCloud)](https://hortonworks.com/products/cloud/aws/) or a pre-configured downloadable [HDP Sandbox](https://hortonworks.com/products/sandbox/).

To complete this tutorial, choose one of the following deployment options:

#### Option 1: Setup Hortonworks Data Cloud (HDCloud) on AWS

1a. Create an [Amazon Web Services (AWS) Account](https://aws.amazon.com/) if you don't have one

1b. Follow this step-by-step doc to [Setup and Launch a Controller on HDCloud](http://hortonworks.github.io/hdp-aws/launch/index.html)

1c. Create a *Data Science* [Cluster](http://hortonworks.github.io/hdp-aws/create/index.html) (use settings listed below)

Select/specify the following for your cluster:

  - HDP Version: HDP 2.6 or later
  - Cluster Type: "Data Science: Apache Spark 2.1+, Apache Zeppelin 0.6.2+" or later
  - Worker instance count: one or more
  - Remote Access: 0.0.0.0/0

Here's a screenshot with sample settings:

![setting-up-hd-cloud](https://raw.github.com/hortonworks/tutorials/hdp-2.6/assets/a-tour-of-spark-in-5-minutes/spinning-up-hdcloud-cluster.jpg)

#### Option 2: Download and Setup Hortonworks Data Platform (HDP) Sandbox

This option is optimal if you prefer to run everything in local environment (laptop/PC).

Keep in mind, that you will need **8GB** of memory dedicated for the virtual machine, meaning that you should have at least **12GB** of memory on your system.

2a. Download and Install [HDP Sandbox 2.6](http://hortonworks.com/products/sandbox/)

2b. Review [Learning the Ropes of HDP Sandbox](http://hortonworks.com/hadoop-tutorial/learning-the-ropes-of-the-hortonworks-sandbox/)

#### Review Zeppelin Tutorial (optional)

If you are new to Zeppelin, review the following tutorial [Getting Started with Apache Zeppelin](https://github.com/hortonworks/tutorials/blob/hdp-2.5/tutorials/hortonworks/getting-started-with-apache-zeppelin/tutorial.md)

### Introduction

As mentioned earlier, we will download and ingest an external dataset about the Silicon Valley Show episodes into a Spark Dataset and perform basic analysis, filtering, and word count.

Spark Datasets are strongly typed distributed collections of data created from a variety of sources: JSON and XML files, tables in Hive, external databases and more. Conceptually, they are equivalent to a table in a relational database or a DataFrame in R or Python.

After a series of transformations, applied to the Datasets, we will define a temporary view (table) that you will be able to explore using SQL queries. Once you have a handle on the data and perform a basic word count, we will add a few more steps for a more sophisticated word count analysis.

By the end of this tutorial, you should have a basic understanding of Spark and an appreciation for its powerful and expressive APIs with the added bonus of a developer friendly Zeppelin notebook environment.

### Notebook Preview

Before you start, here's a preview of the notebook.

![](https://raw.github.com/hortonworks/tutorials/hdp-2.6/assets/a-tour-of-spark-in-5-minutes/notebook-preview-large.jpg)

### Start the Tutorial

To begin the tutorial, import the *Apache Spark in 5 Minutes* notebook into your Zeppelin environment. (If at any point you have any issues, make sure to checkout the [Getting Started with Zeppelin](https://hortonworks.com/hadoop-tutorial/getting-started-apache-zeppelin/) tutorial.)

On the Zeppelin home screen click `Import note` -> `Add from URL` and copy and paste the following URL: https://raw.githubusercontent.com/hortonworks-gallery/zeppelin-notebooks/hdp-2.6/2CBTZPY14/note.json

Once your notebook is imported, you can open it from the Zeppelin home screen by clicking
`Getting Started` -> `Apache Spark in 5 Minutes`

 Once the *Apache Spark in 5 Minutes* notebook is up, follow all the directions within the notebook to complete the tutorial.

### Final words

We hope that you've been able to successfully run this short introductory notebook in either your cloud or local environment and we've got you interested and excited enough to further explore Spark with Zeppelin.

Make sure to checkout other [tutorials](https://hortonworks.com/tutorials/) for more in-depth examples of the Spark SQL module, as well as other Spark modules used for Streaming and/or Machine Learning tasks.
