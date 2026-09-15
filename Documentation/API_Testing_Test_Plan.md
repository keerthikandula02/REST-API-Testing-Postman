# API Testing Test Plan

## 1. Test Objective

Validate the functional behavior and response contracts of the JSONPlaceholder REST endpoints using Postman.

## 2. Scope

### In Scope
- GET user and post resources
- POST create-post scenario
- PUT full-update scenario
- PATCH partial-update scenario
- DELETE scenario
- HTTP status-code validation
- JSON response validation
- Required-field validation
- Response-time check
- Positive and negative scenarios
- Environment-variable usage
- Collection/regression execution

### Out of Scope
- Production security testing
- Load/stress testing
- Real database validation
- Authentication/authorization because the selected demo API does not require it

## 3. Test Approach

1. Prepare endpoint and request data.
2. Execute positive and negative scenarios.
3. Validate HTTP status codes.
4. Validate JSON response structure and important fields.
5. Validate response time for representative requests.
6. Execute the collection as a regression suite.
7. Record failures and investigate request/response details.

## 4. Entry Criteria

- Postman/Newman is available.
- Internet access is available.
- Collection and environment files are imported correctly.
- JSONPlaceholder endpoint is reachable.

## 5. Exit Criteria

- All planned test cases have been executed.
- Critical functional scenarios pass.
- Failed tests are reviewed and documented.
- Regression collection completes successfully.

## 6. Defect Considerations

For a failed test, capture:
- Test case ID
- Endpoint and HTTP method
- Request headers/body
- Expected result
- Actual result
- HTTP status code
- Response body
- Reproduction steps

## 7. Risks / Limitations

JSONPlaceholder is a public demo API. Its behavior is not equivalent to a production business application, and its write operations are simulated rather than persistent production transactions.

## 8. Deliverables

- Postman collection
- Postman environment
- Test-case spreadsheet/CSV
- README documentation
- Newman execution configuration
- GitHub Actions workflow
