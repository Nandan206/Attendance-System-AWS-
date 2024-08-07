# Attendance-System-AWS-
Designed an architecture for smart attendance system with AWS services.
Our proposed solution integrates the power of Amazon Web Services, combining Amazon Rekognition for facial recognition, Amazon S3 for secure storage of facial details, Amazon RDS for efficient management of attendance data, and Lambda functions for seamless automation, Kinesis for real time analysis.
We Use Amazon S3 to store the images of the attendees.
Utilize Amazon Rekognition for real-time image recognition. Set up an event trigger on the S3 bucket so that whenever a new image is uploaded, it triggers a Lambda function.
The Lambda function will be triggered by the S3 event and will invoke the Rekognition API to recognize faces in the uploaded image. It will then extract the recognized faces and compare them against a database of known faces to identify attendees.
Use Amazon RDS (Relational Database Service) to store information about attendees, including their names, email addresses, and other relevant data.
Set up Kinesis Data Streams to capture real-time data about attendance events. This data can include information such as the timestamp, the attendee's ID, and whether they were recognized successfully.
Configure SNS to send email notifications to users once their attendance has been marked. Use SNS to trigger an email notification whenever a successful attendance event is recorded.
Set up an API Gateway to provide a RESTful API for interacting with your attendance system. This API can be used by clients to upload images, query attendance records, and perform other actions.
Tech Stack:
Image Capture: A camera captures student faces at the entry point.
Lambda Trigger: The captured image triggers an AWS Lambda function.
Facial Recognition: AWS Rekognition identifies and matches faces against stored data.
Attendance Record Update: Lambda updates attendance details in Amazon RDS.
Notification Sent: Another Lambda function sends notifications via Amazon SNS based on attendance updates.
Use cases:
Can be used in schools and colleges for Proper attendance system.
Enterprise-wide Attendance Management.
Streamlined Attendance Tracking for Large Organizations.
Can be used to Identify Intruder and Strangers.
