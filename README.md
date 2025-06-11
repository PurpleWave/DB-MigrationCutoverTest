# API Cutover Test Run – Production (Read-Only / GET Endpoints)

This repository supports the validation of modernized API services during the **production cutover phase**, focusing strictly on **read-only (`GET`) endpoints**. The goal is to ensure that the APIs respond correctly and consistently in the live environment without modifying any data.

## 📌 Purpose

- Validate that all **modernized service endpoints** function as expected during the database migration period.
- Provide the **QA team** with a ready-to-use test collection for running **comprehensive regression tests** in **read-only mode**.
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


