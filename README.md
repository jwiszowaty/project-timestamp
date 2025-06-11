# 🕒 Timestamp Microservice

A Node.js and Express.js API that returns Unix and UTC timestamps for valid dates—or the current time when no date is provided. This project fulfills the FreeCodeCamp “Timestamp Microservice” project from the **APIs and Microservices** certification.

---

## 📚 Table of Contents

- [Features](#features)
- [API Endpoints](#api-endpoints)
- [Examples](#examples)
- [💻 Getting Started](#getting-started)
- [✅ Testing](#testing)
- [🛠️ Deployment](#deployment)
- [🐞 Error Handling](#error-handling)
- [🔗 License](#license)

---

## Features

- CORS enabled for cross-origin API testing.
- Serves a static `index.html` landing page.
- Handles URL date parameters in:
  - **ISO date strings** (e.g. `2015-12-25`)
  - **Unix timestamps in milliseconds** (e.g. `1451001600000`)
  - **No parameter**, returning current date/time.
- Validates dates; returns an error JSON if invalid.

---

## API Endpoints

| Method | Endpoint                    | Description                                   |
|--------|-----------------------------|-----------------------------------------------|
| GET    | `/`                         | Serves the project homepage (UI/demo).        |
| GET    | `/api`                      | Returns current time in JSON.                 |
| GET    | `/api/:date`                | Returns Unix & UTC timestamps for the date.   |

---

## Examples

- **Current timestamp**
  ```text
  GET /api
  ↓
  { "unix": 1625884358000, "utc": "Mon, 10 Jul 2021 18:32:38 GMT" }
