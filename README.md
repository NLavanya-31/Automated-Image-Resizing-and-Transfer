# Automated-Image-Resizing-and-Transfer

Project Overview:
The objective of this project is to develop an automated system for image processing and management within the AWS environment. The aim is to simplify the handling of images by resizing them automatically, transferring them to a designated storage location, and notifying stakeholders about the process. Key AWS services including Lambda, S3, and SNS are utilized to orchestrate this workflow.

![Architecture_](https://github.com/NLavanya-31/Automated-Image-Resizing-and-Transfer/assets/155809688/292afe3f-9ae6-4768-b0d8-5c568832d9d8)


Key Features:

##### Image Processing Automation: Implement automated resizing and optimization of images upon upload.
##### Secure Storage: Ensure processed images are stored securely and reliably in an S3 bucket.
##### Real-time Notifications: Enable stakeholders to receive immediate updates regarding image processing via SNS.
##### Scalable Architecture: Design the system to scale effectively to handle varying demands for image processing.
##### Cost-efficient Solution: Utilize AWS serverless technologies to minimize operational costs associated with the solution.

## **Steps involved:**
### 1. Set up AWS S3 Buckets:

- Create two S3 buckets: one for original images (source bucket) and another for resized images (destination bucket).
- Note down the names of both buckets.

### 2. Set up an SNS Topic:

- Create an SNS topic to send notifications about the status of image processing.
- Note down the ARN (Amazon Resource Name) of the SNS topic.

### 3. Create an IAM Role for Lambda:

- Create an IAM role with permissions to read from the source S3 bucket, write to the destination S3 bucket, and publish messages to the SNS topic.
- Attach the necessary policies to this role.

### 4. Create Lambda Function:

- Go to the AWS Lambda console and create a new Lambda function.
- Upload the deployment package containing your function code and dependencies.
- Configure the Lambda function with the IAM role created in step 3.
- Set the trigger for the Lambda function to be the S3 bucket where original images are uploaded.
- Now deploy the changes and test your lambda function code
- Now you're all set, upload an image to the source S3 bucket.
- Monitor the execution of the Lambda function in the AWS Lambda console.
- Check the destination S3 bucket to ensure that the resized image has been uploaded.
- Verify that you receive the appropriate notifications via SNS. You're done!

