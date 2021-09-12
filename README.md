### Udagram - Udacity Project 
This repository contains the YAML code for the "ND9991 - C2- Infrastructure as Code - Deploy a high-availability web app using CloudFormation" project from Udacity. 

The Cloud Formation script was designed to build the following infrastructure:

![](C:\Users\A0097118\Desktop\Curso Udacity\Parte 3\infrastructure-as-code-project\diagram\Udacity-Project-IAC-Diagram.png)

This repository contains the following files:


##### 1. final-project-starter.yml
Cloud Formation code using YAML template to build the cloud infrastructure, as required for the project. 

##### 2. parameters.json
File contaning the parameters:

* EnvironmentName;
* VPCCIDR 
* PrivateSubnet1CIDR
* PrivateSubnet2CIDR
* PublicSubnet1CIDR
* PublicSubnet2CIDR

The description for each parameter can be found in the file **final-project-starter.yml**

### Create the stack 

In order to create the stack in AWS type the following bash command in the terminal:

```bash
aws cloudformation create-stack --stack-name udagram-stack --template-body final-project-starter.yml --parameters parameters.json --capabilities "CAPABILITY_IAM" "CAPABILITY_NAMED_IAM" --region=us-west-2
```

