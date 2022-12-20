## Reader.Services.Payments
 
 - Make Payments
 - Issue Refunds

---

### Workflow

#### This service is a gateway to Payment Gateway like Stripe or RazorPay.

- Service Bus Topic

> Upon successful payment, a message is published to Service Bus Topic.

---

### Subscribers

None

---

### APIs

- [Make Payment](#make-payment)
    - [Make Payment Request](#make-payment-request)
    - [Make Payment Response](#make-payment-response)
- [Issue Refund](#issue-refund)
    - [Issue Refund Request](#issue-refund-request)
    - [Issue Refund Response](#issue-refund-response)