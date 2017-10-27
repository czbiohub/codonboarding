# AWS

Use AWS for STAR Alignments

## Install Aegea

`git clone https://github.com/kislyuk/aegea.git` in your command line use the git clone command to clone the repository for aegea.

## Give r/w file permissions to .pem key-pair file using chmod command
```
chmod 400 /Users/lincoln.harris/Documents/20-AWS_basics/Lincolnharris-1.pem.txt
```

## Login to instance
```
ssh -i /Users/lincoln.harris/Documents/20-AWS_basics/Lincoln.harris-1.pem ubuntu@ec2-34-211-26-157.us-west-2.compute.amazonaws.com
```
## Copy files to instance
```
scp -i /Users/lincoln.harris/Documents/20-AWS_basics/Lincolnharris-1.pem.txt /Users/lincoln.harris/Documents/21-fancyPantz/linc_runBasic.py ubuntu@ec2-34-211-26-157.us-west-2.compute.amazonaws.com:~
```

## Copy files from instance back to local machine

```
scp -i /Users/lincoln.harris/Documents/20-AWS_basics/Lincoln.harris-1.pem -r ubuntu@ec2-34-214-88-13.us-west-2.compute.amazonaws.com://home/ubuntu/myVol/fancyPantz/run1 /Users/lincoln.harris/Desktop/
```
