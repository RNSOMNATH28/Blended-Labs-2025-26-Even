# Lab 6 – Scale and Load Balance Your Architecture

## Author


* **Name**: R N SOMNATH
* **Register Number**: 212224240158
* **Date of Submission**: 17/3/26
---

## Title

Scale and Load Balance Your Architecture

---

## Objective

The objective of this lab is to understand how to design a scalable and highly available architecture on AWS using Auto Scaling and Elastic Load Balancing. This experiment focuses on distributing incoming traffic across multiple EC2 instances, automatically scaling resources based on demand, and validating fault tolerance.

---

## Prerequisites

* Basic knowledge of Amazon EC2 and VPC
* Completion of previous labs (IAM, EC2, EBS, Database Server)
* AWS Academy Lab access
* Stable internet connection

---

## Tools Used

* AWS Management Console
* Amazon EC2
* Elastic Load Balancer (ELB / ALB)
* Auto Scaling Groups (ASG)
* Amazon CloudWatch

---

## Tasks Performed

### Task 1: Review Existing Architecture

Students review the existing EC2-based application architecture created in previous experiments.

### Task 2: Create a Launch Template

Students create a launch template that defines the EC2 instance configuration including AMI, instance type, security group, and user data.

### Task 3: Create an Auto Scaling Group

Students create an Auto Scaling Group using the launch template and configure minimum, maximum, and desired instance capacity.

### Task 4: Configure an Application Load Balancer

Students create an Application Load Balancer and configure target groups for routing traffic to EC2 instances.

### Task 5: Register Auto Scaling Group with Load Balancer

Students attach the Auto Scaling Group to the target group of the load balancer.

### Task 6: Configure Scaling Policies

Students configure scaling policies based on CPU utilization using Amazon CloudWatch alarms.

### Task 7: Test Load Balancing and Scaling

Students test the setup by generating traffic and observing automatic scaling and load distribution.

---

## Workflow (Student Explanation)

1. I reviewed the existing EC2-based application architecture that I had created in previous experiments to understand how the instances were configured and how the application was being accessed.

2. I created a Launch Template by defining the EC2 configuration, including the Amazon Machine Image (AMI), instance type, key pair, security group, and user data script for automatic application setup during instance launch.

3. Using the launch template, I created an Auto Scaling Group. I configured the minimum, maximum, and desired capacity values to control how many EC2 instances should run based on demand. I also selected the appropriate VPC and subnets.

4. Next, I created an Application Load Balancer and configured a target group. I set the protocol and port (HTTP/HTTPS) and defined health check settings to monitor the EC2 instances.

5. I attached the Auto Scaling Group to the target group so that any instances launched by the Auto Scaling Group would automatically register with the Load Balancer.

6. I configured scaling policies based on CPU utilization. I created Amazon CloudWatch alarms to automatically increase the number of instances when CPU usage was high and decrease them when CPU usage was low.

7. Finally, I tested the setup by generating traffic to the Load Balancer DNS name. I observed that the traffic was distributed evenly across instances and that additional instances were launched automatically when the CPU utilization threshold was exceeded.

---

## Output Screenshots 

## TASK 1:
<img width="1600" height="964" alt="image" src="https://github.com/user-attachments/assets/41a2273d-f613-4689-82b3-5d317be0167b" />

## TASK 2:
<img width="1600" height="960" alt="image" src="https://github.com/user-attachments/assets/ea4b4b7c-574f-4d8d-bfb0-f8bd88fca2d8" />

## TASK 3:
<img width="1600" height="960" alt="image" src="https://github.com/user-attachments/assets/9cc677a9-2e82-4522-9dd1-fd6602917d8b" />

## TASK 4:
<img width="1600" height="957" alt="image" src="https://github.com/user-attachments/assets/4ae4b5a1-1b23-4ecb-9736-2ad4800e9338" />

## TASK 5:
<img width="1600" height="959" alt="image" src="https://github.com/user-attachments/assets/9b36f8e4-99d1-4663-b8ea-95196bffb6b7" />

## TASK 6:
<img width="1600" height="907" alt="image" src="https://github.com/user-attachments/assets/36fee4b3-a3b4-4be6-b5c9-3208450c21a7" />

---

## Result

This experiment demonstrated how to build a scalable and fault-tolerant cloud architecture using Auto Scaling Groups and Elastic Load Balancing. The system automatically adjusted resources based on workload and ensured continuous service availability by distributing traffic across multiple instances.
