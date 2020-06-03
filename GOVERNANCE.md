## Governance
Poor governance may be an area that doesn't jump to mind when discussion cost optimization,
but it can play a signficant direct and indirect role.
Microsoft has extensive internal experience with Azure Governance, as it needs to optimize how it runs all its own
SaaS solutions (Microsoft365, Dynamics, etc.) on Azure.
Two excellent starting points include:

* [Azure Cloud Adoption Framework](https://docs.microsoft.com/en-us/azure/cloud-adoption-framework/)
* [Azure Governance](https://azure.microsoft.com/en-us/solutions/governance/)

Note that governance covers more than pure Azure costs - it also results in better operations, management, extensibility, security, etc.

### Take Advantage of DevTest Subscriptions
[DevTest subscriptions](https://azure.microsoft.com/en-us/pricing/dev-test/) can provide significant cost savings
for a customer's non-prod workloads.

### Business-Unit Chargeback
Often, customers start small with Azure and move one or two workloads over.
At times, there is little discussion about what business unit will be paying for the services, and the IT department ends
up footing the bill.
This may work well for a while, but it will inevitibly reach a point where the monthly Azure spend is 
pushing the IT department's budget.
A side effect of this is that the actual business units benefiting from their solutions running in Azure have no incentive
to optimize their applications via many of the means described in this document, driving up costs.

### Budgets
[Azure Budgets](https://docs.microsoft.com/en-us/azure/cost-management-billing/manage/cost-management-budget-scenario)
are a control you can use to create monetary or metric-based thresholds for a scope such as a subscription, resource group or even management group. 
Alerts can be configured that are triggered at a certain configurable threshold of that budget.
For example, at 80% an alert is generated that could send an email, at 90% an email and an Azure Function trigger to send the owner a report of their spending. 
[Azure Action Groups](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/action-groups)
are used to define what actions occur when a given threshold is reached.
Actions that can be performed currently include:
* Automation Runbook.
* Azure Function.
* Email Azure Resource Manager Role.
* Email/SMS message/Push/Voice.
* ITSM.
* Logic App.
* Secure Webhook.
* Webhook.
