# Microservice Development Exercises

## Introduction
Welcome to the **Microservice Development Exercises**! This repository provides hands-on exercises that will help you learn essential web development concepts, including TypeScript, REST API design, real-time communication with Socket.IO, database interaction, authentication, and microservice communication.

## Prerequisites
Before starting these exercises, make sure you have the following installed:

- [Node.js](https://nodejs.org/) (v14.x or above)
- [TypeScript](https://www.typescriptlang.org/) (v4.x or above)
- [PostgreSQL](https://www.postgresql.org/) (or SQLite for simpler setup)
- [Visual Studio Code](https://code.visualstudio.com/) (optional but recommended)

## Getting Started

Clone the repository:
```bash
git clone https://github.com/yourusername/microservice-exercises.git
cd microservice-exercises
```

# Exercises

## 🧩 Exercise 1: Basic TypeScript REST API

**Goal:**  
Build a simple REST API with TypeScript and Express.

**Tasks:**
- Set up a TypeScript project using `ts-node` or `tsup`.
- Create a server with one endpoint: `GET /hello` returns `{"message": "Hello, World"}`.
- Add an endpoint `POST /echo` that returns the same JSON body it received.
- Validate body input using a library like `zod` or `class-validator`.

**Skills Gained:**
- TypeScript syntax
- Express basics
- HTTP routes
- Input validation

**Files to Check:**
- `src/server.ts`
- `src/routes/hello.ts`

---

## 🗃️ Exercise 2: CRUD API with SQLite

**Goal:**  
Create a mini CRUD system using TypeORM or Prisma.

**Tasks:**
- Define a `User` model with `id`, `name`, `email`, and `createdAt`.
- Implement the following endpoints:
  - `POST /users` – create user
  - `GET /users` – list users
  - `GET /users/:id` – get by ID
  - `PUT /users/:id` – update user
  - `DELETE /users/:id` – delete user
- Store data in SQLite for quick testing.

**Skills Gained:**
- DB modeling
- ORM usage
- CRUD logic

**Files to Check:**
- `src/models/User.ts`
- `src/routes/user.ts`

---

## 🔐 Exercise 3: JWT-based Auth System

**Goal:**  
Implement a login and signup system using JWT.

**Tasks:**
- Create `POST /signup` and `POST /login` routes.
- Hash passwords using `bcrypt`.
- Issue JWTs using `jsonwebtoken`.
- Secure a route `GET /me` that returns the current user if the JWT is valid.

**Skills Gained:**
- Authentication flow
- Secure password handling
- Middleware

**Files to Check:**
- `src/auth/authController.ts`
- `src/auth/jwt.ts`

---

## 🔁 Exercise 4: Build a Simple Friend Request System

**Goal:**  
Simulate part of the Connection Management Service.

**Tasks:**
- Create endpoints:
  - `POST /connections/request`
  - `POST /connections/accept`
  - `GET /connections/:userId`
- Store pending and accepted requests.
- Prevent duplicates and self-connections.

**Skills Gained:**
- Relational modeling
- Business logic
- Testing edge cases

**Files to Check:**
- `src/models/Connection.ts`
- `src/routes/connections.ts`

---

## ⚡ Exercise 5: Real-Time Chat using Socket.IO

**Goal:**  
Build a mini WebSocket chat server.

**Tasks:**
- Two clients connect with usernames.
- Send messages via Socket.IO.
- Broadcast messages to others.
- Optionally, show online users.

**Skills Gained:**
- WebSocket basics
- Socket.IO events
- Client-server interaction

**Files to Check:**
- `src/socket/chatServer.ts`
- `src/socket/socketController.ts`

---

## 🧪 Bonus: Write Basic Tests

**Goal:**  
Add testing to any of the above services.

**Tasks:**
- Set up `jest` or `vitest`.
- Write a unit test for one controller/service.
- Write an integration test for a POST/GET route.

**Skills Gained:**
- Test writing
- Mocking
- Reliability

**Files to Check:**
- `src/tests/`
  - `user.test.ts`
  - `auth.test.ts`

## 📁 Folder Structure

```bash
/microservice-exercises
  /src
    /models
      User.ts
      Connection.ts
    /routes
      hello.ts
      user.ts
      connections.ts
    /auth
      authController.ts
      jwt.ts
    /socket
      chatServer.ts
      socketController.ts
    /tests
      user.test.ts
      auth.test.ts
  /package.json
  /tsconfig.json
  /README.md
