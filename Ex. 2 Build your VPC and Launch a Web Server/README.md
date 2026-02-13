# Build Your VPC and Launch a Web Server (AWS) 

## Author

* **Name**: __ISWARIYA R______________________________
* **Register Number**: ___212224220039__________________
* **Date of Submission**: ____13.02.2026______________

---

## Objective

The objective of this experiment is to understand how to design and configure a basic network infrastructure in AWS using a Virtual Private Cloud (VPC). This lab focuses on creating a VPC with a public subnet, configuring an Internet Gateway and route table, launching an EC2 instance, and hosting a simple web server that can be accessed over the internet.

---

## Prerequisites

* Basic understanding of cloud computing concepts
* AWS account or AWS Academy Lab access
* Web browser with internet connectivity

---

## Tools Used

* AWS Management Console
* Amazon VPC
* Amazon EC2
* Internet Gateway
* Route Table
* Security Groups

---

## Tasks Performed

### Task 1: Create a VPC

Create a new Virtual Private Cloud (VPC) with a private IP address range. The VPC acts as a logically isolated network in AWS where all other resources will be deployed.

Students should create a VPC with an appropriate CIDR block (for example, 10.0.0.0/16) and assign a meaningful name.


### Task 2: Create a Public Subnet

Create a subnet inside the VPC to host public resources. Enable auto-assign public IPv4 so that instances launched in this subnet receive a public IP address.

The subnet should use a smaller CIDR range (for example, 10.0.1.0/24).


### Task 3: Create and Attach Internet Gateway

Create an Internet Gateway (IGW) and attach it to the VPC. This allows communication between resources in the VPC and the internet.


### Task 4: Configure Route Table

Create a route table and add a default route (0.0.0.0/0) pointing to the Internet Gateway. Associate this route table with the public subnet.

This step ensures that traffic from the subnet can reach the internet.


### Task 5: Create Security Group

Create a security group to act as a virtual firewall for the EC2 instance. Configure inbound rules to allow:

SSH on port 22

HTTP on port 80


### Task 6: Launch EC2 Instance

Launch an EC2 instance inside the public subnet using Amazon Linux 2 AMI and a suitable instance type (t2.micro).

Attach the previously created security group and key pair.


### Task 7: Configure Web Server

Install and start a web server (Apache HTTPD) on the EC2 instance using user data or manual commands.

Create a simple HTML page and verify that it can be accessed from a web browser using the public IP address of the instance.---

## Workflow (Student Explanation)


1. In this task, you will use the VPC and more option in the VPC console to create multiple resources, including a VPC, an Internet Gateway, a public subnet and a private subnet in a single Availability Zone, two route tables, and a NAT Gateway.
 
4.	In the search box to the right of Services, search for and choose VPC to open the VPC console.
5.	Begin creating a VPC.
o	In the top right of the screen, verify that N. Virginia (us-east-1) is the region. 
o	Choose the VPC dashboard link which is towards the top left of the console.
o	Next, choose Create VPC. 
Note: If you do not see a button with that name, choose the Launch VPC Wizard button instead.
6.	Configure the VPC details in the VPC settings panel on the left:
o	Choose VPC and more.
o	Under Name tag auto-generation, keep Auto-generate selected, however change the value from project to lab.
o	Keep the IPv4 CIDR block set to 10.0.0.0/16
o	For Number of Availability Zones, choose 1.
o	For Number of public subnets, keep the 1 setting.
o	For Number of private subnets, keep the 1 setting.
o	Expand the Customize subnets CIDR blocks section
	Change Public subnet CIDR block in us-east-1a to 10.0.0.0/24
	Change Private subnet CIDR block in us-east-1a to 10.0.1.0/24
o	Set NAT gateways to In 1 AZ.
o	Set VPC endpoints to None.
o	Keep both DNS hostnames and DNS resolution enabled.
 
7.	In the Preview panel on the right, confirm the settings you have configured.
o	VPC: lab-vpc
o	Subnets:
	us-east-1a
	Public subnet name: lab-subnet-public1-us-east-1a
	Private subnet name: lab-subnet-private1-us-east-1a
o	Route tables
	lab-rtb-public
	lab-rtb-private1-us-east-1a
o	Network connections
	lab-igw
	lab-nat-public1-us-east-1a 
 
8.	At the bottom of the screen, choose Create VPC
The VPC resources are created. The NAT Gateway will take a few minutes to activate. 
Please wait until all the resources are created before proceding to the next step.
 
9.	Once it is complete, choose View VPC
The wizard has provisioned a VPC with a public subnet and a private subnet in one Availability Zone with route tables for each subnet. It also created an Internet Gateway and a NAT Gateway. 
To view the settings of these resources, browse through the VPC console links that display the resource details. For example, choose Subnets to view the subnet details and choose Route tables to view the route table details. The diagram below summarizes the VPC resources you have just created and how they are configured
---

## Output Screenshots (Attach 3)

### Screenshot 1: VPC and Subnet Details

<img width="973" height="554" alt="image" src="https://github.com/user-attachments/assets/fbcba155-2501-4686-a340-01e1787b441c" />


---

### Screenshot 2: EC2 Instance Running

<img width="977" height="523" alt="image" src="https://github.com/user-attachments/assets/52fd055d-2496-40d9-ae20-8def3d39a338" />


---

### Screenshot 3: Web Server Output in Browser

<img width="974" height="328" alt="image" src="https://github.com/user-attachments/assets/8e17ba4f-e856-4a29-abb9-a0956dae8e26" />


---

## Result 

This experiment successfully demonstrated the creation of a custom VPC and deployment of a public-facing web server in AWS. By configuring networking components such as subnets, route tables, and security groups, and by launching an EC2 instance with a web server, the basic architecture of a cloud-hosted application was understood.
