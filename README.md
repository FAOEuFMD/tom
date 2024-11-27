# Project Title

**TOM**

## Table of Contents

- [Introduction](#introduction)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
  - [Backend](#backend)
  - [Frontend](#frontend)
- [Configuration](#configuration)
- [Running the Application](#running-the-application)
  - [Backend Running](#backend-running)
  - [Frontend Running](#frontend-running)
- [Running Tests](#running-tests)
  - [Backend Tests](#backend-tests)
  - [Frontend Tests](#frontend-tests)
- [Project Structure](#project-structure)
- [Contributing](#contributing)
- [License](#license)

## Introduction

This project is a full-stack application with a **backend** built using Node.js and TypeScript, and a **frontend** built using [Vue](https://vuejs.org/) with Vite. It includes authentication features and comprehensive testing using Jest.

## Prerequisites

Before you begin, ensure you have met the following requirements:

- **Node.js** (version 18 or higher)
- **npm**
- **Git**

## Installation

### Backend

1. **Navigate to the backend directory:**

   ```bash
   cd backend
   ```

2. **Install backend dependencies:**

   ```bash
   npm install
   ```

### Frontend

1. **Navigate to the frontend directory:**

   ```bash
   cd frontend
   ```

2. **Install frontend dependencies:**

   ```bash
   npm install
   ```

## Configuration

### Root Level

1. **Environment Variables:**

   The root `.env` file contains global configuration variables used by project-wide tools and services.

   ```env
   # Application settings
   APP_ENV=development
   APP_DEBUG=true
   APP_URL=http://localhost:8080
   NODE_ENV=test
   ```

   - **APP_ENV:** Defines the environment mode for global tools.
   - **APP_DEBUG:** Enables or disables debug mode for global services.
   - **APP_URL:** Base URL for the application.
   - **NODE_ENV:** Sets the Node environment; ensure it does not conflict with backend/frontend settings.

### Backend

1. **Environment Variables:**

   Create a `.env` file in the `backend` directory with the following variables:

   ```env
   PORT=3000
   DATABASE_URL=your_database_url
   JWT_SECRET=your_jwt_secret
   ```

   - **PORT:** The port on which the backend server will run.
   - **DATABASE_URL:** Connection string for your database.
   - **JWT_SECRET:** Secret key for JWT authentication.

2. **Database Setup:**

   Ensure your database is set up and the `DATABASE_URL` in the `.env` file is correctly configured.

### Frontend

1. **Environment Variables:**

   Create a `.env` file in the `frontend` directory with the following variables:

   ```env
   VITE_API_URL=http://localhost:3000/api
   ```

   - **VITE_API_URL:** The base URL for the backend API.

## Running the Application

### Backend Running

1. **Start the backend server:**

   ```bash
   npm start
   ```

   The backend server will start on the port specified in the `.env` file (default is `3000`).

### Frontend Running

1. **Start the frontend development server:**

   ```bash
   npm run dev
   ```

   The frontend application will start on `http://localhost:5173` by default and communicate with the backend API.

## Running Tests

### Backend Tests

The backend uses **Jest** for testing.

1. **Navigate to the backend directory:**

   ```bash
   cd backend
   ```

2. **Run the tests:**

   ```bash
   npm test
   ```

   This will execute all tests located in the `backend` directory, including `server.test.ts`. The Node server will run on port 3000 by default, while the test server will run on port 3001.

### Frontend Tests

The frontend also uses **Jest** for testing.

1. **Navigate to the frontend directory:**

   ```bash
   cd frontend
   ```

2. **Run the tests:**

   ```bash
   npm test
   ```

   This will execute all frontend tests using Jest as the configured testing framework.

## Project Structure

- **backend/**: Contains the backend server code, routes, tests, and configuration files.
- **frontend/**: Contains the frontend application code and related files.
- **.gitignore**: Specifies files and directories to be ignored by Git.
- **README.md**: This documentation file.

## License

This project is licensed under the [MIT License](LICENSE).
