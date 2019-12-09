# ec2-image-builder
Custom Build and Test Components developed for AWS EC2 Image Builder (https://docs.aws.amazon.com/imagebuilder/latest/userguide/what-is-image-builder.html)

## Configuration
1. Create a S3 bucket (configuration-bucket) and place files in `S3` folder of component.
2. Create IAM Role
required policies:
- arn:aws:iam::aws:policy/service-role/AmazonEC2RoleforSSM
- arn:aws:iam::aws:policy/EC2InstanceProfileForImageBuilder
3. Replace <bucket-name> with your newly created bucket name (configuration-bucket)
4. Create EC2 Image Builder pipeline with Amazon Linux 2
5. Create components that you want to use and select
6. Select IAM Role that you have created
7. Name your pipeline
8. Name your AMI
9. Run pipeline


## Detailed Documentation of Components
- [CIS Benchmarks](cis-benchmarks.md)
- [Cloudwatch Agent Setup](cloudwatch.md)

> These components are tested on Amazon-linux-2-x86/2019.11.21
