# What is Amazon GuardDuty?
##A continuous security monitoring service that analyzes and processes data sources, such as:
* AWS CloudTrail data events from Amazon S3 logs,
* CloudTrail management event logs,
* DNS logs,
* EBS volume data,
* Amazon EKS audit logs
* Amazon VPC flow logs

## It uses threat intelligence feeds, such as lists of malicious IP addresses and domains, and machine learning to identify unexpected, potentially unauthorized, and malicious activity within your AWS environment.
This can include issues like:
* escalation of privileges
* use of exposed credentials
* communication with malicious IP addresses or domains
* presence of malware on your Amazon EC2 instances and container workloads

For example: GuardDuty can detect compromised EC2 instances and container workloads serving malware, or mining bitcoin.

## Accessing GuardDuty
You can use any of the following ways to access GuardDuty:
1. GuardDuty Console - The console is a browser-based interface to access and use GuardDuty
2. AWS SDKs - AWS provides software development kits (SDKs) that consist of libraries and sample code for various programming languages and platforms. The SDKs provide a convenient way to create programmatic access to GuardDuty.
3. GuardDuty HTTPS API - You can access GuardDuty and AWS programmatically by using the GuardDuty HTTPS API, which lets you issue HTTPS requests directly to the service. 