# AWS Cloud & DevOps – Practical Training Roadmap

## Objective

To help students understand how real companies design, deploy, secure, automate and monitor cloud-based applications using AWS and DevOps tools.

The practicals are arranged in a sequence where each task builds on the knowledge gained from the previous task.

---

# PHASE 1: AWS NETWORKING & INFRASTRUCTURE

**Objective:** Understand how servers communicate with each other and how companies build secure networks in AWS.

## Module 1.1 – Networking Fundamentals

| Order | Task | Explanation in simple English |
|---|---|---|
| 1 | CIDR and IP Address Calculation | Understand how IP addresses are divided into smaller networks. |
| 2 | Subnet Mask Calculation | Calculate how many IP addresses are available in /24, /25, /26 and other subnet ranges. |
| 3 | VPC CIDR Planning | Decide the IP address range for an AWS private network. |
| 4 | VPC CIDR and Subnet Compatibility | Understand why a subnet must belong to the VPC's IP address range. |
| 5 | Subnet Overlapping Scenarios | Identify why two subnets cannot use overlapping IP ranges in the same VPC. |
| 6 | Public and Private Subnets | Understand the difference between servers that can receive direct internet traffic and servers that cannot. |

## Module 1.2 – VPC Creation and Connectivity

| Order | Task | Explanation in simple English |
|---|---|---|
| 7 | Create a Custom VPC | Build your own isolated network in AWS. |
| 8 | Create Public and Private Subnets | Divide the network into different sections for different purposes. |
| 9 | Create an Internet Gateway | Connect public subnets to the internet. |
| 10 | Configure Route Tables | Decide where network traffic should go. |
| 11 | Launch EC2 in a Public Subnet | Create a server that can be reached through the internet, subject to security rules. |
| 12 | Configure Security Groups | Control which traffic is allowed to reach your servers. |
| 13 | Create and Use EC2 Key Pairs | Learn how to securely connect to Linux servers. |
| 14 | Create a Bastion Host | Use one controlled public server to connect to private servers. |
| 15 | Connect to Private EC2 through Bastion | Access a private server without exposing it directly to the internet. |
| 16 | Create a NAT Gateway | Allow private servers to download updates without accepting direct internet connections. |
| 17 | Verify Inbound and Outbound Traffic | Test what traffic can enter and leave public and private servers. |
| 18 | Configure Separate Security Groups | Create different access rules for Bastion, Web and Application servers. |

## Module 1.3 – Advanced Networking

| Order | Task | Explanation in simple English |
|---|---|---|
| 19 | Multi-AZ Network Architecture | Create networks in two Availability Zones to reduce the impact of one zone failing. |
| 20 | Private EC2 without Public IP | Run a server without assigning a public IP address. |
| 21 | Private EC2 Software Installation through NAT | Download software updates from a private server using NAT. |
| 22 | Security Group-to-Security Group Communication | Allow an application server to communicate only with the web server. |
| 23 | Network ACL Configuration | Control traffic entering and leaving a subnet using network-level rules. |
| 24 | Elastic Network Interface (ENI) | Attach an additional network interface and private IP to an EC2 instance. |
| 25 | Elastic IP Address | Keep the same public IP address when replacing an EC2 server. |
| 26 | EC2 Pricing Comparison | Understand On-Demand, Reserved Instances, Savings Plans and Spot Instances. |
| 27 | Application Load Balancer (ALB) | Distribute incoming application requests across multiple servers. |
| 28 | Target Group and Health Checks | Check whether application servers are healthy before sending traffic to them. |
| 29 | ALB Multi-AZ Architecture | Distribute application traffic across servers in different Availability Zones. |
| 30 | Draw AWS Network Architecture | Represent the complete network using Draw.io. |

## Module 1.4 – Private Connectivity and VPC Integration

| Order | Task | Explanation in simple English |
|---|---|---|
| 31 | VPC Gateway Endpoint for S3 | Allow private servers to access S3 without using a NAT Gateway for that traffic. |
| 32 | VPC Interface Endpoints | Connect privately to supported AWS services without requiring public internet access. |
| 33 | VPC Peering | Connect two VPC networks privately. |
| 34 | Cross-Region VPC Peering | Connect VPCs located in different AWS regions. |
| 35 | Systems Manager Session Manager | Connect to EC2 without opening SSH port 22 to the internet. |
| 36 | SSM with NAT Gateway | Access private EC2 using Systems Manager through NAT connectivity. |
| 37 | SSM with Interface Endpoints | Access private EC2 through Systems Manager without depending on NAT for the SSM connection. |

