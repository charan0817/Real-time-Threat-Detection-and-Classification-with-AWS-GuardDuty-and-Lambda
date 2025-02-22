# Real-time-Threat-Detection-and-Classification-with-AWS-GuardDuty-and-Lambda
This project is focused on security and involves integrating AWS GuardDuty to monitor potential threats. When a device with an IP identified as a threat in GuardDuty attempts to log in, GuardDuty is triggered and generates security findings. These findings are then sent to an S3 bucket.

Whenever a file containing these findings is uploaded to the bucket, the Lambda function is triggered. The function:

Retrieves and decompresses the file from the S3 bucket.
Parses the JSON data, extracts critical information like severity, title, description, region, and IP details.
Classifies the severity of the threat (low, medium, or high).
Sends the extracted information to an SQS queue for further analysis or alerting.
In summary, this project automates the detection and classification of security findings related to IP threats, using AWS services like GuardDuty, S3, Lambda, and SQS for real-time monitoring and alerting.
