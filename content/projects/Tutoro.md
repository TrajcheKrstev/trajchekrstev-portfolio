+++
title = 'Tutoro: Connecting Students and Tutors'
draft = false
featured_image = "/images/tutoro.png"
summary = "**Tutoro** is a dynamic web application developed as part of a collaborative group project for the **Web Programming** course. The platform aims to connect students seeking tutoring in various subjects with qualified tutors offering their expertise."
+++

**Tutoro** is a dynamic web application developed as part of a collaborative group project for the **Web Programming** course. The platform aims to connect students seeking tutoring in various subjects with qualified tutors offering their expertise.

## Project Overview

### Key Features

- **User Roles**: Users can register as either students or tutors.
- **Tutor Profiles**: Tutors can create and manage profiles, adding courses they teach and setting their prices.
- **Reviews and Ratings**: Logged-in users can leave reviews and ratings for tutors.
- **Search and Filter**: Users can search and filter tutors based on name, language, price, location, and more.
- **Profile Management**: Users have the ability to edit or delete their profiles.

### Technical Stack

The application is built using the **MEAN** stack, ensuring a robust and scalable solution.

- **Frontend**: Developed with **Angular** and **TypeScript** to create a responsive and dynamic user interface.
- **Backend**: Implemented using **Express** and **Node.js**, providing a reliable and efficient server-side framework.
- **Database**: Utilized **MongoDB** for its flexibility and scalability in handling data.

### RESTful API Implementation

In this project, we implemented a RESTful API to handle various functionalities such as user authentication, profile management, course management, and reviews. Here are the key aspects of our RESTful API:

- **HTTP Methods**: We used standard HTTP methods (GET, POST, PUT, DELETE) for different operations. For example, `GET /students` to retrieve all students, `POST /students` to create a new student, `PUT /students/:studentId` to update a student, and `DELETE /students/:studentId` to delete a student.
- **Resource-Based URL Structure**: Our API endpoints follow a resource-based URL structure. For instance, endpoints for managing students are structured under `/students`, and endpoints for managing tutors are under `/tutors`.
- **Stateless**: Each request contains all the information needed to process the request, making our API stateless and scalable.
- **JSON Responses**: Our API uses JSON for request and response bodies, ensuring ease of integration with various frontend frameworks.
- **JWT Authentication**: We secured our API using JWT (JSON Web Token) for authentication, ensuring that only authorized users can access protected routes.

Here's a glimpse of the backend structure:

- **Routes**: Defined in `routes/app.js`, mapping endpoints to corresponding controller functions.
- **Controllers**: Implemented in `controllers/`, containing the logic for handling requests.
- **Models**: Defined in `models/`, specifying the MongoDB schemas and database interactions.

### Sample Endpoint

```javascript
// routes/app.js
router.post("/students", ctrlStudents.studentsCreate);
```

## Video Demonstration

{{<video src="videos/tutoro.mp4" type="video/mp4" preload="auto" >}}
