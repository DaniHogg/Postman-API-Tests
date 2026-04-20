# ✅ README — `Postman-API-Tests`

> **Tone:** Purposeful, concise, demand‑driven  
> **Goal:** “Yes, I understand practical API testing.”

---

```markdown
# Postman API Tests

A collection of **API tests built in Postman**, created to demonstrate practical API testing skills that are commonly expected in QA roles.

This repository is intentionally lightweight and focused on **test logic and coverage**, not framework abstraction.

---

## 🎯 Purpose of This Repository

This repo exists to show:
- How I design API tests using Postman’s scripting capabilities
- How I validate responses beyond basic status codes
- How I structure collections for clarity and reuse

This complements my Python‑based API testing shown in `qa-automation-template` by demonstrating tooling that many teams actively use day‑to‑day.

---

## 🧪 What’s Included

- Postman collections containing:
  - Status code validation
  - Response body assertions
  - Basic schema and field checks
  - Response time checks
- Use of:
  - JavaScript test scripts
  - Collection‑level and request‑level tests

---

## 🌐 API Under Test

Public API used for testing:
- `https://jsonplaceholder.typicode.com`

Used because it supports:
- CRUD operations
- Nested resources
- Predictable responses ideal for test demonstration

---

## ✅ Example Test Assertions

- Response status is correct (200 / 201 / 404)
- Expected properties exist in the response body
- Response contains valid data types
- Response time remains within acceptable limits

---

## 📁 Repository Structure


Postman-API-Tests/
└── postman/
└── collections/
└── *.json

Collections can be:
- Imported directly into Postman
- Executed via Collection Runner
- Used with Newman if required

---

## 🧭 Why Postman (Alongside Python API Tests)

Many teams:
- Prototype in Postman
- Share collections across QA / Dev / BA roles
- Use Postman for exploratory and contract testing

This repo shows I’m comfortable operating in that space, not just writing code.

---

## 🔗 Related Automation Work

For a production‑style API automation framework using Python and pytest, see:
**qa-automation-template**
