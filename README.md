# Student Management System

A backend application for managing students, courses, and user authentication using NestJS, TypeORM, and PostgreSQL.

## Table of Contents

- [Features](#features)
- [Technologies Used](#technologies-used)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Running the Application](#running-the-application)
- [Project Structure](#project-structure)
- [API Endpoints](#api-endpoints)
- [Contributing](#contributing)
- [License](#license)

## Features

- **Student Management**: Add, update, delete, and retrieve student records.
- **Course Management**: Manage courses and enroll students in courses.
- **User Authentication**: Secure login and signup using JWT.
- **Role-Based Access Control**: Restrict access to certain API endpoints based on user roles (admin, user).

## Technologies Used

- **NestJS**: A progressive Node.js framework for building efficient and scalable server-side applications.
- **TypeORM**: An ORM that can run in NodeJS, browsers, and supports TypeScript.
- **PostgreSQL**: An open-source relational database management system.
- **Docker**: Containerization platform for easy deployment and management.

## Getting Started

### Prerequisites

- Node.js v14 or later
- Docker and Docker Compose
- PostgreSQL

### Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/ibrahimabdalrhman/student-management.git
    cd student-management
    ```

2. Install dependencies:

    ```bash
    npm install
    ```

3. Set up environment variables by creating a `.env` file at the root of the project with the following content:

    ```bash
    PG_HOST=localhost
    PG_PORT=5432
    PG_USERNAME=your_pg_username
    PG_PASSWORD=your_pg_password
    PG_DATABASE=student_management
    JWT_SECRET=your_secret_key
    ```

4. Start the PostgreSQL database using Docker Compose:

    ```bash
    docker-compose up -d
    ```

### Running the Application

1. Start the NestJS server in development mode:

    ```bash
    npm run start:dev
    ```

2. The application will be available at `http://localhost:3000`.

## Project Structure


## API Endpoints

### Authentication

- **POST** `/auth/login`: Authenticate user and return JWT.
- **GET** `/auth/profile`: Get user profile (protected route).

### Students

- **GET** `/student`: Get all students.
- **GET** `/student/:id`: Get a student by ID.
- **POST** `/student`: Create a new student.
- **PATCH** `/student/:id`: Update a student by ID.
- **DELETE** `/student/:id`: Delete a student by ID.

### Courses

- **GET** `/course`: Get all courses.
- **GET** `/course/:id`: Get a course by ID.
- **POST** `/course`: Create a new course.
- **PATCH** `/course/:id`: Update a course by ID.
- **DELETE** `/course/:id`: Delete a course by ID.

### Users

- **POST** `/user/signup`: Create a new user.
- **POST** `/user/login`: Log in a user.
- **GET** `/user`: Get all users.

## Contributing

Contributions are welcome! Please open an issue or submit a pull request.

## License

This project is licensed under the MIT License.
