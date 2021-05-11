# Make an EC2 Instance a webserver and Bootstrapping
## Project Description
This is fairly a simple project in two parts. The first part focuses on creating an EC2 instance from the AWS Management Console and then connecting to this instance from Putty. Then follow some manual process to install Apache Web Server and print the instance id in the html page. The second part of this project focuses on automating the whole process by bootstrapping the EC2 instance.

## Follow Along:
###  Part 1  
Create any Free Tier eligible EC2 instance. Use "Putty" and "PuttyGen" to convert the key-pair pem file to a ppk file. After successfully login to the EC2 instance from command prompt, it should like something like this:

![1](https://user-images.githubusercontent.com/83409681/117763005-b2f8bd00-b247-11eb-8309-236091843d06.png)

Install Apache Web Server in the EC2 instance:

![2](https://user-images.githubusercontent.com/83409681/117763140-ec312d00-b247-11eb-827a-71e2bfbe077c.png)

Print the instance id as the index.html page for the Apache web server

![3](https://user-images.githubusercontent.com/83409681/117763215-1125a000-b248-11eb-8bef-44a991acb6ef.png)

Start the Apache Web Server

![4](https://user-images.githubusercontent.com/83409681/117763261-24d10680-b248-11eb-89d9-05d6b8985f38.png)

Copy the Public IPv4 address and view it in browser

![5](https://user-images.githubusercontent.com/83409681/117763288-30bcc880-b248-11eb-9953-98f36074ebe9.png)

The Final Output for Part 1:

![6](https://user-images.githubusercontent.com/83409681/117763324-416d3e80-b248-11eb-95c9-ff5100c2d8e1.png)

### Part 2: Bootstrap
Create another free tier eligible EC2 instance and in the "User Data" write like the following:

![7](https://user-images.githubusercontent.com/83409681/117763374-5518a500-b248-11eb-859d-f9020d1999e3.png)

The Final Output for Part 2:

<img width="159" alt="8" src="https://user-images.githubusercontent.com/83409681/117763392-5cd84980-b248-11eb-960c-6e2afaeb996d.png">


## Contact 
Priyanka Patel - https://www.linkedin.com/in/priyanka-patel-5088721a9/
