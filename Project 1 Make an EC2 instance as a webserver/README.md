# Make an EC2 Instance a webserver and Bootstrapping
## Project Description
This is fairly a simple project in two parts. The first part focuses on creating an EC2 instance from the AWS Management Console and then connecting to this instance from Putty. Then follow some manual process to install Apache Web Server and print the instance id in the html page. The second part of this project focuses on automating the whole process by bootstrapping the EC2 instance.

## Follow Along:
###  Part 1
Create any Free Tier eligible EC2 instance. Use "Putty" and "PuttyGen" to convert the key-pair pem file to a ppk file. After successfully login to the EC2 instance from putty, it should like something like this:

<img width="328" alt="1" src="https://user-images.githubusercontent.com/83409681/117666084-1d1a4f00-b1c1-11eb-946e-b8da491e892c.png">
Install Apache Web Server in the EC2 instance:

<img width="332" alt="2" src="https://user-images.githubusercontent.com/83409681/117666495-88fcb780-b1c1-11eb-9315-b1440e57a640.png">

Print the instance id as the index.html page for the Apache web server

<img width="333" alt="3" src="https://user-images.githubusercontent.com/83409681/117666645-b34e7500-b1c1-11eb-97b3-45ddb5580b22.png">

Start the Apache Web Server

<img width="332" alt="4" src="https://user-images.githubusercontent.com/83409681/117666746-d11bda00-b1c1-11eb-8df1-04a7e9eb5c91.png">

Copy the Public IPv4 address and view it in browser

<img width="366" alt="5" src="https://user-images.githubusercontent.com/83409681/117666747-d11bda00-b1c1-11eb-8ed5-4b3d9cbddda3.png">

The Final Output for Part 1:

<img width="201" alt="6" src="https://user-images.githubusercontent.com/83409681/117666738-cf521680-b1c1-11eb-9a14-90aca8241387.png">

### Part 2: Bootstrap
Create another free tier eligible EC2 instance and in the "User Data" write like the following:

<img width="473" alt="7" src="https://user-images.githubusercontent.com/83409681/117666743-cfeaad00-b1c1-11eb-91b6-57001c85dc1a.png">

The Final Output for Part 2:

<img width="159" alt="8" src="https://user-images.githubusercontent.com/83409681/117666744-d0834380-b1c1-11eb-99af-5396eb2a1cc6.png">


## Contact 
Priyanka Patel - https://www.linkedin.com/in/priyanka-patel-5088721a9/
