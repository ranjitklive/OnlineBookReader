## Reader.Services.Sync

- Revoke User Access
- Revoke Deleted Book Access

---

### Workflow

> Background service which overlooks user subscription validity.

*Reader.Services.UserMgmt*

> Publish a message to Service Bus Topic when subscription is due to expire. 

*Reader.Services.BooksMgmt*

> Publish a message to Service Bus Topic when book is removed.

- Azure WebJob

> Azure WebJob runs as console application within App Service picks-up message from Service Bus Topic and makes API call to relavent service.

---

### Subscribers

None