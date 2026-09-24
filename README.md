# AWS-Automated-Access-Review
Serverless AWS IAM security review tool using Python, CloudFormation, and Amazon Bedrock 




# AWS Automated Access Review

An automated AWS security scanner built with Python and serverless AWS services to identify identity and access risks.

## Project Overview
This project automatically scans an AWS account on a schedule to spot common security risks, creates an AI-generated executive summary, and delivers the results via email.

## Key Features
* **Automated Scanning:** Checks for IAM users missing MFA, unused access keys, overly permissive policies, and public S3 buckets.
* **AI Summaries:** Uses Amazon Bedrock (Claude) to convert raw technical security findings into a plain-English executive summary.
* **Email Delivery:** Sends formatted CSV audit logs and readable reports straight to your inbox via Amazon SES.
* **Infrastructure as Code:** Deploys automatically using AWS CloudFormation templates.

## Architecture & AWS Services Used
* **AWS Lambda (Python & boto3):** Runs the audit logic and interacts with AWS security APIs.
* **Amazon EventBridge:** Triggers the Lambda function automatically on a recurring schedule.
* **Amazon Bedrock:** Generates AI-powered report summaries.
* **Amazon SES:** Handles email notifications.
* **Amazon S3:** Stores historical audit reports and logs.
* **AWS CloudFormation:** Provisions all infrastructure cleanly in minutes.

## How to Deploy
1. Clone the repository:
   ```bash
   git clone  https://github.com/Omar1l/AWS-Automated-Access-Review.git

Verify your email in Amazon SES.

Run the deployment script:
```bash
./scripts/deploy.sh --email your-email@example.com --region us-east-1
