## Data

### Leverage SQL Elastic Pools
[Azure SQL Elastic Pools](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-elastic-pool)
are a simple, cost-effective solution for managing and scaling multiple databases that have varying and unpredictable usage demands. The databases in an elastic pool are on a single Azure SQL Database server and share a set number of resources at a set price. Elastic pools in Azure SQL Database enable SaaS developers to optimize the price performance for a group of databases within a prescribed budget while delivering performance elasticity for each database.

### Reserved Capacity
Save costs for SQL Database compute resources with Azure SQL Database reserved capacity https://docs.microsoft.com/en-us/azure/sql-database/sql-database-reserved-capacity

### Enterprise Dev/Test Subscription
 https://azure.microsoft.com/en-us/offers/ms-azr-0148p/
- Provides special lower Dev/Test rates
- Only users with MSDN(Visual Studio) subscription users would be able to access a Dev/Test subscription: https://azure.microsoft.com/en-us/offers/ms-azr-0148p/
- Azure SQL Database managed Instance is currently supported on the following subscription types https://docs.microsoft.com/en-us/azure/sql-database/sql-database-managed-instance-resource-limits

### Control SQL Database Compute Time

#### Serverless Tier
- Consider running Serverless tier for Dev environments and when autopause/auto-resume is desired.
- Be aware of cold start with Autostarte when using this solution
-  Pricing: https://docs.microsoft.com/en-us/azure/sql-database/sql-database-serverless#cost
- Autoscaling: https://docs.microsoft.com/en-us/azure/sql-database/sql-database-serverless#autoscaling
- Autopause and Autoresume: https://docs.microsoft.com/en-us/azure/sql-database/sql-database-serverless#autopausing-and-autoresuming

#### Azure Automation to Scale

You can schedule an Azure Automation Powershell script to scale up/down at scheduled times.

https://docs.microsoft.com/en-us/azure/sql-database/scripts/sql-database-monitor-and-scale-database-powershell

### Right Size Underutilized SQL Databases
This is very similar to the underutilized VMs section [above](https://github.com/gamullen/Cost-Optimization-for-CSAs#underutilized-vms), but SQL resources can often be even more expensive than VMs.

### Cosmos DB Optimization
There are numerous ways to optimize Azure Cosmos DB, including:
* Query performance (compute)
* Storage
* Reads and writes
* Multi-region usage
* Dev/Test
* Reserved capacity

[This set of pages](https://docs.microsoft.com/en-us/azure/cosmos-db/plan-manage-costs) contains detailed information on
how to optimize each of these, and more.
