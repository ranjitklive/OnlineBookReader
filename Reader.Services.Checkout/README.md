## Reader.Services.Checkout

- Checkout Book
> update quota of books left

- Start Reading
> update quota of hours left

- Pause Reading
> update quota of hours left

- Resume Reading
> get book chapter and scroll position

- Return Book
> update quota of books left

---

### Workflow

- Azure Service Bus Queue

> When user will checkout a book, a message is added to service bus queue. Service bus trigger will invoke an azure function.

- Azure Functions

> Azure Functions will insert data into database.

- Azure Cosmos DB for NoSQL

> User-Book mapping details will be stored as JSON within NoSQL database. User-Book mapping details once successfully added to database will trigger an Azure function to add a message to Service Bus topic.

- Azure Service Bus Topic

> The message is propogated to subscribers.

---

### Subscribers

*Reader.Services.UserProfile*

> To update quota of books left

---

### APIs

- [Checkout Book](#checkout-book)
    - [Checkout Book Request](#checkout-book-request)
    - [Checkout Book Response](#checkout-book-response)
- [Start Reading](#start-reading)
    - [Start Reading Request](#start-reading-request)
    - [Start Reading Response](#start-reading-response)
- [Pause Reading](#pause-reading)
    - [Pause Reading Request](#pause-reading-request)
    - [Pause Reading Response](#pause-reading-response)
- [Resume Reading](#resume-reading)
    - [Resume Reading Request](#resume-reading-request)
    - [Resume Reading Response](#resume-reading-response)
- [Return Book](#return-book)
    - [Return Book Request](#return-book-request)
    - [Return Book Response](#return-book-response)

---

## Checkout Book

### Checkout Book Request

```js
POST /checkout-book
```

```json
{
    "userid": "00000000-0000-0000-0000-000000000000",
    "bookid": "00000000-0000-0000-0000-000000000000"
}
```

### Checkout Book Response

```js
201 Created
```

```yml
Location: {{host}}/checkout-book/{{userid}}/books/{{bookid}}
```

```json
{
    "userid": "00000000-0000-0000-0000-000000000000",
    "bookid": "00000000-0000-0000-0000-000000000000"
}
```

## Start Reading

### Start Reading Request

```js
PUT /start-book/{{userid}}/books/{{bookid}}
```

```json
{
    "userid": "00000000-0000-0000-0000-000000000000",
    "bookid": "00000000-0000-0000-0000-000000000000"
}
```

### Start Reading Response

```js
200 Ok
```

```json
{
    "userid": "00000000-0000-0000-0000-000000000000",
    "bookid": "00000000-0000-0000-0000-000000000000",
    "chapterid": "<chapter-number>",
    "scroll": "<scroll-position>"
}
```

## Pause Reading

### Pause Reading Request

```js
PUT /pause-book/{{userid}}/books/{{bookid}}
```

```json
{
    "userid": "00000000-0000-0000-0000-000000000000",
    "bookid": "00000000-0000-0000-0000-000000000000",
    "chapterid": "<chapter-number>",
    "scroll": "<scroll-position>"
}
```

### Pause Reading Response

```js
204 No Content
```

## Resume Reading

### Resume Reading Request

```js
GET /resume-book/{{userid}}/books/{{bookid}}
```

### Resume Reading Response

```js
200 Ok
```

```json
{
    "userid": "00000000-0000-0000-0000-000000000000",
    "bookid": "00000000-0000-0000-0000-000000000000",
    "chapterid": "<chapter-number>",
    "scroll": "<scroll-position>"
}
```

## Return Book

### Return Book Request

```js
PUT /returns-book/{{userid}}/books/{{bookid}}
```

```json
{
    "userid": "00000000-0000-0000-0000-000000000000",
    "bookid": "00000000-0000-0000-0000-000000000000"
}
```
### Return Book Response

```js
204 No Content
```