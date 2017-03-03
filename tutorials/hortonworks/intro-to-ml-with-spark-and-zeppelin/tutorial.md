---
layout: tutorial
title: Intro to Machine Learning with Spark and Zeppelin
tutorial-id: 367
tutorial-series: Spark
tutorial-version: hdp-2.6.0
intro-page: true
components: [ spark, zeppelin ]
---

![](https://raw.github.com/hortonworks/tutorials/hdp-2.6/assets/intro-to-ml-with-spark-and-zeppelin/spark-mllib-logo.png)

In this tutorial, we will introduce you to Machine Learning with Apache Spark. The hands-on lab for this tutorial is an Apache Zeppelin notebook that has all the steps necessary to ingest and explore data, train, test, visualize, and save a model. We will cover a basic Linear Regression model that will allow us perform simple predictions on a sample data. This model can be further expanded and modified to fit your needs. Most importantly, by the end of this tutorial, you will understand how to create an end-to-end pipeline for setting up and training simple models in Spark.

### Prerequisites

This tutorial is a part of series of hands-on tutorials to get you started with [Hortonworks Data Platform (HDP)](https://hortonworks.com/products/data-center/hdp/) using either the [Hortonworks Data Cloud (HDCloud)](https://hortonworks.com/products/cloud/aws/) or a pre-configured downloadable [HDP Sandbox](https://hortonworks.com/products/sandbox/).

The Zeppelin notebook uses basic [Scala](http://www.dhgarrette.com/nlpclass/scala/basics.html) syntax. A Python version is coming soon.

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

#
#

Continue here...

#
#

### Concepts

The core concepts of Spark DataFrames will be introduced in the lab itself. Here, we will focus on launching Zeppelin, importing and then starting the lab.

### Setup

**1. Start your Sandbox**

First, start your Sandbox Virtual Machine (VM) in either a local VirtualBox/VMware (or Azure cloud) environment and note your VM IP address.

We will refer to your VM IP address as `<HOST IP>` throughout this tutorial.

If you need help finding your `<HOST IP>` checkout [Learning the Ropes](http://hortonworks.com/hadoop-tutorial/learning-the-ropes-of-the-hortonworks-sandbox/#learn-host-address-environment).

**2. Launch Zeppelin**

Now that your Sandbox is running, open a web browser and go to: `http://<HOST IP>:9995`

Where `<HOST IP>` is the IP address of your Sandbox machine.

For example, the default address for **VirtualBox** is [http://127.0.0.1:9995](http://127.0.0.1:9995)

**3. Import Lab**

The name of the lab you will be running today is *Lab 101_DS: Machine Learning with Spark*.

By now you should see the main Zeppelin screen with a list of notebooks that you can explore later.

Right now, let's import today's lab.

Click Import

![scr4-import](https://raw.github.com/hortonworks/tutorials/hdp-2.5/assets/getting-started-with-apache-zeppelin/scr4-import.png)

Next, click "Add from URL" button.

![src7-click-url](https://raw.github.com/hortonworks/tutorials/hdp-2.5/assets/getting-started-with-apache-zeppelin/scr7-click-url.png)

Finally, copy and paste the following url: [https://raw.githubusercontent.com/hortonworks-gallery/zeppelin-notebooks/hdp-2.5/2BYWFW95E/note.json](https://raw.githubusercontent.com/hortonworks-gallery/zeppelin-notebooks/hdp-2.5/2BU92U2NH/note.json)

and click "Import Note"

![src8-import-url](https://raw.github.com/hortonworks/tutorials/hdp-2.5/assets/getting-started-with-apache-zeppelin/scr8-import-url.png)

Voila! Now you should have your *Lab 101_DS: Machine Learning with Spark* listed in the main Zeppelin directory.

Click on the lab to get started and follow the step-by-step instructions in the notebook to complete the lab.

### Further Resources

Once you're done with the lab, make sure to checkout other Zeppelin Labs and [Spark Tutorials](http://hortonworks.com/hadoop/spark/#tutorials).
