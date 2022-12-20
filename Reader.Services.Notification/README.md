## Reader.Services.Notification

- Send Emails
- Send Push Notifications

---

### Workflow

- Azure Service Bus Topic

> Individual Microservices will add a message to service bus topic whenever notification needs to be issued. *Reader.Services.Notification* is a subscriber. Service bus trigger will invoke an azure function.

- Azure Functions

> Azure Functions will send emails using SendGrid and push notification using Notification Hubs respectively.

- Azure Notification Hubs

> Scalable mobile push notification engine

---

### Subscribers

None

---

### APIs

- [Send Email](#send-email)
    - [Send Email Request](#send-email-request)
    - [Send Email Response](#send-email-response)
- [Send Push Notification](#send-push-notification)
    - [Send Push Notification Request](#send-push-notification-request)
    - [Send Push Notification Response](#send-push-notification-response)
- [Send Message](#send-message)
    - [Send Message Request](#send-message-request)
    - [Send Message Response](#send-message-response)