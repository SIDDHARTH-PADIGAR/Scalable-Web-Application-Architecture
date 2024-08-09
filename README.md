## Architecture Overview

This architecture is designed to deliver a highly available and scalable web application. It leverages several AWS services to ensure efficient operation and management of application resources.

- **AWS Route 53**: Handles DNS management for the domain, routing incoming traffic to the Elastic Load Balancer (ELB). This ensures users are directed to the correct entry point of the application.

- **Elastic Load Balancer (ELB)**: Distributes incoming traffic across the two EC2 instances to balance the load effectively. By doing so, it enhances the application's availability and fault tolerance, preventing any single instance from becoming a bottleneck.

- **Two EC2 Instances**: Provide the necessary compute resources for running the web application. These instances are set up behind the ELB to facilitate load balancing, allowing them to handle varying levels of traffic and maintain performance.

- **AWS S3**: Offers scalable and durable storage for application data, including files, media, and backups. S3's integration with the EC2 instances ensures that application data is readily accessible and can be managed efficiently.

- **AWS RDS**: Manages the relational database used by the application. RDS provides a robust and scalable database solution, handling data storage, backup, and recovery, which simplifies database management and enhances data reliability.

### Key Benefits

- **Scalability**: The architecture is designed to scale with the application’s needs, thanks to the load balancing capabilities of ELB and the scalable nature of AWS S3 and RDS.
- **High Availability**: By distributing traffic and using managed services, the setup ensures high availability and reliability for the web application.
- **Cost Efficiency**: Leveraging AWS services reduces the need for on-premises infrastructure and associated maintenance costs, providing a cost-effective solution for managing application resources.

### Diagram

For a visual representation of this architecture, refer to the diagram below:


![chatuml-diagram (4)](https://github.com/user-attachments/assets/c040cb2c-b86a-442c-a1c7-1a9131fc7b25)




### How It Works

1. **User Request**: A user makes a request to the application’s domain.
2. **DNS Resolution**: AWS Route 53 resolves the domain to the ELB.
3. **Traffic Distribution**: The ELB distributes the request to one of the two EC2 instances.
4. **Compute**: The EC2 instance processes the request and may interact with AWS S3 for file storage or AWS RDS for database queries.
5. **Response**: The processed request is sent back to the user through the ELB.

This architecture ensures that the application remains responsive, reliable, and capable of handling growth as user demand increases.

**Note:** This project is a showcase for learning Terraform and demonstrating the implementation of AWS services using Infrastructure as Code (IaC). The setup serves as an educational example and may be used to explore and practice Terraform skills.

