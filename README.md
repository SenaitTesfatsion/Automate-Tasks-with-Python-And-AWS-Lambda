**Python Lambda Function for Automating Tasks in AWS**

**Overview:**
This project demonstrates the development of an AWS Lambda function using Python to automate file management tasks within an S3 bucket. It operates by triggering the Lambda function whenever a new file is added to the designated S3 bucket. Upon trigger, the function orchestrates the movement of the file to a folder structured as YYYYMMDD/filename, where YYYYMMDD denotes the creation date of the file.
**Setup Instructions:**
1. **Create an S3 Bucket:**
   - Log in to the AWS Management Console.
   - Navigate to the S3 service.
   - Create a new bucket or choose an existing one where you want to trigger the Lambda function upon file upload.

2. **Create the Lambda Function:**
   - Log in to the AWS Management Console.
   - Navigate to the Lambda service.
   - Click on "Create function" and choose "Author from scratch".
   - Provide a name for your function, select "Python" as the runtime, and choose an appropriate execution role that grants access to S3.
   - Copy and paste the provided Python code into the Lambda function's code editor.
   - Add an S3 trigger to the Lambda function, specifying the S3 bucket and event type (e.g., "All object create events").
   - Save the Lambda function.

3. **IAM Permissions:**
   - Ensure that the Lambda function's execution role has the necessary permissions to read from and write to the S3 bucket. You may need to attach the `AmazonS3FullAccess` policy or create a custom policy with the required permissions.

4. **Testing:**
   - Upload a file to the S3 bucket specified in the trigger configuration.
   - Check the CloudWatch logs for the Lambda function to verify that the file was moved successfully.

**Usage:**
Once the setup is complete, the Lambda function will automatically trigger whenever a file is added to the specified S3 bucket. The file will be moved to a folder within the bucket, organized by the creation date of the file.