---

# PHASE 2: AMAZON S3 STORAGE MANAGEMENT

**Objective:** Learn how companies store files, application backups, images, documents and logs in AWS.

## Module 2.1 – S3 Fundamentals

| Order | Task | Explanation in simple English |
|---|---|---|
| 38 | Create an S3 Bucket | Create cloud storage to keep files and documents. |
| 39 | Upload and Download Objects | Store files in S3 and retrieve them whenever required. |
| 40 | S3 Bucket Permissions | Control who can access the files inside a bucket. |
| 41 | IAM User Access to S3 | Give a user permission to access S3. |
| 42 | S3 Bucket Policy | Define access rules directly at the bucket level. |
| 43 | Prefix-Based Access | Allow different teams to access only their own folders. |
| 44 | S3 Versioning | Keep older versions of files so deleted or overwritten files can be recovered. |
| 45 | S3 Storage Classes | Understand different storage options based on how frequently files are accessed. |
| 46 | S3 AWS CLI Operations | Manage buckets and files using terminal commands. |

## Module 2.2 – Advanced S3

| Order | Task | Explanation in simple English |
|---|---|---|
| 47 | S3 Lifecycle Management | Automatically move old files to cheaper storage or delete them. |
| 48 | S3 Access from EC2 using IAM Role | Allow an EC2 server to access S3 without storing AWS access keys inside the server. |
| 49 | S3 Presigned URLs | Share private files using temporary access links. |
| 50 | S3 Cross-Region Replication | Automatically copy files to another AWS region for additional protection. |
| 51 | S3 Explicit Deny | Block access even when another policy allows it, subject to AWS policy evaluation. |
| 52 | S3 Public Access Block | Prevent accidental public access to storage. |
| 53 | S3 Static Website Hosting | Host a basic website using HTML, CSS and JavaScript files in S3. |
| 54 | S3 Log Archiving | Store old application and server logs in cost-effective storage. |
| 55 | Complete S3 Security and Storage Project | Combine IAM, bucket policies, versioning, lifecycle and CLI operations. |

---

# PHASE 3: IAM & AWS SECURITY

**Objective:** Understand how companies manage employee permissions and secure AWS resources.

## Module 3.1 – IAM Fundamentals

| Order | Task | Explanation in simple English |
|---|---|---|
| 56 | Create IAM Users and Groups | Create different user accounts for employees and teams. |
| 57 | IAM Policies | Define what users can and cannot do in AWS. |
| 58 | IAM Inline Policies | Attach a policy directly to one user or role. |
| 59 | Customer-Managed Policies | Create reusable permission policies for multiple users or roles. |
| 60 | S3 Read-Only Access | Allow developers to view S3 files without modifying them. |
| 61 | EC2 Start and Stop Permissions | Allow developers to start and stop servers without giving complete EC2 access. |
| 62 | Developer and Operations Permissions | Give different teams different levels of access. |

## Module 3.2 – Advanced IAM and Security

| Order | Task | Explanation in simple English |
|---|---|---|
| 63 | IAM Roles | Allow AWS services to securely access other AWS services. |
| 64 | EC2 to S3 IAM Role | Give an EC2 instance access to a specific S3 bucket. |
| 65 | Least Privilege Access | Give users only the permissions they actually need. |
| 66 | Explicit Deny and Allow | Understand how AWS decides whether an action is permitted or blocked. |
| 67 | IAM Policy Evaluation | Test multiple policies containing Allow and Deny permissions. |
| 68 | IAM Switch Role | Allow users to switch into another AWS account or role with approved permissions. |
| 69 | Cross-Account IAM Access | Allow one AWS account to securely access resources in another account. |
| 70 | AWS CloudTrail | Track who performed an action in AWS and when it happened. |
| 71 | AWS Config | Check whether AWS resources follow the required configuration rules. |
| 72 | AWS KMS Encryption | Protect stored data using encryption keys. |
| 73 | AWS Secrets Manager | Store application passwords and database credentials securely. |
| 74 | AWS Systems Manager Parameter Store | Store application configuration values and sensitive parameters. |
| 75 | Amazon Inspector | Identify security vulnerabilities in supported AWS workloads. |
| 76 | SNS and EventBridge Alerts | Send notifications when selected AWS events occur. |

