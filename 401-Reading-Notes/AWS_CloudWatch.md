# What is AWS CloudWatch?

Amazon CloudWatch is a service used for real-time monitoring AWS resources like EC2 instances, EBS, RDS, load balancer, lambda, Cognito, S3, etc. and can be used for monitoring on-prem resources.

## Amazon CloudWatch Events
Events allows users to consume a near real-time stream of events as changes to their AWS environment take place. These event changescan afterword trigger notification services like SNS, SMS, etc. or can trigger other AWS services like Lambda, SSM, Step function.
You can create a custom role to trigger targeted AWS resources for automation purposes based on event, role or time schedule.

## CloudWatch Agent
AWS provides CloudWatch agent that can be configured on the EC2 instances to send Custom Metrics to CloudWatch. That agent supports multiple operating systems like Amazon Linux, CentOS, Redhat, Windows Server (2008 onward), Debian, Ubuntu OS. The help of IAM role access, the agent collects live metrics from the server and sends these custom & detailed data to CloudWatch Dashboard for better monitoring experience.

## CloudWatch Alarm
You can create a CloudWatch alarm based on the target CloudWatch metric or the result of a math expression based on CloudWatch metrics. The alarm does perform one or multiple actions based on metric value or specified matrix condition reached a threshold over several time periods.

## Amazon CloudWatch Logs
CloudWatch Logs helps users to access, monitor & store log files from AWS resources like EC2, Lambda functions, CloudTrail, Route 53, and other sources. CloudWatch Logs enables you to centralize the logs from all your systems, applications, and AWS services that you use, in a single, highly scalable service.

## CloudWatch Anomaly Detection
When Anomaly detection is enabled for a metric, CloudWatch applies statistical and machine learning algorithms that continuously analyze metrics of systems or applications and determine normal baselines, and surface inconsistency with minimal user involvement.
### Anomaly Detection Capabilities:
* Learn and model the expected behavior of a metric based on prior data.
* Calculate expected values and generate the Anomaly Detection band. This is based on a lower and an upper band metric generated by the model. Metric generated by the model. Metric values that fall outside the predicted confidence band are considered anomalies.
* Enable you to create alarms based on the Anomaly detection band and immediately detect anomalies.
* AWS API & CloudFormation support 