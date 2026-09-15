# 🚀 REST API Testing using Postman

<p align="center">
  <b>QA / API Testing Portfolio Project</b><br>
  Postman • JavaScript Assertions • Newman • GitHub Actions
</p>

<p align="center">
  <img src="https://img.shields.io/badge/API-REST-orange" alt="REST API">
  <img src="https://img.shields.io/badge/Tool-Postman-orange" alt="Postman">
  <img src="https://img.shields.io/badge/Test%20Cases-25%2B-blue" alt="Test Cases">
  <img src="https://img.shields.io/badge/Automation-Newman-purple" alt="Newman">
  <img src="https://img.shields.io/badge/CI-GitHub%20Actions-green" alt="GitHub Actions">
</p>

---

## 📌 1. Project Overview

This project demonstrates **practical REST API testing using Postman** from a QA fresher perspective.

The project covers API request creation, CRUD operations, positive and negative test scenarios, response validation, JavaScript assertions, environment variables, test-case documentation, Newman command-line execution and GitHub Actions CI execution.

### 🎯 Main Goal

To demonstrate that I can:

- Understand REST APIs and HTTP methods
- Design functional and negative API test scenarios
- Validate status codes, response bodies and important fields
- Write automated assertions in Postman using JavaScript
- Use variables and reusable test data
- Document test cases and defects clearly
- Execute API regression tests using Newman
- Integrate API tests with GitHub Actions

---

## 🧩 2. Application / API Under Test

**API:** JSONPlaceholder

**Base URL:** `https://jsonplaceholder.typicode.com`

JSONPlaceholder is a public fake REST API designed for testing and prototyping. It is used here as a safe learning/portfolio API rather than representing a real production client project.

### Resources Tested

| Resource | Endpoint | Purpose |
|---|---|---|
| Users | `/users` | User retrieval and negative validation |
| Posts | `/posts` | CRUD API testing |

---

## 🛠️ 3. Tools & Technologies

| Technology / Tool | Usage |
|---|---|
| **Postman** | API request creation and execution |
| **JavaScript** | Postman automated assertions |
| **REST API** | System under test |
| **JSON** | Request and response data |
| **Newman** | Command-line API execution |
| **GitHub Actions** | CI regression execution |
| **CSV / Excel** | Test-case documentation |
| **Markdown** | QA documentation |
| **Git / GitHub** | Version control and portfolio hosting |

---

## 🔄 4. API Testing Flow

```text
        API Requirement
              ↓
        Test Scenario Design
              ↓
       Postman Request Setup
              ↓
       Send API Request
              ↓
     ┌────────┴─────────┐
     ↓                  ↓
Response Validation   Negative Testing
     ↓                  ↓
Status / JSON /      Error / Invalid
Headers / Time       Input Validation
     └────────┬─────────┘
              ↓
      JavaScript Assertions
              ↓
       Collection Runner
              ↓
            Newman
              ↓
       GitHub Actions CI
```

---

## 🧪 5. API Test Coverage

### GET Requests

- Get a valid user
- Get all posts
- Get a valid post
- Get an invalid user
- Get an invalid post
- Validate response structure
- Validate required fields
- Validate response time

### POST Request

- Create a post with valid JSON
- Validate `201 Created`
- Validate created response fields
- Validate request content type

### PUT Request

- Update a complete post
- Validate `200 OK`
- Validate updated fields

### PATCH Request

- Partially update a post
- Validate updated title
- Validate `200 OK`

### DELETE Request

- Delete a post
- Validate successful response
- Include invalid-resource negative scenario in documented test coverage

---

## ❌ 6. Positive & Negative Testing

### Positive Scenarios

- Valid user ID
- Valid post ID
- Valid JSON request body
- Successful create operation
- Successful update operation
- Successful delete operation

### Negative Scenarios

- Invalid user ID
- Invalid post ID
- Invalid resource requests
- Missing / invalid request data scenarios documented in the test-case suite

Negative testing is important because a QA engineer should verify not only **what happens when the user does something correctly**, but also **how the API behaves with invalid input**.

---

## ✅ 7. Automated Assertions

Postman test scripts are used to automatically validate API responses.

### Status Code Validation

```javascript
pm.test("Status code is 200", () => {
    pm.response.to.have.status(200);
});
```

### Response Time Validation

```javascript
pm.test("Response time is below 1000ms", () => {
    pm.expect(pm.response.responseTime).to.be.below(1000);
});
```

### JSON Field Validation

```javascript
pm.test("Required user fields exist", () => {
    const body = pm.response.json();

    pm.expect(body).to.have.property("id");
    pm.expect(body).to.have.property("name");
    pm.expect(body).to.have.property("email");
});
```

### Response Type Validation

```javascript
pm.test("Response is an array", () => {
    pm.expect(pm.response.json()).to.be.an("array");
});
```

---

## 🌍 8. Environment Variables

The project uses reusable Postman variables instead of repeating hard-coded values.

| Variable | Example | Purpose |
|---|---|---|
| `baseUrl` | `https://jsonplaceholder.typicode.com` | API base URL |
| `userId` | `1` | User resource ID |
| `postId` | `1` | Post resource ID |

This makes the collection easier to maintain and execute against different environments or test data later.

---

## 📋 9. Test Case Documentation

The project contains **25+ documented API test scenarios** covering functional, negative, validation, configuration, regression and reporting areas.

Test cases include:

- Test Case ID
- Module
- HTTP Method
- Endpoint
- Scenario
- Expected Result
- Priority
- Test Type

Files:

