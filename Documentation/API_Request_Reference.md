# 🔎 API Request Reference

## Base URL

`https://jsonplaceholder.typicode.com`

## Users

### GET valid user

```text
GET /users/{{userId}}
```

Expected: `200 OK`

Validate: `id`, `name`, `email`, response time.

### GET invalid user

```text
GET /users/99999
```

Expected: `404 Not Found`

## Posts

### GET all posts

```text
GET /posts
```

Expected: `200 OK` and JSON array.

### POST create post

```text
POST /posts
Content-Type: application/json
```

Body:

```json
{
  "title": "QA Automation Project",
  "body": "Postman API testing practice",
  "userId": 1
}
```

Expected: `201 Created`.

### PUT update post

```text
PUT /posts/{{postId}}
```

Expected: `200 OK` and updated fields.

### PATCH update title

```text
PATCH /posts/{{postId}}
```

Body:

```json
{
  "title": "Partially Updated"
}
```

Expected: `200 OK`.

### DELETE post

```text
DELETE /posts/{{postId}}
```

Expected: successful delete response.

## Test Design Reminder

For each endpoint, think in this order:

```text
Request
→ Status code
→ Headers
→ Response body
→ Required fields
→ Business validation
→ Negative scenarios
→ Regression execution
```
