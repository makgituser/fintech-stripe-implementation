# Fintech Stripe Implementation

A production-style implementation demonstrating how **Stripe payments and subscriptions**
are integrated into a fintech application using **secure, scalable, and maintainable patterns**.

This repository showcases the same architectural approach I use in real-world fintech
products, without exposing any proprietary or NDA-protected code.

---

## 🚀 What This Project Demonstrates

- Stripe customer creation & management
- Subscription-based payments
- One-time payments
- Invoice lifecycle handling
- Secure webhook processing
- Payment failure & retry scenarios
- Clean separation of business logic

---

## 🧠 Architecture Overview

This project follows a **service-oriented architecture** suitable for fintech systems:

- Controllers handle request/response only
- Business logic is isolated in service classes
- Stripe logic is decoupled from core domain models
- Webhooks are processed asynchronously
- Environment-based configuration for security

---

## 🔐 Security & Compliance Considerations

- No Stripe secrets committed to the repository
- Environment variable-based configuration
- Webhook signature verification
- Idempotent webhook handling
- Clear separation of public vs secure endpoints

---

## 💳 Payment Flows Covered

### 1️⃣ Customer Creation
- Create and store Stripe customer
- Map customer to internal user

### 2️⃣ Subscription Payments
- Create subscriptions
- Handle recurring billing
- Manage plan upgrades & cancellations

### 3️⃣ One-Time Payments
- Payment Intent creation
- Confirmation & status handling

### 4️⃣ Invoices
- Track invoice states:
  - draft
  - open
  - paid
  - payment_failed
- Sync Stripe invoice events with internal records

### 5️⃣ Webhooks
- invoice.paid
- invoice.payment_failed
- customer.subscription.updated
- payment_intent.succeeded

---

## 🛠 Tech Stack

- Backend: Ruby on Rails (API-first)
- Payments: Stripe (Test Mode)
- Database: PostgreSQL
- Background Jobs: Sidekiq (or Active Job)
- Authentication: Token / JWT (demo)

---

## 📁 Project Structure (Simplified)

