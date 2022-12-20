## Reader.Services.Coupons

- Add Coupon Code
- Validate Coupon Code
- Update Coupon Code
- Delete Coupon Code

---

### Workflow

- Azure Service Bus Queue

> When Coupon Codes are added, a message is added to service bus queue. Service bus trigger will invoke an azure function.

- Azure Functions

> Azure Functions will insert data into database.

- Azure Cosmos DB for NoSQL

> Coupon Codes will be stored as JSON within NoSQL database. Coupon Codes once successfully added to database will trigger an Azure function to add a message to Service Bus topic.

---

### Subscribers

None

---

### APIs

- [Add Coupon](#add-coupon)
    - [Add Coupon Request](#add-coupon-request)
    - [Add Coupon Response](#add-coupon-response)
- [Get Coupon](#get-coupon)
    - [Get Coupon Request](#get-coupon-request)
    - [Get Coupon Response](#get-coupon-response)
- [Update Coupon](#update-coupon)
    - [Update Coupon Request](#update-coupon-request)
    - [Update Coupon Response](#update-coupon-response)
- [Delete Coupon](#delete-coupon)
    - [Delete Coupon Request](#delete-coupon-request)
    - [Delete Coupon Response](#delete-coupon-response)