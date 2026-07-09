# DevPilot AI – REST API Design

---

# 1. API Overview

The backend follows RESTful architecture using Django REST Framework.

Base URL:

```
http://localhost:8000/api/v1/
```

Authentication:

JWT Bearer Token

Response Format:

JSON

---

# 2. Authentication APIs

## Register

POST /auth/register

Purpose:
Create a new user account.

---

## Login

POST /auth/login

Purpose:
Authenticate user and generate JWT token.

---

## Logout

POST /auth/logout

Purpose:
Logout authenticated user.

---

## Refresh Token

POST /auth/refresh

Purpose:
Generate new access token.

---

## User Profile

GET /auth/profile

Purpose:
Return logged in user profile.

---

# 3. Team APIs

GET /teams

POST /teams

PUT /teams/{id}

DELETE /teams/{id}

---

# 4. Project APIs

GET /projects

POST /projects

GET /projects/{id}

PUT /projects/{id}

DELETE /projects/{id}

---

# 5. Sprint APIs

GET /sprints

POST /sprints

PUT /sprints/{id}

DELETE /sprints/{id}

---

# 6. Task APIs

GET /tasks

POST /tasks

GET /tasks/{id}

PUT /tasks/{id}

DELETE /tasks/{id}

PATCH /tasks/status

PATCH /tasks/priority

---

# 7. Dashboard APIs

GET /dashboard

GET /dashboard/manager

GET /dashboard/admin

---

# 8. Analytics APIs

GET /analytics

GET /analytics/productivity

GET /analytics/workload

GET /analytics/sprint

GET /analytics/reports

---

# 9. AI APIs

POST /ai/chat

POST /ai/prioritize

POST /ai/report

POST /ai/sprint-prediction

POST /ai/productivity-insights

POST /ai/meeting-summary

POST /ai/code-review

POST /ai/bug-prediction

---

# 10. Resume APIs

POST /resume/generate

GET /resume

PUT /resume/update

DELETE /resume

---

# 11. Learning APIs

GET /learning/recommend

GET /learning/courses

GET /learning/roadmap

POST /learning/complete

---

# 12. Notification APIs

GET /notifications

PATCH /notifications/read

DELETE /notifications

---

# 13. Report APIs

GET /reports

POST /reports/generate

GET /reports/download

---

# 14. Integration APIs

POST /integrations/zoho

POST /integrations/github

POST /integrations/slack

POST /integrations/calendar

GET /integrations/status

---

# 15. Admin APIs

GET /users

POST /users

PUT /users/{id}

DELETE /users/{id}

GET /audit-logs

GET /system-health

---

# 16. Future APIs

POST /voice/chat

POST /ai/interview

POST /ai/career-coach

POST /ai/resource-planner

POST /ai/capacity-planner

POST /ai/release-prediction