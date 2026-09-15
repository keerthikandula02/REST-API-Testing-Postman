# 🧪 Test Execution Guide

## Before execution

1. Install Postman.
2. Import `Postman/API_Testing_Collection_v2.json`.
3. Import `Postman/QA_Environment.json`.
4. Select `QA-JSONPlaceholder-Environment`.
5. Confirm the `baseUrl` resolves correctly.

## Recommended execution order

1. GET valid user
2. GET invalid user
3. GET all posts
4. POST create post
5. PUT update post
6. PATCH update title
7. DELETE post
8. Run the complete collection with Collection Runner

## What to capture

For portfolio evidence, capture your own screenshots showing:

- Request method and URL
- Request body where applicable
- Response status
- Response body
- Postman Tests tab / passing assertions
- Collection Runner summary
- GitHub Actions successful workflow

## Important

Screenshots should come from your own execution. This keeps the portfolio honest and gives you real evidence to discuss in an interview.
