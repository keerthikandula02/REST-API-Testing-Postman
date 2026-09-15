# Postman Assets

## Files

- `API_Testing_Collection.json` — original Postman collection.
- `API_Testing_Collection_v2.json` — enhanced interview-ready collection with grouped requests and automated assertions.
- `QA_Environment.json` — reusable environment variables.

## Import

1. Open Postman.
2. Import the collection JSON.
3. Import the environment JSON.
4. Select `QA-JSONPlaceholder-Environment`.
5. Run requests individually or through Collection Runner.

## Variables

| Variable | Example value | Purpose |
|---|---|---|
| `baseUrl` | `https://jsonplaceholder.typicode.com` | API base URL |
| `userId` | `1` | User resource ID |
| `postId` | `1` | Post resource ID |

Keep environment-specific values in the environment file rather than hard-coding them into every request.
