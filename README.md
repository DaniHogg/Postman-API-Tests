# Postman API Tests

Postman-based API test showcase focused on practical request validation, response assertions, and workflow-driven testing.

This repository is intentionally lightweight and complements the Python automation projects by demonstrating how API testing is done in Postman day to day.

## Purpose

This project demonstrates:
- Request-level test design with Postman scripts
- Positive and negative API test coverage
- Reusable variables across a multi-step CRUD flow
- Clear, reviewer-friendly test intent in each request file

## Scope and Test Workflow

Collection: `Learning Mock API + Tests`

The suite is a mock API workflow designed to run in order:
1. Health check
2. List users
3. Create user (captures `userId`)
4. Get user
5. Update user
6. Delete user
7. Get deleted user (404 negative test)
8. Create user validation error (400 negative test)

Each request is kept in its own file under `postman/collections/.../*.request.yaml` for clarity and maintainability.

## API Target

Default collection target is a Postman-style mock API base URL:
- `https://example.mock.pstmn.io`

Before running, replace `baseUrl` in your environment with your real mock server URL if needed.

## How to Run

### In Postman
1. Open the repository in Postman Local View or import the collection from `postman/collections/Learning Mock API + Tests`.
2. Select `postman/environments/Learning Mock API - Mock Environment.yaml`.
3. Set `baseUrl` for your target mock server.
4. Run the collection in Collection Runner from top to bottom.

### With Newman
If you export the collection/environment to JSON, run with Newman:

```bash
newman run collection.json -e environment.json
```

## What This Repo Shows

- Status and header validation
- Response body field/type assertions
- Response time checks
- Variable capture and reuse (`userId`)
- Negative test handling for `404` and `400`

## Repository Structure

```text
Postman-API-Tests/
├── postman/
│   ├── collections/
│   │   └── Learning Mock API + Tests/
│   │       ├── 1 - Health Check.request.yaml
│   │       ├── ...
│   │       └── 8 - Create User - Validation Error (400).request.yaml
│   ├── environments/
│   │   └── Learning Mock API - Mock Environment.yaml
│   └── globals/
└── README.md
```

## Related Automation Work

For production-style API automation using Python + pytest, see `qa-automation-template`.
