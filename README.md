# AWS-UseCase2-Social-Media-Analysis-Dashboard

This was a project in MCIT AWS practical data science program. The aim of the project is to help you to gain insights into your customer’s conversations and deepen brand awareness by analyzing social media interactions. It automatically provisions and configures the AWS services necessary to capture multi-language tweets in near real-time, translate them, and store both the raw and enriched datasets durably in the solution's data lake and then analyze this data and create meaningful dashboards using Amazon QuickSight to visualize and understand customer sentiment.

Firstly, I used my local PC to stream the tweets to S3 bucket through Kinesis data firehose and save them in a bucket named raw. Secondly, after it is saved in the bucket it triggers a lambda function which calls a comprehend to apply NLP techniques to perform sentiment analysis on the data given. Then we returned the sentiment analysis data to a new S3 bucket called sentiment through Kinesis data firehose.

Last but not least, I used athena to query the data and imported the schema of the data using Glue crawler to crawl the data and save the output in a S3 bucket. Finally, I used AWS Quicksight to visualize the sentiment and build some dashboards to gain some insights of customers interactions.
![Solution](https://user-images.githubusercontent.com/86932668/174322537-7ca9f503-3c0c-4b88-9cd7-3a855465ce8b.png)