---

# PHASE 4: DATABASE MANAGEMENT – RDS & REDIS

**Objective:** Learn how applications store, retrieve and manage data.

## Module 4.1 – Database Fundamentals

| Order | Task | Explanation in simple English |
|---|---|---|
| 77 | Install MySQL or MariaDB on EC2 | Install a database server on a Linux machine. |
| 78 | Create an AWS RDS Database | Create a managed database without manually managing the database server operating system. |
| 79 | RDS Subnet Group | Decide which private subnets AWS can use for the database. |
| 80 | RDS Security Group | Control which application servers can connect to the database. |
| 81 | Connect EC2 to RDS | Allow an application server to communicate with a database. |
| 82 | MySQL Workbench Connectivity | Connect to the database using a graphical interface. |
| 83 | Database and Table Operations | Create databases, tables and perform SQL operations. |
| 84 | Database CLI Connectivity | Manage databases using terminal commands. |

## Module 4.2 – Advanced Database Management

| Order | Task | Explanation in simple English |
|---|---|---|
| 85 | RDS Automated Backups | Automatically maintain database backups. |
| 86 | RDS Snapshots | Create a point-in-time copy of a database for recovery. |
| 87 | Restore RDS from Snapshot | Recover a database using a previously saved snapshot. |
| 88 | RDS Read Replica | Create another database copy to handle read requests. |
| 89 | RDS Storage Scaling | Increase database storage when data grows. |
| 90 | RDS Multi-AZ Deployment | Maintain a standby database in another Availability Zone for availability. |
| 91 | Secrets Manager with RDS | Securely retrieve database credentials from an application. |
| 92 | Secrets Rotation | Automatically rotate database credentials and update applications appropriately. |
| 93 | Parameter Store with RDS | Store and retrieve database configuration securely. |
| 94 | Redis / ElastiCache Integration | Store frequently requested information in memory to reduce database load. |
| 95 | Database Recovery and Failover Testing | Test how applications behave during database recovery or failover. |

---

# PHASE 5: DNS, ROUTE 53 & MULTI-REGION ARCHITECTURE

**Objective:** Understand how users access applications using domain names and how companies manage traffic across regions.

| Order | Task | Explanation in simple English |
|---|---|---|
| 96 | Route 53 Hosted Zone | Manage DNS records for a domain. |
| 97 | Route 53 with ALB | Connect a custom domain name to an application load balancer. |
| 98 | Subdomain Routing | Configure domains such as app.example.com and api.example.com. |
| 99 | Private Hosted Zone | Allow internal servers to resolve private domain names. |
| 100 | Route 53 Health Checks | Check whether an application endpoint is healthy. |
| 101 | Failover Routing | Send users to a backup application when the primary application fails. |
| 102 | Weighted Routing | Divide traffic between two application environments. |
| 103 | Latency-Based Routing | Send users to a region expected to provide lower network latency. |
| 104 | Geolocation Routing | Route users based on their geographic location. |
| 105 | Multi-Region Architecture | Deploy applications in multiple AWS regions for improved availability and disaster recovery. |

---

# PHASE 6: APPLICATION DEPLOYMENT & AUTOMATION

**Objective:** Learn how developers deploy applications and how DevOps engineers automate infrastructure and application operations.

## Module 6.1 – Application Deployment

| Order | Task | Explanation in simple English |
|---|---|---|
| 106 | Install Python Application on EC2 | Deploy and run a Python application on a cloud server. |
| 107 | Install Node.js Application on EC2 | Run a Node.js application on a cloud server. |
| 108 | Nginx Web Server | Use Nginx to receive and forward web requests. |
| 109 | PM2 Process Management | Keep Node.js applications running in the background and restart them when required. |
| 110 | Linux Systemd Service | Configure applications to start automatically when the server starts. |
| 111 | Private EC2 Application Deployment | Deploy applications on private servers without exposing them directly to the internet. |
| 112 | SSM and S3-Based Deployment | Deploy application files to private servers using secure AWS services. |

