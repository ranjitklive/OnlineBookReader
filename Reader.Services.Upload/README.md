## Reader.Services.Upload

### Functionality

- Add/Upload Book
- Get Book
- Update/Replace Book
- Delete Book

> When Admin uploads a book using Web App, this service will load the file into Azure Storage Blob and extract metadata for use by *Reader.Services.Search* service.

---

### Workflow

- Azure Service Bus Queue

> A message is added into Service Bus Queue for the file to be picked-up for upload. 

- Azure Functions

> Azure Function is triggered upon arrival of message in Service Bus Queue. Azure Function will upload the file into Azure Storage Blob asynchronously using SAS token.

- Azure Storage Blob

> File uploaded successfully will trigger an Azure function to add a message to Service Bus topic.

- Azure Service Bus Topic

> The message is propogated to subscribers.

---

### Subscribers

- *Reader.Services.BooksMgmt*

---

### APIs

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
    "filepath": "<file-path>",
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
Location: {{host}}/upload/books/{{id}}
```

```json
{
    "id": "00000000-0000-0000-0000-000000000000",
    "name": "Clean Architecture",
    "description": "Clean Architecture: A Craftsman's Guide to Software Structure and Design",
    "filepath": "<file-path>",
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
GET /upload/books/{{id}}
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

## Update Book

### Update Book Request

```js
PUT /upload/books/{{id}}
```

```json
{
    "name": "Clean Architecture",
    "description": "Clean Architecture: A Craftsman's Guide to Software Structure and Design",
    "filepath": "<file-path>",
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
Location: {{host}}/upload/books/{{id}}
```

## Delete Book

### Delete Book Request

```js
DELETE /upload/books/{{id}}
```

### Delete Book Response

```js
204 No Content
```