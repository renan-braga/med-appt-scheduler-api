# 🩺 Medical Appointment Scheduler API

A learning project built with Spring Boot, designed to manage medical appointments with role-based access control using Spring Security, Spring Data, and Spring Cloud.

## 📌 Goals

This project aims to:
- Demonstrate key features of Spring Security (authentication & authorization)
- Showcase the use of Spring Data JPA for persistence
- Experiment with Spring Cloud modules in a microservice-friendly architecture

---

## 📃 Product Requirements Document (PRD)

### 🧑‍⚕️ User Roles

| Role           | Permissions                                                                 |
|----------------|------------------------------------------------------------------------------|
| `ROLE_PATIENT` | Can view their own appointments and available slots                         |
| `ROLE_DOCTOR`  | Can view their own schedule and appointment history                         |
| `ROLE_STAFF`   | Can manage appointments (create, reschedule, cancel) for doctors and patients |
| `ROLE_ADMIN`   | Full access: manage users, roles, appointments, and system configuration    |

### ✅ Functional Requirements

- Register and authenticate users
- CRUD operations for patients, doctors, and appointments
- Prevent overlapping appointments for the same doctor
- Apply role-based restrictions to each endpoint
- API documentation via Swagger/OpenAPI

### ❌ Non-Functional Requirements

- Secure API with JWT-based authentication
- Modular, layered architecture following Spring best practices
- In-memory DB (H2) for development, PostgreSQL for production
- Well-documented and easily testable REST endpoints

---

## 🧱 Architecture Design (ADP)

### 🔧 Stack

| Layer         | Technology         |
|---------------|--------------------|
| Backend       | Spring Boot        |
| Security      | Spring Security + JWT |
| Persistence   | Spring Data JPA    |
| Database      | PostgreSQL / H2    |
| Documentation | Springdoc OpenAPI  |
| Cloud (optional) | Spring Cloud Gateway, Eureka |

### 🗂️ Key Modules

- `auth-service` – handles login and JWT issuance
- `agenda-service` – manages business logic for doctors, patients, and appointments
- `api-gateway` – optional layer for routing and load balancing
- `eureka-server` – optional service discovery

### 🧩 Entities

- `User` (id, name, email, password, role)
- `Doctor` (id, name, crm, specialty)
- `Patient` (id, name, birthdate, contact info)
- `Appointment` (id, doctor_id, patient_id, datetime, status)

---

## 🚀 Getting Started

_Coming soon..._

---

## 📜 License

This project is licensed under the **MIT License**.

---

## 📚 Notes

This is a personal learning project and not intended for production use. Contributions are welcome for educational purposes.
