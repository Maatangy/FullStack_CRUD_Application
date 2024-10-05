# Full Stack CRUD Application with Spring Boot, Maven, and React

## Overview

This project is a full-stack CRUD (Create, Read, Update, Delete) application built using Spring Boot for the backend and React for the frontend. The backend provides RESTful APIs for managing `Course` resources, while the frontend allows users to interact with the system via a web interface.

### Backend
The backend is a Spring Boot application that exposes CRUD operations on `Course` objects through RESTful services. It uses Maven as a build tool and is configured to interact with a frontend via CORS.

### Frontend
The frontend is built with React, providing a user-friendly interface to interact with the courses. Users can add, update, delete, and view courses.

---

## Technologies Used

### Backend (Spring Boot):
- Spring Boot
- Spring MVC (RESTful services)
- Maven
- CORS Configuration for Frontend interaction
- Java 17

### Frontend (React):
- React (with Hooks)
- Axios for API calls
- HTML/CSS for UI design
- Node.js and npm for package management

---

## Features

### Backend Features:
- CRUD operations for `Course` resources
- RESTful API endpoints:
  - **GET** `/instructors/{username}/courses`: Fetch all courses for a given instructor.
  - **GET** `/instructors/{username}/courses/{id}`: Fetch a single course by ID.
  - **POST** `/instructors/{username}/courses`: Create a new course.
  - **PUT** `/instructors/{username}/courses/{id}`: Update an existing course.
  - **DELETE** `/instructors/{username}/courses/{id}`: Delete a course by ID.
- CORS support for cross-origin requests from frontend.

### Frontend Features:
- Fetch and display all courses.
- Add a new course.
- Update an existing course.
- Delete a course.
- Form validation for course creation and updates.
  
---

## Project Structure

### Backend (Spring Boot) Folder Structure:
```
src
├── main
│   ├── java
│   │   └── com.in28minutes.fullstack.springboot.maven.crud.springbootcrudfullstackwithmaven.course
│   │        ├── Course.java          # Entity class representing Course
│   │        ├── CourseResource.java   # REST Controller handling requests
│   │        ├── CoursesHardcodedService.java   # Service class with hardcoded data
│   └── resources
│        ├── application.properties    # Spring Boot configuration
```

### Frontend (React) Folder Structure:
```
src
├── components
│   ├── CourseList.js   # Displays list of courses
│   ├── CourseForm.js   # Form for creating/updating courses
│   ├── Course.js       # Component to show individual course details
├── App.js              # Main application file
├── index.js            # Entry point
└── api
    └── CourseService.js  # Axios API calls for CRUD operations
```

---

## API Endpoints

### GET All Courses:
```http
GET /instructors/{username}/courses
```

### GET Single Course by ID:
```http
GET /instructors/{username}/courses/{id}
```

### POST Create New Course:
```http
POST /instructors/{username}/courses
```

### PUT Update Course:
```http
PUT /instructors/{username}/courses/{id}
```

### DELETE Course by ID:
```http
DELETE /instructors/{username}/courses/{id}
```

---

## Running the Application

### Backend Setup (Spring Boot):
1. Clone the repository.
2. Open the backend project in your favorite IDE.
3. Run the Spring Boot application using the command:
   ```bash
   mvn spring-boot:run
   ```
4. The backend will be available at `http://localhost:8080`.

### Frontend Setup (React):
1. Navigate to the `frontend` directory.
2. Install the dependencies:
   ```bash
   npm install
   ```
3. Start the React development server:
   ```bash
   npm start
   ```
4. The frontend will be available at `http://localhost:3000`.

---

## Example Usage

1. **View All Courses**:
   - Visit `http://localhost:3000` to see all courses.

2. **Add a Course**:
   - Use the "Add Course" button in the frontend, fill in the course details, and click submit.

3. **Edit a Course**:
   - Click the "Edit" button next to a course, modify the fields, and save the changes.

4. **Delete a Course**:
   - Click the "Delete" button next to a course to remove it from the list.

---

## CORS Configuration

CORS is enabled to allow the React frontend to communicate with the Spring Boot backend. The configuration allows requests from `http://localhost:3000` (React) and `http://localhost:4200` (Angular, if needed).

---

## Authors and Contributions

This project was developed by the following contributors:
  - [Maatangy](https://github.com/Maatangy/)
  - [Bruhathi](https://github.com/bruhathisp/)
