# Building Real-Time AWS Log Analytics Solution
Here in this project I have used to the aws services(AWS KINESIS ,AWS LAMBDA ,AWS S3) to analyze the how the real time data streaming happens.
In this project I have a taken a text file and uploaded it in s3 bucket.
When we made any changes then it will be reflected in the cloud watch logs.

![Architecture](https://user-images.githubusercontent.com/121667024/228306430-1c3083c8-1180-4d64-a9d8-d5b161ae3bf5.png)

SERVICES

AWS KINESIS: 
       Amazon Kinesis Stream works by ingesting data from multiple sources and processing it in real-time. The data is organized into data streams, which are made up of shards. Each shard can process a fixed rate of data records per second, and businesses can add or remove shards as needed to increase or decrease processing capacity.
       
       
AWS LAMBDA:
      AWS Lambda function reads data from the stream and sends the data in real-time to an Amazon DynamoDB table to be stored. The delivery stream archives the events in an Amazon S3 bucket and sends the data to a Kinesis Data Analytics application for processing. Once the data is processed, it is sent to Kinesis Data Streams.
      
      
 AWS S3:
       Amazon Simple Storage Service (Amazon S3) is storage for the Internet. It is designed to make web-scale computing easier. Amazon S3 has a simple web services interface that you can use to store and retrieve any amount of data, at any time, from anywhere on the web.
       
IAM ROLE:
     AWS Identity and Access Management (IAM) is a web service that helps you securely control access to AWS resources. You use IAM to control who is authenticated (signed in) and authorized (has permissions) to use resources. In this work, we granted full access permissions for S3,LAMBDA,KINESIS.





STEPS:

1.Create an IAM ROLE 
Select the use case as Lambda
 

2. Attach permissions policies 
         Grant full Access to CloudFrontFullAccess , AmazonKinesisFullAccess, AmazonS3FullAccess



3.ROLE Created with the name kinesis-project.
 

4.Create a lambda function named as Producer.
 

 

5.create one more lambda as consumer1_Kinesis
 
 

6.Create one more lambda function for consumer2
 
 

7.Create a S3 Bucket 
 


8.Create a Event Notification for this S3 Bucket to trigger the lambda function.
 

9.Create one kinesis Data Stream
 

10. Edit encryption for kinesis_project.
 


11.Edit the code for producer_kinesis lambda function.

 

12.Edit the code for consumer1_kinesis and consumer2_kinesis lambda functions



13.Add trigger to consumer1_kinesis function 
 

14.Create and one .txt file and upload it in s3 bucket
 


15.Go to monitor tab in producer_kinesis lambda function and click on CloudWatch metrics
 


Hence the real-time streaming of the s3 buclet activities are noticed with the log activities of the cloud watch .
We used serverless services (AWS Kinesis) which is a data streaming service along with S3 and lambda.
 











