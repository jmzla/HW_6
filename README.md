# TaskBoard API — Homework 6 (Spring Data JPA)

## 📌 Project Description

This project is a RESTful API built with Spring Boot that manages tasks.
In Homework 6, the application was upgraded to use **Spring Data JPA** with an **H2 in-memory database**, allowing tasks to be stored and queried using a real database instead of an ArrayList.

The API supports CRUD operations, filtering, searching, and pagination.

---

## ⚙️ Technologies Used

* Java
* Spring Boot
* Spring Data JPA
* H2 Database
* Maven
* Lombok

---

## ▶️ How to Run the Project

1. Clone the repository:

```
git clone https://github.com/jmzla/HW_6.git
```

2. Open in IntelliJ

3. Run the main application class

4. The server will start at:

```
http://localhost:8080
```

---

## 🗄️ H2 Database Console

Access the H2 console:

```
http://localhost:8080/h2-console
```

### Connection Settings:

* JDBC URL: `jdbc:h2:mem:taskboarddb`
* Username: `sa`
* Password: (leave empty)

---

## 📡 API Endpoints

### 🔹 Get All Tasks

```
GET /api/tasks
```

---

### 🔹 Create Task

```
POST /api/tasks
```

Example Body:

```json
{
  "title": "Finish Homework",
  "description": "Complete JPA assignment",
  "completed": false,
  "priority": "HIGH"
}
```

---

### 🔹 Get Completed Tasks

```
GET /api/tasks/completed
```

---

### 🔹 Get Incomplete Tasks

```
GET /api/tasks/incomplete
```

---

### 🔹 Filter by Priority

```
GET /api/tasks/priority/{priority}
```

Example:

```
GET /api/tasks/priority/HIGH
```

---

### 🔹 Search Tasks

```
GET /api/tasks/search?keyword=homework
```

---

### 🔹 Pagination & Sorting

```
GET /api/tasks/paginated?page=0&size=5&sortBy=title
```

---

## 📊 Pagination Response Example

```json
{
  "content": [
    { "id": 1, "title": "Task 1" },
    { "id": 2, "title": "Task 2" }
  ],
  "totalElements": 10,
  "totalPages": 2,
  "size": 5,
  "number": 0,
  "first": true,
  "last": false
}
```

---

## 🧠 Key Concepts Learned

* **JPA Entities**: Used `@Entity`, `@Id`, `@GeneratedValue`, and `@Column` to map Java objects to database tables.
* **Repositories**: Extended `JpaRepository` to get built-in CRUD operations.
* **Query Methods**: Used method naming conventions like `findByCompletedTrue()` to auto-generate SQL queries.
* **Custom Queries**: Implemented search using `@Query`.
* **Pagination**: Used `Page`, `Pageable`, and `PageRequest` for efficient data handling.

---

## 🎥 Video Explanation

(Insert your video link here)

---

## ⚠️ Notes

* H2 is an **in-memory database**, so data resets when the application stops.
* `spring.jpa.hibernate.ddl-auto=update` is used for automatic schema updates.
