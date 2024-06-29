# FinMan Project Documentation

## Overview

FinMan is a microservices-based financial management system designed to handle various financial tasks, including user management, transaction processing, role management, and authentication. The system is built using Go and follows a hexagonal architecture to promote maintainability and scalability.

## Helitech Company Task

This project is a solution to a task provided by Helitech. For more information about Helitech, visit [Helitech Technology](https://heli.technology/).

### Task Description

The task involves creating a system for managing financial affairs with the following requirements:

1. **Transaction Management**: 
   - Allow registration and tracking of financial transactions with details such as transaction type (deposit or withdrawal), amount, and date.

2. **Deposit and Withdrawal**: 
   - Users should be able to deposit and withdraw from their accounts.

3. **User Authentication and Management**: 
   - Implement an authentication system to manage access to data and manage users with different roles.

4. **Microservice Architecture**: 
   - Use microservice architecture to separate different parts of the application.

5. **gRPC Communication**: 
   - Use gRPC for service communication.

6. **Protobuf for API**: 
   - Use Protobuf for defining APIs.

7. **Separation of UI and Business Logic**: 
   - Separate the user interface from business logic.

8. **Database Migration**: 
   - Use database migration for managing schemas.

9. **Password Hashing**: 
   - Use Bcrypt for hashing passwords.

10. **Session Management**: 
    - Use JWT for managing sessions.

11. **Notifications**: 
    - Send notifications after any transaction.

12. **Concurrent Transaction Management**: 
    - Handle concurrent transactions properly.

13. **Testing**: 
    - Implement unit tests and integration tests.

14. **API Documentation**: 
    - Document the API using Swagger.

15. **Readme Documentation**: 
    - Add a README to explain how to use the system.

## Architecture

![Architecture Diagram](architecture.png)

### Services

1. **Authentication Service (`finman-auth-service`)**
    - Handles user authentication and JWT generation.
    - Provides endpoints for user login.
    - Communicates with the User Service to validate user existence.

2. **User Service (`finman-user-service`)**
    - Manages user profiles and information.
    - Provides endpoints for user creation, update, and retrieval.

3. **Transaction Service (`finman-transaction-service`)**
    - Manages financial transactions including deposits and withdrawals.
    - Provides endpoints for creating and retrieving transactions.
    - Sends notifications after any transaction.

4. **Role Management Service (`finman-role-service`)**
    - Manages roles and permissions for users.
    - Provides endpoints for creating roles, assigning roles to users, and retrieving roles.

5. **API Gateway (`finman-api-gateway`)**
    - Routes incoming HTTP requests to the appropriate microservice.
    - Handles API aggregation and provides a unified entry point for the clients.
    - Manages authentication and authorization.

### Communication

- **gRPC**: Used for inter-service communication.
- **Protobuf**: Used for defining the API for gRPC communication.
- **REST**: Exposed via the API Gateway for client interactions.

### Security

- **Authentication**: Managed by the `finman-auth-service` using JWT.
- **Authorization**: Managed by the `finman-role-service`.
- **Password Hashing**: Using Bcrypt.
- **Session Management**: Using JWT.

### Database

- Each service has its own database.
- Database migrations are used to manage schemas.

### Notification

- The system sends notifications after any transaction.

### Testing and Documentation

- Unit tests and integration tests are implemented for all services.
- API documentation is provided using Swagger.
- Each repository includes a README to explain how to use the service.

## Setup Instructions

### Prerequisites

- Go 1.12 or higher
- Docker (optional, for containerization)
- gRPC and Protobuf tools
- PostgreSQL

### Cloning the Repositories

1. Clone the documentation repository:
    ```bash
    git clone https://github.com/yourusername/finman-docs.git
    cd finman-docs
    ```

2. Clone the individual service repositories:
    ```bash
    git clone https://github.com/nullexp/finman-auth-service.git
    git clone https://github.com/nullexp/finman-user-service.git
    git clone https://github.com/nullexp/finman-transaction-service.git
    git clone https://github.com/nullexp/finman-role-service.git
    git clone https://github.com/nullexp/finman-api-gateway.git
    ```

### Running the Services

Each service has its own setup and configuration. Please refer to the individual README files in each service repository for detailed setup instructions.

## Contributing

We welcome contributions from the community. Please read our [Contributing Guidelines](CONTRIBUTING.md) for details on our code of conduct, and the process for submitting pull requests.

## API Documentation

Each service uses Swagger for API documentation. You can view the API documentation by running the service and navigating to `/swagger/index.html` in your browser.

## Frequently Asked Questions (FAQ)

**How do I start the project?**

- Follow the setup instructions for each service in their respective repositories.
- Use Docker Compose or Kubernetes to orchestrate the services.

**How do I run the tests?**

- Each service repository contains instructions for running unit and integration tests.

**How do I handle user roles?**

- User roles are managed by the `finman-role-service`. Please refer to its README for more details.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
