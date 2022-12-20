## Reader.Services.Search

- Search Books
- Create Search Indexes

---

### Workflow

- Azure WebJob

> Azure WebJob runs as console application within App Service picks-up message from Service Bus Topic (*Reader.Services.BooksMgmt*).

- Azure Search

> Create search index on the book data availabe in Azure Storage Blob. Search indexes created will be used during search activity on WebApp.

---

### Subscribers

None

---

### APIs

- [Create Search Index](#add-search-index)
    - [Add Search Index Request](#add-search-index-request)
    - [Add Search Index Response](#add-search-index-response)
- [Search](#get-search-index)
    - [Get Search Index Request](#get-search-index-request)
    - [Get Search Index Response](#get-search-index-response)
- [Update Search Index](#update-book)
    - [Update Search Index Request](#update-search-index-request)
    - [Update Search Index Response](#update-search-index-response)
- [Delete Search Index](#delete-book)
    - [Delete Search Index Request](#delete-search-index-request)
    - [Delete Search Index Response](#delete-search-index-response)

---