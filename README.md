# Cost Optimization for CSAs
Cost optimization guidelines for CSAs

## Introduction
One of the primary job responsibilities of Cloud Solution Architects (CSA) is to help customers optimize their Azure spend. 
While there are many tools available to help with this, they are often spread out across multiple domains, and some are documented more as "tribal knowledge" than sharable guidelines.

The goal of this documentation is to provide CSAs with a repository to not only learn cost optimization ideas and best practices, but in addition serve as a place for them to add ones of their own.
If you want to assist, please contact [Gary Mullen-Schultz](mailto:gamullen@microsoft.com).

### Azure Advisor
[Azure Advisor](https://docs.microsoft.com/en-us/azure/advisor/advisor-overview) is a great first place to look for "low-hanging fruit" ideas on cost savings. Advisor also provides other valuable guidance for Azure usage, including:
* Security
* High Availability
* Operational Excellence
* Performance

We recommend this as your best first starting point for cost optimization analysis.

## Compute
Compute is typically a high-leverage area for cost optimization, as it encompasses much of the Infrastructure as a Service (IaaS) world. 

### Underutilized VMs
[GearUp](https://gearup.microsoft.com/checklists/well-architected)

### Reserved Instances



### App Service Environment
Many customers, especially those in highly-regulated industries such as healthcare and financial services, are using [App Service Environments](https://docs.microsoft.com/en-us/azure/app-service/environment/intro) (ASE) over cheaper [App Services](https://docs.microsoft.com/en-us/azure/app-service/) because they wanted to avoid exposing the web applications and APIs running there from the public internet. In the past, using an ASE was the only way to accomplish this.

Recently, however, [Private Link](https://docs.microsoft.com/en-us/azure/private-link/private-link-overview) support has been added to App Services. This allows a customer to add a private IP address to an App Service, and then access it privately from other Azure services on VNets, or from on premises via a site-to-site Virtual Private Network (VPN) or ExpressRoute. This is a much less expensive alternative than running an ASE.

Note that there are other benefits provided by the ASE service that may require the client to remain on that environment.
However, the capabilities provided by Private Link solve address the primary reason many customers originally chose ASE over App Services.

### Virtual Machine Scale Sets

## Data

### Right Size Underutilized SQL Databases

### Cosmos?

## Storage

### Hot vs. Cool vs. Archive

## Networking

### ExpressRoute SKUs

### Unused Public IPs

## Governance

### Business-Unit Chargeback
