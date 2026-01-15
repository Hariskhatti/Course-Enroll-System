🎓 Course Enrollment System
A Complete Spring Boot + Thymeleaf + PostgreSQL Web Application
<p align="center"> <img src="https://img.shields.io/badge/Spring%20Boot-3.x-brightgreen?style=for-the-badge"> <img src="https://img.shields.io/badge/Thymeleaf-Template-orange?style=for-the-badge"> <img src="https://img.shields.io/badge/PostgreSQL-Database-blue?style=for-the-badge"> <img src="https://img.shields.io/badge/Status-Stable-brightgreen?style=for-the-badge"> </p>

A full-stack Course Enrollment Web Application built using Spring Boot, Thymeleaf, and PostgreSQL.
The system supports Admin & User portals, secure role-based access, course management, enrollment requests, approval/rejection workflows, and detailed dashboards.

🔗 Demo Video (LinkedIn)
👉 https://shorturl.at/aNTSQ

🌐 UI Preview (Design Concept)
🏠 Home Page
🎓 COURSE ENROLLMENT SYSTEM
------------------------------------------------
• Browse available courses
• View course details with icons
• Login / Register

[ Search / Filter Courses ]

Clean, modern layout with gradient background

📊 User Dashboard
👤 Welcome, Student
------------------------------------------------
🟦 Browse Courses     🟦 My Enrollments
🟦 Enrollment History 🟦 Profile Settings
🟦 Logout

🛠️ Admin Dashboard
👑 Admin Control Panel
------------------------------------------------
📚 Manage Courses
🎟️ Enrollment Requests
👥 Manage Users
⚙️ Settings
🔒 Logout

🔑 System Roles & Access Control
👨‍💼 Admin Role (ROLE_ADMIN)

Admins are registered via service layer using a dedicated admin registration logic.

Capabilities

📚 Add / Update / Delete Courses

🎟️ Approve or Reject Enrollment Requests

👥 View & Manage Users

👤 Profile, Password Update, Logout

👤 User Role (ROLE_USER)
Capabilities

📚 Browse available courses with icons

✍️ Send enrollment requests

⏳ Track Pending / Approved enrollments

🧾 View complete enrollment history

👤 Profile management & logout

🛠️ Admin Registration Logic (Important)

Admins are not hardcoded and not manually assigned via DB.

✅ Service Layer Approach

A boolean flag or method like registerAdmin() is used.

If roleAdmin = true → user is saved with ROLE_ADMIN

Otherwise → default role is ROLE_USER

Example Logic (Concept)
if (roleAdmin) {
    userRoles.add(ROLE_ADMIN);
} else {
    userRoles.add(ROLE_USER);
}


✔️ This ensures:

Secure role assignment

No duplicate entity for Admin

Same StudentEntity used for both roles

🛠️ Tech Stack
Layer	Technology
Backend	Spring Boot 3.x
Frontend	Thymeleaf + Bootstrap 5
Database	PostgreSQL
Security	Spring Security (Role-Based Access)
IDE	IntelliJ / Eclipse
🗃️ Database Setup (PostgreSQL)
1️⃣ Create Database
CREATE DATABASE course_enroll;

2️⃣ Create Tables

Use the schema.sql file provided in the repository.

3️⃣ Configure Database Connection

src/main/resources/application.properties

spring.datasource.url=jdbc:postgresql://localhost:5432/course_enroll
spring.datasource.username=postgres
spring.datasource.password=your_pg_password
spring.jpa.hibernate.ddl-auto=update

🚀 How to Run the Project

1️⃣ Import project into IntelliJ / Eclipse
2️⃣ Ensure PostgreSQL is running
3️⃣ Update application.properties
4️⃣ Run Spring Boot application
5️⃣ Open browser:

http://localhost:8080/

📁 Project Structure
CourseEnrollmentSystem/
│
├── src/main/java/
│   └── hello/security/main/
│       ├── controller/
│       ├── entities/
│       ├── repository/
│       └── service/
│
├── src/main/resources/
│   ├── templates/        # Thymeleaf HTML files
│   └── application.properties
│
└── README.md

✅ Feature Matrix
Role	Features
Admin	Manage Courses, View Requests, User Management
Admin	Approve / Reject Enrollments
User	Browse Courses, Send Requests
User	Enrollment History
Shared	Secure Login, Logout, Role-Based Access
🌱 Future Enhancements

📩 Email / OTP Notifications

💳 Payment Integration for Premium Courses

🔍 Advanced Course Search & Filters

📊 Admin Analytics Dashboard

👨‍💻 Author

Haris Khatti
🔗 Demo Video: https://shorturl.at/aNTSQ

📄 License

This project is created for educational and demo purposes.
