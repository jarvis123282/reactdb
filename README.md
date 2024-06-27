**Project Title**:
To architect a solution that is secure, scalable, highly available, and cost-effective using AWS

**Project Description**:
A start-up company wants to host its Python and React-based application (Backend: Python
API and Frontend React) using AWS. But they are not familiar with the AWS cloud platform.
They want to ensure that the application is secure, scalable, highly available, and costefficient. As a solutions architect, you have to design a proper solution to meet their below
requirements

**Architecture Overview**

**Virtual Private Cloud (VPC)**: 
1)Create a dedicated VPC with private and public subnets.
2)Security Groups: Define security groups to control inbound and outbound traffic. Allow only necessary traffic (e.g., HTTP, HTTPS) to reach the frontend servers. Ensure database servers are in private subnets not accessible from the internet.

**Application Deployment**
1)Frontend (React) Deployment: Use AWS Elastic Beanstalk for deploying React applications.
2)Configure Elastic Beanstalk to automatically deploy updates when code changes are pushed to the master branch of your repository.

**Storage for UI Images**
1)Secure Storage: Utilize Amazon S3 (Simple Storage Service) to store UI images securely.
2)Configure S3 buckets to enable encryption at rest and manage access permissions using IAM roles.

**High Availability and Scalability**
1)Auto Scaling for EC2 Instances: Set up Auto Scaling groups to manage the number of EC2 instances based on traffic demand.
2)Minimum of 2 instances always running (desired capacity).
3)Scale out to a maximum of 4 instances during high load using scaling policies based on CPU utilization or other metrics.
4)Load Balancing: Implement an Elastic Load Balancer (ELB) to distribute traffic across multiple EC2 instances and ensure high availability.

**Disaster Recovery and Backup**
1)Backups: Configure Amazon RDS (Relational Database Service) for the database backend with automated backups enabled.
2)For the EC2 instances hosting the web application, ensure regular snapshots or AMI backups to restore instances in case of failure.

**Global Caching**
1)Content Delivery Network (CDN): Use Amazon CloudFront to cache content globally.
2)Configure CloudFront to distribute React application assets (static files) with low latency to users worldwide.

**AWS Services Used**
1)Compute: Amazon EC2 (for backend instances), AWS Elastic Beanstalk (for frontend deployment).
2)Storage: Amazon S3 (for storing UI images).
3)Database: Amazon RDS (for hosting the database).
4)Networking: Amazon VPC, Elastic Load Balancing (ELB), Amazon CloudFront (CDN).
5)Backup and Recovery: AWS RDS automated backups, EC2 instance snapshots.
6)Security: IAM (Identity and Access Management), Security Groups, Encryption (S3 encryption at rest).
