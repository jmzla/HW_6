# Campus Task Board API

## Project Description
This project is a Spring Boot REST API for managing tasks in a campus task board. It supports creating, retrieving, updating, and deleting tasks (CRUD operations). The application also includes validation to ensure that task data meets required constraints.

## Technologies Used
- Java 17+
- Spring Boot
- Maven
- Lombok
- Postman (for testing)

## How to Run the Application

1. Clone the repository:
   ```bash
   git clone <(https://github.com/jmzla/HW_5.git)>
2. Open the project in your IDE
3. Make sure Java 17 or newer is installed
4. Run the application:
Right-click CampusTaskboardApplication.java
Click Run
5. The application will start at:
 http://localhost:8080

API Endpoints
GET /api/tasks

Returns all tasks.

GET /api/tasks/{id}

Returns a task by ID.

POST /api/tasks

Creates a new task.

Example request:
{
"title": "Complete Homework 5",
"description": "Finish Spring Boot API assignment",
"completed": false,
"priority": "HIGH"
}

PUT /api/tasks/{id}

Updates an existing task.

DELETE /api/tasks/{id}

Deletes a task.

Validation
Title must not be blank
Title must be between 3 and 100 characters
Description must not exceed 500 characters

Example validation error response:
{
"title": "Title must be between 3 and 100 characters",
"description": "Description cannot exceed 500 characters"
}





Video LINK :
https://youtu.be/k67clEQrc0Q
