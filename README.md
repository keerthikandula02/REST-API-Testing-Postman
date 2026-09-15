# 🚀 REST API Testing using Postman

<p align="center">
  <b>QA / Software Testing Portfolio Project</b><br>
  Postman • REST API Testing • JavaScript • Newman • GitHub Actions
</p>

<p align="center">
  <img src="https://img.shields.io/badge/API-REST-orange">
  <img src="https://img.shields.io/badge/Tool-Postman-orange">
  <img src="https://img.shields.io/badge/Test%20Cases-25%2B-blue">
  <img src="https://img.shields.io/badge/Automation-Newman-purple">
  <img src="https://img.shields.io/badge/CI-GitHub%20Actions-green">
</p>

## 👩‍💻 About Me

Hi, I'm **Keerthi Kandula**, an MCA graduate and aspiring **Software Tester / QA Engineer** with a strong interest in Manual Testing, Automation Testing and API Testing.

My technical skills include **Python, Selenium WebDriver, PyTest, SQL, Postman, REST APIs, Git, GitHub, STLC, SDLC and Agile Scrum**. I created this project to demonstrate my practical understanding of REST API testing and to maintain an interview-ready QA portfolio on GitHub.

---

## 📌 Project Overview

This project demonstrates a practical **REST API testing workflow using Postman** with the public [JSONPlaceholder](https://jsonplaceholder.typicode.com/) API.

The project covers API request creation, CRUD operations, positive and negative testing, JavaScript assertions, environment variables, test-case documentation, Newman execution and GitHub Actions CI.

> **Portfolio note:** This is a personal learning and demonstration project created to showcase my QA/API testing skills. It does not represent production testing experience for a real company.

### 🔗 API Used

**Base URL:** `https://jsonplaceholder.typicode.com`

---

## 🎯 Objectives

- Understand and test REST API endpoints
- Validate HTTP methods and status codes
- Design positive and negative API test scenarios
- Validate JSON response data
- Validate response headers and response time
- Write JavaScript assertions in Postman
- Use environment variables for reusable test configuration
- Execute collections using Newman
- Demonstrate API regression execution through GitHub Actions
- Document test cases and QA testing approach

---

## 🛠️ Tools & Technologies

| Category | Tools / Technologies |
|---|---|
| API Testing | Postman, REST APIs |
| Scripting | JavaScript |
| CLI Automation | Newman |
| CI/CD | GitHub Actions |
| Test Documentation | Excel, CSV, Markdown |
| Version Control | Git, GitHub |
| API Format | JSON |
| QA Concepts | Manual Testing, Positive/Negative Testing, STLC, SDLC |

---

## 🔄 API Testing Workflow

```text
Requirement
     ↓
Test Scenario / Test Case
     ↓
Postman Request
     ↓
API Response
     ↓
JavaScript Assertions
     ↓
Pass / Fail Result
     ↓
Collection Runner
     ↓
Newman CLI
     ↓
GitHub Actions CI
```

---

## 🧪 API Test Coverage

| HTTP Method | Scenario | Validation |
|---|---|---|
| GET | Get valid user | Status code + JSON fields |
| GET | Get all posts | Status code + array response |
| GET | Invalid user/post | Negative 404 validation |
| POST | Create post | 201 + response fields |
| POST | Empty request body | Negative validation |
| PUT | Update complete post | 200 + updated fields |
| PATCH | Update selected field | 200 + updated field |
| DELETE | Delete post | Successful response |
| GET/POST | Response validation | JSON, headers, response time |

### Test Scenarios

The project contains **25+ documented test scenarios**, including:

- Valid API requests
- Invalid resource IDs
- Non-numeric IDs
- Empty request body
- Missing required fields
- CRUD operations
- Status-code validation
- Response-time validation
- Content-Type validation
- Required JSON field validation
- Array response validation
- Environment variable validation
- Collection Runner execution
- Reporting and execution evidence

---

## ✅ Postman Assertions

Example JavaScript assertions used in the collection:

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

These assertions help validate both the **HTTP response** and the **actual response content** instead of checking only whether an API request returned successfully.

---

## 🌍 Environment Variables

| Variable | Example |
|---|---|
| `baseUrl` | `https://jsonplaceholder.typicode.com` |
| `userId` | `1` |
| `postId` | `1` |

Environment variables make the collection easier to maintain and reuse across requests.

---

## 📋 Test Case Documentation

Test cases are documented with details such as:

- Test Case ID
- Module
- HTTP Method
- Endpoint
- Test Scenario
- Preconditions
- Expected Result
- Priority
- Test Type

Files:

- `TestCases/API_Test_Cases.csv`
- `TestCases/API_Test_Cases.xlsx`
- `TestCases/Test_Data.json`

---

## 📝 QA Documentation

The `Documentation/` folder contains supporting QA documents:

- `PROJECT_OVERVIEW.md` — project summary
- `INTERVIEW_READY_GUIDE.md` — interview explanation and questions
- `API_Testing_Test_Plan.md` — testing scope and approach
- `API_Testing_Checklist.md` — API testing checklist
- `API_Request_Reference.md` — endpoint reference
- `TEST_EXECUTION_GUIDE.md` — execution instructions
- `Defect_Report_Template.md` — defect reporting format

---

## 📸 Test Case Evidence

The `Screenshots/` folder contains a dedicated Postman-style visual for each documented test case from **TC001 to TC025**.

> **Transparency:** these visuals are illustrative portfolio mockups, not claimed as screenshots captured from a live Postman execution. After running the collection yourself, the mockups can be replaced with actual Postman execution screenshots.

### Featured Test Evidence

| Test Case | Evidence |
|---|---|
| TC001 — GET Valid User | ![TC001](Screenshots/TC001_GET_Valid_User.svg) |
| TC003 — GET Invalid User | ![TC003](Screenshots/TC003_GET_Invalid_User_404.svg) |
| TC008 — POST Create Post | ![TC008](Screenshots/TC008_POST_Create_Post.svg) |
| TC011 — PUT Update Post | ![TC011](Screenshots/TC011_PUT_Update_Post.svg) |
| TC013 — PATCH Update | ![TC013](Screenshots/TC013_PATCH_Update_Title.svg) |
| TC015 — DELETE Post | ![TC015](Screenshots/TC015_DELETE_Post.svg) |
| TC024 — Collection Run | ![TC024](Screenshots/TC024_Collection_Run.svg) |

---

## ▶️ How to Run the Project

### Run with Postman

1. Clone or download this repository.
2. Open Postman.
3. Import `Postman/API_Testing_Collection_v2.json`.
4. Import `Postman/QA_Environment.json`.
5. Select the `QA-JSONPlaceholder-Environment` environment.
6. Run individual requests or execute the complete collection using Collection Runner.
7. Review the response and **Test Results**.

### Run with Newman

Install dependencies:

```bash
npm install
```

Run the API test collection:

```bash
npm test
```

---

## 🔄 GitHub Actions CI

The project includes a GitHub Actions workflow at:

```text
.github/workflows/api-tests.yml
```

It is configured to execute the Postman collection using **Newman** as part of CI-based API regression testing.

This demonstrates how API tests can be integrated into a basic CI workflow instead of being executed only manually.

---

## 📁 Repository Structure

```text
REST-API-Testing-Postman/
│
├── .github/
│   └── workflows/
│       └── api-tests.yml
│
├── Documentation/
│   ├── PROJECT_OVERVIEW.md
│   ├── INTERVIEW_READY_GUIDE.md
│   ├── API_Testing_Test_Plan.md
│   ├── API_Testing_Checklist.md
│   ├── API_Request_Reference.md
│   ├── TEST_EXECUTION_GUIDE.md
│   └── Defect_Report_Template.md
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
│   ├── TC001_*.svg
│   ├── TC002_*.svg
│   ├── ...
│   └── TC025_*.svg
│
├── .gitignore
├── package.json
└── README.md
```

---

## 💡 Key QA Skills Demonstrated

This project supports my profile as an entry-level **Software Tester / QA Engineer** by demonstrating:

- Manual test-case design
- Functional API testing
- Positive and negative testing
- REST API fundamentals
- CRUD testing
- HTTP status-code validation
- JSON response validation
- Header validation
- Response-time validation
- JavaScript assertions
- Test data and environment variables
- Test documentation
- Defect reporting approach
- Newman command-line execution
- GitHub Actions CI
- Git and GitHub

---

## 🎤 Interview Explanation

> “I created a REST API testing project using Postman to demonstrate my practical QA skills. I used the JSONPlaceholder REST API and covered GET, POST, PUT, PATCH and DELETE operations. I designed more than 25 positive and negative test scenarios and added JavaScript assertions to validate status codes, JSON response fields, headers and response time. I also used environment variables for reusable configuration, documented my test cases and prepared the collection for Newman execution and GitHub Actions CI. This project helped me strengthen my understanding of API testing and QA processes.”

---

## ❓ Interview Questions I Prepared

**What is API testing?**  
Testing an API directly by validating requests, responses, business rules, status codes, data and error handling without depending on the UI.

**Why did you use Postman?**  
Postman provides an easy way to create, organize and execute API requests and supports JavaScript-based test assertions.

**What is the difference between PUT and PATCH?**  
PUT is generally used for a complete resource update, while PATCH is used for a partial update.

**Why Newman?**  
Newman allows Postman collections to run from the command line, which makes them useful for automation and CI pipelines.

**Why GitHub Actions?**  
It demonstrates how API regression tests can be executed automatically as part of a CI workflow.

**What do you do when an API test fails?**  
I check the request method, URL, parameters, headers and body, then inspect the response status, headers and body. I compare the actual result with the expected result, reproduce the issue and document the defect with clear steps and evidence when required.

---

## 👩‍💻 Keerthi Kandula

**Software Tester | QA Engineer**

- 🎓 MCA — KL University, 2023–2025
- 💻 Manual Testing • Automation Testing • Selenium • Python • SQL • Postman • REST APIs • PyTest
- 🔧 Git • GitHub • STLC • SDLC • Agile Scrum
- 📌 Open to Software Tester / QA Engineer opportunities

### Connect with Me

- **GitHub:** https://github.com/keerthikandula02
- **LinkedIn:** https://linkedin.com/in/keerthi-kandula-13b661254
- **Email:** keerthikandula12@gmail.com

---

⭐ If you are reviewing this repository as part of my portfolio, this project represents my practical learning and hands-on approach to **API Testing and Quality Assurance**.
