# azure-cloud-migration

VMware-to-Azure migration project using Azure Migrate — covers assessment, lift-and-shift execution, application validation, and failover testing.

![Azure](https://img.shields.io/badge/Azure-Migrate-0078D4?style=flat&logo=microsoftazure)
![Windows Server](https://img.shields.io/badge/Windows-Server_2022-0078D6?style=flat&logo=windows)

## Overview

Migrated two Windows Server 2022 VMs from VMware Workstation Pro to Azure using Azure Migrate's lift-and-shift approach. Project covers the full migration lifecycle: readiness assessment, replication, cutover, application deployment, and failover simulation.

Also includes a multi-cloud resource comparison across AWS, Azure, and Google Cloud, and a cloud migration strategy document for a real-world financial services company (Bankingly).

## Projects

### 1. VMware-to-Azure VM Migration

Full migration of on-premises VMs to Azure using Azure Migrate.

| Phase | Details |
|---|---|
| Assessment | Azure Migrate appliance discovery, readiness evaluation, cost estimation |
| Migration | Lift-and-shift replication with final sync for data consistency |
| Validation | IIS-hosted Hello World app deployed and verified on public IP |
| Failover Testing | VM shutdown simulation, recovery verification, zero data loss |

**Key outcomes:**
- Both VMs migrated successfully with no data loss or performance degradation
- Application accessible post-migration at VM public IP
- Failover test confirmed application recovery after VM restart

### 2. Cloud Migration Strategy — Bankingly

Migration and expansion plan for a financial services company already on Azure.

- RACI matrix for migration stakeholders
- Phased 10-week migration schedule
- Security, compliance, and scalability recommendations
- Cost optimization analysis using Azure pay-as-you-go model

### 3. Multi-Cloud Resource Comparison

Side-by-side comparison of equivalent services across AWS, Azure, and Google Cloud — compute, storage, networking, databases, and managed services.

## Challenges and Solutions

**Azure Migrate appliance not detecting VMs**
Treated VMware Workstation VMs as physical servers instead of vCenter-managed — added IPs manually for discovery.

**SSL certificate error on appliance web interface**
Bypassed SSL errors via PowerShell and configured HTTPS manually.

**Credential validation failure**
Added outbound firewall rules on VMs to allow HTTPS (port 443) connectivity to Azure.

## Screenshots

Migration assessment and validation screenshots are in the Lab-VM-Migration/images/ directory.
