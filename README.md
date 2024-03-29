#BS23Test

## User Management System with Kafka Integration and Docker Containers

This project is a Java-based user management system that utilizes Spring Boot, JPA, and Kafka to perform CRUD operations on user entities. Additionally, it includes functionality to produce events using Kafka when a user is created, updated, or deleted, and consumes these events to save `LogCrudEntity` into the database. The entire system is containerized using Docker.

## Features

- CRUD operations on user entities.
- Kafka integration to produce events for user creation, update, and deletion.
- Consumption of Kafka events to save `LogCrudEntity` into the database.
- Containerization with Docker for easy deployment and scalability.

## Components

### 1. User Entity
The `UserEntity` represents the data model for users in the system.

### 2. UserController
The `UserController` handles incoming HTTP requests related to user operations such as create, read, update, and delete.

### 3. UserService
The `UserService` contains the business logic for user-related operations. It interacts with the `UserRepository` to perform CRUD operations on `UserEntity`.

### 4. UserRepository
The `UserRepository` interfaces with the database using JPA to perform CRUD operations on `UserEntity`.

### 5. Kafka Integration
The project integrates with Kafka to produce events when a user is created, updated, or deleted. It also consumes these events to save `LogCrudEntity` into the database.

### 6. LogCrudEntity
The `LogCrudEntity` represents the logs generated upon user CRUD operations. These logs are saved into the database upon consumption of Kafka events.

### 7. Docker
The entire application is containerized using Docker, which simplifies deployment and ensures consistent runtime environments across different platforms.
