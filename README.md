# resilient-email-servic

This is a resilient email sending microservice built with TypeScript. It uses two mock providers and implements reliability patterns such as retry with exponential backoff, fallback provider switching, idempotency checks, basic rate limiting, and status tracking.
🔁 **Retry with Exponential Backoff** (3 attempts per provider)
- 🔀 **Fallback Mechanism** (tries second provider if the first fails)
- 🆔 **Idempotency Support** (prevents duplicate email sends)
- 🚦 **Basic Rate Limiting** (5 emails/second)
- 📊 **Email Status Tracking** (PENDING, SENT, FAILED, RETRYING)
- 🔌 **Simple Logging**
- 🧪 **Unit Tests using Jest**

> Bonus Features (not implemented): Circuit Breaker, Queue System

---

## 🏗 Project Structure

src/
├── providers/ # Email provider interfaces & mocks
├── utils/ # Logger, RateLimiter
├── types/ # Type definitions
├── EmailService.ts # Core logic
└── index.ts # Entry point for testing

tests/
└── EmailService.test.ts # Jest test for email sending
