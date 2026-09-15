# 📘 Project Overview — Quick Read

## What is this project?

A QA portfolio project that demonstrates REST API testing using Postman. The project covers API requests, automated assertions, test-case design, negative testing, regression execution and CI integration.

## Application used

JSONPlaceholder public demo API.

## Main flow

```text
Requirement
  ↓
Test Scenarios
  ↓
Postman Request
  ↓
API Response
  ↓
Assertions
  ↓
Pass / Fail
  ↓
Collection Runner
  ↓
Newman
  ↓
GitHub Actions
```

## What an interviewer can review

1. `Postman/API_Testing_Collection_v2.json` — executable collection.
2. `Postman/QA_Environment.json` — reusable variables.
3. `TestCases/API_Test_Cases.xlsx` — planned scenarios.
4. `Documentation/API_Testing_Test_Plan.md` — test strategy.
5. `Documentation/API_Request_Reference.md` — endpoint reference.
6. `Documentation/INTERVIEW_GUIDE.md` — concepts to explain.
7. `.github/workflows/api-tests.yml` — CI execution.

## One-minute explanation

“I created this project to practice the complete API QA workflow. I designed CRUD requests in Postman, added JavaScript assertions, covered positive and negative scenarios, documented test cases, and configured Newman with GitHub Actions so the collection can be executed repeatedly in CI. I used JSONPlaceholder as a public demo API, so this is a portfolio project rather than production experience.”
