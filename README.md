# AWS-Monitoring-and-Alert-Management


## What is monitoring in AWS ?
- Amazon Web Services (AWS) monitoring is a set of practices you can use to verify the security and performance of your AWS resources and data.
  These practices rely on various tools and services to collect, analyze, and present data insights.
  
- Cloud monitoring is the process of evaluating the health of cloud-based IT infrastructures.
- Using cloud-monitoring tools, organizations can proactively monitor the availability, performance, and security of their cloud environments to find and fix problems  before they impact the end-user experience.

- Tools we use for monitoring on AWS are cloud watch and SNS:

## Benefits of Monitoring:

![image](https://user-images.githubusercontent.com/110182832/186391766-5e20bc09-7b55-46ef-9b24-290b58c41364.png)



- Amazon CloudWatch gives you the facility of checking the resource on Cloud.
- It enables you to respond quickly to the events or error occurred at run time.
- The notifications from AWS services delivered in near real-time will facilitate Amazon CloudWatch events to respond quickly.


## What is cloud watch ?
- Amazon CloudWatch is a monitoring and management service that provides data and actionable insights for AWS, hybrid, and on-premises applications and infrastructure resources. You can collect and access all your performance and operational data in the form of logs and metrics from a single platform rather than monitoring them in silos (server, network, or database).


## What services cloud watch can monitor ?
- CloudWatch enables you to monitor your complete stack (applications, infrastructure, and services) and use alarms, logs, and events data to take automated actions and reduce mean time to resolution (MTTR).
- This frees up important resources and allows you to focus on building applications and business value.


## What is SNS ?
- Amazon Simple Notification Service (Amazon SNS) is a fully managed messaging service for
   both application-to-application (A2A) and application-to-person (A2P) communication

## What is SQS ?
- SQS is a message queue service used by distributed applications to exchange messages through a polling model, 
  and can be used to decouple sending and receiving components.



## What are 4 golder rules that should be monitored ?
- To consistently keep track of end-user experiences, Google's team of software reliability engineers (SREs) created
   a standard set of four metrics known as the Golden Signals: latency, traffic, errors and saturation.
   
   
   
   ![image](https://user-images.githubusercontent.com/110182832/186391997-033f24a4-6792-425b-aa55-bd0d4e81c630.png)
   
   



### It is also very important to set the thresold , when to send notification.

### Important link for monitoring: https://aws.amazon.com/blogs/mt/alarms-incident-management-and-remediation-in-the-cloud-with-amazon-cloudwatch/
   
   
   
   ## Monitoring and Alert management:
   
   
   
   
 
   ![cloudwatcjjj](https://user-images.githubusercontent.com/110182832/186460534-03642422-dd0b-416b-9669-c8ef3fce4df8.png)

 

      
   
   
   ## Resources that can be monitored by cloudwatch:
   - S3
   - EC2
   - Load balancer
   
   
   
   ### Steps to set-up an alarm for EC2:
 
 - Select your Instance and go into monitoring
 - Here we need to setup alarm if CPU utilization of EC2 instance goes more than 20%, then you should 
   receive an email.
 - so under monitoring, select first graph which is for CPU utilization and then select view in metrics.
 
<img width="776" alt="alarm first" src="https://user-images.githubusercontent.com/110182832/186429234-4959ba2b-c25c-46ef-95f5-e5d750143887.png">








- On the next page, set the threshold limit for CPU utilization, so if CPU utilization will go above from the thresold then you'll receive an email.


<img width="844" alt="alarmsecond" src="https://user-images.githubusercontent.com/110182832/186429318-5ed0379f-bce2-4112-8907-a698ccbcee44.png">





<img width="632" alt="alarm1" src="https://user-images.githubusercontent.com/110182832/186429398-5a3dfe81-8500-4d9d-b09d-6eacab96cafd.png">


- Next create a new SNS topic and add your email id.

![sns](https://user-images.githubusercontent.com/110182832/186476807-d6cb4859-f0fe-4ab8-aa9d-bcd027a5a7ac.png)


- Now, create an alarm and confirm your email id from your email.



<img width="449" alt="alarm-2" src="https://user-images.githubusercontent.com/110182832/186429444-c5d88ddb-5023-454a-8452-363ded616540.png">






## AWS Auto scaling and load balancer:

![autoscaling and load balancer](https://user-images.githubusercontent.com/110182832/186459704-973d6d3a-50d6-434f-bbf0-caca54c62e48.png)






## - First of all, make your APP EC2 completely working and then create an image (AMI) of that EC2 instance.
## - So, if you launch an instance from AMI and copy & paste public id of launched instance to the browser, you'll be able to see the app.

## To make App EC2 works completely:
- Install all the dependencies in the app (You can do it while creating the instance - write scipt in userdata or do it manually after creating the instance)
- After downloading all the dependencies, we need to automate 'npm start' and for this
- In your app instance go to /etc/systemd/system
- 'cd /etc/systemd/system'
- 'sudo nano npm.service'
- add the following in to that file: (Creating service script to automate npm start)

```
[Unit]
Description=running npm app

[Service]
User=ubuntu
WorkingDirectory=/home/ubuntu/eng_virtualisation/app  ## (give path of app file from where you run npm start, where the app.js file is)
ExecStart=/usr/bin/npm start
Restart=always

[Install]
WantedBy=multi-user.target
```


## Steps to create Load balancer and Auto balancing group:




![load balacer](https://user-images.githubusercontent.com/110182832/186765928-91ebc8f0-6444-4d3f-802c-6f5a87e748b2.png)








![1](https://user-images.githubusercontent.com/110182832/186753946-0e40ac22-b656-4345-8421-9018076c011d.png)








![2](https://user-images.githubusercontent.com/110182832/186753970-c4a5a80d-b082-482c-b756-8dfc6f72c0e9.png)






![3](https://user-images.githubusercontent.com/110182832/186753993-e637a2e6-27a0-4f0f-8179-ef23a6d48ea7.png)





![4](https://user-images.githubusercontent.com/110182832/186754015-e2b7a563-5a28-4cff-975f-3c2ee3c2fd2b.png)



![5](https://user-images.githubusercontent.com/110182832/186754036-f0d5ff82-65bd-4257-8e98-28e4d28af8cb.png)




![6-a](https://user-images.githubusercontent.com/110182832/186754071-725b4659-1db7-495a-9c95-277fea03acd2.png)




![6-b](https://user-images.githubusercontent.com/110182832/186754084-f364b6e2-b9e2-4d69-98fe-04cc3107ee2c.png)




![7](https://user-images.githubusercontent.com/110182832/186754096-30698de2-ba4e-4bcf-94e7-efd3108fdcc4.png)




![8](https://user-images.githubusercontent.com/110182832/186754126-9a8ce777-db08-464d-92af-c134160b6eae.png)
