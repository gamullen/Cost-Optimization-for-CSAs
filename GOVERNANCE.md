## Governance
Poor governance may be an area that doesn't jump to mind when discussion cost optimization,
but it can play a signficant direct and indirect role.
Microsoft has extensive internal experience with Azure Governance, as it needs to optimize how it runs all its own
SaaS solutions (Microsoft365, Dynamics, etc.) on Azure.
Two excellent starting points include:

* [Azure Cloud Adoption Framework](https://docs.microsoft.com/en-us/azure/cloud-adoption-framework/)
* [Azure Governance](https://azure.microsoft.com/en-us/solutions/governance/)

Note that governance covers more than pure Azure costs - it also results in better operations, management, extensibility, security, etc.

### Business-Unit Chargeback
Often, customers start small with Azure and move one or two workloads over.
At times, there is little discussion about what business unit will be paying for the services, and the IT department ends
up footing the bill.
This may work well for a while, but it will inevitibly reach a point where the monthly Azure spend is 
pushing the IT department's budget.
A side effect of this is that the actual business units benefiting from their solutions running in Azure have no incentive
to optimize their applications via many of the means described in this document, driving up costs.
