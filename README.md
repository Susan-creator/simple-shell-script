

AWS Resource List Script

Description
The AWS Resource List Script (aws_resource_list.sh) is a Bash script designed to interact with the AWS Command Line Interface (CLI). It retrieves and displays information about various AWS resources within a specified region. This script is a handy tool for cloud administrators and DevOps engineers to quickly access details about their AWS infrastructure.

Features
Supports listing resources for popular AWS services such as:
EC2
S3
RDS
DynamoDB
Lambda
EBS
ELB
CloudFront
SNS
SQS
Route53
VPC
CloudFormation
IAM
Validates the presence of AWS CLI and configuration.
Displays error messages for invalid or unsupported services.

Prerequisites
AWS CLI: The script requires the AWS CLI to be installed and configured.
Bash Shell: This script is intended for Linux or macOS environments.
AWS Configuration: Ensure that AWS CLI is configured with appropriate credentials and a default profile.

Installing AWS CLI
# Install AWS CLI (Linux example)
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
unzip awscliv2.zip
sudo ./aws/install


Usage
Running the Script
bash
Copy code
./aws_resource_list.sh <region> <service_name>
Example
To list all EC2 instances in the us-east-1 region:
./aws_resource_list.sh us-east-1 EC2


Supported Services
Service Name	Description
EC2	Lists all EC2 instances.
S3	Lists all S3 buckets.
RDS	Lists all RDS instances.
DynamoDB	Lists all DynamoDB tables.
Lambda	Lists all Lambda functions.
EBS	Lists all EBS volumes.
ELB	Lists all Elastic Load Balancers.
CloudFront	Lists CloudFront distributions.
SNS	Lists SNS topics.
SQS	Lists SQS queues.
Route53	Lists Route53 hosted zones.
VPC	Lists all VPCs.
CloudFormation	Lists CloudFormation stacks.
IAM	Lists all IAM users.


Error Handling
If the AWS CLI is not installed:

aws cli is not installed. please install it and try again.

If the AWS CLI is not configured:
Aws cli is not configured. please configure it and try again.

If an invalid service name is provided:
invalid service name. please provide a valid service name.

Logging Output (Optional)
You can redirect the script's output to a log file for auditing:
./aws_resource_list.sh us-east-1 EC2 >> aws_resource_list.log 2>&1


Scheduling with Cron
To automate the script, you can create a cron job:

crontab -e

Add the following line to schedule the script (e.g., daily at 3:00 AM):
0 3 * * * /path/to/aws_resource_list.sh us-east-1 EC2 >> /path/to/aws_resource_list.log 2>&1


Contributing
Contributions are welcome! Feel free to fork this repository and submit a pull request for any improvements or additional features.


Authors
DevOps Team
Contributions and maintenance by the DevOps team.
