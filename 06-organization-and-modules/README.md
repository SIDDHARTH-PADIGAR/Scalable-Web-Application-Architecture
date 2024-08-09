## Architecture Overview

- **AWS Route 53**: Manages DNS for the domain, directing traffic to the Elastic Load Balancer (ELB).
- **Elastic Load Balancer (ELB)**: Distributes incoming traffic across the EC2 instances to ensure high availability and reliability.
- **Two EC2 Instances**: Provide compute resources for running the web application. These instances are configured behind the ELB for load balancing.
- **AWS S3**: Used for scalable and durable storage of application data, such as files and backups, accessible by the EC2 instances.
- **AWS RDS**: Hosts the database instance, providing a managed relational database service for storing application data.



![chatuml-diagram (3)](https://github.com/user-attachments/assets/d7c4aea9-feae-4f56-9a25-ac4011be5a80)
