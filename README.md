# API Cutover Test Run for DB Migration – Production (Read-Only / GET Endpoints)

This repository supports the validation of modernized and existing API services during the **production cutover phase**, focusing strictly on **read-only (`GET`) endpoints**. The goal is to ensure that the APIs respond correctly and consistently in the live environment without modifying any data.

## 📌 Purpose

- Validate that all **modernized and existing service endpoints** function as expected during the database migration period.
- Confirm the correctness of API behavior, response schemas, and performance in a production-like setting.

---

## 📁 Repository Contents

- `/collections`
  - Postman collection files (`.json`) with grouped `GET` endpoints.
- `/environment`
  - Postman environment configuration (e.g., base URL, headers).
- `/tests`
  - Custom test scripts (optional JavaScript-based assertions).
- `run-tests.sh`
  - CLI script to execute Postman tests via `newman`.


## 🧭 Testing Approach: Postman CLI (vs. Newman)

### ✅ Why Postman CLI?

We are using the **[Postman CLI](https://www.postman.com/product/cli/)** (via the `postman` command) instead of the legacy **Newman** tool for running test collections.

| Feature              | Postman CLI        | Newman              |
|----------------------|--------------------|---------------------|
| CI integration       | Built-in GitHub Actions, GitLab, etc. | Manual setup         |
| Reporting            | Modern dashboards & team analytics | Local CLI or HTML    |
| Postman Workspace integration | Yes                | No                  |
| OAuth 2.0 and token-based auth | Seamless with Postman setup | Manual               |
| Collection syncing   | Directly uses Postman Cloud | Manual `.json` files |

**Key Benefits**:
- Streamlines regression runs across environments.
- Automatically syncs with your **Postman workspace**.
- Provides rich, web-based reporting and analytics.
- Better support for API-first workflows in CI/CD.

---

## 🛠️ Prerequisites & Setup

### 1. Install Postman CLI

Follow the instructions for your OS:  
📘 https://www.postman.com/downloads/cli/


## 🔐 Notes

1. Only GET endpoints are tested to ensure read-only safety in production.

2. Make sure credentials and tokens are stored securely or managed via Postman Environment variables.

3. Avoid triggering sensitive endpoints accidentally—this suite is for non-destructive validation only.
   

## 📄 API Documentation

Refer to the official API documentation for:

1. Endpoint descriptions

2. Response schemas

3. Auth and header requirements

