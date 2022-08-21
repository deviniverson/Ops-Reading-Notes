# Anatomy of a Cloud Breach

## Major financial institution data breach
A US-based major financial institute had a data in 2019, which exposed the personal data of more than 100,000 customers. This was one of the most devastating data breaches of all time. When the news of the data breach was released, unwarranted speculation spread on the internet, including suggestions that a single product or set of professional services could have prevented such an attack. 

On July 29, 2019, the FBI arrested Paige A. Thompson (alias “erratic”) for allegedly hacking into Financial Institution databases and stealing the data. Financial Institute disclosed that the event affected approximately 100 million individuals in the United States and approximately 6 million in Canada. It also includes data loss of approximately 1 million Social Insurance Numbers of Canadian credit card customers, about 140,000 Social Security numbers, and 80,000 linked bank account numbers of the credit card customers.

AWS provided with their assessment of the incident: “Financial Institution outlined in their public announcement the attack occurred due to a misconfiguration error at the application layer of a firewall installed by Financial Institution, exacerbated by permissions set by Financial Institution that were likely broader than intended. After gaining access through the misconfigured firewall and having broader permission to access resources, we believe an SSRF attack was used.”

## Best Guess of Steps taken by “erratic” to compromise the data
1. Identified and Exploited Misconfigured WAF
Attacker identified a misconfigured WAF that enabled accessing the corresponding AWS EC2 instance/ ECS task using Server-side Request Forgery (SSRF) and call the metadata service endpoint using “http://169.254.169.154/iam/security-credentials command”. The endpoint must have returned a role name to use.

2. Gain temporary credentials
Using the role name, the attacker then queried the specific endpoint to gain access to temporary credentials, this code would return the full set of temporary credentials, 
“http://169.254.169.254/iam/security-credentials/*****-WAF-Role”

3. Gain access to S3 buckets by calling AWS S3 list and Sync
CLI commands used would be:
$ aws s3 ls
This ls command would list all the S3 buckets accessible using the IAM role
$ aws s3 sync s3://somebucket
This sync command would download all resources from the bucket

The most likely root cause of the attack was a poor security architecture design that exposed S3 buckets via AWS WAF/EC2 instance to anyone with an IAM role. While S3 buckets were not exposed to the internet like many other breaches, an EC2 instance with an excessive IAM role might have been the culprit.


## AWS Configurations
Following AWS configurations would prevent such attacks:
1.	AWS IAM: Enforce least privileged IAM controls
2.	AWS IAM: Ensure IAM policies are attached only to groups or roles
3.	AWS S3: Ensure AWS S3 buckets do not allow public READ access
4.	AWS S3: Ensure AWS S3 buckets do not allow public READ_ACP access
5.	AWS S3: Ensure AWS S3 buckets do not allow public WRITE_ACP access
6.	AWS S3: Ensure S3 buckets do not allow FULL_CONTROL access to AWS authenticated users via S3ACLs
7.	AWS S3: Ensure that Amazon S3 buckets access is limited only to specific IP addresses
8.	AWS S3: Ensure S3 buckets do not allow READ access to AWS authenticated users through ACLs
9.	AWS S3: Ensure S3 buckets do not allow FULL_CONTROL access to AWS authenticated users via S3 ACLs
10.	AWS S3: Ensure all S3 buckets have policy to require server-side and in transit encryption for all objects stored in bucket
11.	AWS Networking: Ensure no security groups allow ingress from 0.0.0.0/0 to port 22
12.	AWS Networking: Ensure Application Load Balancer (ALB) with administrative service: SSH (TCP:22) is not exposed to the public internet
13.	AWS Networking: Ensure no security groups allow ingress from 0.0.0.0/0 to port 22 (SSH)
14.	AWS Networking: Ensure no security groups allow ingress from 0.0.0.0/0 to port 3389 (RDP)
15.	AWS – Audit and Logging: Ensure S3 bucket access logging is enabled on the CloudTrail S3 bucket
16.	AWS – Audit and Logging: Ensure CloudTrail is enabled in all regions
17.	AWS – Audit and Logging: Ensure CloudTrail trails are integrated with CloudWatch Logs 
18.	AWS – Audit and Logging: Ensure the S3 bucket used to store CloudTrail logs is not publicly accessible
19.	AWS - Monitoring: Ensure a log metric filter and alarm exist for CloudTrail configuration changes.

## Sources cited
https://www.zscaler.com/resources/white-papers/capital-one-data-breach.pdf


