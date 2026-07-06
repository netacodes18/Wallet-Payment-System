# 💳 Wallet Payment System

A secure, scalable, and event-driven wallet-based payment system built with Spring Boot, Hibernate/JPA, and PostgreSQL. It is designed to handle user authentication, robust wallet balance management, transaction operations, and real-time email notifications via RabbitMQ.

## ⚡ Features

- ✅ **User Authentication & Authorization**: Secure JWT-based authentication.
- ✅ **Role-based Access Control**: Clear separation between Admin and User roles.
- ✅ **Wallet Management**: Easily check balance, deposit, and withdraw funds securely.
- ✅ **Transaction History**: Keeps a secure log of all financial transactions.
- ✅ **Event-Driven Architecture**: Uses RabbitMQ for async notification processing.
- ✅ **Email Alerts**: Automatic email notifications for wallet transactions via SMTP.
- ✅ **RESTful APIs**: Clean and standardized APIs for smooth integration.
- ✅ **API Documentation**: Interactive API documentation using Swagger UI / OpenAPI.
- ✅ **Application Monitoring**: Health and metrics monitoring using Spring Boot Actuator.

## 🛠️ Tech Stack

- **Backend**: Java 21, Spring Boot 3.5.x
- **Database**: PostgreSQL
- **ORM**: Hibernate, Spring Data JPA
- **Security**: Spring Security, JWT (JSON Web Tokens)
- **Message Broker**: RabbitMQ (AMQP)
- **Mail Service**: Java Mail Sender (SMTP)
- **API Documentation**: SpringDoc OpenAPI (Swagger UI)
- **Build Tool**: Maven

## 🚀 Getting Started

### 1. Clone the Repository
```bash
git clone https://github.com/netacodes18/Wallet-Payment-System.git
cd Wallet-Payment-System/Wallet-Payment-System
```

### 2. Configure Dependencies

Ensure you have the following installed and running:
- **PostgreSQL** (Default Port: 5432)
- **RabbitMQ** (Default Port: 5672)

### 3. Database Setup

Create a PostgreSQL database named `Wallet_System`. Update `src/main/resources/application.properties` with your PostgreSQL credentials:
```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/Wallet_System
spring.datasource.username=postgres
spring.datasource.password=your_password
```

### 4. Email Configuration

To enable fully working email notifications, update the SMTP settings in `application.properties` with your credentials:
```properties
spring.mail.username=your_email@gmail.com
spring.mail.password=your_app_password
```

### 5. Run the Application

Navigate to the project root (where the `pom.xml` is located) and run the application using Maven:
```bash
mvn spring-boot:run
```
The server will start on port `8082`.

## 📌 API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/auth/register` | Register a new user |
| POST | `/api/auth/login` | Login user & retrieve JWT token |
| GET | `/api/wallet/balance` | Get current wallet balance |
| POST | `/api/wallet/deposit` | Deposit amount into the wallet |
| POST | `/api/wallet/withdraw` | Withdraw amount from the wallet |

*Tip: You can explore and test all APIs interactively via Swagger UI by navigating to `http://localhost:8082/swagger-ui.html` once the server is running.*

## 👨‍💻 Author

**Utkarsh Pratap (netacodes18)**

## ⭐ Contribute

Want to improve this project? Feel free to fork it, create a new branch, and submit a Pull Request! 🚀
