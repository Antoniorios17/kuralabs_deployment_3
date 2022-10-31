<h1 align=center>Deployment 3</h1>
<div align=center>Deploy a flask application through a jenkins agent on a VPC</div>

# Table of contents


1. Install Jenkins on an EC2
2. Install terraform on the EC2
3. Configure credentials on Jenkins
4. Create a pipeline build on Jenkins
5. Create a VPC with terraform and deploy the application
6. Additions
7. Diagram
 
![tables](<link>)

## Install Jenkins on an EC2
The EC2 doesn't need to be part of the vpc, we are trying to connect the jenkins server from outside the VPC with an agent
* Create an EC2 on AWS and use an Ubuntu image.
* Configure RSA authentication for ssh remote access
* Configure the proper security groups for jenkins to function properly (22, 80, 8080).
* Install jenkins on the EC2 with all dependencies
* Create a multiplebranch pipeline
* Connect to the repository on github using personal token
* Test to verify authentication is successful

# Additions
## Webhook
* To make the current configuration more automated you can connect jenkins to the github repository:
  * Log in to github and access the repository online
  * "Settings" of the repository
  * Select "Webhoooks"
  * Add Webhook
  * ```
    http://{Ip-address}:8080/github-webhook/
    ```
## Update the front end
* this is a very simple change to the UI
* I added my name as part of the website page
* Updated the color of the front page
* This is the original page:

![UI-before](https://github.com/Antoniorios17/kuralabs_deployment_3/blob/main/images/UI-before.PNG)

* This is the website after the changes:

![UI-after](https://github.com/Antoniorios17/kuralabs_deployment_3/blob/main/images/UI-after.PNG)


# Diagram

![diagram](https://github.com/Antoniorios17/kuralabs_deployment_3/blob/main/images/diagram.PNG)

# Stack

![stack](https://github.com/Antoniorios17/kuralabs_deployment_3/blob/main/images/STACK.PNG)





