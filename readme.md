## Traditional IT Overview  

Compute: CPU, RAM  
Storage: Data  
Database: Structured data  
Network: Routers, switches, DNS  

__Terminology__  
Router sends and receives data packets between networks  
Switch sends data packets to server or client on network  

__Problems with the traditional approach__  
rent  
power/cooling and maintenance  
adding replacing hardware takes time  
scaling is limited  
Hire team for monitoring  
How do you deal with DR  

__What is cloud computing?__  
...is the on-demand delivery of compute, power, database storage, applications and other IT resources.  

Benefits:  
through a cloud service, you get pay-as-you-go pricing.
you can provision exactly what you want, right type and size of computing resources.  
access to resources almost instantly.  
simple way to access servers, storage, databases and a set of application services.  

AWS owns and maintains backend for these services, so you provision what you want, when you want and there is no need to concern for any back-end infra.  


### Cloud Models  
Private: 
  - single org, not exposed to the public  
  - complete control  
  - security for sensitive applications   
  - meet a specific business need  
Public:  
  - Azure, AWS, GCP (owned and operated by cloud service provider)  
  - 6 advantages (See below)  
Hybrid:  
  - keep some servers on prem and extend some capabilities to the cloud  
  - control over sensitive assets in your private cloud infra  
  - flexibility and cost effectiveness of public cloud  

### 5 characteristics of cloud computing  
On-demand self service:  
  - Users can provision resources without intervention from the service provider.  
Broad network access:  
  - resources availabe over the network and can be accessed by diverse client platforms.  
Multi-tenancy and Resource Pooling:  
  - Multiple customers can share the same infrastructure and applications with security and privacy in place.  
  - Multiple customers are serviced from the same physical resource.  
Rapid elasticity and scalability:  
  - Provision and de-provision resources when needed.  
  - Scale on demand quickly and easily.  
Measured Service:  
  - Usage is measured and users pay for exactly what they have used.  


### 6 Advantages of Cloud Computing  
- Trade CAPEX for OPEX  
  - Pay on demand, don't own hardware.  
  - reduced TCO & OPEX.  
- Benefit from massive economies of scale  
  -  Prices are reduced as AWS is more efficient in terms of cost due to their large scale.  
- Stop guessing capacity  
  - scale based on measured usage.  
- Increase of speed and agility  
- Stop spending money running and maintaining data centers  
- Go global in minutes:  
  - by leveraging the AWS global infrastructure.  

### The Problems Solved by Cloud Computing  
- **Flexibility:** Change resources when needed.  
- **Cost-Effective:** pay as you go, for exactly what you are using.  
- **Scalability:** accommodate larger loads by making hardwarechoices and adding/removing additional nodes.  
- **Elasticity:** ability to scale-in and scale-out when needed.  
- **High-Availability and Fault-Tolerance:** build across DCs.  
- **Agility:** rapdily develop, test and launch software applications.  

### Types of Cloud Computing  
IaaS  
  - Provides building blocks for cloud IT  
  - network, computing, storage  

PaaS  
  - org doesn't need to manage underlying infra  
  - focus on deployment and management of apps  

SaaS  
  - complete product that is run and managed by a service provider  

On-Prem: Manage everything. 

IaaS: Virtualisation, Serers, Storage and networking managed by others.  
  - GCP, Azure, AWS  
  - EC2    

PaaS: Manage Data and Apps  
  - AWS Elastic Beanstalk  
  - Azure App Service  

SaaS: Manage nothing  
  - AWS Rekognition for ML  
  - GMail, DropBox, Zoom  

### Pricing Models  
AWS has three pricing fundamentals:  
  - Compute:  
    - Pay for compute time  
  - Storage:  
    - Pay for data stored in the cloud  
  - Network:  
    - Data transferred **out** of the Cloud only  

**This solves the expensive issue of traditional IT**  

### AWS Cloud History  
2002: Launched internally  
2004: Public offering with SQS  
2006: Re-launched with SQS, S3 and EC2  
2007: Launched in Europe  

### AWS Facts  
AWS is a leader (47%) followed by Azure (22%) and the GCP  
Leader for 9th consecutive year  
Over 1 million active users  

### AWS Cloud Use Cases  
Enables you to build sophisticated, scalable applications  
Applicable to a diverse set of industries  
Use cases:
  - Enterprise IT, Backup and Storage, Big Data analytics  
  - Website hosting, Mobile & Social Apps  
  - Gaming  

### AWS Global Infrastructure  
- AWS Regions  
- AWS Availability Zones  
- AWS Data Centres  
- AWS Edge Locations / Points of Presence  
- Refer to https://infrastructure.aws  

### AWS Regions  
It is a cluster of DCs  
Most services are **region** scoped.  
Examples of regions:  
- us-east-1  
- ap-southeast-2  

