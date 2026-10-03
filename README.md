# Employee Management System (Full Stack)

A full-stack **Employee Management System** built with **Spring Boot (Backend)** and **React (Frontend)**.  
The application supports **JWT-based authentication**, **role-based access control**, and complete **CRUD operations** for employees.

---

## 🚀 Features

### 🔐 Authentication & Authorization
- JWT-based authentication
- Role-based access control:
  - **ADMIN** → Full access (Create, Update, Delete)
  - **USER** → Read-only access

### 👨‍💼 Employee Management
- Add new employees (Admin only)
- Update employee details (Admin only)
- Delete employees (Admin only)
- View employee list (Admin & User)
- Pagination, sorting, and search

### 🧑‍💻 Frontend
- React + Vite
- Axios with JWT interceptor
- Protected routes
- Admin-only UI actions
- Proper error handling (409 conflict, validation errors)

### 🛠 Backend
- Spring Boot
- Spring Security
- JWT Authentication Filter
- JPA + Hibernate
- MySQL Database
- Validation with Hibernate Validator

---

## 🧰 Tech Stack

### Backend
- Java 17
- Spring Boot
- Spring Security
- JWT (jjwt)
- JPA / Hibernate
- MySQL
- Maven

### Frontend
- React
- Vite
- Axios
- React Router
- Bootstrap

---

## ⚙️ Setup Instructions

### 1️⃣ Backend Setup (Spring Boot)

```bash
cd employee-backend
mvn clean install
mvn spring-boot:run
```

### 2️⃣ Frontend Setup (React)

```bash
cd ems-frontend
npm install
npm run dev<img width="376" height="137" alt="Screenshot 2026-10-03 053013" src="https://github.com/user-attachments/assets/1e1704d8-58d6-4446-8f6f-a861f9dc4772" />
<img width="1152" height="637" alt="Screenshot 2026-10-03 053029" src="https://github.com/user-attachments/assets/3843ad85-c247-46ee-8ce4-42d9e665c4b6" />
<img width="1400" height="466" alt="Screenshot 2026-10-03 053121" src="https://github.com/user-attachments/assets/4ca6b698-7a13-4dcb-8117-35e020aba939" />
<img width="1368" height="575" alt="Screenshot 2026-10-03 053349" src="https://github.com/user-attachments/assets/7e6ef9c3-5b65-41c0-af2d-06852344bd88" />



