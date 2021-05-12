

![alt 16](Images/16.png)

### Create Custom VPC with public and private subnet
## Project Description

In this project I have created a custom VPC in AWS. The reference architecture diagram is provided as the project logo. I have created two subnets where one is a public subnet and the other is a private subnet. The public subnet could simulate as Web Server which is the Application Tier. For maintaining security concerns, the private subnet could simulate as Database Server which is the Database Tier.

## Follow Along:

# Part 1: Designing the VPC Architecture

Create VPC in the AWS Management Console:

![alt 1](Images/1.png)

Create new subnets, I will create two subnets where I will make one public subnet and one private subnet. Make sure the CIDR ranges don't clash between the subnets:

![alt 2](Images/02.png)

![alt 3](Images/3.png)

![alt 4](Images/4.png)

Now we need to create an Internet Gateway:

![alt 5](Images/5.png)

After creating an Internet Gateway, we need to attach this to our Custom VPC to give our VPC internet access:

![alt 6](Images/6.png)

After successfully attaching this Internet Gateway to our custom VPC, the Internet Gateway State should specify as "Attached":

![alt 7](Images/7.png)

Now we need to create a new Route Table and we will associate this route table with the Internet Gateway:

![alt 8](Images/8.png)

![alt 9](Images/9-10.png)

Now we will make our Subnet 1 as our Public Subnet. To do this, select "Edit Subnet Associations" and then choose the Subnet 1 that we created earlier:

![alt 11](Images/11.png)

One crucial task to make any subnet as public subnet is by enabling " Auto-Assign IPv4 address". We need to ebnable this option for our Subnet 1:

![alt 12](Images/12.png)

# Part 2: Creating EC2 Resources to put our Application Tier and Database Tier inside our Custom VPC:
Now we can start putting resources inside our VPC. Let's assume the Application and Database Tier will be put on two different EC2 Instances. We will create two new EC2 Instances. We will put Application Tier EC2 instance in Public Sunet 1 and then we will put the Database Tier EC2 Instance in Private Subnet of our VPC:

![alt 13](Images/13.png)

![alt 14](Images/14.png)

![alt 15](Images/15.png)


## Contact 
Priyanka Patel - https://www.linkedin.com/in/priyanka-patel-5088721a9/
