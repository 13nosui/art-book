# API Documentation

## Overview

This document provides comprehensive documentation for the API endpoints available in the AI Development Template. The API is built using Next.js API routes and follows RESTful principles.

## API Design Principles

The API follows these core design principles:

1. **RESTful Design** - Resource-oriented endpoints with standard HTTP methods
2. **JSON Format** - All requests and responses use JSON format
3. **Authentication** - Secure authentication using Firebase Auth tokens
4. **Validation** - Input validation using Zod schemas
5. **Error Handling** - Consistent error response format
6. **Rate Limiting** - Protection against abuse
7. **Documentation** - OpenAPI specification for all endpoints

## Base URL

The base URL for all API endpoints is:

```
https://your-app-domain.com/api
```

For local development:

```
http://localhost:3000/api
```

## Authentication

Most API endpoints require authentication. Authentication is handled using Firebase Authentication tokens.

### Authentication Header

Include the Firebase ID token in the Authorization header:

```
Authorization: Bearer <firebase-id-token>
```

### Obtaining a Token

1. Authenticate with Firebase Authentication
2. Get the ID token from the Firebase Auth user object
3. Include the token in the Authorization header

## Request Format

All requests should use JSON format for the request body:

```json
{
  "property1": "value1",
  "property2": "value2"
}
```

## Response Format

All responses follow a consistent format:

### Success Response

```json
{
  "success": true,
  "data": {
    // Response data
  }
}
```

### Error Response

```json
{
  "success": false,
  "error": {
    "code": "ERROR_CODE",
    "message": "Error message",
    "details": {
      // Additional error details (optional)
    }
  }
}
```

## API Endpoints

The API is organized into the following categories:

### Authentication

- `POST /api/auth/register` - Register a new user
- `POST /api/auth/login` - Login with email and password
- `POST /api/auth/logout` - Logout the current user
- `GET /api/auth/me` - Get the current user's profile

### Users

- `GET /api/users/:id` - Get a user's profile
- `PUT /api/users/:id` - Update a user's profile
- `DELETE /api/users/:id` - Delete a user

### Projects

- `GET /api/projects` - List all projects
- `POST /api/projects` - Create a new project
- `GET /api/projects/:id` - Get a project
- `PUT /api/projects/:id` - Update a project
- `DELETE /api/projects/:id` - Delete a project

### Files

- `GET /api/files` - List all files
- `POST /api/files` - Upload a new file
- `GET /api/files/:id` - Get a file
- `DELETE /api/files/:id` - Delete a file

### AI Services

- `POST /api/ai/analyze` - Analyze content with AI
- `POST /api/ai/generate` - Generate content with AI
- `POST /api/ai/translate` - Translate content with AI

## Rate Limiting

API endpoints are rate-limited to prevent abuse. Rate limits are applied per user and per IP address.

Default rate limits:

- 100 requests per minute per user
- 50 requests per minute per IP address

Rate limit headers are included in all responses:

```
X-RateLimit-Limit: 100
X-RateLimit-Remaining: 99
X-RateLimit-Reset: 1619194800
```

## Error Codes

Common error codes:

- `AUTHENTICATION_REQUIRED` - Authentication is required
- `INVALID_TOKEN` - Invalid authentication token
- `PERMISSION_DENIED` - User does not have permission
- `RESOURCE_NOT_FOUND` - Requested resource not found
- `VALIDATION_ERROR` - Invalid request data
- `RATE_LIMIT_EXCEEDED` - Rate limit exceeded
- `INTERNAL_SERVER_ERROR` - Server error

## OpenAPI Specification

The complete API specification is available in OpenAPI format:

- [OpenAPI Specification](./openapi.yaml)

## API Versioning

API versioning is handled through the URL path:

```
/api/v1/resource
```

The current API version is v1.

## CORS

Cross-Origin Resource Sharing (CORS) is enabled for all API endpoints. The following origins are allowed:

- `https://your-app-domain.com`
- `http://localhost:3000` (development only)

## Additional Resources

- [Usage Examples](./usage-examples.md) - Examples of API usage
- [Error Handling](./error-handling.md) - Detailed error handling documentation
- [Security & Rate Limiting](./security-and-rate-limiting.md) - Security and rate limiting details
