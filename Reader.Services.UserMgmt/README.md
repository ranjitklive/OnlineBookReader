## Reader.Services.UserMgmt

- Approve Registration

- Get User Details
> User Information, Discounts, Status

- Get All Users Details
> User Information, Discounts, Status

- Update User Details
> De-activate user account

---

Registered User details will be available in NoSQL database. Admin will approve user registration upon payment verification.

- Azure Service Bus Queue

> When a user registration is approved, a message is added to service bus queue. Service bus trigger will invoke an azure function.

- Azure Functions

> Azure Functions will update user profile data into NoSQL database with ***status=Active***. 

- Azure Cosmos DB for NoSQL

> Registered user data in database is now turned from ***Inactive*** to ***Active***.

- Azure Service Bus Topic

> The message is propogated to registered user via email or push notification.

---

### Subscribers

*Reader.Services.Notification*

> Send email notification / push notification using Azure Functions about newly added book to subscribed users

*Reader.Services.UserProfile*

> Update user profile status into ***Active***.

---

### APIs

- [Approve User Registration](#approve-user-registration)
    - [Approve User Registration Request](#approve-user-registration-request)
    - [Approve User Registration Response](#approve-user-registration-response)
- [Get Users Details](#get-user-details)
    - [Get Users Details Request](#get-user-details-request)
    - [Get Users Details Response](#get-user-details-response)
- [Get All Users Details](#get-all-users-detail)
    - [Get Users Details Request](#get-all-users-detail-request)
    - [Get Users Details Response](#get-all-users-detail-response)
- [Update Users Details](#update-user-details)
    - [Update Users Details Request](#update-user-details-request)
    - [Update Users Details Response](#update-user-details-response)