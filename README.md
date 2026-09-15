# REST API Testing using Postman

![API Testing](https://img.shields.io/badge/API-Testing-orange)
![Tool](https://img.shields.io/badge/Tool-Postman-orange)
![Tests](https://img.shields.io/badge/Test%20Cases-25%2B-blue)
![CI](https://img.shields.io/badge/CI-GitHub%20Actions-green)

## 📌 Project Overview

This project demonstrates practical **REST API testing using Postman**. It is structured as a QA portfolio project and covers functional, negative, validation and regression-oriented API scenarios.

The project uses **JSONPlaceholder**, a public REST API designed for testing and prototyping.

## 🎯 Objectives

- Validate REST API endpoints and HTTP methods
- Verify HTTP status codes and JSON response bodies
- Validate required response fields and response time
- Use Postman environment variables instead of hard-coded values
- Automate assertions using Postman JavaScript test scripts
- Document functional and negative test scenarios
- Execute the collection with Newman through GitHub Actions

## 🛠️ Tools & Technologies

| Tool / Technology | Purpose |
|---|---|
| Postman | API request creation and execution |
| JavaScript | Postman test assertions |
| Newman | Command-line collection execution |
| GitHub Actions | CI regression execution |
| JSON | Request/response and Postman collection format |
| Excel/CSV | Test-case documentation |
| Markdown | Project documentation |

## 🔗 API Under Test

**JSONPlaceholder:** https://jsonplaceholder.typicode.com

Main resources used:
- `/users`
- `/posts`

## 🧪 API Coverage

### GET
- Get a valid user
- Get all posts
- Get a valid post
- Invalid user/post scenarios

### POST
- Create a post with valid JSON
- Validate HTTP 201 response
- Validate response fields

### PUT
- Update a complete post
- Validate HTTP 200 response
- Validate updated fields

### PATCH
- Partially update a post
- Validate updated title

### DELETE
- Delete a post
- Validate successful response

## ✅ Assertions Implemented

Examples of automated validations included in the Postman collection:

```javascript
pm.test("Status code is 200", () => {
    pm.response.to.have.status(200);
});

pm.test("Response time is below 1000ms", () => {
    pm.expect(pm.response.responseTime).to.be.below(1000);
});

pm.test("Required fields exist", () => {
    const body = pm.response.json();
    pm.expect(body).to.have.property("id");
    pm.expect(body).to.have.property("name");
    pm.expect(body).to.have.property("email");
});
```

## 📁 Repository Structure

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
│   └── QA_Environment.json
│
├── TestCases/
│   ├── API_Test_Cases.csv
│   └── API_Test_Cases.xlsx
│
├── Screenshots/
│   └── README.md
│
├── .gitignore
├── package.json
└── README.md
```

## ▶️ How to Run in Postman

1. Install Postman.
2. Import `Postman/API_Testing_Collection_v2.json`.
3. Import `Postman/QA_Environment.json`.
4. Select `QA-JSONPlaceholder-Environment`.
5. Run individual requests or use Collection Runner.
6. Review the **Test Results** tab for assertion results.

## 💻 Run from Command Line with Newman

Install dependencies:

```bash
npm install
```

Run the collection:

```bash
npm test
```

The CI workflow also executes the collection automatically using Newman.

## 🔄 CI / GitHub Actions

The workflow in `.github/workflows/api-tests.yml` runs the Postman collection with Newman whenever changes are pushed to the repository or a pull request is opened.

## 📋 Test Documentation

See `TestCases/API_Test_Cases.csv` and `TestCases/API_Test_Cases.xlsx` for the documented test scenarios.

See `Documentation/API_Testing_Test_Plan.md` for scope, test approach, entry/exit criteria and defect considerations.

## 📸 Screenshots

The `Screenshots` folder is reserved for **actual Postman execution screenshots**. After running the collection locally, add screenshots showing request/response details and Collection Runner results.

> Do not present mock or illustrative images as real execution evidence. Replace them with your own Postman results before using this repository in an interview.

## 👨‍💻 Interview Summary

> "I created a REST API testing project using Postman covering GET, POST, PUT, PATCH and DELETE operations. I implemented JavaScript assertions for status codes, response fields and response time, used environment variables, documented positive and negative test cases, and configured Newman with GitHub Actions for repeatable regression execution."

## 📌 Disclaimer

JSONPlaceholder is a public fake REST API intended for testing and prototyping. This repository is a learning/portfolio project and does not represent testing performed for a real production company.
