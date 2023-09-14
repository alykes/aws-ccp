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

