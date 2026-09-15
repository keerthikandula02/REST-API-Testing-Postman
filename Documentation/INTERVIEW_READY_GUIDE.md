# Interview-Ready Guide

## What is this project?
A portfolio REST API testing project using Postman and the public JSONPlaceholder API. It demonstrates functional testing, negative testing, JavaScript assertions, test documentation, Newman execution and GitHub Actions CI.

## What did I test?
- GET valid and invalid users
- GET posts
- POST create post
- PUT full update
- PATCH partial update
- DELETE resource
- Status codes, JSON fields, response type and response time
- Positive and negative scenarios

## How did I automate validation?
Postman JavaScript tests validate status codes, response fields, response type and response time.

```javascript
pm.test("Status code is 200", () => {
    pm.response.to.have.status(200);
});

pm.test("Response time is below 1000ms", () => {
    pm.expect(pm.response.responseTime).to.be.below(1000);
});
```

## Why variables?
`baseUrl`, `userId` and `postId` make requests reusable and reduce hard-coded values.

## Why Newman?
Newman runs Postman collections from the command line, making them suitable for automation and CI.

## Why GitHub Actions?
It runs the API regression suite automatically on repository changes and supports manual execution.

## 60-second interview answer
> I created a REST API testing project using Postman on the JSONPlaceholder API. I covered GET, POST, PUT, PATCH and DELETE operations with positive and negative scenarios. I added JavaScript assertions for status codes, response fields, response type and response time. I used environment variables for reusable configuration and documented more than 25 test scenarios. I also configured Newman for command-line execution and GitHub Actions for API regression in CI.

## Disclaimer
This is a learning and portfolio project. JSONPlaceholder is a public fake API and the project does not claim production testing experience for a real company. Actual execution screenshots should be captured after running the collection.