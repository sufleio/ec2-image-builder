# ec2-image-builder
Custom Build and Test Components developed for AWS EC2 Image Builder (https://docs.aws.amazon.com/imagebuilder/latest/userguide/what-is-image-builder.html)

## Configuration
1. Create a S3 bucket (configuration-bucket) and place files in `S3` folder of component.
2. Create IAM Role and attach following required policies:
- arn:aws:iam::aws:policy/service-role/AmazonEC2RoleforSSM
- arn:aws:iam::aws:policy/EC2InstanceProfileForImageBuilder
3. [Create Components](https://eu-west-1.console.aws.amazon.com/imagebuilder/home#createComponent) that you want to use by copying yaml component file
4. [Create EC2 Image Builder](https://eu-west-1.console.aws.amazon.com/imagebuilder/home#createPipeline) pipeline with Amazon Linux 2 and specify the component from step 3
5. Specify your bucket name under `S3BucketNameParameter` with your newly created bucket name (configuration-bucket) in yaml component file
6. Select IAM Role that you have created on Step 2
7. Name your pipeline
8. Name your AMI
9. Trigger pipeline

## Troubleshooting
- You can disable `Terminate instance on failure` option and select a keypair while creating a pipeline to connect and troubleshoot any errors on the build instance.
- You can follow and check AWS Systems Manager logs from, https://eu-west-1.console.aws.amazon.com/systems-manager/automation/executions

## Detailed Documentation of Components
- [CIS Benchmarks](cis-benchmarks.md)
- [Cloudwatch Agent Setup](cloudwatch.md)

> These components are tested on Amazon-linux-2-x86/2019.11.21