- `TestCases/API_Test_Cases.csv`
- `TestCases/API_Test_Cases.xlsx`

---

## 📝 10. Test Plan

The test plan documents:

- Test objective
- Scope and out-of-scope areas
- Test approach
- Entry criteria
- Exit criteria
- Defect information to capture
- Risks and limitations
- Project deliverables

File:

`Documentation/API_Testing_Test_Plan.md`

---

## 🐞 11. Defect Reporting Approach

For a failed API test, the following information should be captured:

```text
Defect ID
Test Case ID
API Endpoint
HTTP Method
Request Headers
Request Body
Expected Result
Actual Result
Status Code
Response Body
Steps to Reproduce
Severity
Priority
```

This demonstrates the QA practice of converting a failed test into a clear, reproducible defect.

---

## 💻 12. Run Tests with Postman

### Step 1 — Import Collection

Import:

`Postman/API_Testing_Collection_v2.json`

### Step 2 — Import Environment

Import:

`Postman/QA_Environment.json`

### Step 3 — Select Environment

Select:

`QA-JSONPlaceholder-Environment`

### Step 4 — Execute

Run individual requests or execute the complete collection using **Collection Runner**.

### Step 5 — Review

Check:

- HTTP status
- Response body
- Test Results
- Assertion pass/fail status
- Response time

---

## ⚙️ 13. Run Tests with Newman

Newman allows the Postman collection to be executed from the command line.

### Install dependencies

```bash
npm install
```

### Run API tests

```bash
npm test
```

The command is configured in `package.json` to execute the Postman collection with the QA environment.

---

## 🔄 14. CI/CD with GitHub Actions

The repository contains:

`.github/workflows/api-tests.yml`

The workflow runs the API collection with Newman when changes are pushed to `main`, when a pull request targets `main`, or when manually triggered.

This demonstrates a basic **API regression + CI workflow** rather than limiting testing to manual Postman execution.

---

## 📁 15. Repository Structure

```text
REST-API-Testing-Postman/
│
├── .github/
│   └── workflows/
│       └── api-tests.yml
│
├── Documentation/
│   └── API_Testing_Test_Plan.md
│
├── Postman/
│   ├── API_Testing_Collection.json
│   ├── API_Testing_Collection_v2.json
│   ├── QA_Environment.json
│   └── README.md
│
├── TestCases/
│   ├── API_Test_Cases.csv
│   ├── API_Test_Cases.xlsx
│   └── Test_Data.json
│
├── Screenshots/
│   └── README.md
│
├── .gitignore
├── package.json
└── README.md
```

---

## 📸 16. Execution Evidence

The `Screenshots/` folder is prepared for actual execution evidence.

Recommended screenshots:

1. GET request + response + passing assertions
2. POST request + request body + `201` response
3. PUT update request + response
4. PATCH request + response
5. DELETE request + response
6. Negative `404` scenario
7. Collection Runner results
8. Successful GitHub Actions workflow

> **Important:** screenshots should be captured from your own Postman/Newman execution. Do not present mock screenshots as real test execution evidence.

---

## 🎤 17. Interview Explanation — 60 Seconds

> **“I created a REST API testing project using Postman on the JSONPlaceholder API. I covered GET, POST, PUT, PATCH and DELETE operations and designed both positive and negative test scenarios. I added JavaScript assertions to validate status codes, response fields, response type and response time. I used environment variables for reusable configuration and documented more than 25 test scenarios. I also configured Newman to execute the collection from the command line and integrated it with GitHub Actions so the API regression suite can run automatically when code changes are pushed.”**

---

## ❓ 18. Interview Questions I Can Answer from This Project

### Q1. Why did you use Postman?

Postman provides an easy way to create, organize and execute API requests and supports JavaScript-based automated assertions.

### Q2. What is the difference between PUT and PATCH?

**PUT** is generally used for a complete resource update, while **PATCH** is used for a partial update.

### Q3. How did you validate the response?

I used Postman test scripts to validate status codes, JSON fields, response type and response time.

### Q4. Why use environment variables?

They reduce hard-coded values and make collections easier to maintain and reuse across environments.

### Q5. Why Newman?

Newman allows Postman collections to run from the command line, which makes them suitable for automation and CI pipelines.

### Q6. Why GitHub Actions?

It allows the API regression suite to run automatically when repository changes occur.

### Q7. What would you test if authentication existed?

I would add valid/invalid credentials, missing token, expired token, unauthorized access, role-based authorization and token validation scenarios.

### Q8. What would you do if an API test failed?

I would inspect the request, headers, body, status code and response, reproduce the issue, compare expected vs actual behavior, and document a defect with clear reproduction steps.

---

## 🚧 19. Future Enhancements

The project can be extended with:

- Authentication / authorization testing
- Data-driven API testing
- More complex API chaining
- Schema validation
- Additional response-header validation
- HTML test reports
- API performance testing
- Integration with a real test environment
- Database validation when a real backend is available

---

## ⚠️ 20. Project Disclaimer

This is a **learning and portfolio project** created to demonstrate QA/API testing skills.

JSONPlaceholder is a public fake REST API for testing and prototyping. This project does **not** claim testing experience for a real company or production application.

---

## ⭐ Skills Demonstrated

**API Testing • Postman • REST • HTTP Methods • JSON • JavaScript Assertions • Positive Testing • Negative Testing • Test Case Design • Test Planning • Defect Reporting • Newman • Git • GitHub • GitHub Actions • CI Regression Testing**

---

<p align="center">
  <b>Built as a QA Automation / API Testing Portfolio Project</b>
</p>
