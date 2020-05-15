## Data

### Reserved Capacity
Save costs for SQL Database compute resources with [Azure SQL Database reserved capacity](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-reserved-capacity).

### Leverage SQL Elastic Pools for SaaS implementations
[Azure SQL Elastic Pools](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-elastic-pool)
are a simple, cost-effective solution for managing and scaling multiple databases that have varying and unpredictable usage demands. The databases in an elastic pool are on a single Azure SQL Database server and share a set number of resources at a set price. Elastic pools in Azure SQL Database enable SaaS developers to optimize the price performance for a group of databases within a prescribed budget while delivering performance elasticity for each database.

### Control SQL Database Compute Time

#### Serverless Tier
[Azure SQL Database serverless](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-serverless)
is a capability worth investigation for reducing SQL costs.
* Consider running serverless for Dev/Test environments and when auto-pause/auto-resume is desired.
* Be aware of [cold start](https://azure.microsoft.com/en-us/blog/understanding-serverless-cold-start/)
with auto-start when using this solution.
* Look into further details on [pricing](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-serverless#cost),
[auto-scaling](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-serverless#autoscaling), 
and [auto-pause/resume](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-serverless#autopausing-and-autoresuming).

#### Azure Automation
You can schedule an Azure Automation PowerShell script to 
[scale your databases up and down](https://docs.microsoft.com/en-us/azure/sql-database/scripts/sql-database-monitor-and-scale-database-powershell)
at scheduled times.

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
