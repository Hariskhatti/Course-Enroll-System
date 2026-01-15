🎓 Course Enrollment System
A Complete Spring Boot + Thymeleaf + PostgreSQL Web Application
<p align="center"> <img src="https://img.shields.io/badge/Spring%20Boot-3.x-brightgreen?style=for-the-badge"> <img src="https://img.shields.io/badge/Thymeleaf-Template-orange?style=for-the-badge"> <img src="https://img.shields.io/badge/PostgreSQL-Database-blue?style=for-the-badge"> <img src="https://img.shields.io/badge/Status-Stable-brightgreen?style=for-the-badge"> </p>

A full-stack Course Enrollment Web Application built using Spring Boot, Thymeleaf, and PostgreSQL.
Supports Admin and User portals, secure role-based access, course management, enrollment requests, approval/rejection flows, and detailed dashboards.

🌐 UI Preview (Design Concept)
🏠 Home Page
┌───────────────────────────────────────────────────────────────┐
│  🎓 COURSE ENROLLMENT SYSTEM                                  │
│---------------------------------------------------------------│
│   • Browse available courses                                   │
│   • View course details and icons                              │
│   • Login / Register                                           │
│                                                               │
│   [ Search / Filter Courses ]                                  │
│                                                               │
│   Clean, modern layout with gradient background                │
└───────────────────────────────────────────────────────────────┘

📊 User Dashboard
┌───────────────────────────────────────────────────────────────┐
│  👤 Welcome, Student                                           │
│---------------------------------------------------------------│
│   🟦 Browse Courses       🟦 My Enrollments        🟦 History   │
│   🟦 Profile Settings     🟦 Logout                               │
└───────────────────────────────────────────────────────────────┘

🛠️ Admin Dashboard
┌───────────────────────────────────────────────────────────────┐
│  👑 Admin Control Panel                                        │
│---------------------------------------------------------------│
│   📚 Manage Courses     👥 Manage Users                         │
│   🎟️ Enrollment Requests   ⚙️ Settings                          │
│   🔒 Logout                                                    │
└───────────────────────────────────────────────────────────────┘

🔑 System Roles & Features
👨‍💼 Admin Panel

⚠️ Admin must be created manually in the database with ROLE_ADMIN.

Capabilities

📚 Course Management – Add, Update, Delete Courses

🎟️ Enrollment Requests – Approve / Reject student enrollments

👥 User Management – View all users, delete if needed

⚙️ Settings – Edit profile, change password, logout

👤 User Panel
Capabilities

📚 Course Catalog – View courses with details & icons

✍️ Enrollment System – Send enroll requests, view pending/approved status

🧾 Enrollment History – Track all past enrollments

👤 Profile Settings – Edit profile, change password, logout

🛠️ Tech Stack
Layer	Technology
Backend	Spring Boot 3.x
Frontend	Thymeleaf + Bootstrap 5
Database	PostgreSQL
IDE	IntelliJ / Eclipse
🗃️ Database Setup (PostgreSQL)
1. Create Database
CREATE DATABASE course_enroll;

2. Create Tables

Use the Schemas.sql file in the repository.

3. Add Admin User
INSERT INTO student_entity (username, email, password)
VALUES ('admin', 'admin@example.com', '<bcrypt_password_here>');

4. Configure DB Connection

src/main/resources/application.properties

spring.datasource.url=jdbc:postgresql://localhost:5432/course_enroll
spring.datasource.username=postgres
spring.datasource.password=your_pg_password
spring.jpa.hibernate.ddl-auto=update

🚀 How to Run the Project
1. Import Project in IntelliJ / Eclipse

File → Open / Import Project

2. Configure Spring Boot

Make sure PostgreSQL is running

Update application.properties with your credentials

3. Run Application
http://localhost:8080/

📁 Project Structure
CourseEnrollmentSystem/
│
├── src/main/java/
│   ├── hello/security/main/          # Controllers, Entities, Services
│
├── src/main/resources/
│   ├── templates/                   # Thymeleaf templates
│   └── application.properties
│
└── README.md

✅ Feature Matrix
Role	Features
Admin	Manage Courses, View Enrollment Requests, User Management
Admin	Approve/Reject Requests, Profile & Password Update
User	Browse Courses, Send Enrollment Requests, View History
Shared	Secure Login, Logout, Role-Based Access
🌱 Future Enhancements

📩 Email/OTP Notifications

💳 Payment Integration for premium courses

🔍 Advanced Course Search & Filtering

📊 Admin Analytics Dashboard

👨‍💻 Author
Haris Khatti
📄 License

For educational/demo purposes only.
Check the demo on linkedin  https://shorturl.at/aNTSQ
