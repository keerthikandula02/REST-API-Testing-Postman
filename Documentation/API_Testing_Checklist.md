# API Testing Checklist

## Request Validation
- [ ] HTTP method is correct
- [ ] Endpoint URL is correct
- [ ] Path/query parameters are valid
- [ ] Required headers are present
- [ ] Request body uses valid JSON

## Response Validation
- [ ] Status code is correct
- [ ] Response body is valid JSON
- [ ] Required fields are present
- [ ] Field values/types are correct
- [ ] Response headers are appropriate
- [ ] Response time is acceptable

## Functional Scenarios
- [ ] Positive scenarios
- [ ] Negative scenarios
- [ ] Boundary/invalid input scenarios
- [ ] CRUD operations where applicable

## Regression
- [ ] Collection Runner executed
- [ ] Failed tests reviewed
- [ ] Defects documented
- [ ] Newman execution reviewed
- [ ] GitHub Actions workflow checked

## Evidence
- [ ] Actual Postman screenshots captured
- [ ] Execution report updated
- [ ] README reflects the real project state