## Module 6.2 – AWS Automation

| Order | Task | Explanation in simple English |
|---|---|---|
| 113 | Python Boto3 Fundamentals | Use Python to communicate with AWS services. |
| 114 | Boto3 EC2 Automation | Create, start, stop and manage EC2 instances using Python. |
| 115 | Boto3 S3 Automation | Create buckets and upload or download files using Python. |
| 116 | Boto3 VPC Automation | Create networking resources programmatically. |
| 117 | Boto3 RDS Automation | Automate database resource operations using Python. |
| 118 | AWS Lambda Fundamentals | Run code without managing a dedicated server. |
| 119 | Lambda to Create EC2 | Automatically create EC2 instances using a Lambda function. |
| 120 | Lambda with VPC and RDS | Allow Lambda functions to communicate with private database resources. |
| 121 | Lambda with Secrets Manager | Retrieve database credentials securely from Lambda. |
| 122 | Lambda with Layers | Reuse external Python libraries across Lambda functions. |
| 123 | API Gateway with Lambda and DynamoDB | Build an API that accepts requests, executes Lambda code and stores information in DynamoDB. |

---

# PHASE 7: FULL-STACK APPLICATION & HTTPS

**Objective:** Understand how frontend, backend and databases work together in a real company application.

| Order | Task | Explanation in simple English |
|---|---|---|
| 124 | Create a Basic Python GET API | Build an API that returns information when a user sends a request. |
| 125 | Flask Application Deployment | Deploy a Python web application on EC2. |
| 126 | Flask with RDS | Connect a backend application to a database. |
| 127 | Frontend and Backend Integration | Connect the website users see with the backend that processes their requests. |
| 128 | Nginx Reverse Proxy | Forward user requests from Nginx to the backend application. |
| 129 | Full-Stack Deployment with ALB | Place a load balancer in front of the application. |
| 130 | Read Replica Integration | Send database read operations to a read replica. |
| 131 | Redis Cache Integration | Cache frequently accessed information to improve application performance. |
| 132 | Secrets Manager Integration | Retrieve application database credentials securely. |
| 133 | AWS Certificate Manager (ACM) | Request and manage SSL/TLS certificates. |
| 134 | HTTPS Configuration on ALB | Enable secure HTTPS communication between browsers and the load balancer. |
| 135 | HTTP to HTTPS Redirect | Automatically redirect users from HTTP to HTTPS. |
| 136 | HTTPS with Nginx Reverse Proxy | Configure secure application routing through Nginx and ALB. |

---

# PHASE 8: MONITORING & OBSERVABILITY

**Objective:** Understand how companies identify application failures, server problems, high CPU usage, memory issues, network problems and performance bottlenecks.

**Simple real-time example:** Imagine a company website suddenly becomes slow. Customers complain that the website is not opening. The DevOps team needs to identify whether the problem is with the server, application, database or network. Monitoring tools help the team identify the problem before it affects more customers.

## Module 8.1 – AWS Native Monitoring

| Order | Task | Explanation in simple English |
|---|---|---|
| 137 | AWS CloudWatch Fundamentals | Monitor AWS resources and check their performance. |
| 138 | EC2 CPU and Network Monitoring | Identify whether a server is using too much CPU or network capacity. |
| 139 | CloudWatch Memory Monitoring | Monitor server memory usage using the CloudWatch Agent. |
| 140 | CloudWatch Logs | Collect application and system logs in one place. |
| 141 | CloudWatch Alarms | Get an alert when CPU, memory or another metric crosses a defined limit. |
| 142 | SNS Email Notifications | Receive an email when an important monitoring alert occurs. |
| 143 | CloudWatch Dashboard | Display important server and application metrics in one dashboard. |
| 144 | CloudWatch Log Groups and Retention | Organize logs and decide how long they should be stored. |
| 145 | CloudWatch Logs to S3 | Archive application logs in S3 for long-term storage. |
| 146 | Athena Log Analysis | Search and analyze archived logs using SQL queries. |
| 147 | AWS CloudTrail Monitoring | Investigate AWS API activity and identify who made a resource change. |

