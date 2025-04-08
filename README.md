# codetech-task1
Task 1 cloud Computing


Steps to Create and Configure an S3 Bucket
1. Create an S3 Bucket
1.	Log in to your AWS Management Console.
2.	Navigate to S3.
3.	Click "Create bucket".
4.	Provide a unique bucket name 
5.	Choose an AWS region closest to your users.
6.	Select Block Public Access settings (Keep private unless public access is required).
7.	Click Create bucket.
2. Upload Example Files
1.	Open your bucket.
2.	Click "Upload".
3.	Add example files 
4.	Click Upload.
3. Configure Bucket Permissions
Option A: Public Read-Only Bucket (If Needed)
•	Uncheck "Block all public access".
•	Add a Bucket Policy for public access:
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Effect": "Allow",
            "Principal": "*",
            "Action": "s3:GetObject",
            "Resource": "arn:aws:s3:::taskbucket--001/*"
        }
    ]
}Verification
•	If public, verify by accessing https://taskbucket--001.s3.ap-south-1.amazonaws.com/Task+1.txt.
