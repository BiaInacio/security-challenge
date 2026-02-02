# Incident Management System - QA Challenge

This repository contains the quality assurance deliverables for the Incident Management System. The project focuses on validating core functionalities, security protocols, and API integrity for a Node.js (Backend) and Vue.js (Frontend) application.

## 📋 Project Overview
The goal of this challenge was to perform a comprehensive audit of the system, including manual exploratory testing, API automated testing, and a documentation gap analysis.

## 🚀 Deliverables

### 1. Test Documentation
- **[Test Plan](./Test%20Plan%20-%20Full%20test%20plan.csv):** A detailed CSV containing 40+ test cases covering Authentication, Incident Creation, and Search functionality.
- **[Bug Reports](./Bug_Reports.md):** Documentation of 6 critical/high-priority bugs, including security vulnerabilities like stack trace exposure and UI functional failures.

### 2. API Testing (Postman)
- **[Postman Collection](./JOES%20Test.postman_collection.json):** A comprehensive suite of API requests.
- **Key Features:**
    - Automated Bearer Token inheritance.
    - Global scripts for **Security Validation** (detecting leaked internal server paths).
    - Response schema and performance baseline checks.

### 3. Documentation Gap Analysis
During the testing process, several inconsistencies and missing requirements were identified:
- **RBAC (Role-Based Access Control):** Lack of a defined permission matrix for the four existing user roles.
- **UI/API Parity:** Discrepancies between available fields in the API (e.g., Priority updates) vs. the Frontend.
- **Technical Specs:** Missing definitions for JWT expiration times and character limit constraints for input fields.

## 🛠 Tech Stack & Tools
- **Backend:** Node.js
- **Frontend:** Vue.js
- **API Testing:** Postman / Newman
- **Documentation:** Markdown / CSV

## 🧪 Automation Strategy
The proposed automation strategy follows the **Testing Pyramid**:
- **Unit Testing:** Vitest for Vue components.
- **Integration Testing:** Newman for automated API collection runs.
- **E2E Testing:** Playwright (specifically for cross-browser validation, including Safari/WebKit).

## 🛡️ Security Focus
Special attention was given to:
- **Information Leakage:** Ensuring 404/500 errors do not expose server directory structures.
- **Input Sanitization:** Validating system resilience against SQL and Command Injection.

---
**Author:** [Beatriz Inacio](https://github.com/BiaInacio)
