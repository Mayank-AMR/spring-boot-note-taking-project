# Spring Boot Note-Taking API

A RESTful API for managing notes built with Spring Boot, Kotlin, and MongoDB. This project demonstrates secure note
management with user-specific data access.

## Technologies

- **Spring Boot 3.4.5**: Framework for building Java/Kotlin applications
- **Kotlin 1.9.25**: Modern JVM language with concise syntax
- **MongoDB**: NoSQL database for storing notes
- **Spring Security**: Authentication and authorization
- **Spring Data MongoDB**: Data access layer for MongoDB
- **JWT**: JSON Web Tokens for stateless authentication

## Features

- Create, read and delete notes
- Notes are associated with specific users
- Secure endpoints with authentication
- MongoDB storage for persistence
- JSON-based RESTful API

## API Endpoints

| Method | URL | Description |
|--------|-----|-------------|
| GET | `/notes` | Get all notes for the authenticated user |
| POST | `/notes` | Create or update a note |
| DELETE | `/notes/{id}` | Delete a note by ID |

## Prerequisites

- JDK 17 or later
- MongoDB database
- Gradle build tool

## Getting Started

1. Clone the repository
2. Configure MongoDB connection in `application.properties`
3. Build the project: `./gradlew build`
4. Run the application: `./gradlew bootRun`

## Configuration

The application can be configured through `application.properties`:

```properties
spring.application.name=backend_project
spring.data.mongodb.uri=your-mongodb-connection-string
```

## Data Model

### Note

- `id`: Unique identifier (MongoDB ObjectId)
- `title`: Note title
- `content`: Note content
- `color`: Color value for the note (as a Long)
- `createdAt`: Timestamp when the note was created
- `ownerId`: ID of the user who owns the note

## License

This project is licensed under the terms found in the LICENSE file.