# Aegea

## Intro
`aegea` is a comman line interace that provides a set of essectial commands and terminal dashboards for operators of AWS accounts. `aegea` lets you build AMIs and Docker images using the cloud-init config management package, manage config roles, launch and monitor instances and services, and manage AWS resources including ELB, RDS, and AWS Batch. It is intended to be used in conjuction with the existing functionality of the AWS CLI and boto3

More info: https://github.com/kisluk/aegea

## Installation
- Before installing Aegea, make sure Xcode is installed
- To install `aegea`, check if `python3` is installed by typing `python3` on your terminal
  - Quit `python3` enter `quit()` and install `aegea` by entering command `pip install aegea`

## Launching AWS via Aegea
  - To check if `aegea` is correctly installed run `aegea ls`
    - If `aegea` is installed but not configured, configure via `aws configure` and enter the AWS Access Key ID and AWS Secret Access Key obtain
      - To get the AWS Access Key ID and AWS Secret Access Key, go to: https://aws.amazon.com/ and sign in to the Console. From there go to `services` -> `IAM` -> `users` -> [your name] -> `security credentials` -> `create access key`

## Aegea Commands
`aegea launch --instance-type [API Name] [hostname]`
- Launch instance based on the selected [API Name] from www.ec2instance.info under the [hostname] you choose

`aegea launch --instance-type XXX -ami XXX [instance name]`
- Creates ssh key for you and associates with local account; next command can connect to that machine
  - AMI - Amazon machine image

`aegea ssh ubuntu@[instance]`
- Access instance via aegea

`aegea start [instance]`
- Start an instance

`aegea stop [instance]`
- Stop an instance

`aegea ls -t Name=[user name]`
- Shows what instances you are running

'aegea images'
- Shows all current machine images that are custom created by Biohub in us-west-2

`aegea -h` or `aegea ls -h`
- Aegea help

`aegea terminate [hostname]`
- Terminate the [hostname] instance that was launched


# Trying to demux or align?

## You may want to check out the utilities repo at A collection of scripts for common data management and processing tasks

