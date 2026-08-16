# 🎓 EduTrack

### Online Learning & Course Management Platform

**EduTrack** is a full-stack e-learning platform built with **Java and Spring Boot**, designed to manage courses, students, trainers, enrollments, online payments, learning progress, mock tests, reviews, and certificates.

---

## ✨ Features

### 👨‍🎓 Student

* 🔐 Registration & secure login
* 📧 Email OTP verification
* 📚 Browse and enroll in courses
* 💳 Online course payment with Razorpay
* 📈 Track course & module progress
* 📝 Attempt mock tests
* ⭐ Submit course reviews
* 🏆 Generate & verify certificates
* 📄 Download certificates as PDF

### 👨‍🏫 Trainer

* 🔐 Trainer authentication
* 📚 Create & manage courses
* 📂 Manage course categories
* 📦 Manage modules & lessons
* 📝 Create mock tests
* ❓ Manage questions
* 👥 Manage course content

### 👨‍💼 Admin

* 📊 Admin dashboard
* 👨‍🎓 Manage students
* 👨‍🏫 Manage trainers
* 📚 Manage courses
* 📂 Manage categories
* 📋 Monitor enrollments

---

## 🛠️ Tech Stack

### Backend

![Java](https://img.shields.io/badge/Java-21-orange?style=for-the-badge\&logo=openjdk)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.x-brightgreen?style=for-the-badge\&logo=springboot)
![Spring Security](https://img.shields.io/badge/Spring%20Security-6.x-green?style=for-the-badge\&logo=springsecurity)
![Hibernate](https://img.shields.io/badge/Hibernate-ORM-brown?style=for-the-badge\&logo=hibernate)
![Maven](https://img.shields.io/badge/Maven-Build-red?style=for-the-badge\&logo=apachemaven)

### Frontend

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge\&logo=html5)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge\&logo=css3)
![Thymeleaf](https://img.shields.io/badge/Thymeleaf-005F0F?style=for-the-badge\&logo=thymeleaf)

### Database & Integration

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge\&logo=postgresql)
![Razorpay](https://img.shields.io/badge/Razorpay-3395FF?style=for-the-badge)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge\&logo=git)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge\&logo=github)

---

## 🏗️ Architecture

```text
                    ┌─────────────────────┐
                    │      Frontend       │
                    │ HTML • CSS •        │
                    │ Thymeleaf           │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │    Controllers      │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │      Services       │
                    │   Business Logic    │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │    Repositories     │
                    │    Spring Data JPA  │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │     PostgreSQL      │
                    └─────────────────────┘
```

---

## 📚 Learning Workflow

```text
Register
   ↓
Email Verification
   ↓
Login
   ↓
Browse Courses
   ↓
Select Course
   ↓
Razorpay Payment
   ↓
Course Enrollment
   ↓
Modules & Lessons
   ↓
Track Progress
   ↓
Mock Test
   ↓
Course Completion
   ↓
Certificate Generation
```

---

## 💳 Payment Integration

EduTrack uses **Razorpay** for online course payments.

```text
Select Course
      ↓
Create Payment Order
      ↓
Razorpay Checkout
      ↓
Payment
      ↓
Payment Verification
      ↓
Course Enrollment
```

---

## 🔐 Security

The application uses **Spring Security** with role-based access control.

### Roles

```text
👨‍💼 ADMIN
👨‍🏫 TRAINER
👨‍🎓 STUDENT
```

Security functionality includes:

* Authentication
* Role-based authorization
* Email OTP verification
* Password recovery
* Protected admin operations
* Protected trainer operations
* Protected student operations

---

## 🏆 Certificate System

Students can receive certificates after completing their courses.

**Certificate features:**

* Certificate generation
* Unique certificate identification
* Certificate verification
* PDF certificate download

---

## 📂 Project Structure

```text
EduTrack/
│
├── .mvn/
│   └── wrapper/
│
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com/jsp/CourseHub/
│   │   │       ├── config/
│   │   │       ├── controller/
│   │   │       ├── dto/
│   │   │       ├── entity/
│   │   │       ├── enums/
│   │   │       ├── exception/
│   │   │       ├── payment/
│   │   │       ├── repository/
│   │   │       ├── response/
│   │   │       ├── security/
│   │   │       ├── service/
│   │   │       └── util/
│   │   │
│   │   └── resources/
│   │       ├── static/
│   │       └── templates/
│   │
│   └── test/
│
├── .gitignore
├── pom.xml
├── mvnw
├── mvnw.cmd
└── README.md
```

---

## ⚙️ Configuration

Create your local:

```text
src/main/resources/application.properties
```

Configure your PostgreSQL, Gmail SMTP, and Razorpay credentials.

Example:

```properties
spring.application.name=CourseHub

spring.datasource.url=jdbc:postgresql://localhost:5432/eduTrack
spring.datasource.username=YOUR_USERNAME
spring.datasource.password=YOUR_PASSWORD

spring.jpa.hibernate.ddl-auto=update

spring.mail.host=smtp.gmail.com
spring.mail.port=587
spring.mail.username=YOUR_EMAIL
spring.mail.password=YOUR_APP_PASSWORD

razorpay.key=YOUR_RAZORPAY_KEY
razorpay.secret=YOUR_RAZORPAY_SECRET
```

> ⚠️ **Never commit real passwords, API keys, or secrets to GitHub.**

---

## 🎯 Project Highlights

| Feature        | Implementation           |
| -------------- | ------------------------ |
| Authentication | Spring Security          |
| Database       | PostgreSQL               |
| ORM            | JPA + Hibernate          |
| Payment        | Razorpay                 |
| Email          | Gmail SMTP               |
| Frontend       | Thymeleaf + HTML + CSS   |
| Build Tool     | Maven                    |
| Testing        | JUnit / Spring Boot Test |
| Architecture   | Layered Architecture     |

---

## 📌 Key Concepts Demonstrated

This project demonstrates practical experience with:

* Java
* Spring Boot
* Spring Security
* Spring Data JPA
* Hibernate
* REST & MVC architecture
* CRUD operations
* Role-based authorization
* PostgreSQL
* Payment gateway integration
* Email OTP
* Exception handling
* DTOs
* Repository pattern
* Service layer architecture
* Git & GitHub

---

## 👩‍💻 Author

### Sadiya A Hospetkazi

**B.E. Computer Science & Engineering (AI & ML)**

**Java Full Stack Developer | Software Engineer | AI Enthusiast**

Interested in:

`Java` • `Spring Boot` • `Backend Development` • `REST APIs` • `SQL` • `Full-Stack Development` • `AI`

---

## ⭐ Support

If you like this project, consider giving it a ⭐ on GitHub!

**Built with Java & Spring Boot ❤️**
