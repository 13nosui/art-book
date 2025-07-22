# API Endpoints

## Overview

This document contains documentation for all REST API endpoints in the project.

**Total Endpoints:** 5

## Endpoints


### GET /figma/:fileId

**File:** `src/app/api/figma/[fileId]/route.ts`
**Handler:** GET handler



**Authentication Required:** Yes
**Validation:** Yes

**Middleware:** Validation, Security


**Example Request:**
```bash
curl -X GET \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer <token>" \
  http://localhost:3000/figma/:fileId
```

---

### POST /figma/:fileId

**File:** `src/app/api/figma/[fileId]/route.ts`
**Handler:** POST handler



**Authentication Required:** Yes
**Validation:** Yes

**Middleware:** Validation, Security


**Example Request:**
```bash
curl -X POST \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer <token>" \
  http://localhost:3000/figma/:fileId
```

---

### PUT /figma/:fileId

**File:** `src/app/api/figma/[fileId]/route.ts`
**Handler:** PUT handler



**Authentication Required:** Yes
**Validation:** Yes

**Middleware:** Validation, Security


**Example Request:**
```bash
curl -X PUT \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer <token>" \
  http://localhost:3000/figma/:fileId
```

---

### DELETE /figma/:fileId

**File:** `src/app/api/figma/[fileId]/route.ts`
**Handler:** DELETE handler



**Authentication Required:** Yes
**Validation:** Yes

**Middleware:** Validation, Security


**Example Request:**
```bash
curl -X DELETE \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer <token>" \
  http://localhost:3000/figma/:fileId
```

---

### PATCH /figma/:fileId

**File:** `src/app/api/figma/[fileId]/route.ts`
**Handler:** PATCH handler



**Authentication Required:** Yes
**Validation:** Yes

**Middleware:** Validation, Security


**Example Request:**
```bash
curl -X PATCH \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer <token>" \
  http://localhost:3000/figma/:fileId
```

