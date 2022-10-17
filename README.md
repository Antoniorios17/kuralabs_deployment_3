<h1 align=center>Deployment 3</h1>
<div align=center>Deploy a flask application through a jenkins agent on a VPC</div>

# Table of contents

1. Set up and configure VPC
2. Install Jenkins on an EC2
3. Create an EC2 on the public subnet of your VPC
4. Configure the Jenkins agent on the VPC
5. Create a pipeline build on Jenkins
6. Additions
7. Diagram

## Set up and configure VPC
* Create a VPC on AWS
* Create 2 subnets a private and a public subnet 
* Configure the internet gateway
* Configure the routing tables
![tables](https://github.com/Antoniorios17/kuralabs_deployment_3/blob/main/images/routing%20tables.PNG)

## Install Jenkins on an EC2
The EC2 doesn't need to be part of the vpc, we are trying to connect the jenkins server from outside the VPC with an agent
* Create an EC2 on AWS and use an Ubuntu image.
* Configure RSA authentication for ssh remote access
* Configure the proper security groups for jenkins to fucntion properly (22, 80, 8080).
* Create a multiplebranch pipeline
* Connect to the repository on github using personal token
* Test to verify authentication is successful 


