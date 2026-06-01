<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Cloud Security with AWS IAM

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-security-iam)

**Author:** Kyah Owens  
**Email:** kyahdowens@gmail.com

---

![Image](http://learn.nextwork.org/delighted_gold_peaceful_elderberry/uploads/aws-security-iam_1c864649)

---

## Introducing Today's Project!

### Project overview

In this project, I will demonstrate...  using the 
AWS Identity and Access Management (IAM) service to control who is authenticated (signed in) and authorized (has permissions) in your AWS account.

### Tools and concepts

Services I used were: AWS Identity and Access Management (IAM) and Amazon EC2. IAM was used to create policies, user groups, and users to manage access permissions, while EC2 was used to launch and manage development and production virtual server instances.
Key concepts I learnt include: Identity and Access Management (IAM), the principle of least privilege, authentication vs. authorization, IAM policies, user groups, users, resource tagging, access control through conditions, and managing cloud infrastructure with EC2 instances. I also learned how to use IAM policies to restrict access to specific resources based on tags and how user groups simplify permission management for multiple users.

### Project reflection

This project took me approximately... 55 minutes The most challenging part was...create users. It was most rewarding to...finish the project

---

## Tags

### What I did in this step

In this step, I will... Launch two Amazon EC2 instances because...I need to increase computing power

### Understanding tags

Tags are...like labels you can attach to AWS resources for organization.

### My tag configuration

The tag I’ve used on my EC2 instances is called...Name and Env. The value I’ve assigned for my instances are...nextwork-prod-kyahowens,nextwork-dev-kyahowens and production

![Image](http://learn.nextwork.org/delighted_gold_peaceful_elderberry/uploads/aws-security-iam_2e0e5a5d)

---

## IAM Policies

### What I did in this step

In this step, I will... create an IAM policy that gives access to the development instance because...it's time to onboard the team's new intern and set up permission policies

### Understanding IAM policies

IAM Policies are... rules for who can do what with your AWS resources. It's all about giving permissions to IAM users, groups, or roles, saying what they can or can't do on certain resources, and when those rules kick in.

### The policy I set up

For this project, I’ve set up a policy using...JSON

### Policy effect

I’ve created a policy that...defines a list of permissions.

### Understanding Effect, Action, and Resource

The Effect, Action, and Resource attributes of a JSON policy means...Effect:This can have two values - either Allow or Deny - to indicate whether the policy allows or denies a certain action. Deny has priority. Looking at the first statement, "Effect": "Allow" means this statement is trying to allow for an action.

‍Action:
‍A list of the actions that the policy allows or denies. In this case, "Action": "ec2:*" means all actions that you could possibly take on EC2 instances are allowed. Woohoo!

‍Resource:
‍Which resources does this policy apply to? Specifying "*" means all resources within the defined scope (see the next point).

---

## My JSON Policy

![Image](http://learn.nextwork.org/delighted_gold_peaceful_elderberry/uploads/aws-security-iam_1c864649)

---

## Account Alias

### What I did in this step

In this step, I will... simplify user login to your AWS account using an Account Alias because...its easier for the intern to access.

### Understanding account aliases

An account alias is...a friendly name for your AWS account that you can use instead of your account ID (which is usually a bunch of digits) to sign in to the AWS Management Console.

### Setting up my account alias

Creating an account alias took me...1 minute. Now, my new AWS console sign-in URL is...nextwork-alias-kyahowens.


![Image](http://learn.nextwork.org/delighted_gold_peaceful_elderberry/uploads/aws-security-iam_0eb4439b)

---

## IAM Users and User Groups

### What I did in this step

In this step, I will...set up a dedicated IAM group for all NextWork interns, so you can manage all interns' permissions from one place and set up a dedicated IAM user for your new intern, so they have a way to log in.

### Understanding user groups

IAM user groups are...the people that will get access to your resources/AWS account

### Attaching policies to user groups

I attached the policy I created to this user group, which means...managing permissions and ensures consistency across users who have similar access to AWS resources.

### Understanding IAM users

IAM users are...Individual login credentials with their own username and password, so nobody shares the main account

---

## Logging in as an IAM User

### Sharing sign-in details

The first way is...email sign-in instructions


### Observations from the IAM user dashboard

Once I logged in as my IAM user, I noticed... ashboard panels are showing Access denied already. This was because...of the permission policy set 


![Image](http://learn.nextwork.org/delighted_gold_peaceful_elderberry/uploads/aws-security-iam_6f2ab446)

---

## Testing IAM Policies

### What I did in this step

In this step, I will...log into AWS using the intern's IAM use because...i need to test the intern's access to your production and development instance.

### Testing policy actions

I tested my JSON IAM policy by...testing the intern's access to your production and development instance.

### Stopping the production instance

When I tried to stop the production instance... Failed. This was because...user is not authorized to perform this operation

![Image](http://learn.nextwork.org/delighted_gold_peaceful_elderberry/uploads/aws-security-iam_0e7a9d6a)

### Stopping the development instance

Next, when I tried to stop the development instance... it stopped it This was because...the user was allow to perform the operation

![Image](http://learn.nextwork.org/delighted_gold_peaceful_elderberry/uploads/aws-security-iam_1811801c)

---

## IAM Policy Simulator

To extend my project, I'm going to...You can use a special IAM tool called the 
Policy Simulator to validate policies without affecting your actual AWS resources.

### Understanding the IAM Policy Simulator

The IAM Policy Simulator is to validate policies without affecting your actual AWS resources.

### How I used the simulator

I set up a simulation for... delete tag and stop instances The results were... both denied until I had to adjust...the instance

![Image](http://learn.nextwork.org/delighted_gold_peaceful_elderberry/uploads/aws-security-iam_069d8a621)

---

---
