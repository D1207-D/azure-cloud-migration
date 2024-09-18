# Cloud Migration Architecture

This document includes diagrams illustrating the architecture of the application in different environments.

## On-Premise Architecture


Description: The on-premise architecture diagram represents application running in a traditional data center. It includes:

UI Front End: The user interface of the application, developed with React.
Load Balancer: Distributes incoming traffic to multiple web servers.
Web Server: Hosts the application logic, built with Flask.
Cache: Stores temporary data to speed up response times (e.g., Redis).
Database: Persistent storage for application data (Postgres).
Monitoring: Tools for monitoring the health and performance of the application.
Diagram Explanation: This diagram shows how different components interact within the on-premise environment. The UI interacts with the load balancer, which distributes traffic to the web server. The web server queries the cache and database, and monitoring tools keep track of the system's performance.


![On-Premise Architecture](images/1.png)

## IaaS Architecture

Description: The IaaS diagram illustrates how the on-premise application is migrated to an Infrastructure as a Service (IaaS) model. In this setup:

UI Front End VM: The UI is hosted on a virtual machine in the cloud.
Web Server VM: The web server is also hosted on a virtual machine.
Database VM: The database runs on a separate virtual machine.
Cache VM: Caching services are provided by a virtual machine.
Monitoring VM: Monitoring tools are hosted on a virtual machine.
Network Security Group (NSG): Controls network traffic and provides security at the network level.
Diagram Explanation: The diagram shows the migration of each component from physical servers to virtual machines in the cloud. The Network Security Group ensures that only authorized traffic can access the virtual machines. The architecture retains most of the original application's design but leverages virtualized resources.



![IaaS Architecture](images/2.png)

## PaaS Architecture

Description: The PaaS diagram shows the application running on a Platform as a Service (PaaS) environment. In this model:

Static Web App: The UI front end is deployed as a static web application service.
Web App: The application logic is hosted on a managed app service (e.g., Azure App Service).
Managed DB: The database is replaced with a managed database service (e.g., Azure Database for PostgreSQL).
Cache: A managed caching service (e.g., Azure Cache for Redis) is used.
Monitoring: Integrated monitoring tools (e.g., Azure Monitor) are used.
Diagram Explanation: This diagram illustrates the use of managed services for different components. The application is deployed on PaaS services that handle infrastructure, scaling, and management, allowing you to focus on development and deployment. Integration between services is managed by the PaaS provider.


![PaaS Architecture](images/3.png)

## SaaS Architecture

Description: The SaaS diagram represents the application as a Software as a Service (SaaS) offering. Here:

Third-Party SaaS Application: The application logic is hosted by a third-party SaaS provider.
Third-Party SaaS UI: The user interface is also provided as a service.
Third-Party SaaS Database: Database services are managed by the SaaS provider.
Third-Party SaaS Cache: Caching is handled by the SaaS provider.
Third-Party SaaS Monitoring: Monitoring and performance tracking are managed by the SaaS provider.
Diagram Explanation: In this model, all application components are provided and maintained by an external vendor. The diagram shows that the entire application, including the front end, back end, database, and monitoring, is managed by a SaaS provider. This model abstracts away the need for infrastructure and platform management.


![SaaS Architecture](images/4.png)
