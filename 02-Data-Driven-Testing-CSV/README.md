# 📊 Data-Driven API Automation (Multi-Environment & CSV)

## 📌 Project Overview
This project demonstrates advanced **Data-Driven Testing (DDT)** methodologies using **Postman**. It simulates a real-world enterprise scenario where a single test suite is executed across multiple server environments (**QA & Staging**) using an external **CSV dataset** to validate bulk user registration and lifecycle management.

## 🚀 Key Technical Features
* **Bulk Data Integration:** Utilized a `users.csv` file containing 13 unique user records to drive 13 separate iterations of the test suite in a single execution.
* **Dynamic Variable Injection:** Implemented `{{name}}` and `{{job}}` placeholders in the request body, dynamically mapped from the CSV headers.
* **Multi-Environment Configuration:** Developed modular environment files (`QA.json` & `Staging.json`) with dynamic `baseURL` variables to ensure API consistency across different server tiers.
* **Full CRUD Lifecycle:** Automated the complete flow:
    1. **Auth:** Single login to capture a session token.
    2. **Create:** Bulk user creation via CSV data.
    3. **Update:** Modifying user attributes for each record.
    4. **Delete:** Cleaning up test data after each iteration.

## 🛠️ Technical Stack
* **Tool:** Postman (Collection Runner)
* **Data Format:** CSV (Comma-Separated Values)
* **Environments:** QA & Staging
* **Testing Type:** Functional, Regression, and Data-Driven Testing (DDT)

## 📂 Project Structure
| File | Description |
| :--- | :--- |
| `User_Registration.postman_collection.json` | Core automation logic and test scripts. |
| `users.csv` | External dataset with 13 unique test cases. |
| `QA.postman_environment.json` | Configuration for the QA server. |
| `Staging.postman_environment.json` | Configuration for the Staging server. |

## 📊 Execution Results
Below is the visual proof of the **100% Pass Rate** across 13 iterations using the Collection Runner.

![Test Execution Results](https://github.com/user-attachments/assets/19efecb9-8e3d-43e5-9536-9185e54b9116)


| Iterations | Status | Pass Rate |
| :--- | :--- | :--- |
| 13 Records | 201 Created / 200 OK | 100% |
