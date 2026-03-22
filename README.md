# Task Manager REST API

A RESTful API built with Java and Spring Boot for managing tasks.
Supports full CRUD operations with PostgreSQL as the database.

## Tech Stack

- Java 21
- Spring Boot
- Spring Data JPA
- PostgreSQL
- Maven

## Getting Started

### Prerequisites
- Java 21
- PostgreSQL
- Maven

### Database Setup
1. Create a PostgreSQL database named `task_manager`
2. Update `src/main/resources/application.properties` with your credentials:
```
spring.datasource.url=jdbc:postgresql://localhost:5432/task_manager
spring.datasource.username=your_username
spring.datasource.password=your_password
```

### Running the App
```
./mvnw spring-boot:run
```
The API will start at `http://localhost:8080`

## API Endpoints

### Get all tasks
```
GET /api/tasks
```

### Get task by ID
```
GET /api/tasks/{id}
```

### Get tasks by status
```
GET /api/tasks/status/{status}
```
Status options: `TODO` `IN_PROGRESS` `DONE`

### Create a task
```
POST /api/tasks
Content-Type: application/json

{
    "title": "My task",
    "description": "Task description",
    "status": "TODO",
    "dueDate": "2026-04-01"
}
```

### Update a task
```
PUT /api/tasks/{id}
Content-Type: application/json

{
    "title": "Updated title",
    "description": "Updated description",
    "status": "IN_PROGRESS",
    "dueDate": "2026-04-01"
}
```

### Delete a task
```
DELETE /api/tasks/{id}
```

## Author
Johnathan Savoy  
[linkedin.com/in/john-savoy](https://linkedin.com/in/john-savoy)