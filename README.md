# JWT Authentication System – Spring Boot

This project implements a secure JWT-based authentication and authorization system using Spring Boot and Spring Security.

## 🔐 Features

- User Registration
- User Login
- JWT Access Token
- Refresh Token
- Secured APIs
- Logout Handling
- Role-Based Authorization (USER / ADMIN)

## 🧩 Tech Stack

- Java
- Spring Boot
- Spring Security
- JWT
- JPA / Hibernate
- Maven
- H2 database for testing


## 🔄 Authentication Flow

1. User logs in
2. Server returns access token + refresh token
3. Access token is used for secured APIs
4. Refresh token is used to generate new access tokens
5. Logout deletes refresh token from DB

## 🔑 Access vs Refresh Token

| Token | Purpose | Expiry |
|------|--------|-------|
| Access Token | API authorization | Short-lived |
| Refresh Token | Generate new access token | Long-lived |

## 🚪 Logout Handling

Since JWT is stateless:
- Access tokens are short-lived
- Refresh tokens are stored in DB
- Logout deletes refresh token
- New access tokens cannot be generated after logout

## 👥 Role-Based Authorization

Roles supported:
- ROLE_USER
- ROLE_ADMIN

Authorization implemented using:
- JWT claims
- Spring Security authorities
- `@PreAuthorize`

## 🛡 Security

- Passwords encrypted using BCrypt
- JWT validation filter
- Role-based endpoint protection

## 🚀 How to Run

1. Clone repository
2. Configure database in `application.properties`
3. Run Spring Boot application
4. Test APIs using Postman

## 📌 Future Enhancements

- Email verification
- Token blacklist using Redis
- Swagger integration
- Dockerization

---
