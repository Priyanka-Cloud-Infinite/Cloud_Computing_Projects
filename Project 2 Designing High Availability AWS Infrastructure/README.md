### Designing High Availability AWS Infrastructure
## Project Description
This is a medium difficulty level project. Based on the reference architecture diagram, we will design high available system. We will create AMI for our desired EC2 Instances which will be bootstrapped for starting an Apache Webserver. We will create load balancers, launch configurations and auto scaling groups. We will run 2 EC2 instances in different public subnets and it gets auto provisioned when old EC2 Instances are down.
## Follow Along:
# Part 1: Create AMI from an EC2 Instance
Head over to EC2 in services from AWS Management Console. Then "Launch Instance" :

![alt 2](Images/02.png)

We will create free tier eligible instance :

![alt 3](Images/3.png)

Keep everything default, we will provide the Bootstrap Script in the "User Data" from the "Advanced Settings" :

![alt 4](Images/4.png)

Here is the Bootstrap Script for better view:

![alt 5](Images/5.png)

In the security group we will open another rule for "HTTP" connection:

![alt 6](Images/6.png)

Now let's check if our webserver is serving the desired content properly or not. Grab the Public IPv4 address:

![alt 7](Images/7.png)

If the webserver is working correctly, then it should view this in a new browser :

![alt 8](Images/8.png)

Now, we will create an AMI from this EC2 instance that we have just deployed. Follow the picture given below to create an image:

![alt 9](Images/9.png)

Keep veryhting default and give a name to this image:

![alt 10](Images/10.png)

Now go to "Images" section and click "AMIs". Our new image should show "available" in status:

![alt 11](Images/11.png)

Now we can terminate the EC2 instance that we have created, the main purpose was to create a custom AMI which we have completed:

![alt 12](Images/12.png)

# Part 2: Creating Application Load Balancer
Go to Load Balancer, create a new load balancer and choose Application Load Balancer :

![alt 13](Images/13.png)

Give a name to the Load Balancer and choose two availability zones. Make sure these availability zones are part of public subnet and not private subnet :

![alt 14](Images/14.png)

We will create a new security group and keep the default rule :

![alt 15](Images/15.png)

After successfully creating the load balancer:

![alt 16](Images/16.png)

# Part 3: Creating Launch Configuration and Auto Scaling Group
Select " Create Launch Configuration" :

![alt 17](Images/17.png)

This is an important stage, we will open another rule in the security group in our launch configuration and this new rule type should be of HTTP and the source should be security group ID of the the one that we created for our Application Load Balancer:

![alt 18](Images/18.png)

Now we will create the auto scaling group and we will select the launch configuration that we have created earlier :

![alt 19](Images/19.png)

Configure the settings for the Auto Scaling Group like this below :

![alt 20](Images/20.png)

Don't forget to attach our existing Application Load Balancer in this Auto Scaling Group:

![alt 21](Images/21.png)

Since the design requires two EC2 Instances, we will custoize the group size based on that:

![alt 22](Images/22.png)

After successful creation of the Auto Scaling Group, it should like this as the picture given below:

![alt 23](Images/23.png)

# Part 4: Accessing our High Availability Infrastrcuture Design :
Let's see if everything is working properly. Goto the created Load Balancer and copy the DNS Name. We will check this DNS name in a separate browser window:

![alt 24](Images/24.png)

It should look like this in the browser:

![alt 25](Images/25.png)


## Contact 
Priyanka Patel - https://www.linkedin.com/in/priyanka-patel-5088721a9/
