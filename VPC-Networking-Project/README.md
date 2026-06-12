[README-3.md](https://github.com/user-attachments/files/28883621/README-3.md)
<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Build a Virtual Private Cloud

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-networks-vpc)

**Author:** Kyah Owens  
**Email:** kyahdowens@gmail.com

---

## Build a Virtual Private Cloud (VPC)

![Image](http://learn.nextwork.org/delighted_gold_peaceful_elderberry/uploads/aws-networks-vpc_2facf927)

---

## Introducing Today's Project!

In this project, I will demonstrate my ability to create and configure a Virtual Private Cloud (VPC) in AWS, including setting up networking components that allow cloud resources to communicate securely and efficiently.
I'm doing this project to learn the fundamentals of AWS networking and gain hands-on experience with core cloud infrastructure concepts such as VPCs, subnets, route tables, and internet gateways.

### What is Amazon VPC?

### Personal reflection

---

## Virtual Private Clouds (VPCs)

### What I did in this step

In this step, I will create a VPC in AWS because it is the foundation of a cloud network. This will help me learn how AWS networking is set up and how resources can be organized within a private network.

### How VPCs work

VPCs are private networks in AWS that allow you to organize, manage, and secure cloud resources. They provide control over networking settings such as IP addresses, connectivity, and access to resources.

### Why there is a default VPC in AWS accounts

There was already a default VPC in my account when it was created because AWS automatically provides one in each region. This allows users to launch resources quickly without having to configure a custom network first.

![Image](http://learn.nextwork.org/delighted_gold_peaceful_elderberry/uploads/aws-networks-vpc_2facf927)

### Defining IPv4 CIDR blocks

To set up my VPC, I had to define an IPv4 CIDR block, which is the range of private IP addresses my VPC can use

---

## Subnets

### What I did in this step

In this step, I will create subnets in my VPC because they help divide the network into smaller sections where different resources can be placed and managed.

### Creating and configuring subnets

Subnets are smaller sections of a VPC that help organize resources within a network.
There are already subnets existing in my account, one for every Availability Zone in the default VPC created by AWS.

### Public vs private subnets

The difference between public and private subnets is that resources in a public subnet can access the internet directly, while resources in a private subnet cannot.
For a subnet to be considered public, it has to have a route to an Internet Gateway.

![Image](http://learn.nextwork.org/delighted_gold_peaceful_elderberry/uploads/aws-networks-vpc_157c4219)

### Auto-assigning public IPv4 addresses

Once I created my subnet, I enabled auto-assign public IPv4 addresses. This setting makes sure new resources automatically receive a public IP address so that they can communicate with the internet.

---

## Internet gateways

### What I did in this step

In this step, I will create and attach an Internet Gateway to my VPC because it allows resources in my public subnet to connect to the internet.

### Setting up internet gateways

Internet gateways are AWS resources that connect a VPC to the internet, allowing resources inside the VPC to send and receive internet traffic.

Attaching an Internet Gateway to a VPC means connecting the VPC to the internet so resources can communicate outside the AWS network.
If I missed this step, resources in my public subnet would not be able to access the internet, even if they had public IP addresses.

![Image](http://learn.nextwork.org/delighted_gold_peaceful_elderberry/uploads/aws-networks-vpc_4ae90410)

---

## Using the AWS CLI

### What I'm doing in this extension

In this project extension, I will use the AWS CLI to launch my VPC resources because it can make the setup faster, more repeatable, and more efficient than clicking through each step in the AWS console.

### Exploring CloudShell and CLI

CloudShell is a browser-based terminal in AWS that lets you run commands and manage AWS resources without installing any software on your computer.
The AWS CLI (Command Line Interface) is a tool that lets you create, manage, and automate AWS resources by typing commands instead of using the AWS Management Console.

### Debugging my setup

To set up a VPC or a subnet, you can use the aws ec2 create-vpc or aws ec2 create-subnet command. Make sure to avoid errors by including the correct VPC ID and a valid CIDR block that fits inside your VPC’s IP range.

![Image](http://learn.nextwork.org/delighted_gold_peaceful_elderberry/uploads/aws-networks-vpc_9b2465411)

### Comparing CloudShell vs AWS Console

Compared to using the AWS Console, an advantage of using commands is that they can be faster and allow you to automate tasks without clicking through multiple screens.
An advantage of using the Console is that it provides a visual interface that makes it easier to see and manage resources.
Overall, I preferred the AWS Console because it was easier to understand and verify that my resources were configured correctly, although the CLI was faster once I knew the commands.

---

---
