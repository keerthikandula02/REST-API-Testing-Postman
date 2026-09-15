# 🚀 REST API Testing using Postman

<p align="center"><b>Interview-Ready QA / API Testing Portfolio Project</b><br>Postman • JavaScript Assertions • Newman • GitHub Actions</p>

<p align="center"><img src="https://img.shields.io/badge/API-REST-orange"><img src="https://img.shields.io/badge/Tool-Postman-orange"><img src="https://img.shields.io/badge/Test%20Cases-25%2B-blue"><img src="https://img.shields.io/badge/Automation-Newman-purple"><img src="https://img.shields.io/badge/CI-GitHub%20Actions-green"></p>

> **Fresher QA portfolio:** a complete REST API testing example showing request design, CRUD testing, positive/negative scenarios, JavaScript assertions, documentation, Newman execution and GitHub Actions CI.

## 📌 What is this project?

This project demonstrates a practical QA workflow using the public **JSONPlaceholder** REST API. It is a learning/portfolio project and does not claim production testing experience for a real company.

**Base URL:** `https://jsonplaceholder.typicode.com`

### 🎯 Skills demonstrated

- REST API and HTTP fundamentals
- GET, POST, PUT, PATCH, DELETE
- Functional and negative testing
- JSON response validation
- Status-code, header and response-time validation
- JavaScript assertions in Postman
- Environment variables
- Test-case design and documentation
- Defect reporting approach
- Newman command-line execution
- GitHub Actions CI regression
- Git/GitHub

## 🔄 API Testing Flow

```text
Requirement → Test Scenario → Postman Request → API Response
                                      ↓
                              JavaScript Assertions
                                      ↓
                               Pass / Fail Result
                                      ↓
                              Collection Runner
                                      ↓
                                    Newman
                                      ↓
                              GitHub Actions CI
```

## 🧪 Test Coverage

| Method | Scenario | Main validation |
|---|---|---|
| GET | Valid user | 200 + required JSON fields |
| GET | All posts | 200 + array response |
| GET | Invalid user/post | Negative 404 validation |
| POST | Create post | 201 + created fields |
| PUT | Full update | 200 + updated fields |
| PATCH | Partial update | 200 + updated title |
| DELETE | Delete post | Successful response |

## ✅ Example Postman Assertions

```javascript
pm.test("Status code is 200", () => {
    pm.response.to.have.status(200);
});

pm.test("Response time is below 1000ms", () => {
    pm.expect(pm.response.responseTime).to.be.below(1000);
});

pm.test("Required user fields exist", () => {
    const body = pm.response.json();
    pm.expect(body).to.have.property("id");
    pm.expect(body).to.have.property("name");
    pm.expect(body).to.have.property("email");
});
```

## 🌍 Environment Variables

| Variable | Example |
|---|---|
| `baseUrl` | `https://jsonplaceholder.typicode.com` |
| `userId` | `1` |
| `postId` | `1` |

## 📋 Test Cases

The project contains **25+ documented scenarios** with Test Case ID, module, HTTP method, endpoint, scenario, expected result, priority and test type.

- `TestCases/API_Test_Cases.csv`
- `TestCases/API_Test_Cases.xlsx`
- `TestCases/Test_Data.json`

## 📝 QA Documentation

- `Documentation/PROJECT_OVERVIEW.md` — project in one page
- `Documentation/INTERVIEW_READY_GUIDE.md` — interview explanation and questions
- `Documentation/API_Testing_Test_Plan.md` — test scope and approach
- `Documentation/API_Request_Reference.md` — endpoint reference
- `Documentation/TEST_EXECUTION_GUIDE.md` — execution steps
- `Documentation/Defect_Report_Template.md` — defect template

## ▶️ How to Run

### Postman

1. Import `Postman/API_Testing_Collection_v2.json`.
2. Import `Postman/QA_Environment.json`.
3. Select `QA-JSONPlaceholder-Environment`.
4. Run requests individually or with Collection Runner.
5. Review response and Test Results.

### Newman

```bash
npm install
npm test
```

## 🔄 GitHub Actions

`.github/workflows/api-tests.yml` runs the collection with Newman for CI regression on repository changes and supports manual execution.

## 📸 Screenshots

The `Screenshots/` folder contains the checklist for **real execution evidence**. Capture screenshots from your own Postman run and GitHub Actions run rather than presenting mock results as real evidence.

Recommended evidence:

1. GET + response + passing assertions
2. POST + JSON body + 201
3. PUT + response
4. PATCH + response
5. DELETE + response
6. Negative 404 test
7. Collection Runner results
8. GitHub Actions successful run

## 📁 Repository Structure

```text
REST-API-Testing-Postman/
├── .github/workflows/api-tests.yml
├── Documentation/
├── Postman/
├── TestCases/
├── Screenshots/
├── .gitignore
├── package.json
└── README.md
```

## 🎤 60-Second Interview Answer

> “I created a REST API testing project using Postman on the JSONPlaceholder API. I covered GET, POST, PUT, PATCH and DELETE operations with positive and negative scenarios. I added JavaScript assertions for status codes, response fields, response type and response time. I used environment variables for reusable configuration and documented more than 25 test scenarios. I also configured Newman for command-line execution and GitHub Actions for API regression in CI.”

## ❓ Questions to Prepare

**Why Postman?** It is convenient for creating, organizing and executing API requests and supports JavaScript assertions.

**PUT vs PATCH?** PUT is generally used for a complete update; PATCH is for a partial update.

**Why Newman?** It executes Postman collections from the command line, making them suitable for CI.

**Why GitHub Actions?** To run API regression automatically when repository changes occur.

**What if a test fails?** Inspect request, headers, body, status and response; reproduce the issue; compare expected vs actual; document a clear defect.

## ⚠️ Portfolio Disclaimer

JSONPlaceholder is a public fake API for testing and prototyping. This repository is a learning/portfolio project and does not claim production testing experience for a real company.

<p align="center"><b>QA Automation / API Testing Portfolio Project</b></p>
