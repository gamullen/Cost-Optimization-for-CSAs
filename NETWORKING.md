## Networking

### ExpressRoute SKUs
We had one customer who initially designed its network without using the commonly-recommended ["Hub and Spoke" architecture](https://docs.microsoft.com/en-us/azure/architecture/reference-architectures/hybrid-networking/hub-spoke).
Because of this, they eventually grew their subscriptions to a point where the Standard SKU was insufficient, as it limits 10 virtual network links per circuit. This, in turn, necessitated the Premium ExpressRoute SKU, which is significantly more expensive than the Standard SKU.

We worked with them to change to a Hub and Spoke network topology, allowing them to revert to the Standard SKU. In their case, this resulted in approximately $36K in savings annually. It also led to a more modern and flexible network architecture better suited for future growth.

### Unused Public IPs
Currently, static public IPs in Azure cost over $40 annually. Eliminating unused ones is simple,
and Azure Advisor does a
nice job highlighting underutilized public IP addresses as shown in 
[this screenshot](https://github.com/gamullen/Cost-Optimization-for-CSAs/blob/master/README.md#underutilized-vms).
