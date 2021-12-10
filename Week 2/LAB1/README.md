# Lab 1: Create a Linux virtual machine with the AWS CLI

1. Launch AWS Cloud Shell
3. Create virtual machine
4. Open port 80 for web traffic
5. Connect to virtual machine
6. Install web server
7. View the web server in action

### Notes:

Quickstart: Create a Linux VM
* https://aws.amazon.com/getting-started/launch-a-virtual-machine-B-0/

Quickstart for AWS CloudShell
* https://docs.aws.amazon.com/cloudshell/latest/userguide/working-with-cloudshell.html

Downloaded and installed AWS on my system.
Using EC2 Service for VM
Picked Amazon Linux 2
Used instance t2.micro 1gb memory
Using the default VPC
Also used default storage disck
Using my IP address 105.112.252.122/32
Cloud shell created for Adedayowk2
Once shell was lunched the below sript popped up
Preparing your terminal...
Failed to open session : Timed out while opening the session
Trying to open session (Retrying. Attempt #1)
Connection is lost. Please refresh the browser to re-establish the connection.
[cloudshell-user@ip-10-0-125-88 ~]$ Try these commands to get started:
aws help  or  aws <command> help  or  aws <command> --cli-auto-prompt
[cloudshell-user@ip-10-0-125-88 ~]$ 
[cloudshell-user@ip-10-0-125-88 ~]$ aws ec2 run-instances --image-id ami-002068ed284fb165b --instance-type t2.micro --key-name linux-aws-week2
Using Git Bash to create my server
DELL@DESKTOP-779B2CR MINGW64 ~/Desktop
$ ssh -i "linux-aws-week2.pem" ec2-user@ec2-18-216-39-12.us-east-2.compute.amazonaws.com
The authenticity of host 'ec2-18-216-39-12.us-east-2.compute.amazonaws.com (18.216.39.12)' can't be established.
ED25519 key fingerprint is SHA256:bu1UYJXNCortnIfux8f2vCF0XVrEXsgjrv0wSnzS890.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added 'ec2-18-216-39-12.us-east-2.compute.amazonaws.com' (ED25519) to the list of known hosts.

       __|  __|_  )
       _|  (     /   Amazon Linux 2 AMI
      ___|\___|___|

https://aws.amazon.com/amazon-linux-2/
6 package(s) needed for security, out of 14 available
Run "sudo yum update" to apply all updates.
[ec2-user@ip-172-31-36-23 ~]$

    "Groups": [],
    "Instances": [
        {
            "AmiLaunchIndex": 0,
            "ImageId": "ami-002068ed284fb165b",
            "InstanceId": "i-0692b6b9f20e2d2dc",
            "InstanceType": "t2.micro",
            "KeyName": "linux-aws-week2",
            "LaunchTime": "2021-12-10T16:27:27+00:00",
            "Monitoring": {
                "State": "disabled"
            },
            "Placement": {
                "AvailabilityZone": "us-east-2b",
                "GroupName": "",
                "Tenancy": "default"
            },
            "PrivateDnsName": "ip-172-31-25-214.us-east-2.compute.internal",
            "PrivateIpAddress": "172.31.25.214",
            "ProductCodes": [],
            "PublicDnsName": "",
            "State": {
                "Code": 0,
                "Name": "pending"
            },
            "StateTransitionReason": "",
            "SubnetId": "subnet-0ea23bf27b5eb2f60",
            "VpcId": "vpc-0eacb7b9c20d03870",
            "Architecture": "x86_64",
            "BlockDeviceMappings": [],
            "ClientToken": "4122bd01-f251-41fe-8774-4b30deb57ad3",
            "EbsOptimized": false,
            "EnaSupport": true,
            "Hypervisor": "xen",
            "NetworkInterfaces": [
                {
                    "Attachment": {
                        "AttachTime": "2021-12-10T16:27:27+00:00",
                        "AttachmentId": "eni-attach-0ae1957b8b94dea1f",
                        "DeleteOnTermination": true,
                        "DeviceIndex": 0,
                        "Status": "attaching",
                        "NetworkCardIndex": 0
                    },
                    "Description": "",
                    "Groups": [
                        {
