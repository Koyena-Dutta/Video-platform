# JS-BACKEND

A production-ready Node.js + Express + MongoDB REST API.

## 📁 Structure

```
src/
├── controllers/       # Route handler logic
│   └── user.controller.js
├── db/                # MongoDB connection
│   └── index.js
├── middlewares/       # Express middlewares
│   ├── auth.middleware.js
│   └── error.middleware.js
├── models/            # Mongoose schemas
│   └── user.model.js
├── routes/            # Express routers
│   └── user.routes.js
├── utils/             # Reusable utilities
│   ├── asyncHandler.js
│   ├── ApiError.js
│   └── ApiResponse.js
├── app.js             # Express app setup
├── constants.js       # App-wide constants
└── index.js           # Entry point
```

## 🚀 Getting Started

```bash
npm install
# Fill in your .env values
npm run dev
```

## 🔌 API Endpoints

| Method | Endpoint                  | Auth | Description       |
|--------|---------------------------|------|-------------------|
| POST   | /api/v1/users/register    | ❌   | Register user     |
| POST   | /api/v1/users/login       | ❌   | Login             |
| POST   | /api/v1/users/logout      | ✅   | Logout            |
| GET    | /api/v1/users/me          | ✅   | Get current user  |
| GET    | /health                   | ❌   | Health check      |

## 🔐 Auth

JWT-based with access + refresh tokens stored in HTTP-only cookies.
Pass token as `Authorization: Bearer <token>` or via cookies.

