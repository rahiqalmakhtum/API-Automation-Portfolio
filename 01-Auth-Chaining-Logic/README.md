# API Test Automation: Authentication Chaining & Dynamic Data Handling

## 📌 Project Overview
This project demonstrates a real-world API testing scenario using **Postman** and **JavaScript**. It focuses on the critical "Auth-Chaining" workflow: authenticating a user, capturing a dynamic **Bearer Token**, and passing that token into subsequent protected requests to validate data integrity.

## 🚀 Key Features
- **Dynamic Token Extraction:** Automated the retrieval of JWT/Auth tokens from JSON responses using Postman Tests.
- **Environment Variable Management:** Implemented dynamic variable scoping to store and reuse tokens and base URLs across the collection.
- **API Chaining:** Developed a sequential workflow where the output of the Login API (Token) is required as the input for the "Get User" API.
- **Pre-request Scripting:** Utilized JavaScript to generate real-time timestamps for request headers, ensuring data freshness.

## 🛠️ Technical Stack
- **Tool:** Postman
- **Language:** JavaScript (Postman Sandbox)
- **API Environment:** ReqRes (Mock API)
- [cite_start]**Testing Methodology:** Functional Testing & Integration Testing [cite: 16]

## 📊 Execution & Test Results
Below is the execution proof from the Postman Collection Runner, demonstrating 100% pass rate and successful console logging of the dynamic data:

![Postman Execution Results](https://github.com/user-attachments/assets/37fc46a6-90fb-440e-b7f7-32d2df9c96b7)
### Key Observations from Logs:
- **Token Capture:** Successfully logged "Response token" from the Login endpoint.
- **State Persistence:** The environment variable `token` was updated in real-time.
- **Assertion Success:** Validated status codes (200 OK) and response body structure for all requests.

## 🧪 Test Scenarios Covered
1. **Positive Auth:** Verify successful login with valid credentials.
2. **Token Validation:** Ensure the `token` exists in the response and is a string.
3. **Authorized Access:** Verify that the "Get User" request succeeds only when the Bearer token is provided in the header.
4. **Dynamic Headers:** Verify that a unique timestamp is sent with every request via Pre-request scripts.

## ⚙️ Setup Instructions
1. Clone this repository.
2. Import the `Postman_Collection.json` into your Postman Workspace.
3. Import the `Environment.json` file.
4. Select "Environment 1" from the top-right dropdown.
5. Click **Run Collection**.
