## Data

### Leverage SQL Elastic Pools
[Azure SQL Elastic Pools](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-elastic-pool)
are a simple, cost-effective solution for managing and scaling multiple databases that have varying and unpredictable usage demands. The databases in an elastic pool are on a single Azure SQL Database server and share a set number of resources at a set price. Elastic pools in Azure SQL Database enable SaaS developers to optimize the price performance for a group of databases within a prescribed budget while delivering performance elasticity for each database.

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