### How do you choose an AWS Region?
- Compliance: Data governance and legal requirements (Data doesn't leave a region without your explicit permission).  
- Proximity: Where are the bulk of the customers, to try to reduce latency.  
- Available Services: Not all regions have all services and new features aren't always available in every region.  
- Pricing: This varies from region to region.

### AWS Availability Zones  
Each region has many availability zones (usually 3; min 3; max 6)  
- ap-southeast-2a, ap-southeast-2b, ap-southeast-2c  
Each AZ is one or more discreet DC with redundant power, networking and connectivity.  
They are isolated from one another in case of disaster.  
They are connected with high bandwidth, ultra-low latency networking.  


### Points of Presence (Edge Locations)  
AWS has 400+ PoP (400+ Edge Locations & 10+ Regional Caches) in 90+ cities across 40+ countries  
Content is delivered to end user with low latency  

### Services  
**Global**  
IAM  
Route 53  
Cloudfront  
WAF  
**Regional**  
EC2  
Beanstalk  
Lambda  
Rekognition  

For a list of services that are available by region, refer to the link that follows:  
https://aws.amazon.com/about-aws/global-infrastructure/regional-product-services  


### Quick summary of the default console page  
Recently visited  
Welcome to AWS  
AWS Health  
Cost and Usage  
Build a Solution  
Explore AWS  
Security Hub  
Applications  
Trusted Advisor  
Latest Announcements  
Recent AWS blog posts  

### Shared Responsibility Model  
https://aws.amazon.com/compliance/shared-responsibility-model/  

Basically, customer is responsible for the security **in** the cloud  
AWS is responsible for the security **of** the cloud  

**Customer:**  
  - Data, platform, application and identity and access management    
  - OS, network and FW config  
  - Clinet-side data encryption/integrity and authentication  
  - Server-side encryption (File system and/or data)  
  - Network Traffic protection (encryption, integrity, identity)  

**AWS:**  
  - Software  
  - compute, storage, database, networking  
  - HW/AWS Global infra  
  - Regions, AZ and Edge Locations  

### AWS Acceptable Usage Policy  
https://aws.amazon.com/aup/ 

No illegal, harmful or offensive use of content  
No security violations  
No network abuse  
No e-mail or other message abuse  

## Section 4 - IAM  

**Identity & Access Management -> Global Service**  

Root account is created by default, it shouldn't be used or shared. (Create additional accounts for AWS).   
Users are people in the org and can be grouped.  
Users do not need to belong to a group, this is not generally considered best practise.  
Users can also belong to multiple groups.  

Groups can only contain users and **NOT** other groups  

### IAM Permissions  
Users or Groups can be assigned JSON documents called policies. (effect, action, resource)  
Policies define user permissions.  
Best practise to apply **least privilege principle**.  

**You can create an account alias to replace the 12 number account ID**  

### IAM Policy Inheritance  
Group level attachment, all users in group get them.  
An **inline** policy is when a policy is attached directly to a user!  

### IAM Policy Structure  
Consists of:  
  - **Version** the language or version to be used eg `2012-10-17`.    
  - **ID** an identifier for the policy. (OPTIONAL)  
  - **statements** one or more individual statements, this is a required field.  

A `statment` consists of:  
  - **sid** the statement id (OPTIONAL)  
  - **Effect** whether the statement will be `Allow` or `Deny`  
  - **Principal** the account/user/role to which this policy will apply  
  - **Action** the actions this policy __allows__ or __denies__  
  - **Resource** the list of resources to which the actions applies to  
  - **Condition** conditions for when this policy is in effect (OPTIONAL)  

```
{
  "Version": "2012-10-17",
  "Id": "S3-Account-Permissions",
  "Statement": [
    {
      "Sid":"1",
      "Effect":"Allow",
      "Principal": {
        "AWS":["arn:aws:iam::123456789012:root"],
      },
      "Action": [
        "s3:GetObject",
        "s3:PutObject"
      ],
      "Resource":["arn:aws:s3:::mybucket/*"]
    }
  ]
}
```  

### Creating IAM Policies  
Two ways to do this:  
  - Visual Editor, which is a point and click wizard. Selecting `Service`, `Actions`, `Resources` and `Request Conditions`.     
  - Write JSON directly.  

### IAM - Password Policy  
You can set up a password policy in AWS  
The settings are in **IAM -> Access Management -> Account Settings**  

Password policy customisable configurations are:  
  - Minimum password length  
  
  - Password Strength: 
    - uppercase/lowercase  
    - numbers  
    - non-alphanumberic characters  
  - Other Requirements:  
    - Allow IAM users to change their own passwords  
    - Password expiry  
    - Password expiry requires admin reset  
    - Prevent password reuse  

### MFA Overview  
Multi-Factor Authentication  
You should protect your Root Account and IAM users  
MFA => password __you know__ and device that __you own__  
**Benefit:** If the password is stolen or hacked, the account will not be compromised without the **device** for the MFA password.  

**MFA device Options in AWS**  
Virtual MFA device  
- Google Authenticator  
- Authy  
  - Support for multiple tokens on a single device

U2F - Universal 2nd Factor Security Key  
- Yubikey by Yubico (3rd Party)  
  - Provides support for multiple root and IAM users using a single security key.  

Hardware Key Fob MFA Device  
- Provided by **Gemalto** (3rd Party)  

Hardware Key Fob MFA Device for AWS GovCloud (US)  
- Provided by **SurePassID** (3rd Party)  

