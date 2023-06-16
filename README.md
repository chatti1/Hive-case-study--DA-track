# Hive-case-study--DA-track

Problem Statement
Introduction
So far, in this course, you have learned about the Hadoop Framework, RDBMS design, and Hive Querying. You have understood how to work with an EMR cluster and write optimised queries on Hive. 

 

This assignment aims at testing your skills in Hive, and Hadoop concepts learned throughout this course. Similar to Big Data Analysts, you will be required to extract the data, load them into Hive tables, and gather insights from the dataset.
 

Problem Statement
With online sales gaining popularity, tech companies are exploring ways to improve their sales by analysing customer behaviour and gaining insights about product trends. Furthermore, the websites make it easier for customers to find the products they require without much scavenging. Needless to say, the role of big data analysts is among the most sought-after job profiles of this decade. Therefore, as part of this assignment, we will be challenging you, as a big data analyst, to extract data and gather insights from a real-life data set of an e-commerce company.

One of the most popular use cases of Big Data is in eCommerce companies such as Amazon or Flipkart. So before we get into the details of the dataset, let us understand how eCommerce companies make use of these concepts to give customers product recommendations. This is done by tracking your clicks on their website and searching for patterns within them. This kind of data is called a clickstream data. Let us understand how it works in detail.

![image](https://github.com/chatti1/Hive-case-study--DA-track/assets/55474657/f9f08338-2f12-45c1-ba19-00c98812121c)


The clickstream data contains all the logs as to how you navigated through the website. It also contains other details such as time spent on every page, etc. From this, they make use of data ingesting frameworks such as Apache Kafka or AWS Kinesis in order to store it in frameworks such as Hadoop. From there, machine learning engineers or business analysts use this data to derive valuable insights.

For this assignment, you will be working with a public clickstream dataset of a cosmetics store. Using this dataset, your job is to extract valuable insights which generally data engineers come up within an e-retail company

You will find the data in the link given below.

https://e-commerce-events-ml.s3.amazonaws.com/2019-Oct.csv
https://e-commerce-events-ml.s3.amazonaws.com/2019-Nov.csv

You can find the description of the attributes in the dataset given below. In the next video, you will learn about the various implementation stages involved in this case study.
Attribute discription file name.

The implementation phase can be divided into the following parts:

Copying the data set into the HDFS:

Launch an EMR cluster that utilizes the Hive services, and

Move the data from the S3 bucket into the HDFS 

Creating the database and launching Hive queries on your EMR cluster:

Create the structure of your database, 

Use optimized techniques to run your queries as efficiently as possible

Show the improvement of the performance after using optimization on any single query.

Run Hive queries to answer the questions given below.

Cleaning up
Drop your database, and
Terminate your cluster 
 

You are required to provide answers to the questions given below.

Find the total revenue generated due to purchases made in October.

Write a query to yield the total sum of purchases per month in a single output. 

Write a query to find the change in revenue generated due to purchases from October to November.

Find distinct categories of products. Categories with null category code can be ignored.

Find the total number of products available under each category.

Which brand had the maximum sales in October and November combined?

Which brands increased their sales from October to November?

Your company wants to reward the top 10 users of its website with a Golden Customer plan. Write a query to generate a list of top 10 users who spend the most.

Note:

To write your queries, please make necessary optimizations, such as selecting the appropriate table format and using partitioned/bucketed tables. You will be awarded marks for enhancing the performance of your queries.
Each question should have one query only.

Use a 2-node EMR cluster with both the master and core nodes as M4.large.

Make sure you terminate the cluster when you are done working with it.

Since EMR can only be terminated and cannot be stopped, always have a copy of your queries in a text editor so that you can copy-paste them every time you launch a new cluster.

Do not leave PuTTY idle for so long. Do some activity like pressing the space bar at regular intervals. If the terminal becomes inactive, you don't have to start a new cluster. You can reconnect to the master node by opening the puTTY terminal again, giving the host address and loading  .ppk key file. 

For your information, if you are using emr-6.x release, certain queries might take a longer time, we would suggest you use emr-5.29.0 release for this case study.

There are different options for storing the data in an EMR cluster. You can briefly explore them in this link. In your previous module on hive querying, you copied the data to the local file system, i.e., to the master node's file system and performed the queries. Since the size of the dataset is large here in this case study, it is a good practice to load the data into the HDFS and not into the local file system. You can revisit the segment on 'Working with HDFS' from the earlier module on 'Introduction to Big data and Cloud'.

You may have to use CSVSerde with the default properties value for loading the dataset into a Hive table. You can refer to this link for more details on using CSVSerde. Also, you may want to skip the column names from getting inserted into the Hive table. You can refer to this link on how to skip the headers.
