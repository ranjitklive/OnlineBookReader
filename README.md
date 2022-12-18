# Online Book Reader

## Reader.Web

- Azure Front Door
- Azure CDN
- Azure DNS
- Azure Static Web Apps
- Azure API Gateway

## Azure API Gateway

- Authorisation
- Validate Token
- Routing
- Rate Limiting
- Caches Response

## Reader.Services.Identity

- Register User
- Token Creation
- Validate Credentials

- [Register User](#add-book)
    - [Register User Request](#add-book-request)
    - [Register User Response](#add-book-response)
  - [Get Book](#get-book)
    - [Get Book Request](#get-book-request)
    - [Get Book Response](#get-book-response)
  - [Update Book](#update-book)
    - [Update Book Request](#update-book-request)
    - [Update Book Response](#update-book-response)
  - [Delete Book](#delete-book)
    - [Delete Book Request](#delete-book-request)
    - [Delete Book Response](#delete-book-response)

## Register User

### Register User Request

```js
POST /books
```

```json
{
    "name": "Clean Architecture",
    "description": "Clean Architecture: A Craftsman's Guide to Software Structure and Design",
    "Tags": [
        "Software",
        "Design",
        "Architecture"
    ],
    "Author": [
        "Robert Cecil Martin"
    ]
}
```

### Register User Response

```js
201 Created
```

```yml
Location: {{host}}/Books/{{id}}
```

```json
{
    "id": "00000000-0000-0000-0000-000000000000",
    "name": "Clean Architecture",
    "description": "Clean Architecture: A Craftsman's Guide to Software Structure and Design",
    "Tags": [
        "Software",
        "Design",
        "Architecture"
    ],
    "Author": [
        "Robert Cecil Martin"
    ]
}
```

## Get Book

### Get Book Request

```js
GET /books/{{id}}
```

### Get Book Response

```js
200 Ok
```

```json
{
    "id": "00000000-0000-0000-0000-000000000000",
    "name": "Clean Architecture",
    "description": "Clean Architecture: A Craftsman's Guide to Software Structure and Design",
    "Tags": [
        "Software",
        "Design",
        "Architecture"
    ],
    "Author": [
        "Robert Cecil Martin"
    ]
}
```

## Update Book

### Update Book Request

```js
PUT /books/{{id}}
```

```json
{
    "name": "Clean Architecture",
    "description": "Clean Architecture: A Craftsman's Guide to Software Structure and Design",
    "Tags": [
        "Software",
        "Design",
        "Architecture"
    ],
    "Author": [
        "Robert Cecil Martin"
    ]
}
```

### Update Book Response

```js
204 No Content
```

or

```js
201 Created
```

```yml
Location: {{host}}/Books/{{id}}
```

## Delete Book

### Delete Book Request

```js
DELETE /books/{{id}}
```

### Delete Book Response

```js
204 No Content
```

## Reader.Services.UserMgmt

- Approve Registration
- User Information
- User Discount
- User Status

- [Add Book](#add-book)
    - [Add Book Request](#add-book-request)
    - [Add Book Response](#add-book-response)
  - [Get Book](#get-book)
    - [Get Book Request](#get-book-request)
    - [Get Book Response](#get-book-response)
  - [Update Book](#update-book)
    - [Update Book Request](#update-book-request)
    - [Update Book Response](#update-book-response)
  - [Delete Book](#delete-book)
    - [Delete Book Request](#delete-book-request)
    - [Delete Book Response](#delete-book-response)

## Add Book

### Add Book Request

```js
POST /books
```

```json
{
    "name": "Clean Architecture",
    "description": "Clean Architecture: A Craftsman's Guide to Software Structure and Design",
    "Tags": [
        "Software",
        "Design",
        "Architecture"
    ],
    "Author": [
        "Robert Cecil Martin"
    ]
}
```

### Add Book Response

```js
201 Created
```

```yml
Location: {{host}}/Books/{{id}}
```

```json
{
    "id": "00000000-0000-0000-0000-000000000000",
    "name": "Clean Architecture",
    "description": "Clean Architecture: A Craftsman's Guide to Software Structure and Design",
    "Tags": [
        "Software",
        "Design",
        "Architecture"
    ],
    "Author": [
        "Robert Cecil Martin"
    ]
}
```

## Get Book

### Get Book Request

```js
GET /books/{{id}}
```

### Get Book Response

```js
200 Ok
```

```json
{
    "id": "00000000-0000-0000-0000-000000000000",
    "name": "Clean Architecture",
    "description": "Clean Architecture: A Craftsman's Guide to Software Structure and Design",
    "Tags": [
        "Software",
        "Design",
        "Architecture"
    ],
    "Author": [
        "Robert Cecil Martin"
    ]
}
```

## Update Book

### Update Book Request

```js
PUT /books/{{id}}
```

```json
{
    "name": "Clean Architecture",
    "description": "Clean Architecture: A Craftsman's Guide to Software Structure and Design",
    "Tags": [
        "Software",
        "Design",
        "Architecture"
    ],
    "Author": [
        "Robert Cecil Martin"
    ]
}
```

### Update Book Response

```js
204 No Content
```

or

```js
201 Created
```

```yml
Location: {{host}}/Books/{{id}}
```

## Delete Book

### Delete Book Request

```js
DELETE /books/{{id}}
```

### Delete Book Response

```js
204 No Content
```

## Reader.Services.UserProfile

- User Details
- Subscription Details
- Books Reading

- [Add Book](#add-book)
    - [Add Book Request](#add-book-request)
    - [Add Book Response](#add-book-response)
  - [Get Book](#get-book)
    - [Get Book Request](#get-book-request)
    - [Get Book Response](#get-book-response)
  - [Update Book](#update-book)
    - [Update Book Request](#update-book-request)
    - [Update Book Response](#update-book-response)
  - [Delete Book](#delete-book)
    - [Delete Book Request](#delete-book-request)
    - [Delete Book Response](#delete-book-response)

## Add Book

### Add Book Request

```js
POST /books
```

```json
{
    "name": "Clean Architecture",
    "description": "Clean Architecture: A Craftsman's Guide to Software Structure and Design",
    "Tags": [
        "Software",
        "Design",
        "Architecture"
    ],
    "Author": [
        "Robert Cecil Martin"
    ]
}
```

### Add Book Response

```js
201 Created
```

```yml
Location: {{host}}/Books/{{id}}
```

```json
{
    "id": "00000000-0000-0000-0000-000000000000",
    "name": "Clean Architecture",
    "description": "Clean Architecture: A Craftsman's Guide to Software Structure and Design",
    "Tags": [
        "Software",
        "Design",
        "Architecture"
    ],
    "Author": [
        "Robert Cecil Martin"
    ]
}
```

## Get Book

### Get Book Request

```js
GET /books/{{id}}
```

### Get Book Response

```js
200 Ok
```

```json
{
    "id": "00000000-0000-0000-0000-000000000000",
    "name": "Clean Architecture",
    "description": "Clean Architecture: A Craftsman's Guide to Software Structure and Design",
    "Tags": [
        "Software",
        "Design",
        "Architecture"
    ],
    "Author": [
        "Robert Cecil Martin"
    ]
}
```

## Update Book

### Update Book Request

```js
PUT /books/{{id}}
```

```json
{
    "name": "Clean Architecture",
    "description": "Clean Architecture: A Craftsman's Guide to Software Structure and Design",
    "Tags": [
        "Software",
        "Design",
        "Architecture"
    ],
    "Author": [
        "Robert Cecil Martin"
    ]
}
```

### Update Book Response

```js
204 No Content
```

or

```js
201 Created
```

```yml
Location: {{host}}/Books/{{id}}
```

## Delete Book

### Delete Book Request

```js
DELETE /books/{{id}}
```

### Delete Book Response

```js
204 No Content
```

## Reader.Services.Subscription

- Add Subscription Plan
- Modify Subscription Plan
- Delete Subscription Plan

- [Add Book](#add-book)
    - [Add Book Request](#add-book-request)
    - [Add Book Response](#add-book-response)
  - [Get Book](#get-book)
    - [Get Book Request](#get-book-request)
    - [Get Book Response](#get-book-response)
  - [Update Book](#update-book)
    - [Update Book Request](#update-book-request)
    - [Update Book Response](#update-book-response)
  - [Delete Book](#delete-book)
    - [Delete Book Request](#delete-book-request)
    - [Delete Book Response](#delete-book-response)

## Add Book

### Add Book Request

```js
POST /books
```

```json
{
    "name": "Clean Architecture",
    "description": "Clean Architecture: A Craftsman's Guide to Software Structure and Design",
    "Tags": [
        "Software",
        "Design",
        "Architecture"
    ],
    "Author": [
        "Robert Cecil Martin"
    ]
}
```

### Add Book Response

```js
201 Created
```

```yml
Location: {{host}}/Books/{{id}}
```

```json
{
    "id": "00000000-0000-0000-0000-000000000000",
    "name": "Clean Architecture",
    "description": "Clean Architecture: A Craftsman's Guide to Software Structure and Design",
    "Tags": [
        "Software",
        "Design",
        "Architecture"
    ],
    "Author": [
        "Robert Cecil Martin"
    ]
}
```

## Get Book

### Get Book Request

```js
GET /books/{{id}}
```

### Get Book Response

```js
200 Ok
```

```json
{
    "id": "00000000-0000-0000-0000-000000000000",
    "name": "Clean Architecture",
    "description": "Clean Architecture: A Craftsman's Guide to Software Structure and Design",
    "Tags": [
        "Software",
        "Design",
        "Architecture"
    ],
    "Author": [
        "Robert Cecil Martin"
    ]
}
```

## Update Book

### Update Book Request

```js
PUT /books/{{id}}
```

```json
{
    "name": "Clean Architecture",
    "description": "Clean Architecture: A Craftsman's Guide to Software Structure and Design",
    "Tags": [
        "Software",
        "Design",
        "Architecture"
    ],
    "Author": [
        "Robert Cecil Martin"
    ]
}
```

### Update Book Response

```js
204 No Content
```

or

```js
201 Created
```

```yml
Location: {{host}}/Books/{{id}}
```

## Delete Book

### Delete Book Request

```js
DELETE /books/{{id}}
```

### Delete Book Response

```js
204 No Content
```

## Reader.Services.Payments
 
 - Accept Payments
 - Issue Refunds

 - [Add Book](#add-book)
    - [Add Book Request](#add-book-request)
    - [Add Book Response](#add-book-response)
  - [Get Book](#get-book)
    - [Get Book Request](#get-book-request)
    - [Get Book Response](#get-book-response)
  - [Update Book](#update-book)
    - [Update Book Request](#update-book-request)
    - [Update Book Response](#update-book-response)
  - [Delete Book](#delete-book)
    - [Delete Book Request](#delete-book-request)
    - [Delete Book Response](#delete-book-response)

## Add Book

### Add Book Request

```js
POST /books
```

```json
{
    "name": "Clean Architecture",
    "description": "Clean Architecture: A Craftsman's Guide to Software Structure and Design",
    "Tags": [
        "Software",
        "Design",
        "Architecture"
    ],
    "Author": [
        "Robert Cecil Martin"
    ]
}
```

### Add Book Response

```js
201 Created
```

```yml
Location: {{host}}/Books/{{id}}
```

```json
{
    "id": "00000000-0000-0000-0000-000000000000",
    "name": "Clean Architecture",
    "description": "Clean Architecture: A Craftsman's Guide to Software Structure and Design",
    "Tags": [
        "Software",
        "Design",
        "Architecture"
    ],
    "Author": [
        "Robert Cecil Martin"
    ]
}
```

## Get Book

### Get Book Request

```js
GET /books/{{id}}
```

### Get Book Response

```js
200 Ok
```

```json
{
    "id": "00000000-0000-0000-0000-000000000000",
    "name": "Clean Architecture",
    "description": "Clean Architecture: A Craftsman's Guide to Software Structure and Design",
    "Tags": [
        "Software",
        "Design",
        "Architecture"
    ],
    "Author": [
        "Robert Cecil Martin"
    ]
}
```

## Update Book

### Update Book Request

```js
PUT /books/{{id}}
```

```json
{
    "name": "Clean Architecture",
    "description": "Clean Architecture: A Craftsman's Guide to Software Structure and Design",
    "Tags": [
        "Software",
        "Design",
        "Architecture"
    ],
    "Author": [
        "Robert Cecil Martin"
    ]
}
```

### Update Book Response

```js
204 No Content
```

or

```js
201 Created
```

```yml
Location: {{host}}/Books/{{id}}
```

## Delete Book

### Delete Book Request

```js
DELETE /books/{{id}}
```

### Delete Book Response

```js
204 No Content
```

## Reader.Services.Coupons

- Add Promo Code
- Activate Promo Code
- Deactivate Promo Code

- [Add Book](#add-book)
    - [Add Book Request](#add-book-request)
    - [Add Book Response](#add-book-response)
  - [Get Book](#get-book)
    - [Get Book Request](#get-book-request)
    - [Get Book Response](#get-book-response)
  - [Update Book](#update-book)
    - [Update Book Request](#update-book-request)
    - [Update Book Response](#update-book-response)
  - [Delete Book](#delete-book)
    - [Delete Book Request](#delete-book-request)
    - [Delete Book Response](#delete-book-response)

## Add Book

### Add Book Request

```js
POST /books
```

```json
{
    "name": "Clean Architecture",
    "description": "Clean Architecture: A Craftsman's Guide to Software Structure and Design",
    "Tags": [
        "Software",
        "Design",
        "Architecture"
    ],
    "Author": [
        "Robert Cecil Martin"
    ]
}
```

### Add Book Response

```js
201 Created
```

```yml
Location: {{host}}/Books/{{id}}
```

```json
{
    "id": "00000000-0000-0000-0000-000000000000",
    "name": "Clean Architecture",
    "description": "Clean Architecture: A Craftsman's Guide to Software Structure and Design",
    "Tags": [
        "Software",
        "Design",
        "Architecture"
    ],
    "Author": [
        "Robert Cecil Martin"
    ]
}
```

## Get Book

### Get Book Request

```js
GET /books/{{id}}
```

### Get Book Response

```js
200 Ok
```

```json
{
    "id": "00000000-0000-0000-0000-000000000000",
    "name": "Clean Architecture",
    "description": "Clean Architecture: A Craftsman's Guide to Software Structure and Design",
    "Tags": [
        "Software",
        "Design",
        "Architecture"
    ],
    "Author": [
        "Robert Cecil Martin"
    ]
}
```

## Update Book

### Update Book Request

```js
PUT /books/{{id}}
```

```json
{
    "name": "Clean Architecture",
    "description": "Clean Architecture: A Craftsman's Guide to Software Structure and Design",
    "Tags": [
        "Software",
        "Design",
        "Architecture"
    ],
    "Author": [
        "Robert Cecil Martin"
    ]
}
```

### Update Book Response

```js
204 No Content
```

or

```js
201 Created
```

```yml
Location: {{host}}/Books/{{id}}
```

## Delete Book

### Delete Book Request

```js
DELETE /books/{{id}}
```

### Delete Book Response

```js
204 No Content
```

## Reader.Services.Search

- Search Books
- Search Text

- [Add Book](#add-book)
    - [Add Book Request](#add-book-request)
    - [Add Book Response](#add-book-response)
  - [Get Book](#get-book)
    - [Get Book Request](#get-book-request)
    - [Get Book Response](#get-book-response)
  - [Update Book](#update-book)
    - [Update Book Request](#update-book-request)
    - [Update Book Response](#update-book-response)
  - [Delete Book](#delete-book)
    - [Delete Book Request](#delete-book-request)
    - [Delete Book Response](#delete-book-response)

## Add Book

### Add Book Request

```js
POST /books
```

```json
{
    "name": "Clean Architecture",
    "description": "Clean Architecture: A Craftsman's Guide to Software Structure and Design",
    "Tags": [
        "Software",
        "Design",
        "Architecture"
    ],
    "Author": [
        "Robert Cecil Martin"
    ]
}
```

### Add Book Response

```js
201 Created
```

```yml
Location: {{host}}/Books/{{id}}
```

```json
{
    "id": "00000000-0000-0000-0000-000000000000",
    "name": "Clean Architecture",
    "description": "Clean Architecture: A Craftsman's Guide to Software Structure and Design",
    "Tags": [
        "Software",
        "Design",
        "Architecture"
    ],
    "Author": [
        "Robert Cecil Martin"
    ]
}
```

## Get Book

### Get Book Request

```js
GET /books/{{id}}
```

### Get Book Response

```js
200 Ok
```

```json
{
    "id": "00000000-0000-0000-0000-000000000000",
    "name": "Clean Architecture",
    "description": "Clean Architecture: A Craftsman's Guide to Software Structure and Design",
    "Tags": [
        "Software",
        "Design",
        "Architecture"
    ],
    "Author": [
        "Robert Cecil Martin"
    ]
}
```

## Update Book

### Update Book Request

```js
PUT /books/{{id}}
```

```json
{
    "name": "Clean Architecture",
    "description": "Clean Architecture: A Craftsman's Guide to Software Structure and Design",
    "Tags": [
        "Software",
        "Design",
        "Architecture"
    ],
    "Author": [
        "Robert Cecil Martin"
    ]
}
```

### Update Book Response

```js
204 No Content
```

or

```js
201 Created
```

```yml
Location: {{host}}/Books/{{id}}
```

## Delete Book

### Delete Book Request

```js
DELETE /books/{{id}}
```

### Delete Book Response

```js
204 No Content
```

## Reader.Services.Upload

- Upload Book
- Extract Metadata

- [Add Book](#add-book)
    - [Add Book Request](#add-book-request)
    - [Add Book Response](#add-book-response)
  - [Get Book](#get-book)
    - [Get Book Request](#get-book-request)
    - [Get Book Response](#get-book-response)
  - [Update Book](#update-book)
    - [Update Book Request](#update-book-request)
    - [Update Book Response](#update-book-response)
  - [Delete Book](#delete-book)
    - [Delete Book Request](#delete-book-request)
    - [Delete Book Response](#delete-book-response)

## Add Book

### Add Book Request

```js
POST /books
```

```json
{
    "name": "Clean Architecture",
    "description": "Clean Architecture: A Craftsman's Guide to Software Structure and Design",
    "Tags": [
        "Software",
        "Design",
        "Architecture"
    ],
    "Author": [
        "Robert Cecil Martin"
    ]
}
```

### Add Book Response

```js
201 Created
```

```yml
Location: {{host}}/Books/{{id}}
```

```json
{
    "id": "00000000-0000-0000-0000-000000000000",
    "name": "Clean Architecture",
    "description": "Clean Architecture: A Craftsman's Guide to Software Structure and Design",
    "Tags": [
        "Software",
        "Design",
        "Architecture"
    ],
    "Author": [
        "Robert Cecil Martin"
    ]
}
```

## Get Book

### Get Book Request

```js
GET /books/{{id}}
```

### Get Book Response

```js
200 Ok
```

```json
{
    "id": "00000000-0000-0000-0000-000000000000",
    "name": "Clean Architecture",
    "description": "Clean Architecture: A Craftsman's Guide to Software Structure and Design",
    "Tags": [
        "Software",
        "Design",
        "Architecture"
    ],
    "Author": [
        "Robert Cecil Martin"
    ]
}
```

## Update Book

### Update Book Request

```js
PUT /books/{{id}}
```

```json
{
    "name": "Clean Architecture",
    "description": "Clean Architecture: A Craftsman's Guide to Software Structure and Design",
    "Tags": [
        "Software",
        "Design",
        "Architecture"
    ],
    "Author": [
        "Robert Cecil Martin"
    ]
}
```

### Update Book Response

```js
204 No Content
```

or

```js
201 Created
```

```yml
Location: {{host}}/Books/{{id}}
```

## Delete Book

### Delete Book Request

```js
DELETE /books/{{id}}
```

### Delete Book Response

```js
204 No Content
```

## Reader.Services.BooksMgmt

 - Add Book
 - Modify Book
 - Delete Book

  - [Add Book](#add-book)
    - [Add Book Request](#add-book-request)
    - [Add Book Response](#add-book-response)
  - [Get Book](#get-book)
    - [Get Book Request](#get-book-request)
    - [Get Book Response](#get-book-response)
  - [Update Book](#update-book)
    - [Update Book Request](#update-book-request)
    - [Update Book Response](#update-book-response)
  - [Delete Book](#delete-book)
    - [Delete Book Request](#delete-book-request)
    - [Delete Book Response](#delete-book-response)

## Add Book

### Add Book Request

```js
POST /books
```

```json
{
    "name": "Clean Architecture",
    "description": "Clean Architecture: A Craftsman's Guide to Software Structure and Design",
    "Tags": [
        "Software",
        "Design",
        "Architecture"
    ],
    "Author": [
        "Robert Cecil Martin"
    ]
}
```

### Add Book Response

```js
201 Created
```

```yml
Location: {{host}}/Books/{{id}}
```

```json
{
    "id": "00000000-0000-0000-0000-000000000000",
    "name": "Clean Architecture",
    "description": "Clean Architecture: A Craftsman's Guide to Software Structure and Design",
    "Tags": [
        "Software",
        "Design",
        "Architecture"
    ],
    "Author": [
        "Robert Cecil Martin"
    ]
}
```

## Get Book

### Get Book Request

```js
GET /books/{{id}}
```

### Get Book Response

```js
200 Ok
```

```json
{
    "id": "00000000-0000-0000-0000-000000000000",
    "name": "Clean Architecture",
    "description": "Clean Architecture: A Craftsman's Guide to Software Structure and Design",
    "Tags": [
        "Software",
        "Design",
        "Architecture"
    ],
    "Author": [
        "Robert Cecil Martin"
    ]
}
```

## Update Book

### Update Book Request

```js
PUT /books/{{id}}
```

```json
{
    "name": "Clean Architecture",
    "description": "Clean Architecture: A Craftsman's Guide to Software Structure and Design",
    "Tags": [
        "Software",
        "Design",
        "Architecture"
    ],
    "Author": [
        "Robert Cecil Martin"
    ]
}
```

### Update Book Response

```js
204 No Content
```

or

```js
201 Created
```

```yml
Location: {{host}}/Books/{{id}}
```

## Delete Book

### Delete Book Request

```js
DELETE /books/{{id}}
```

### Delete Book Response

```js
204 No Content
```

## Reader.Services.Checkout

- Start Reading
- Pause Reading
- Return Book

- [Add Book](#add-book)
    - [Add Book Request](#add-book-request)
    - [Add Book Response](#add-book-response)
  - [Get Book](#get-book)
    - [Get Book Request](#get-book-request)
    - [Get Book Response](#get-book-response)
  - [Update Book](#update-book)
    - [Update Book Request](#update-book-request)
    - [Update Book Response](#update-book-response)
  - [Delete Book](#delete-book)
    - [Delete Book Request](#delete-book-request)
    - [Delete Book Response](#delete-book-response)

## Add Book

### Add Book Request

```js
POST /books
```

```json
{
    "name": "Clean Architecture",
    "description": "Clean Architecture: A Craftsman's Guide to Software Structure and Design",
    "Tags": [
        "Software",
        "Design",
        "Architecture"
    ],
    "Author": [
        "Robert Cecil Martin"
    ]
}
```

### Add Book Response

```js
201 Created
```

```yml
Location: {{host}}/Books/{{id}}
```

```json
{
    "id": "00000000-0000-0000-0000-000000000000",
    "name": "Clean Architecture",
    "description": "Clean Architecture: A Craftsman's Guide to Software Structure and Design",
    "Tags": [
        "Software",
        "Design",
        "Architecture"
    ],
    "Author": [
        "Robert Cecil Martin"
    ]
}
```

## Get Book

### Get Book Request

```js
GET /books/{{id}}
```

### Get Book Response

```js
200 Ok
```

```json
{
    "id": "00000000-0000-0000-0000-000000000000",
    "name": "Clean Architecture",
    "description": "Clean Architecture: A Craftsman's Guide to Software Structure and Design",
    "Tags": [
        "Software",
        "Design",
        "Architecture"
    ],
    "Author": [
        "Robert Cecil Martin"
    ]
}
```

## Update Book

### Update Book Request

```js
PUT /books/{{id}}
```

```json
{
    "name": "Clean Architecture",
    "description": "Clean Architecture: A Craftsman's Guide to Software Structure and Design",
    "Tags": [
        "Software",
        "Design",
        "Architecture"
    ],
    "Author": [
        "Robert Cecil Martin"
    ]
}
```

### Update Book Response

```js
204 No Content
```

or

```js
201 Created
```

```yml
Location: {{host}}/Books/{{id}}
```

## Delete Book

### Delete Book Request

```js
DELETE /books/{{id}}
```

### Delete Book Response

```js
204 No Content
```

## Reader.Services.Notification

- Send Emails
- Send Push Notifications

- [Add Book](#add-book)
    - [Add Book Request](#add-book-request)
    - [Add Book Response](#add-book-response)
  - [Get Book](#get-book)
    - [Get Book Request](#get-book-request)
    - [Get Book Response](#get-book-response)
  - [Update Book](#update-book)
    - [Update Book Request](#update-book-request)
    - [Update Book Response](#update-book-response)
  - [Delete Book](#delete-book)
    - [Delete Book Request](#delete-book-request)
    - [Delete Book Response](#delete-book-response)

## Add Book

### Add Book Request

```js
POST /books
```

```json
{
    "name": "Clean Architecture",
    "description": "Clean Architecture: A Craftsman's Guide to Software Structure and Design",
    "Tags": [
        "Software",
        "Design",
        "Architecture"
    ],
    "Author": [
        "Robert Cecil Martin"
    ]
}
```

### Add Book Response

```js
201 Created
```

```yml
Location: {{host}}/Books/{{id}}
```

```json
{
    "id": "00000000-0000-0000-0000-000000000000",
    "name": "Clean Architecture",
    "description": "Clean Architecture: A Craftsman's Guide to Software Structure and Design",
    "Tags": [
        "Software",
        "Design",
        "Architecture"
    ],
    "Author": [
        "Robert Cecil Martin"
    ]
}
```

## Get Book

### Get Book Request

```js
GET /books/{{id}}
```

### Get Book Response

```js
200 Ok
```

```json
{
    "id": "00000000-0000-0000-0000-000000000000",
    "name": "Clean Architecture",
    "description": "Clean Architecture: A Craftsman's Guide to Software Structure and Design",
    "Tags": [
        "Software",
        "Design",
        "Architecture"
    ],
    "Author": [
        "Robert Cecil Martin"
    ]
}
```

## Update Book

### Update Book Request

```js
PUT /books/{{id}}
```

```json
{
    "name": "Clean Architecture",
    "description": "Clean Architecture: A Craftsman's Guide to Software Structure and Design",
    "Tags": [
        "Software",
        "Design",
        "Architecture"
    ],
    "Author": [
        "Robert Cecil Martin"
    ]
}
```

### Update Book Response

```js
204 No Content
```

or

```js
201 Created
```

```yml
Location: {{host}}/Books/{{id}}
```

## Delete Book

### Delete Book Request

```js
DELETE /books/{{id}}
```

### Delete Book Response

```js
204 No Content
```

## Reader.Services.Sync

- Revoke User Access
- Revoke Deleted Book Access

- [Add Book](#add-book)
    - [Add Book Request](#add-book-request)
    - [Add Book Response](#add-book-response)
  - [Get Book](#get-book)
    - [Get Book Request](#get-book-request)
    - [Get Book Response](#get-book-response)
  - [Update Book](#update-book)
    - [Update Book Request](#update-book-request)
    - [Update Book Response](#update-book-response)
  - [Delete Book](#delete-book)
    - [Delete Book Request](#delete-book-request)
    - [Delete Book Response](#delete-book-response)

## Add Book

### Add Book Request

```js
POST /books
```

```json
{
    "name": "Clean Architecture",
    "description": "Clean Architecture: A Craftsman's Guide to Software Structure and Design",
    "Tags": [
        "Software",
        "Design",
        "Architecture"
    ],
    "Author": [
        "Robert Cecil Martin"
    ]
}
```

### Add Book Response

```js
201 Created
```

```yml
Location: {{host}}/Books/{{id}}
```

```json
{
    "id": "00000000-0000-0000-0000-000000000000",
    "name": "Clean Architecture",
    "description": "Clean Architecture: A Craftsman's Guide to Software Structure and Design",
    "Tags": [
        "Software",
        "Design",
        "Architecture"
    ],
    "Author": [
        "Robert Cecil Martin"
    ]
}
```

## Get Book

### Get Book Request

```js
GET /books/{{id}}
```

### Get Book Response

```js
200 Ok
```

```json
{
    "id": "00000000-0000-0000-0000-000000000000",
    "name": "Clean Architecture",
    "description": "Clean Architecture: A Craftsman's Guide to Software Structure and Design",
    "Tags": [
        "Software",
        "Design",
        "Architecture"
    ],
    "Author": [
        "Robert Cecil Martin"
    ]
}
```

## Update Book

### Update Book Request

```js
PUT /books/{{id}}
```

```json
{
    "name": "Clean Architecture",
    "description": "Clean Architecture: A Craftsman's Guide to Software Structure and Design",
    "Tags": [
        "Software",
        "Design",
        "Architecture"
    ],
    "Author": [
        "Robert Cecil Martin"
    ]
}
```

### Update Book Response

```js
204 No Content
```

or

```js
201 Created
```

```yml
Location: {{host}}/Books/{{id}}
```

## Delete Book

### Delete Book Request

```js
DELETE /books/{{id}}
```

### Delete Book Response

```js
204 No Content
```

## Reader.Services.Events

- Event Sourcing
- Transactions across services

- [Add Book](#add-book)
    - [Add Book Request](#add-book-request)
    - [Add Book Response](#add-book-response)
  - [Get Book](#get-book)
    - [Get Book Request](#get-book-request)
    - [Get Book Response](#get-book-response)
  - [Update Book](#update-book)
    - [Update Book Request](#update-book-request)
    - [Update Book Response](#update-book-response)
  - [Delete Book](#delete-book)
    - [Delete Book Request](#delete-book-request)
    - [Delete Book Response](#delete-book-response)

## Add Book

### Add Book Request

```js
POST /books
```

```json
{
    "name": "Clean Architecture",
    "description": "Clean Architecture: A Craftsman's Guide to Software Structure and Design",
    "Tags": [
        "Software",
        "Design",
        "Architecture"
    ],
    "Author": [
        "Robert Cecil Martin"
    ]
}
```

### Add Book Response

```js
201 Created
```

```yml
Location: {{host}}/Books/{{id}}
```

```json
{
    "id": "00000000-0000-0000-0000-000000000000",
    "name": "Clean Architecture",
    "description": "Clean Architecture: A Craftsman's Guide to Software Structure and Design",
    "Tags": [
        "Software",
        "Design",
        "Architecture"
    ],
    "Author": [
        "Robert Cecil Martin"
    ]
}
```

## Get Book

### Get Book Request

```js
GET /books/{{id}}
```

### Get Book Response

```js
200 Ok
```

```json
{
    "id": "00000000-0000-0000-0000-000000000000",
    "name": "Clean Architecture",
    "description": "Clean Architecture: A Craftsman's Guide to Software Structure and Design",
    "Tags": [
        "Software",
        "Design",
        "Architecture"
    ],
    "Author": [
        "Robert Cecil Martin"
    ]
}
```

## Update Book

### Update Book Request

```js
PUT /books/{{id}}
```

```json
{
    "name": "Clean Architecture",
    "description": "Clean Architecture: A Craftsman's Guide to Software Structure and Design",
    "Tags": [
        "Software",
        "Design",
        "Architecture"
    ],
    "Author": [
        "Robert Cecil Martin"
    ]
}
```

### Update Book Response

```js
204 No Content
```

or

```js
201 Created
```

```yml
Location: {{host}}/Books/{{id}}
```

## Delete Book

### Delete Book Request

```js
DELETE /books/{{id}}
```

### Delete Book Response

```js
204 No Content
```