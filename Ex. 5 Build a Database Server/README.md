# Lab 5 – Build a Database Server (AWS)

## Author

* **Name**: _ISHWARYA R_______________________________
* **Register Number**: __212224220039___________________
* **Date of Submission**: ___18/3/2026_______________

---
## Objective
The objective of this experiment is to understand how to deploy and configure a database server in AWS. This lab focuses on launching an EC2 instance, installing a database management system (DBMS), configuring basic database settings, creating a sample database, and validating connectivity to the database server.

## Prerequisites
Basic understanding of cloud computing concepts
AWS account or AWS Academy Lab access
An existing VPC and EC2 knowledge (from previous labs)
Basic knowledge of Linux commands and SQL
Tools Used
AWS Management Console
Amazon EC2
Security Groups
SSH Client (Terminal / PuTTY)
MySQL / MariaDB / PostgreSQL (any one)
Tasks Performed
Task 1: Launch EC2 Instance for Database Server
Launch a new EC2 instance using Amazon Linux 2 AMI. Select an appropriate instance type and configure key pair and security group.

Task 2: Configure Security Group for Database Access
Modify the security group to allow:

SSH (Port 22) for remote access
Database port (e.g., MySQL – 3306 or PostgreSQL – 5432)
Task 3: Connect to EC2 Instance
Connect to the EC2 instance using SSH from your local machine.

Task 4: Install Database Server
Install a database server software such as MySQL, MariaDB, or PostgreSQL on the EC2 instance using package manager commands.

Task 5: Start and Configure Database Service
Start the database service and configure basic settings such as root password and user privileges.

Task 6: Create a Sample Database
Create a sample database and a table inside it. Insert a few records into the table.

Task 7: Test Database Connectivity
Test the database server by connecting to it locally or remotely and performing basic SQL queries.

## Workflow (Student Explanation)
(Write the steps you followed in your own words)

Logged in to AWS Management Console and opened Amazon EC2.

Launched a new EC2 instance using Amazon Linux 2 AMI and selected an appropriate instance type.

Created/selected a key pair and configured a security group for the instance.

Modified the security group to allow SSH (Port 22) and database access (3306 for MySQL or 5432 for PostgreSQL).

Connected to the EC2 instance using an SSH client such as PuTTY or terminal.

6.Installed the database server (e.g., MySQL, MariaDB, or PostgreSQL) using Linux package manager commands.

Started the database service and configured basic settings such as the root password and user privileges.

Created a sample database and table and inserted a few records.

Tested database connectivity by running basic SQL queries.

## Output Screenshots (Attach 3)
## Screenshot 1: EC2 Instance for Database Server
<img width="1264" height="711" alt="image" src="https://github.com/user-attachments/assets/9c8fb984-ad15-473b-972b-986556b9ff6e" />
<img width="1259" height="653" alt="image" src="https://github.com/user-attachments/assets/8393d596-4e83-4957-b710-0fc41054df07" />

## Screenshot 2: Database Service Running
<img width="1263" height="707" alt="image" src="https://github.com/user-attachments/assets/22b7d4a4-7d10-469c-ba30-709b118b0065" />

## Screenshot 3: Sample Database and Table
<img width="1258" height="787" alt="image" src="https://github.com/user-attachments/assets/ccf15f8a-e5bf-4902-835f-5944534cbc80" />

## Result
This experiment demonstrated how to build a database server in AWS using an EC2 instance. By installing and configuring a DBMS, creating a sample database, and testing connectivity, the fundamentals of hosting and managing a cloud-based database server were underst

