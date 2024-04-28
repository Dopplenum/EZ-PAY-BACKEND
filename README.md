# EZ PAY BACKEND

This is the backend application for a payment system. It provides APIs for user authentication, account management, and fund transfers.
Full backend features with authentication and follows ACID properties.

## Features

- User signup and signin functionality with JWT authentication.
- Retrieval of account balance.
- Transfer funds between accounts.

## Technologies Used

- **Node.js**: A JavaScript runtime environment.
- **Express.js**: A web application framework for Node.js.
- **MongoDB**: A NoSQL database used for storing user and account data.
- **Mongoose**: An ODM (Object Data Modeling) library for MongoDB and Node.js.
- **jsonwebtoken (JWT)**: For user authentication and authorization.
- **Zod**: For schema validation of request data.

## Getting Started

## Install dependencies:

```bash
cd backend-payment-app
npm install
```

Configure environment variables:
Create a .env file in the root directory and add the following variables:
PORT=3000
MONGODB_URI=<mongodb-uri>
JWT_SECRET=<jwt-secret>

Replace <mongodb-uri> and <jwt-secret> with your MongoDB connection string and JWT secret key respectively.

Start the server:
npm start

## API Endpoints

### Authentication

- **POST /api/v1/user/signup**: Create a new user account.
  - **Request body**: `{ "username": "", "password": "", "firstname": "", "lastname": "" }`
  - **Response**: `{ "message": "User created successfully", "token": "" }`

- **POST /api/v1/user/signin**: Sign in to an existing user account.
  - **Request body**: `{ "username": "", "password": "" }`
  - **Response**: `{ "token": "" }`

### Account Management

- **GET /api/v1/account/balance**: Get the account balance.
  - **Requires authentication** (JWT token in header).

### Funds Transfer

- **POST /api/v1/account/transfer**: Transfer funds to another account.
  - **Request body**: `{ "amount": , "to": "" }`
  - **Requires authentication** (JWT token in header).


