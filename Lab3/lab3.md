Cloud Migration Lab

Objective
This lab explores the process of migrating a mid-sized retail company’s infrastructure from an on-premises solution to the cloud. The migration strategies leverage PaaS, IaaS, and SaaS services from cloud providers like Azure.

1. On-Premises Solution Design

On-Premises Architecture Diagram

img

Description
Users: Connect via HTTP requests that pass through the firewall.
Load Balancer: Distributes traffic to the Web Application Servers.
SQL Database: The primary database and its replica handle the data storage for the application.
File Storage: Local storage is used for file management (e.g., uploads, downloads).
Email Service: Handles client notifications via an external email provider.
Networking: Routers and DNS are operated in-house for connectivity, and a backup server is set up for disaster recovery.
2. Migration Plan

This section details the migration strategies for each component of the on-premises infrastructure, specifying which cloud services (PaaS, IaaS, or SaaS) would be best suited for each component.

Web Application
Migration Strategy:

Option 1 (IaaS): Lift and Shift the web application to Azure VMs.
Option 2 (PaaS): Refactor the application to run on Azure App Service, leveraging cloud-native PaaS offerings.
Reasoning:

Moving to PaaS reduces the operational overhead by offloading server management, scaling, and maintenance. For applications requiring more control, IaaS might be the initial choice.
Database
Migration Strategy:

Migrate the on-premises SQL Server to Azure SQL Database (PaaS).
Reasoning:

PaaS offers automatic backups, scaling, and high availability, reducing the need to manage the underlying infrastructure.
File Storage
Migration Strategy:

Migrate file storage to Azure Blob Storage (IaaS).
Reasoning:

Blob Storage provides scalable, secure, and cost-effective storage, with easy integration into cloud-native applications.
Networking
Migration Strategy:

Replace on-premises networking components with Azure Virtual Network (VNet) and Azure DNS.
Reasoning:

Azure VNet provides flexibility and security through Network Security Groups (NSGs) and seamless integration with other Azure services, offering cloud-native networking solutions.
Email Service
Migration Strategy:

Migrate the email service to SendGrid (SaaS).
Reasoning:

Offloading the email service to SaaS ensures high deliverability and scalability without the need to manage the infrastructure. SendGrid manages the email infrastructure, allowing the company to focus on business logic.
3. Cloud Architecture Design

Cloud Migration Architecture Diagram

img

Description
VMs (IaaS): The web application is hosted on Azure VMs.
App Service (PaaS): Alternatively, the web application can be hosted on Azure App Service for easier scaling and management.
Azure SQL Database (PaaS): The SQL Database is migrated to Azure SQL Database to leverage a managed database solution.
Azure Blob Storage (IaaS): File storage is moved to Azure Blob Storage for scalable and secure storage.
SendGrid (SaaS): The email service is handled by SendGrid, providing email delivery as a service.
Azure VNet and DNS: Cloud-native networking components like Azure VNet and Azure DNS replace the on-premises networking infrastructure.