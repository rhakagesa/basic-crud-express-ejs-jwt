# Basic CRUD Todos Web App.

Basic CRUD with NodeJS, ExpressJS, EJS and PostgreSQL. Using authentication and authorization to manage tasks and users.

## Features

- User authentication and authorization
- CRUD operations for todos
- Task completion status

## Getting Started

1. Clone the repository
2. Install dependencies with `npm install`
3. Start the server with `npm start`


## Routes
# Auth Route
This file contains the routes for user authentication:

- `GET /login`: Renders the login page.
- `POST /login`: Handles the login POST request and authenticates the user.
- `GET /register`: Renders the registration page.
- `POST /register`: Handles the registration POST request and creates a new user.
- `GET /logout`: Logs out the user and redirects to the login page.

# Task Route
- `GET /create`: Renders the `createTask` view for creating a new task.
- `POST /create`: Creates a new task using the `TaskController.createTask` handler.
- `GET /`: Retrieves all tasks using the `TaskController.getAllTasks` handler.
- `GET /mytask`: Retrieves the tasks created by the authenticated user using the `TaskController.getMyTask` handler.
- `POST /update/:id`: Updates a task with the specified ID using the `TaskController.updateTask` handler. Requires authentication and authorization.
- `GET /delete/:id`: Deletes a task with the specified ID using the `TaskController.deleteTask` handler. Requires authentication and authorization.

# User Route
- `GET /user :Retrieves all users. Requires authentication.
- `GET /user/info : Retrieves information about a specific user. Requires authentication.
- `POST /user/update/:id : Updates a user. Requires authentication and user authorization.
- `GET /user/delete/:id : Deletes a user. Requires authentication and user authorization.

## Middleware

This file uses the following middleware:

- `authentication`: Ensures that the user is authenticated before allowing access to the routes.
- `userAuthorization`: Ensures that the user is authorized to perform the requested action before allowing it.

The routes are protected by the `authentication` middleware, which ensures that only authenticated users can access certain routes.
