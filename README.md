 
🌐🚀**Guide to Deploy NodeJs Application on AWS Ec2**🌐🚀

Welcome to our step-by-step guide on deploying the DeployNodeJs_AWS project! Whether you're a beginner or someone unfamiliar with technical jargon, we've crafted this guide to make the process easy to follow.

Whenever you have start any project ,Please make sure your project is running successfully in locally .

**Testing the Project Locally**
* Clone the Project
  First things first, let's get the project onto your computer. Open a command prompt or terminal and run the following command:
  git clone https://github.com/sprasadpujari/DeployNodeJs_AWS.git
  ![image](https://github.com/sprasadpujari/DeployNodeJs_AWS/assets/136614692/0e6d7bd6-354f-4cbf-bbe1-b2345b2e9940)

* Download and installed Node Js using below URL
  https://nodejs.org/en/download
  
* Create a .env file using below command
  touch .env
  
* Set Up Environment Variables
  Now, let's configure some basic settings. Create a file named .env in the project's main folder and add the following lines:
  Create a .env file in the project root and add the following variables:
  DOMAIN=""
  PORT=3000
  STATIC_DIR="./client"
  PUBLISHABLE_KEY=""
  SECRET_KEY=""
  ![image](https://github.com/sprasadpujari/DeployNodeJs_AWS/assets/136614692/85eeb29b-57b1-458e-9d5d-6caeec4d162c)

* Initialise and Start the Project
  npm install
  npm run start
  ![image](https://github.com/sprasadpujari/DeployNodeJs_AWS/assets/136614692/19aa1def-dcb5-4538-bc1b-30a9f8dfdcee)

**Now lets start Set Up an AWS EC2 Instance**
* Create an IAM User
  1.Log in to your AWS Console.
  2.Create a new IAM user with access type "Password" and permissions set to "Admin".
* Create an EC2 Instance
  1.Launch a new EC2 instance with the following configurations:
  2.OS Image: Ubuntu
  3.Key Pair: Create a new key pair and download the .pem file
  4.Instance Type: t2.micro

* Connect to the Instance Using SSH
  Once connected, update the system and install some necessary tools:
  ssh -i instance.pem ubuntu@<IP_ADDRESS>
  ![image](https://github.com/sprasadpujari/DeployNodeJs_AWS/assets/136614692/56cb2a59-e10c-4506-92c7-262b0b2e9d7e)

* Configure Ubuntu on Remote VM
  Update outdated packages and dependencies:
  ![image](https://github.com/sprasadpujari/DeployNodeJs_AWS/assets/136614692/af49d391-53ae-4e42-92a9-518fa32aa9e8)z
 Follow the guides by DigitalOcean to install Git, Node.js, and npm.


**Deploying the Project on AWS**
* Clone the Project on Remote VM
  Back in the terminal, clone the project onto your AWS instance:
  ![image](https://github.com/sprasadpujari/DeployNodeJs_AWS/assets/136614692/b680fe7e-350e-42a9-b657-151f57fcf0b8)

* Set Up Environment Variables on Remote VM
  Create a .env file in the project root and add the following variables:
  ![image](https://github.com/sprasadpujari/DeployNodeJs_AWS/assets/136614692/5fcdd68f-05e1-49e6-b01d-c4ff211f0bda)

* Elastic IP Address Setup
  For this project, you'll need an Elastic IP Address for your EC2 instance. This will act as your project's domain.

* Initialise and Start the Project on Remote VM
  Back in the terminal, run these commands:
  ![image](https://github.com/sprasadpujari/DeployNodeJs_AWS/assets/136614692/11cc7744-5264-4232-8a21-58d3b852644a)

 **Note**
  Don't forget to adjust the inbound rules in your EC2's security group to allow traffic on the specified port.
  our port is 3000

  Congratulations! Your project is now deployed on AWS. 🎉

  This guide should help you navigate through the technicalities and successfully deploy your Node.js project on AWS. If you encounter any difficulties, feel free to reach out for assistance. Happy coding! 🚀
  

  






  


