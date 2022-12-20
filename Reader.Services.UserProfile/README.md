## Reader.Services.UserProfile

- Get User Profile

> Fetches User Information, Discounts, Account Status, Subscription, Reading Details (Books/Hours left)

- Delete User Profile

> Deletes User Information, Discounts, Account Status, Subscription, Reading Details (Books/Hours left)

---

### Workflow

Upon user login to WebApp, their user profile data needs to be fetched. 

- Azure Service Bus Queue

> Upon user login, a message is added into service bus topic. Service bus trigger will invoke an azure function.

- Azure Functions

> Azure Functions will query data from Azure Cache for Redis or database.

- Azure Cache for Redis

> User profile information is returned if already available in cache, else from database.

- Azure Cosmos DB for NoSQL

> User Profile details are stored as JSON in database.

---

### Subscribers

None

---

### APIs

- [Get User Profile](#get-user-profile)
    - [Get User Profile Request](#get-user-profile-request)
    - [Get User Profile Response](#get-user-profile-response)

- [Delete User Profile](#delete-user-profile)
    - [Delete User Profile Request](#delete-user-profile-request)
    - [Delete User Profile Response](#delete-user-profile-response)

---
## Get Book

### Get Book Request

```js
GET /profile/users/{{id}}
```

### Get Book Response

```js
200 Ok
```

```json
{
    "userinfo": {
        "id":"00000000-0000-0000-0000-000000000000", 
        "firstname":"<firstname>", 
        "lastname":"<lastname>"
    },
    "discounts": {
        "promoCode": "NEWYEAR"
    },
    "subscription": {
        "plan":"silver", 
        "status":"active"
    },
    "quotaForMonth": {
        "minutesRemaining":1200, 
        "booksRemaining":4
    }
}
```

## Delete User Profile

### Delete User Profile Request

```js
DELETE /profile/users/{{id}}
```

### Delete User Profile Response

```js
204 No Content
```