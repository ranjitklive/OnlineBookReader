## Reader.Services.BooksMgmt

 - Add Book
 - Modify Book
 - Delete Book
 - Azure SQL Database

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