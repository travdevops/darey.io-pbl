# The LEMP Webstack Implementation Project

 * Lemp Implementation Involves Installing Various Programs and Packages, Another technology stack which is a set of frameworks and tools used to develop a software product.

 * LEMP (Linux, Nginx, MySQL, PHP)

       - Linux - The Operating System Environment. 
       - Nginx - The Web Server.
       - MySQL - The Database Management System.
       - Php   - The Programming Language.
     

 * Project 2 covers similar concepts as Project 1 (LAMPstack) and helps to cement the skills needed for deploying Web solutions using webstacks.

* In this project we will implement a similar stack, but with an alternative Web Server – [NGINX](https://nginx.org/en/), which is also very popular and widely used by many websites in the Internet.

# Gathering the Prerequisities

 To successfully finish this project, we'll require an AWS account and a virtual server running Ubuntu Server OS. I already have ec2 Instance of t2.micro family with Ubuntu Server 20.04 LTS (HVM) image. 

 * After successfully launching the ec2 Instance on AWS and spinning up the server on the command line, (we'll be making use of [TERMIUS](termius.com) as the command line as opposed to the normal local machine terminal)

# Install the NGINX Web Server.

* We'll first of all update the apt package manager to have all the latest server package indexes.
* `sudo apt update`

<img width="937" alt="Screenshot 2023-08-25 at 7 37 58 PM" src="https://github.com/travdevops/darey.io-pbl/assets/137777644/ce7af212-88c1-4540-b92e-1153fe1587dd">



* Then we install the web server NGINX
* `sudo apt install nginx`

<img width="1222" alt="Screenshot 2023-08-25 at 7 39 59 PM" src="https://github.com/travdevops/darey.io-pbl/assets/137777644/8fa0e466-eb80-4042-8c76-423f8c561bb4">

* Verify that NGINX was successfully installed and is running as a service
* ` sudo systemctl status nginx`

<img width="930" alt="Screenshot 2023-08-25 at 7 41 30 PM" src="https://github.com/travdevops/darey.io-pbl/assets/137777644/153cb84c-209d-4bc1-8856-c84d2eed245b">

* Before any traffic can on the web server we just installed, we need to open TCP Port 80 (default port) that web browsers use to access the webpages online.

*  On the security settings of the ec2 Instance on AWS, We will edit inbound rules and add a new rule for the HTTP to listen to the default port 80 and to be accessible through the IP Address.

<img width="1316" alt="Screenshot 2023-08-25 at 7 43 03 PM" src="https://github.com/travdevops/darey.io-pbl/assets/137777644/24c99bac-cd17-4e2a-b9c8-80d434a3782f">

* Proceeding on saving the new inbound rule, run the command below to access it locally
* `$ curl http://localhost:80` or $ `curl http://127.0.0.1:80`
* We can either use our Public DNS Name or Public IP Address to access it locally.

<img width="591" alt="Screenshot 2023-08-25 at 7 49 29 PM" src="https://github.com/travdevops/darey.io-pbl/assets/137777644/5f561c12-4875-4c90-bd6e-3546ee23681d">


* Now, we'll test to see how the NGINX server responds to internet requests on any browser.
* Run this http://(Public-IP-Address):80
* The webpage shows this result confirmed our NGINX server's Installation. 

<img width="836" alt="Screenshot 2023-08-25 at 7 51 34 PM" src="https://github.com/travdevops/darey.io-pbl/assets/137777644/1eecf5df-742c-4a87-93e2-f2c684202d4a">



