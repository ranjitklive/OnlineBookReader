## Reader.Services.Identity

- Register User
- Validate Credentials
- Token Creation

---

### Workflow

- Azure Service Bus Queue

> When user registers, form data goes as a message into service bus queue. Service bus trigger will invoke an azure function.

- Azure Functions

> Azure Functions will insert JSON data into NoSQL database with ***status=Inactive***.

- Azure Cosmos DB for NoSQL

> User registration details will be stored as JSON within NoSQL database. User registration details once successfully added to database will trigger an Azure function to add a message to Service Bus topic.

- Azure Service Bus Topic

> Once user registration details are saved in database successfully, a message is published to Service Bus topic.

---

### Subscribers

*Reader.Services.UserMgmt*

---

### APIs

- [Register User](#register-user)
    - [Register User Request](#register-user-request)
    - [Register User Response](#register-user-response)
- [Get User Registration](#get-user-registration)
    - [Get User Registration Request](#get-user-registration-request)
    - [Get User Registration Response](#get-user-registration-response)
- [Update User Registration](#update-user-registration)
    - [Update User Registration Request](#update-user-registration-request)
    - [Update User Registration Response](#update-user-registration-response)
- [Delete User Registration](#delete-user-registration)
    - [Delete User Registration Request](#delete-user-registration-request)
    - [Delete User Registration Response](#delete-user-registration-response)    
- [Validate User](#validate-user)
    - [Validate User Request](#validate-user-request)
    - [Validate User Response](#validate-user-response)
> Validates user login and retrieves JWT token from Identity Provider like Azure AD B2C or Auth0. 
- [Get Access Token](#get-access-token)
    - [Get Access Token Request](#validate-access-token-request)
    - [Get Access Token Response](#validate-access-token-response)
> Gets access token from Azure AD for the app registration in order to call individual microservice using API Management. 