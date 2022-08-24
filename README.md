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
   