## Module 8.2 – Prometheus and Grafana

| Order | Task | Explanation in simple English |
|---|---|---|
| 148 | Prometheus Installation | Install a monitoring system that collects application and server metrics. |
| 149 | Node Exporter Installation | Collect Linux server information such as CPU, memory, disk and network usage. |
| 150 | Prometheus Target Configuration | Tell Prometheus which servers it needs to monitor. |
| 151 | Prometheus Queries (PromQL) | Write queries to check CPU, memory and other performance information. |
| 152 | Grafana Installation | Install a dashboard tool to display monitoring information visually. |
| 153 | Prometheus and Grafana Integration | Connect Grafana to Prometheus to display collected metrics. |
| 154 | Create EC2 Monitoring Dashboard | Display CPU, memory, disk and network usage in Grafana. |
| 155 | Grafana Alerting | Send alerts when a server metric crosses a defined threshold. |
| 156 | Monitor Multiple EC2 Instances | Monitor multiple Linux servers from one central dashboard. |
| 157 | Application Monitoring with Prometheus | Collect application-level metrics such as request counts and response times. |
| 158 | Monitor Nginx Using Prometheus | Monitor web server activity and performance. |
| 159 | Grafana with CloudWatch | Display AWS CloudWatch metrics inside Grafana. |

## Module 8.3 – Advanced Monitoring Tools

| Order | Task | Explanation in simple English |
|---|---|---|
| 160 | Grafana Loki | Collect and search application logs using Grafana tools. |
| 161 | Promtail or Grafana Alloy | Collect server logs and send them to Loki. |
| 162 | ELK Stack / Elastic Stack | Collect, search and visualize logs from different servers and applications. |
| 163 | OpenSearch and OpenSearch Dashboards | Analyze and visualize application logs and operational information. |
| 164 | Dynatrace Installation and Configuration | Use an enterprise monitoring platform to observe applications and infrastructure. |
| 165 | Dynatrace OneAgent | Install an agent that collects information about servers and applications. |
| 166 | Dynatrace Application Performance Monitoring | Identify slow application requests and performance problems. |
| 167 | Distributed Tracing | Follow a single request as it moves between frontend, backend and database services. |
| 168 | AWS X-Ray | Trace application requests and identify delays between application components. |
| 169 | OpenTelemetry Fundamentals | Learn a common standard for collecting metrics, logs and traces. |
| 170 | OpenTelemetry Collector | Collect and forward telemetry information to supported monitoring platforms. |
| 171 | Incident Detection and Troubleshooting | Investigate a simulated production issue using monitoring dashboards and logs. |
| 172 | Monitoring and Alerting Integration Project | Monitor an application using metrics, logs, alerts and dashboards. |

## Module 8.4 – Production Monitoring Scenarios

| Order | Task | Explanation in simple English |
|---|---|---|
| 173 | High CPU Usage Scenario | Simulate high CPU usage and identify which process is consuming resources. |
| 174 | High Memory Usage Scenario | Identify applications consuming excessive memory. |
| 175 | Disk Space Monitoring | Alert the team when a server's disk is almost full. |
| 176 | Application Downtime Alert | Detect when an application becomes unavailable. |
| 177 | ALB Target Health Monitoring | Identify unhealthy application servers behind a load balancer. |
| 178 | Database Performance Monitoring | Identify slow database queries and high database load. |
| 179 | End-to-End Application Monitoring | Monitor frontend, backend, database and infrastructure together. |
| 180 | Production Incident Report | Document the issue, root cause, impact and resolution. |

---

# PHASE 9: CLOUDFRONT & WEB APPLICATION FIREWALL

**Objective:** Understand how companies improve website performance and protect applications from unwanted traffic.

