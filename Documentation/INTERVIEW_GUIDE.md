# 🎤 API Testing Interview Guide

Use this file to revise the project before an interview.

## 1. What is API testing?

API testing validates the behavior of an application's backend services by sending requests and checking responses without depending on the UI.

## 2. Why Postman?

Postman makes it easy to create requests, manage environments, inspect responses and write JavaScript assertions. It is also easy to run the same collection with Newman.

## 3. HTTP methods used in this project

| Method | Purpose | Project example |
|---|---|---|
| GET | Retrieve data | Get user / posts |
| POST | Create data | Create post |
| PUT | Replace/update a resource | Update post |
| PATCH | Partially update a resource | Update title |
| DELETE | Remove a resource | Delete post |

## 4. Important status codes

- `200 OK` — successful request
- `201 Created` — resource created
- `400 Bad Request` — invalid request format/data
- `401 Unauthorized` — authentication required/failed
- `403 Forbidden` — request understood but not allowed
- `404 Not Found` — resource not found
- `500 Internal Server Error` — server-side failure

## 5. What did you validate?

- Status codes
- Response body
- Required JSON fields
- Response time
- Request headers
- Request payload
- Positive scenarios
- Negative scenarios

## 6. What is an assertion?

An assertion is an automated check that compares the actual result with the expected result.

Example:

```javascript
pm.test("Status code is 200", () => {
    pm.response.to.have.status(200);
});
```

## 7. Why environment variables?

Variables such as `baseUrl`, `userId` and `postId` prevent repeated hard-coded values and make requests reusable.

## 8. What is Newman?

Newman is the command-line runner for Postman collections. It allows API tests to run outside the Postman GUI and can be integrated into CI/CD pipelines.

## 9. Why GitHub Actions?

GitHub Actions can automatically execute the API collection when code changes are pushed or a pull request is opened. This gives repeatable regression feedback.

## 10. How to explain the project

> “I created a REST API testing portfolio project using Postman and JSONPlaceholder. I covered CRUD operations with GET, POST, PUT, PATCH and DELETE, added JavaScript assertions for status codes, response fields and response time, documented positive and negative scenarios, and configured Newman with GitHub Actions for repeatable CI execution.”

## 11. Honest project statement

This repository is a learning/portfolio project. JSONPlaceholder is a public demo API and does not represent a real production system. Do not claim production experience based on this project.
