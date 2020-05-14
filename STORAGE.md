## Storage

### Hot vs. Cool vs. Archive
Most customers start with hot storage for their needs, as it is the most performant. 
However, as data accumulate, it often happens that older blobs get accessed infrequently if at all.
In addition many clients, especially those in regulated industries, must follow archiving requirements. 

To address this, Azure has created three access tier levels: [hot, cool and archive](https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers?tabs=azure-portal). They allow customers to pay less in exchange for reduced performance and access.

Although the access tier of any given blob can be changed individually (via the portal, PowerShell, etc.) this can be tedious
and time consuming for large amounts of data.
Azure has created [lifecycle management](https://docs.microsoft.com/en-us/azure/storage/blobs/storage-lifecycle-management-concepts?tabs=azure-portal) to address this.
This feature allows you to create rules to automatically move blobs between access levels based on "last touched" status.
For example, this rule sends a given blob to archive if it hasn't been accessed in one year:
![Blob Lifecycle Rule](images/BlobLifecycleRule.JPG).

### Delete Unattached Disks
Often, when virtual machines get deleted the disks that were created for them do not.
This can result in many unused disks that are racking up charges.
See [this](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/find-unattached-disks) documentation
for PowerShell scripts to both discover and delete such resources.

### Double-Check Redundancy Needs
When a storage account is created via PowerShell or CLI, a SKU must by specified.
This forces the creator to consider what level of redundancy is required for the storage needs.

However, when a storage account is created from the Azure Portal, Read-access geo-redundant storage (RA-GRS) is the default,
and it is the most expensive SKU.
For example, RA-GRS is approximately three times more expensive than locally-redundant storage (LRS).

Double checking the redundancy requirements for each storage account can result in the ability to 
downgrade the level, saving money.
It may also discover accounts that should have a *higher* level of redundancy, potentially avoiding a disaster.

### Investigate Storage Reserved Capacity
As for virtual machine reserved instances, [storage reserved capacity](https://docs.microsoft.com/en-us/azure/cost-management-billing/reservations/save-compute-costs-reservations)
can result in significant long-term savings, currently up to 72% compared to pay-as-you-go.
If the customer has workloads that they are confident will exist for at least one or three years,
this option is well worth examining. 

### Double Check Size Needs

### Double Check Performance Needs
Depending on the storage type under review (storage account, managed disk, etc.) there are typically several levels of performance
available to choose.
For example, when creating a managed disk it's possible (depending on region) to select from Standard HDD, Standard SSD, Premium SSD and Ultra Disk. 
It may be possible to save costs by examining the usage patterns for each storage use case in the event that 
the performance level in use is higher than actually needed.
