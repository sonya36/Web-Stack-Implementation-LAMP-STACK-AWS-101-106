# Documentation of LAMP-STACK-AWS-102-106
## AWS-102 : Setting up AWS account and Virtual Ubuntu 
### Created Aws account
 - Went to AWS home page
 - Chose create an Aws account
 - Entered email address in root user email address and got verified with  verification email
 - Completed other set up process like ( Billing addresss, mastercard verification etc)
 - Finally, Aws free tier account created.
### Setting up virtual ubuntu server
- First, created an ec2 instance named it as "First-instance-aws" in a region "Ohio" with instance type "t2.micro", AMIAMI (Amazon Machine Image ) as "ubuntu" security group and all other required configuration was selected as default here.
![EC2 Instance](./images/EC2.png)
- Latest version of ubuntu was selected which is "Ubuntu Server 22.04 LTS (HVM)". An AMI is a template that contains the software configuration (operating system, application server, and applications) required to launch your instance.
![Ubuntu AMI](./images/AMI_ubuntu.png)
- Private key was generated and named it as "First-instance-private-key" and downloaded ".pem" file.
### Connecting virtual server to EC2 instance
Used the same private key previously downloaded to connect to EC2 instace via ssh:
- Changed the permission for "First-Instance-Key.pem" file as

```
chmod 400 "First-Instance-Key.pem"
```
- Connected to the instance as
```
ssh -i "First-instance-private-key.pem" ubuntu@ec2-18-219-15-149.us-east-2.compute.amazonaws.com
```
![Ubuntuip](./images/ubuntuip.png)
Conclusion, Linux Server in the cloud as created.

## AWS-103 : Installing apache and Updating the Firewall
- Apache was installed using Ubuntu's package manager 'apt'
```
sudo apt update
sudo apt install apache2
```
![AptUpdate](./images/aptupdate.png)
![AptInstall](./images/aptinstall.png)

- Verified that apache2 is running as a service in ubuntu as
```
sudo systemctl status apache2
```



















