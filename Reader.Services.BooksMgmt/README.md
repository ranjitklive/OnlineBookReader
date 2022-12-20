## Reader.Services.BooksMgmt

### Functionality

- Add Book Details
- Get Book Details
- Get All Books Details
- Update Book Details
- Delete Book Details

> *Reader.Services.Upload* service will upload the book file. However, details regarding the book will be handled by this service.
 
---

### Workflow

- Azure Service Bus Queue

> When book details are posted, a message is added to service bus queue. Service bus trigger will invoke an azure function.

- Azure Functions

> Azure Functions will insert data into database.

- Azure Cosmos DB for NoSQL

> Book details will be stored as JSON within NoSQL database. Book details once successfully added to database will trigger an Azure function to add a message to Service Bus topic.

- Azure Service Bus Topic

> The message is propogated to subscribers.

---

### Subscribers

*Reader.Services.Notification*

> Send email notification / push notification using Azure Functions about newly added book to subscribed users

*Reader.Services.Search*

> Extract metadata from Book available in Storage Blob. Possibly using Azure Search / Azure Cognitive Search.

---

### APIs

- [Add Book](#add-book)
    - [Add Book Request](#add-book-request)
    - [Add Book Response](#add-book-response)
- [Get Book](#get-book)
    - [Get Book Request](#get-book-request)
    - [Get Book Response](#get-book-response)
- [Get All Book](#get-all-book)
    - [Get All Book Request](#get-all-book-request)
    - [Get All Book Response](#get-all-book-response)
- [Update Book](#update-book)
    - [Update Book Request](#update-book-request)
    - [Update Book Response](#update-book-response)
- [Delete Book](#delete-book)
    - [Delete Book Request](#delete-book-request)
    - [Delete Book Response](#delete-book-response)

---

## Add Book

### Add Book Request

```js
POST /books
```

```json
{
    "name": "Clean Architecture",
    "description": "Clean Architecture: A Craftsman's Guide to Software Structure and Design",
    "url": "<blob-path>",
    "tags": [
        "Software",
        "Design",
        "Architecture"
    ],
    "authors": [
        "Robert Cecil Martin"
    ]
}
```

### Add Book Response

```js
201 Created
```

```yml
Location: {{host}}/books/{{id}}
```

```json
{
    "id": "00000000-0000-0000-0000-000000000000",
    "name": "Clean Architecture",
    "description": "Clean Architecture: A Craftsman's Guide to Software Structure and Design",
    "url": "<blob-path>",
    "tags": [
        "Software",
        "Design",
        "Architecture"
    ],
    "authors": [
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
    "url": "<blob-path>",
    "tags": [
        "Software",
        "Design",
        "Architecture"
    ],
    "authors": [
        "Robert Cecil Martin"
    ]
}
```

## Get All Books

### Get All Books Request

```js
GET /books
```

### Get All Books Response

```js
200 Ok
```

```json
[
    {
        "id": "00000000-0000-0000-0000-000000000000",
        "name": "Clean Architecture",
        "description": "Clean Architecture: A Craftsman's Guide to Software Structure and Design",
        "url": "<blob-path>",
        "tags": [
            "Software",
            "Design",
            "Architecture"
        ],
        "authors": [
            "Robert Cecil Martin"
        ]
    },
    {   
        "id": "00000000-0000-0000-0000-100000000001",
        "name": "Azure Serverless Computing",
        "description": "Azure Serverless Computing Cookbook: Build and monitor Azure applications",
        "url": "<blob-path>",
        "tags": [
            "Software",
            "Design",
            "Architecture"
        ],
        "authors": [
            "Praveen Kumar Sreeram"
        ]
    }
]
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
    "url": "<blob-path>",
    "tags": [
        "Software",
        "Design",
        "Architecture"
    ],
    "authors": [
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
Location: {{host}}/books/{{id}}
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