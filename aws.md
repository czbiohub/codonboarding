# BioHub AWS Quick Start Guide

*big thank you to Min and Lincoln for their awesome notes!*

Set up an AWS Account
AWS stands for Amazon Web Services.

Slack James Wang (@jwang) to get a user login and password.
Set up your account by going to: https://czbiohub.signin.aws.amazon.com/console

Login to your AWS account at: console.aws.amazon.com
Make sure you’re connected to the Oregon region.

# Creating and Working with S3

## Creating an S3 Bucket
S3 stands for Simple Storage Service.
Buckets are an object store (not a file store) for files.
The cost for data storage is ~$0.023/GB/month.

Go to Services > S3 (under Storage)
Click Create bucket.
Input a Bucket name that starts with your AWS login name, followed by a dash. E.g. mcho-bucket
Ensure the correct Region is selected: US West (Oregon)
Click Next twice, then Create bucket.

## Working with S3

### List contents of s3 directory
`aws s3 ls s3://mybucket/test/`

### Copying a s3 file to local
`aws s3 cp s3://mybucket/test.txt test2.txt`


# Initiating and Working with an EC2 Instance

## Initiating an EC2 Instance

EC2 stands for Elastic Computing Cloud.

Go to Services > EC2 (under Compute)
Click Launch Instance.

Step 1: Select Ubuntu Server 16.04 LTS (HVM), SSD Volume Type

Step 2: Select the appropriate type of instance based on your computing needs. Click Next: Configure Instance Details. For more info on instance type go to: http://www.ec2instances.info/

Step 3: Change any details as needed. Click Next: Add Storage.

Step 4: Input the amount of storage you’ll need. Click Next: Add Tags.

Step 5: Add tags if necessary. Click Next: Configure Security Group.

Step 6: Select Select an existing security group, and choose a security group. Click Review and Launch.

Step 7: Review details, and click Launch.

Creating a Key Pair
A key pair consists of a public key that AWS stores, and a private key file that you store. Together, they allow you to connect to your instance securely. For Windows AMIs, the private key file is required to obtain the password used to log into your instance. For Linux AMIs, the private key file allows you to securely SSH into your instance.

If you already have a key pair, select it from the drop down menu.

Otherwise, select Create a new key pair.
Name your key pair, e.g. mcho-key-pair
Click Download Key Pair and place .pem file in a safe location on your computer. TIP: you will need to this .pem file later

Check the acknowledgement box, then click Launch Instances.

Go to your new instance by clicking on the instance name in the green box, e.g. i-0135a4becdc895a23.
Rename your instance, e.g. mcho-instance1. Take note of the IPv4 Public IP.

## Working with an EC2 Instance

Open a Terminal window.

### Give r/w file permissions to .pem key-pair file using chmod command
```
chmod 400 /Users/lincoln.harris/Documents/20-AWS_basics/Lincolnharris-1.pem.txt
```

### Login to instance
```
ssh -i /Users/lincoln.harris/Documents/20-AWS_basics/Lincoln.harris-1.pem ubuntu@ec2-34-211-26-157.us-west-2.compute.amazonaws.com
```

### Install AWS CLI (command line interface for AWS)
In the Ubuntu command line of your EC2 interface type:

`sudo apt install awscli`

Type Y at the prompt.

### To configure AWS CLI

`aws configure`

### To get the AWS Access KEY ID and AWS Secret Access Key

Go to: Services > IAM > Users > [your user name] > Security credentials > Create access key.
Copy and paste Access key ID and Secret access key into Terminal window.

For Default region name, input us-west-2.
Leave Default output format empty and return.

### Copy files to instance
```
scp -i /Users/lincoln.harris/Documents/20-AWS_basics/Lincolnharris-1.pem.txt /Users/lincoln.harris/Documents/21-fancyPantz/linc_runBasic.py ubuntu@ec2-34-211-26-157.us-west-2.compute.amazonaws.com:~
```

### Copy files from instance back to local machine

```
scp -i /Users/lincoln.harris/Documents/20-AWS_basics/Lincoln.harris-1.pem -r ubuntu@ec2-34-214-88-13.us-west-2.compute.amazonaws.com://home/ubuntu/myVol/fancyPantz/run1 /Users/lincoln.harris/Desktop/
```
