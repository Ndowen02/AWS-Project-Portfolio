<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Host a Website on Amazon S3

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-host-a-website-on-s3)

**Author:** Kyah Owens  
**Email:** kyahdowens@gmail.com

---

![Image](http://learn.nextwork.org/delighted_gold_peaceful_elderberry/uploads/aws-host-a-website-on-s3_5d4474f9)

---

## Introducing Today's Project!

### Project overview

In this project, I will demonstrate... I'm doing this project to learn how to use Amazon S3  (which stands for Amazon Simple Storage Service) to host a website.

### Tools and concepts

The key services I learned in this project were Amazon Web Services S3 buckets, static website hosting, object permissions/ACLs, and bucket policies. Key concepts I learned include how website hosting works, how static websites are deployed using S3, how to make files publicly accessible, and how bucket policies and ACLs control access and security for files stored in the bucket.

### Time, challenges, and wins

This project took me approximately... 1 hour The most challenging part was...policy. It was most rewarding to...figure out I was just missing an ' " ' in my json line of code .

---

## How I Set Up an S3 Bucket

### What I did in this step

In this step, I will create a storage space for my website files 

### How long it took to create the bucket

Creating an S3 bucket took me...10-15 minutes 

### Region selection

The Region I picked for my S3 bucket was... ohio because it was closest.

### Understanding bucket name uniqueness

S3 bucket names are globally unique! This means...no other AWS account in the world will be able to use my bucket's name.

![Image](http://learn.nextwork.org/delighted_gold_peaceful_elderberry/uploads/aws-host-a-website-on-s3_ba6d42ad)

---

## Upload Website Files to S3

### What I did in this step

In this step, I will... download an HTML file and zip fille because...i need to upload it into my S3 bucket.


### Files I uploaded

I uploaded two files to my S3 bucket - they were...index HTML file and a zipped folder


### How the files work together

Both files are necessary for this project as...HTML is to structually setup the website and the folder contains all the images and etc to insert into the website 


![Image](http://learn.nextwork.org/delighted_gold_peaceful_elderberry/uploads/aws-host-a-website-on-s3_a265af88)

---

## Static Website Hosting on S3

### What I did in this step

In this step, I will... configure my S3 bucket for statice website hosting because...i need to able to visit my public website link.


### Understanding website hosting

Website hosting means...making your website publicly available on the internet so anyone can visit it! 

### How I enabled website hosting

To enable website hosting with my S3 bucket, I...enable static web hosting  in the static website hosting panel at the bottom of the properties tab then select hosting type and enter the index .html 

### Access Control Lists (ACLs)

An ACL is...a set of rules that decides who get access to what resource. I enabled ACLS so i can control who can access and do things with my website files

![Image](http://learn.nextwork.org/delighted_gold_peaceful_elderberry/uploads/aws-host-a-website-on-s3_c22c54c0)

---

## Bucket Endpoints

### Understanding bucket endpoint URLs

Once static website is enabled, S3 produces a bucket endpoint URL, which is...just like a regular website URL. It lets people visit your S3 bucket's files as a website.

### What I saw when I tested the endpoint

When I first visited the bucket endpoint URL, I saw... The reason for this error was...the HTML and images files I uploaded are private by default. This default setting helps keep your account's data secure.

![Image](http://learn.nextwork.org/delighted_gold_peaceful_elderberry/uploads/aws-host-a-website-on-s3_22ce4daf)

---

## Success!

### What I did in this step

In this step, I will... make my websites files in S3 publicaly accessible because...i need to see my website live on the internet.

### How I resolved the 403 error

To resolve this 403 Forbidden error, I...went to object page , selected the file then made them publuc using ACLs

![Image](http://learn.nextwork.org/delighted_gold_peaceful_elderberry/uploads/aws-host-a-website-on-s3_5d4474f9)

---

## Bucket Policies

### What I did in this extension

In this project extension I'm about to... Set up a bucket policy and 'm doing this so that... it stops people from deleting my index.html file.

### Understanding bucket policies

An alternative to ACLs are bucket policies, The benefit of using bucket policies is... controlling access for the entire bucket at once while ACLs are useful for... controlling access for individual objects (e.g., making just one file public while keeping others private) 

![Image](http://learn.nextwork.org/delighted_gold_peaceful_elderberry/uploads/aws-host-a-website-on-s3_sm2sm2sm)

### What my bucket policy does

My bucket policy makes everything public, or blockes all deleted actions tested this by...setting up a bucket policy that stops people from deleting your index.html file and saw...that i wasnt able to delete the file.

---

---
