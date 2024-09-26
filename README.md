# Carbon Footprint Monitoring System

## Project Description

The **Carbon Footprint Monitoring System** is designed to help users track and manage their carbon footprint. By logging various activities such as electricity consumption, travel, water usage, and dietary habits, the system calculates the corresponding carbon emissions. This tool aims to promote environmental awareness and sustainable behavior by providing users with real-time insights into their emissions patterns.

This platform enables users to view historical data, generate reports, and visualize their emissions trends over time, empowering them to make more eco-friendly decisions. The system follows a microservices architecture to ensure scalability, performance, and security, making it ideal for a growing user base.

## Key Functionalities

- **User Account Management**: Users can sign up, log in, and manage their personal profiles, ensuring data security and personalized insights.
- **Activity Tracking and Emission Calculation**: Users can input data about their daily activities like electricity usage, travel, and other carbon-impacting behaviors, and the system will calculate the resulting carbon emissions.
- **Monthly Emissions Overview**: A history of emissions is available, allowing users to see how their carbon footprint evolves month by month.
- **Data Visualization and Reporting**: The platform offers graphical representations of emissions data and enables users to generate detailed reports.

## System Requirements and Constraints

- **Responsiveness**: The system must return calculated emissions data within 2 seconds of user input.
- **Scalability**: The system should scale seamlessly as the number of users increases.
- **Security**: User data is protected by JWT authentication, and all communications are encrypted.
- **Uptime**: A 99.9% uptime is required, with failover strategies in place for reliability.

## Technology Overview

### Backend Technologies

The backend of the application is implemented using the following technologies:

- **Java 17**: Core programming language for building robust services.
- **Spring Boot**: Provides a foundation for the microservices architecture, simplifying backend development and allowing for modularity.
- **Spring Security**: Ensures secure access to resources with JWT authentication and authorization.
- **MongoDB**: A NoSQL database used for storing persistent data, optimized for high performance and flexibility in handling large datasets.
- **Docker**: Containerization technology to deploy the application across multiple environments, ensuring consistency and easy scaling.

### Frontend Development with Angular

The frontend is developed using **Angular**, a powerful, modern web framework that allows the creation of dynamic, single-page applications (SPAs) with a clean, modular structure. Angular is particularly suited for this project due to the following:

- **Component-Based Architecture**: Angular’s component system promotes reusability and modularity, making it easier to manage the complex user interface required for data visualization and user interactions.
- **Two-Way Data Binding**: This feature allows real-time synchronization between the model and the view, making the interface more responsive to user actions.
- **Routing**: Angular's routing capabilities enable seamless navigation within the application, such as moving between the user dashboard, emissions history, and report generation pages.
- **Built-in HTTP Client**: Angular’s HTTP client service is used to communicate with the backend RESTful APIs, ensuring efficient data transfer and real-time updates for users.
- **Responsive UI**: The frontend leverages **Bootstrap** alongside Angular to ensure the interface is responsive and accessible on both mobile and desktop devices.
- **State Management**: Through services and Observables, Angular efficiently handles user input, API responses, and real-time updates, making the data flow streamlined.

### API Communication

The frontend communicates with the backend via **RESTful APIs**, which expose endpoints for user actions such as logging activities, retrieving emissions data, and generating reports. The backend services are containerized using Docker, allowing for seamless integration across environments.

## Architectural Design

### Microservices Overview

This system is built following a **microservices architecture**, where each service is responsible for a distinct business capability. The core services include:

- **API Gateway**: Acts as the main entry point for all requests, routing traffic to appropriate microservices.
- **User Service**: Handles user-related operations, such as registration, login, and profile management.
- **Carbon Emissions Service**: Manages the tracking of user activities and computes the corresponding carbon emissions.
- **History Service**: Stores historical data on user emissions and allows retrieval for reporting and visualization purposes.
- **Reporting Service**: Generates detailed reports and visualizations of user emissions data, helping users understand their carbon footprint over time.

### Security Mechanisms

- **JWT Authentication**: Ensures secure access to the system. Each user receives a JSON Web Token (JWT) upon login, which is used to verify their identity for future requests.
- **Role-Based Authorization**: Only authorized users can perform specific actions, ensuring data privacy and preventing unauthorized access.
- **Data Encryption**: Sensitive data is encrypted both in transit and at rest to maintain confidentiality and integrity.

## Performance Optimization

- **Caching**: Frequently accessed data is cached to reduce server load and minimize database queries.
- **Load Balancing**: Requests are distributed across multiple instances of each microservice to ensure even load distribution.
- **Asynchronous Processing**: Time-intensive operations, such as report generation, are handled asynchronously to prevent blocking the user interface.


