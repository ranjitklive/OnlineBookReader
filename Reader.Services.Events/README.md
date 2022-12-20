## Reader.Services.Events

- Event Sourcing
- Transactions across services
- EventStoreDB / Azure Table Storage / Azure Cosmos DB for Table

---

### Workflow

#### Event Sourcing Pattern is used whenever a transaction (like User Registration) spans across multiple microservices:

- *Reader.Services.UserMgmt*

- *Reader.Services.Subscription*

- *Reader.Services.Coupons*

- *Reader.Services.Payments*

> Upon completing distributed transactions, a success message is posted into Azure Service Bus Topic.

- Azure Service Bus Topic

> Whenever individual steps is completed, each of above services will publish a message to Service Bus Topic. Service bus trigger will invoke an azure function.

- Azure Functions

> Azure Functions will insert data into database.

- Azure Cosmos DB for NoSQL

> Distributed transactions success status will be stored as JSON within NoSQL database.

- Azure WebJob

> Azure WebJob runs as console application within App Service will perform commit transaction (if all stages successful) or carry out compensating transaction by adding a message into Azure Service Bus Topic.

---

### Subscribers

> Services part of distributed transaction.

---

### APIs

- [Add Event](#add-event)
    - [Add Event Request](#add-event-request)
    - [Add Event Response](#add-event-response)
- [Get Event](#get-event)
    - [Get Event Request](#get-event-request)
    - [Get Event Response](#get-event-response)
- [Update Event](#update-event)
    - [Update Event Request](#update-event-request)
    - [Update Event Response](#update-event-response)
- [Delete Event](#delete-event)
    - [Delete Event Request](#delete-event-request)
    - [Delete Event Response](#delete-event-response)