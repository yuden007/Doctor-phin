# Clinic Management System (Phase 1 - MVP)

## Overview
This project is a **Clinic Management System** designed for a single clinic. It provides core features for patient management, appointment scheduling, billing, and staff user management. The system is built with a **JavaFX desktop application (frontend)** connected to a **Spring Boot backend (cloud-hosted)** with a **PostgreSQL database**.

## Tech Stack
- **Frontend:** JavaFX Desktop Application
- **Backend:** Spring Boot (Java)
- **Database:** PostgreSQL (Cloud-hosted)
- **Hosting:** Cloud server (Azure VM or equivalent)
- **Authentication:** Spring Security (role-based access control)

## Phase 1 Features (MVP)
1. **Patient Management**
    - Register, update, and search patient records
2. **Appointments**
    - Create and manage appointments
    - Assign doctors and view schedule
3. **Billing**
    - Record services and generate simple invoices
4. **User Management**
    - Staff login with role-based access (Admin, Doctor, Receptionist)

## Future Features
- Audio-to-text transcription (doctor notes)
- Consultation dialogue summarization
- Mobile application support (Android/iOS)
- Cloud-native scaling with managed services

## Architecture
```
Clinic Staff PC (JavaFX App)
    |
 (HTTPS)
    |
Cloud Server (Spring Boot REST API)
    |
PostgreSQL Database
```

```plaintext
## Project Structure
clinic-management-system/
│
├── backend/                       # Spring Boot backend (APIs, business logic)
│    ├── src/main/java/com/clinic/
│    │    ├── controller/          # REST controllers (Patients, Appointments, Billing, Users)
│    │    ├── service/             # Business logic services
│    │    ├── model/               # Entity classes (JPA/Hibernate)
│    │    ├── repository/          # Database repositories (JPA interfaces)
│    │    └── ClinicApplication.java # Spring Boot entry point
│    ├── src/main/resources/
│    │    ├── application.yml      # Spring Boot configuration (DB, server settings)
│    │    └── schema.sql           # Optional DB initialization
│    └── pom.xml                   # Maven dependencies for backend
│
├── frontend/                      # JavaFX desktop client
│    ├── src/main/java/com/clinic/ui/
│    │    ├── controllers/         # JavaFX controllers for UI forms
│    │    ├── views/               # FXML files for UI layout
│    │    └── MainApp.java         # JavaFX entry point
│    ├── src/main/resources/
│    │    └── styles.css           # CSS for UI styling
│    └── pom.xml                   # Maven dependencies for frontend
│
├── docs/                          # Documentation
│    ├── README.md                 # Project overview
│    └── Clinic_System_Phase1_Specification.pdf
│
└── build/                         # Build and deployment artifacts
```

## Getting Started
1. Clone the repository
2. Set up PostgreSQL on a cloud server
3. Configure Spring Boot application.yml with DB credentials
4. Run the backend server
5. Launch the JavaFX desktop client

## License
MIT License