| Order | Task | Explanation in simple English |
|---|---|---|
| 181 | CloudFront Fundamentals | Deliver website content to users through geographically distributed edge locations. |
| 182 | CloudFront with S3 | Distribute static website files using CloudFront. |
| 183 | CloudFront with ALB | Deliver dynamic application traffic through CloudFront and an ALB. |
| 184 | CloudFront with Private EC2 | Build an architecture where application servers are not directly exposed to the internet. |
| 185 | CloudFront Cache Behavior | Understand which content should be cached and for how long. |
| 186 | CloudFront Cache Invalidation | Remove outdated cached content when website files are updated. |
| 187 | Lambda-Based Cache Invalidation | Automatically invalidate CloudFront cache through Lambda. |
| 188 | AWS WAF Fundamentals | Protect applications by filtering unwanted web requests. |
| 189 | WAF IP Blocking | Block requests from selected IP addresses. |
| 190 | WAF Rate Limiting | Restrict excessive requests from clients. |
| 191 | WAF Geographic Restrictions | Control access based on geographic locations. |
| 192 | WAF and ALB Integration | Protect an application load balancer using WAF rules. |

---

# PHASE 10: INFRASTRUCTURE AS CODE & CI/CD – ADDITIONAL DEVOPS MODULE

**Objective:** Stop creating infrastructure manually and learn how companies automate infrastructure and application deployments.

| Order | Task | Explanation in simple English |
|---|---|---|
| 193 | Git Fundamentals | Track code changes and collaborate with team members. |
| 194 | GitHub Repository Management | Store application and infrastructure code in GitHub. |
| 195 | Terraform Fundamentals | Create AWS resources using configuration files instead of manual clicks. |
| 196 | Terraform Providers and Resources | Understand how Terraform communicates with AWS and creates resources. |
| 197 | Terraform Variables and Outputs | Reuse configurations and display important resource information. |
| 198 | Terraform State Management | Maintain information about resources created by Terraform. |
| 199 | Terraform Modules | Reuse infrastructure code across multiple environments. |
| 200 | Terraform Remote Backend | Store Terraform state centrally in S3 with appropriate state-locking configuration. |
| 201 | Terraform VPC and EC2 Project | Create complete AWS networking and servers using Terraform. |
| 202 | Terraform RDS and ALB Project | Automate database and load balancer infrastructure. |
| 203 | Jenkins Installation and Configuration | Set up a tool that automates software build and deployment activities. |
| 204 | Jenkins Freestyle Job | Automate a simple task using a Jenkins job. |
| 205 | Jenkins Pipeline | Define the complete build and deployment process as code. |
| 206 | GitHub Webhook Integration | Automatically trigger Jenkins when developers push new code. |
| 207 | CI Pipeline | Automatically build and test application code after a code change. |
| 208 | CD Pipeline | Automatically deploy tested application code to an environment. |
| 209 | Jenkins with Docker | Build and manage Docker images through Jenkins pipelines. |
| 210 | GitHub Actions Fundamentals | Automate build, test and deployment workflows directly from GitHub. |
| 211 | Terraform Plan and Apply through GitHub Actions | Automatically validate and deploy infrastructure changes. |
| 212 | Environment-Based Deployment | Maintain separate development, testing and production environments. |
| 213 | Manual Approval for Production Deployment | Require approval before deploying changes to production. |
| 214 | CI/CD Rollback | Restore an earlier application version when a new deployment fails. |

---

# PHASE 11: CONTAINERIZATION & KUBERNETES – ADDITIONAL DEVOPS MODULE

**Objective:** Understand how companies package applications and manage them at scale.

| Order | Task | Explanation in simple English |
|---|---|---|
| 215 | Docker Fundamentals | Package an application and its dependencies into a container. |
| 216 | Dockerfile Creation | Define the steps required to build an application image. |
| 217 | Docker Image and Container Management | Build, run and manage application containers. |
| 218 | Docker Volumes | Keep application data even when containers are replaced. |
| 219 | Docker Networking | Allow containers to communicate with each other. |
| 220 | Docker Compose | Run multiple connected containers using one configuration file. |
| 221 | Push Images to Amazon ECR | Store Docker images in AWS container registry. |
| 222 | Deploy Containers on EC2 | Run Docker-based applications on cloud servers. |
| 223 | Kubernetes Fundamentals | Understand how Kubernetes manages containerized applications. |
| 224 | Kubernetes Pods and Deployments | Run application containers and maintain the required number of replicas. |
| 225 | Kubernetes Services | Allow users and other applications to communicate with pods. |
| 226 | Kubernetes ConfigMaps and Secrets | Manage application configuration and sensitive information. |
| 227 | Kubernetes Ingress | Route external HTTP and HTTPS requests to applications inside the cluster. |
| 228 | Kubernetes TLS and HTTPS | Secure application communication using TLS certificates. |
| 229 | Helm Fundamentals | Deploy Kubernetes applications using reusable Helm charts. |
| 230 | Kubernetes Monitoring with Prometheus and Grafana | Monitor cluster nodes, pods and application performance. |
| 231 | Kubernetes Logging | Collect and investigate logs generated by containers. |
| 232 | Kubernetes Autoscaling | Automatically increase or decrease application replicas based on workload. |
| 233 | Kubernetes Deployment Rollback | Restore an earlier working application version. |
| 234 | End-to-End Kubernetes CI/CD | Build, push and deploy container images through an automated pipeline. |

