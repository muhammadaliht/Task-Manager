# Task Manager API Documentation

## Base URL
```
http://localhost:5000/api
```

## Authentication
### Register User
- **Endpoint:** `POST /auth/register`
- **Description:** Registers a new user.
- **Request Body:**
  ```json
  {
    "username": "exampleUser",
    "password": "securePassword"
  }
  ```
- **Response:**
  ```json
  {
    "message": "User registered successfully"
  }
  ```

### Login User
- **Endpoint:** `POST /auth/login`
- **Description:** Logs in an existing user and returns a JWT token.
- **Request Body:**
  ```json
  {
    "username": "exampleUser",
    "password": "securePassword"
  }
  ```
- **Response:**
  ```json
  {
    "token": "jwt-token"
  }
  ```

## Task Management
### Create Task
- **Endpoint:** `POST /tasks`
- **Description:** Creates a new task.
- **Headers:**
  ```json
  {
    "Authorization": "Bearer <token>"
  }
  ```
- **Request Body:**
  ```json
  {
    "title": "New Task",
    "description": "Task description"
  }
  ```
- **Response:**
  ```json
  {
    "_id": "taskId",
    "title": "New Task",
    "description": "Task description",
    "user": "userId"
  }
  ```

### Get All Tasks
- **Endpoint:** `GET /tasks`
- **Description:** Retrieves all tasks for the authenticated user.
- **Headers:**
  ```json
  {
    "Authorization": "Bearer <token>"
  }
  ```
- **Response:**
  ```json
  [
    {
      "_id": "taskId",
      "title": "Task 1",
      "description": "Task description",
      "user": "userId"
    }
  ]
  ```

### Get Task by ID
- **Endpoint:** `GET /tasks/:id`
- **Description:** Retrieves a specific task.

### Update Task
- **Endpoint:** `PUT /tasks/:id`
- **Description:** Updates an existing task.

### Delete Task
- **Endpoint:** `DELETE /tasks/:id`
- **Description:** Deletes a specific task.

## Error Handling
- `400` - Bad Request
- `401` - Unauthorized
- `404` - Not Found
- `500` - Server Error

## Author
- [Name](Ali Hassan)
- [GitHub](github.com/muhammadaliht/task-manager.git)
- [Email](muhammadali38906@gmail.com)
- [number](0312-6038906)
