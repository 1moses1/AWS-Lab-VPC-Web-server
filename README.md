# AWS Cloud Computing Lab: VPC and Web Server Deployment

## Overview

This repository contains the documentation and scripts for a lab exercise completed as part of the ALX AWS Cloud Computing Course. The lab, taken in a sandbox environment, focuses on building a customized network infrastructure on Amazon Web Services (AWS), including the creation of a Virtual Private Cloud (VPC), subnets, security groups, and launching a web server using Amazon EC2.

## Lab Duration

Approximately 30 minutes

## Lab Tasks

### Task 1: Created Your VPC

1. Access the AWS Management Console
2. Create a VPC with public and private subnets
3. Configure route tables, Internet Gateway, and NAT Gateway

### Task 2: Create Additional Subnets

1. Create public and private subnets in a second Availability Zone
2. Associate route tables with new subnets

### Task 3: Create a VPC Security Group

1. Create a security group for the web server
2. Allow inbound HTTP traffic

### Task 4: Launch a Web Server Instance

1. Launch an EC2 instance with Amazon Linux
2. Configure network settings, security groups, and storage
3. Run a script to install Apache Web Server and PHP

## Accessing the Web Server

1. Wait until the EC2 instance status shows 2/2 checks passed
2. Copy the Public IPv4 DNS from the AWS console
3. Open a web browser and paste the DNS to view the web page

## Repository Structure

- `/scripts`: Contains scripts used in the lab
- `/images`: Screenshots or diagrams related to the lab
- `/docs`: Additional documentation or insights gained during the lab

## Lab Scripts

### Install Web Server Script

```bash
#!/bin/bash
# Install Apache Web Server and PHP
dnf install -y httpd wget php mariadb105-server
# Download Lab files
wget https://aws-tc-largeobjects.s3.us-west-2.amazonaws.com/CUR-TF-100-ACCLFO-2/2-lab2-vpc/s3/lab-app.zip
unzip lab-app.zip -d /var/www/html/
# Turn on web server
chkconfig httpd on
service httpd start

```

## Resources

- [AWS Documentation](https://aws.amazon.com/vpc/)
- [ALX AWS Cloud Computing Course](https://www.alxafrica.com/aws-cloud-computing/)

## Lab Complete
