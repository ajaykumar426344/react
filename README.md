# smartcrow.ai

Envirnoment choosen = AWS
Services used = Route53, EC2
O.S version = Ubuntu 20.04.1 LTS
Packages used : Nginx, Gunicorn, Docker, Docker-compose, python3, NodeJS, NPM, Flask.


Task -1 ->Dockerizing Application

#EC2 - configuration 
Choosen t2.micro which has 1 vcpu and 1gb memory to host the application. which cost's arround 9.50$ + tax for the usage of 750hrs.

#EC2 - security
Blocked all the ports which are not used and allowed 22, 443, 5000, 3000, 80.

#EC2 - Accessing
Using Putty to login into the instance.

#Hosting Application:
  ->As per the requirement, created 3 container's i.e 1st React app, 2nd Nginx proxy server and 3rd Gunicorn server with flask application.
  
  ->Apart from Python container, other two container's were built in alpine flavour to comsume less space.
  
  ->Entered the dependencies which were required in requirements.txt file under api folder for the Python Appllication.
  
  ->Hosted the React App in Nginx and configured a reverse proxy server.
  
  ->Hosted Flask app in gunicorn and exposed it to 5000.
  
  ->Used Docker-compose to spin up the complete application in one go with the command " docker-compose up --build".
  
  ->Bought reactai.tk domain from freenom.com and created a hosted zone in Route53 and mapped it to the instance.
  
  
#Task 2 - Deploying in Cloud

As stated above Cloud platform choosen was AWS.

#Nginx - Hosting Application to the internet

  ->Assgined Elastic I.P to the container and configured teh Route53 as well as the Application accordingly.
  
  ->Configured Nginx container in such way that it listens the traffic at port 80 and communicate with the React Application.
  
  ->As checked with the web address www.reactai.tk , the application was up and running.
  
  ->Created an IAM role to monitor, access and modify, if required.
  
  ->Only the required ports were exposed to the internet form the docker as well as from the AWS level.
  
  
  
************************************************************************END of the Documentation*******************************************************************************
