# Cloudwatch Agent
This build script is install and configure Cloudwatch Agent to send system logs automatically.

https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/download-cloudwatch-agent-commandline.html

## Configuration File
Configuration file includes following files,

- /var/log/messages
- /var/log/secure
- /var/log/audit/audit.log
- /var/log/aide/aide.log

### Additional Configuration
You need to attach arn:aws:iam::aws:policy/CloudWatchAgentServerPolicy policy to send logs to Cloudwatch Logs from EC2 Instance.
