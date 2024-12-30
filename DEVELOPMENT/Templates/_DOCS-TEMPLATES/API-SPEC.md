# [ PROJECT NAME ] - API Specification
*Version: 1.0.0*

## Base URL
```
Development: http://localhost:3000/api
Production:  https://api.example.com
```

## Authentication
```
Authorization: Bearer <token>
```

## Endpoints

### Auth
```
POST   /auth/login
POST   /auth/register
POST   /auth/refresh
DELETE /auth/logout
```

### Users
```
GET    /users
GET    /users/:id
POST   /users
PUT    /users/:id
DELETE /users/:id
```

### Resources
```
GET    /resources
GET    /resources/:id
POST   /resources
PUT    /resources/:id
DELETE /resources/:id
```

## Status Codes
- 200: Success
- 201: Created
- 400: Bad Request
- 401: Unauthorized
- 403: Forbidden
- 404: Not Found
- 500: Server Error

## Response Format
```json
{
  "success": true,
  "data": {},
  "error": null
}
```

## Error Format
```json
{
  "success": false,
  "data": null,
  "error": {
    "code": "ERROR_CODE",
    "message": "Error message"
  }
}