---

# PHASE 12: FINAL CAPSTONE PROJECT

**Objective:** Combine all the major concepts and build an application architecture similar to a real production environment.

## Project: Highly Available, Secure and Monitored Full-Stack Application on AWS

### Architecture requirements

1. Create a custom VPC.
2. Create public and private subnets across two Availability Zones.
3. Configure Internet Gateway and NAT Gateway.
4. Deploy an Application Load Balancer.
5. Deploy multiple application servers in private subnets.
6. Deploy a frontend and backend application.
7. Connect the backend to Amazon RDS.
8. Integrate Redis for application caching.
9. Store application files in S3.
10. Configure IAM roles and least-privilege access.
11. Store credentials in Secrets Manager.
12. Configure Route 53 and a custom domain.
13. Enable HTTPS using AWS Certificate Manager.
14. Configure CloudFront and AWS WAF.
15. Automate infrastructure using Terraform.
16. Build a CI/CD pipeline using Jenkins or GitHub Actions.
17. Deploy application containers using Docker.
18. Integrate Kubernetes as an additional deployment option.
19. Monitor EC2 and AWS resources using CloudWatch.
20. Monitor infrastructure and applications using Prometheus and Grafana.
21. Integrate centralized logging using Loki or OpenSearch.
22. Configure alerting and notifications.
23. Perform application failure and recovery testing.
24. Prepare the final architecture diagram and project documentation.

### Final demonstration scenarios

- What happens when one EC2 instance goes down?
- What happens when the application server CPU reaches 90%?
- What happens when the database becomes unavailable?
- How does the application continue running when one Availability Zone has a problem?
- How does a developer deploy a new application version?
- How does the team identify an application performance issue?
- How does the team receive alerts when the application goes down?
- How can the team roll back an unsuccessful deployment?
- How does the company protect application credentials?
- How does the application communicate securely using HTTPS?

---

# Recommended Learning Order – Summary

| Phase | Main Area | Expected Outcome |
|---|---|---|
| 1 | AWS Networking | Build secure AWS networks |
| 2 | S3 Storage | Store and manage cloud data |
| 3 | IAM and Security | Control access and protect resources |
| 4 | RDS and Redis | Manage application databases |
| 5 | Route 53 | Manage domains and traffic routing |
| 6 | Application Deployment and Automation | Deploy and automate applications |
| 7 | Full Stack and HTTPS | Build secure web applications |
| 8 | Monitoring and Observability | Identify failures and troubleshoot production issues |
| 9 | CloudFront and WAF | Improve performance and application security |
| 10 | Terraform and CI/CD | Automate infrastructure and deployments |
| 11 | Docker and Kubernetes | Manage containerized applications |
| 12 | Capstone Project | Integrate everything into a production-style project |

## Important training guidelines

1. Every task should include theory, architecture explanation, hands-on execution and troubleshooting.
2. Students should understand why a particular AWS service is required, not just how to create it.
3. Each major module should end with a small integration project.
4. Students should draw the architecture before starting complex implementation tasks.
5. Monitoring should be introduced early through CloudWatch and expanded later through Prometheus, Grafana, Dynatrace and centralized logging.
6. Every project should include a failure-testing scenario.
7. Cost awareness and resource cleanup should be part of every AWS lab.
8. Use development environments for experiments and never leave expensive resources running unnecessarily.

**Final expected outcome:** Students should be able to design, deploy, automate, secure, monitor and troubleshoot a cloud-based application using AWS and modern DevOps tools.
