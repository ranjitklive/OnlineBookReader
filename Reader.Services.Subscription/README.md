## Reader.Services.Subscription

- Add Subscription Plan
- Modify Subscription Plan
- Delete Subscription Plan
- Azure Cosmos DB for NoSQL

---

### Workflow

- Azure Service Bus Queue

> When Subscription Plans are added, a message is added to service bus queue. Service bus trigger will invoke an azure function.

- Azure Functions

> Azure Functions will insert data into database.

- Azure Cosmos DB for NoSQL

> Subscription Plans will be stored as JSON within NoSQL database. Subscription Plans once successfully added to database will trigger an Azure function to add a message to Service Bus topic.

---

### Subscribers

None

---

### APIs

- [Add Subscription Plan](#add-subscription-plan)
    - [Add Subscription Plan Request](#add-subscription-plan-request)
    - [Add Subscription Plan Response](#add-subscription-plan-response)
- [Get Subscription Plan](#get-subscription-plan)
    - [Get Subscription Plan Request](#get-subscription-plan-request)
    - [Get Subscription Plan Response](#get-subscription-plan-response)
- [Update Subscription Plan](#update-subscription-plan)
    - [Update Subscription Plan Request](#update-subscription-plan-request)
    - [Update Subscription Plan Response](#update-subscription-plan-response)
- [Delete Subscription Plan](#delete-subscription-plan)
    - [Delete Subscription Plan Request](#delete-subscription-plan-request)
    - [Delete Subscription Plan Response](#delete-subscription Plan-response)