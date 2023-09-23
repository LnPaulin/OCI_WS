# Deploying a Webserver on Oracle Cloud

# <b>Introduction</b>

In this project, I successfully implementation of a project on Oracle Cloud Infrastructure (OCI). The project's primary objective was to create a Virtual Cloud Network (VCN), configure security lists to accept incoming TCP requests on port 80, deploy an Ubuntu instance in a public subnet, connect to the instance, install and configure the Uncomplicated Firewall (UFW), install the Apache2 web server, and replace the default Apache index.html file with a simple static website from a GitHub repository.

# <b>Project Objectives</b>
<b>VCN Creation:</b> Create a Virtual Cloud Network (VCN) within Oracle Cloud Infrastructure (OCI) to host the project resources.

**Security List Configuration:** Configure security lists to allow incoming TCP requests on port 80 to ensure web accessibility.

**Instance Deployment:** Deploy an Ubuntu instance within a public subnet of the VCN.

**Instance Access:** Establish SSH connectivity to the Ubuntu instance.

**Firewall Configuration:** Install and configure the Uncomplicated Firewall (UFW) on the Ubuntu instance to manage traffic.

**Web Server Installation:** Install and configure the Apache2 web server on the Ubuntu instance.

**Static Website Deployment**: Replace the default Apache index.html file with a static website retrieved from a GitHub repository.

Project Execution
# 1. VCN Creation
The project began with the creation of a Virtual Cloud Network (VCN) within the Oracle Cloud Infrastructure Console. The VCN was configured with a CIDR block of 10.0.0.1/16 , a public subnet with CIDR block of 10.0.0.1/24, and a private subnet with CIDR block of 10.0.1.1/14. The public subnet was designated for the Ubuntu instance, ensuring external accessibility, while the private subnet was intended for future internal resources.

# 2. Security List Configuration
Security lists were configured to allow incoming TCP traffic on port 80 (HTTP) within the public subnet. The following rules were added to the security list:

<img src="https://i.imgur.com/enBQh5N.png">

Ingress Rule: Allow TCP traffic from any source to destination port 80.
# 3. Instance Deployment
An Ubuntu instance was created in the public subnet of the VCN. The instance was provisioned with suitable hardware specifications and was associated with a key pair for secure SSH access. The instance was equally provided with a public IPv4 address that will be used to communicate with the instance from the public internet.

<img src="https://i.imgur.com/u0eFeB0.png">

# 4. Instance Access
SSH access to the Ubuntu instance was established using the provided key pair onc the OCI cloud shell. The private key was used to securely login to the instance. I used the following command <i>ssh -i ssh-key-2023-09-03.key ubuntu@150.136.160.133</i>

<img src="https://i.imgur.com/irZmXTz.png">

# 5. Firewall Configuration (UFW)
The Uncomplicated Firewall (UFW) was installed and configured on the Ubuntu instance to manage incoming and outgoing traffic. The following rules were applied:

Allow incoming SSH connections (port 22).
Allow incoming HTTP connections (port 80).
Block all other incoming connections.
6. Web Server Installation
Apache2, a widely used web server software, was installed on the Ubuntu instance. This enabled the instance to serve web content to incoming requests on port 80.

# 7. Static Website Deployment
The default Apache index.html file located at /var/www/html/ was replaced with a simple static website. This website was obtained from my GitHub repository, and the necessary files were cloned to the server.

Conclusion
The project was successfully completed, meeting all of its objectives. A Virtual Cloud Network (VCN) was created, security lists were configured to allow HTTP traffic, an Ubuntu instance was deployed, SSH access was established, the Uncomplicated Firewall (UFW) was configured, Apache2 was installed and configured as the web server, and a static website from a GitHub repository was deployed.

<img src="https://i.imgur.com/24Ec1JI.png">

# YouTube Demonstration

Here is a step by step guid to this project:  <a href="https://www.youtube.com/watch?v=2KKESuTnyTM&list=PL9V0QedB-FPI1HwJTUFYdE05aSCZj1wnf">Tutorial</a>

This project demonstrates the effective use of Oracle Cloud Infrastructure (OCI) for creating a secure and accessible web hosting environment. The skills and knowledge gained from this project can be applied to various scenarios within the cloud environment.


