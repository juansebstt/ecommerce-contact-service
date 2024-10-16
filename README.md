# E-commerce Contact Service

## Overview

The **E-commerce Contact Service** provides functionality for customers to contact the business via WhatsApp. This service integrates with the WhatsApp Business API to enable real-time communication, enhancing customer support and engagement.

## Features

- **WhatsApp Integration**: Allows customers to send messages to the business via WhatsApp.
- **Message Handling**: Processes incoming messages and responses.
- **Logging and Monitoring**: Keeps track of message exchanges for quality assurance and analysis.
- **Error Handling**: Implements standard error handling for communication failures.

## Technologies Used

- **Java**
- **Spring Boot**
- **Maven** (for dependency management)
- **WhatsApp Business API** (for sending and receiving messages)

## Prerequisites

Before running this service, ensure you have the following:

- **Java JDK 11 or higher**
- **Maven** (for building the project)
- A **WhatsApp Business Account** and access to the WhatsApp Business API.
- Access to the relevant microservices (e.g., API Gateway, Auth Service).

## Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/juansebstt/ecommerce-contact-service.git
    ```

2. Navigate to the project directory:

    ```bash
    cd ecommerce-contact-servic
    ```

3. Build the project using Maven:

    ```bash
    mvn clean instal
    ```


## Configuration

You need to configure the WhatsApp API credentials and other settings in your `application.yml` or `application.properties` file.

### Sample Configuration

```yaml
server:
  port: 8090

whatsapp:
  apiUrl: "https://your-whatsapp-api-url"
  token: "your-whatsapp-api-token"
  phoneNumber: "your-business-phone-number"

spring:
  application:
    name: ecommerce-contact-service
```

## Inter-Service Communication

The E-commerce Contact Service can be utilized by the following microservices:

- **[E-commerce API Gateway](https://github.com/juansebstt/ecommerce-api-gateway)**:
    - All requests from the frontend are routed through the API Gateway, which forwards them to the appropriate microservices.
- **[E-commerce Auth Service](https://github.com/juansebstt/ecommerce-auth-service)**:
    - Manages user authentication and authorization, providing JWT tokens for secure access.
- **[E-commerce Notification Service](https://github.com/juansebstt/ecommerce-notification-service)**:
    - Sends notifications and updates to users regarding their orders and account activities.

## WhatsApp API Integration

### Sending Messages

To send a message to a customer, you can call the API endpoint exposed by this service. Make sure you include the necessary authentication token.

### Receiving Messages

The service can also handle incoming messages from customers via the WhatsApp API. Implement the webhook to process and respond to incoming messages.

## Usage

This service runs in the background and can be triggered by other microservices to handle customer contact requests. The integration with WhatsApp enhances customer engagement and provides a seamless communication channel.

## Testing the Service

You can use tools like Postman or curl to test the API endpoints of the contact service. Ensure to replace placeholders with actual WhatsApp API credentials.

## Contributing

Feel free to submit pull requests or open issues if you find bugs or want to contribute to the project.