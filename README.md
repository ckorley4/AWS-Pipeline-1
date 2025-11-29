# AWS-Pipeline-1
This AWS Pipeline utilizes the ff AWS service to create a data piple


SNS and sqs is used between S3 source and ETL lambda becuase S3 ALLOWS FOR ONLY ONE PUBLISHED LOCATION PERPATH  and if there are other users or teams they cannot create a new notification for that same path


This is why SNS Topics are used to allow fo flexibly of publisshin multiple notification for the same bpath that can be subscribed by other teams



![Alt text for your diagram] <img width="2560" height="1110" alt="GlueSNSSQS" src="https://github.com/user-attachments/assets/f9501b8e-e5c9-4e84-8299-f66e48027af7" />



1. Create an S3 source bucket
2. Create an S3 target bucket
3. Create SNS topic
4. Cretate SQS
5. SQS will subscribe to SNS topic
6. arn:aws:sns:us-east-2:076767436203:edp-topic
7. arn:aws:sqs:us-east-2:076767436203:edp-queue
