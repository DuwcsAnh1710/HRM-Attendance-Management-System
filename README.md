# HRM & Attendance Management System

> A web-based Human Resource Management and Attendance Management System designed to support employee management, attendance tracking, leave management, organizational structure, role-based access control, and HR reporting.

![Project Status](https://img.shields.io/badge/status-in%20development-yellow)
![Project Type](https://img.shields.io/badge/type-academic%20project-blue)
![License](https://img.shields.io/badge/license-MIT-green)

---

## Overview

**HRM & Attendance Management System** is a web-based application designed to support businesses in managing employee information and daily attendance activities.

The project aims to centralize essential HR data, reduce manual management processes, and provide a structured platform for employees, managers, and HR staff to manage attendance and leave requests.

The system is currently under development as an academic software engineering project.

---

## Project Objectives

The main objective of this project is to analyze, design, and develop a centralized Human Resource Management and Attendance system.

The system aims to:

- Centralize employee information.
- Manage departments and positions.
- Provide employee attendance tracking.
- Record check-in and check-out activities.
- Support employee leave requests and approval workflows.
- Apply role-based access control.
- Provide basic HR dashboards and reports.
- Improve the efficiency and consistency of HR data management.

---

## 🔍 Problem Statement

Human resource management involves maintaining various types of information such as employee profiles, departments, positions, attendance records, and leave requests.

When these processes are managed manually or through separate spreadsheets and documents, businesses may face difficulties such as:

- Scattered employee information.
- Time-consuming data retrieval and updates.
- Inconsistent attendance records.
- Difficulty monitoring employee attendance.
- Inefficient leave request and approval processes.
- Limited visibility into HR statistics.

This project proposes a centralized web-based system to support these core HR activities.

---

## MVP Scope

The first version of the system focuses on six core modules:

### 1. Authentication & Authorization

- User login and logout.
- User authentication.
- Role-based access control.
- Protected system resources.

Planned roles:

- `Admin`
- `HR`
- `Manager`
- `Employee`

### 2. Employee Management

- View employee list.
- Create employee profiles.
- View employee details.
- Update employee information.
- Activate/deactivate employees.
- Search and filter employees.
- Assign departments and positions.

### 3. Department & Position Management

- Manage departments.
- Manage positions.
- Assign employees to departments.
- Assign positions to employees.
- Maintain basic organizational structure.

### 4. Attendance Management

- Employee check-in.
- Employee check-out.
- Attendance history.
- Working-time calculation.
- Late-arrival tracking.
- Early-leave tracking.
- HR attendance monitoring.

### 5. Leave Management

- Submit leave requests.
- View leave request history.
- Track request status.
- Approve leave requests.
- Reject leave requests.

Basic workflow:

```text
PENDING
   │
   ├──> APPROVED
   │
   └──> REJECTED
```

### 6. Dashboard & Reporting

Planned dashboard information includes:

- Total employees.
- Employees by department.
- Daily attendance overview.
- Late employees.
- Absence information.
- Pending leave requests.
- Basic attendance statistics.

---

## Out of MVP Scope

To keep the initial version focused and achievable, the following features are not included in the MVP:

- Payroll management.
- Personal income tax calculation.
- Social insurance management.
- Recruitment management.
- Candidate tracking.
- KPI and performance evaluation.
- Employee training management.
- Employee benefits management.
- Fingerprint attendance.
- Face recognition attendance.
- GPS/geofencing attendance.
- Native mobile applications.
- AI-based HR analytics.

These features may be considered for future development.

---

## User Roles

| Role | Main Responsibilities |
|------|-----------------------|
| **Admin** | System administration, account and access management |
| **HR** | Employee, department, position, attendance, and leave management |
| **Manager** | Monitor team attendance and process employee leave requests |
| **Employee** | Manage personal activities, attendance, and leave requests |

---

## Functional Requirements

The system is planned to provide the following core functional requirements:

| ID | Requirement |
|----|-------------|
| FR-01 | User authentication |
| FR-02 | Role-based authorization |
| FR-03 | Employee management |
| FR-04 | Employee search and filtering |
| FR-05 | Department management |
| FR-06 | Position management |
| FR-07 | Employee check-in |
| FR-08 | Employee check-out |
| FR-09 | Attendance history |
| FR-10 | Working-time calculation |
| FR-11 | Late and early-leave detection |
| FR-12 | Leave request submission |
| FR-13 | Leave request approval/rejection |
| FR-14 | Dashboard and HR statistics |

Detailed requirements will be documented in the `docs/requirements` directory.

---

## Non-Functional Requirements

The project will consider the following quality requirements:

### Security

- Passwords must not be stored in plain text.
- Protected APIs require authentication.
- Access to features must follow user roles and permissions.
- Sensitive configuration must be stored using environment variables.

### Performance

Common operations should provide reasonable response times under normal system load.

### Usability

The user interface should be:

- Clear and consistent.
- Easy to navigate.
- Responsive across common screen sizes.
- Equipped with understandable validation and error messages.

### Data Integrity

The database design should use appropriate:

- Primary keys.
- Foreign keys.
- Unique constraints.
- Data validation.

### Maintainability

The project should maintain a clear separation between:

- Frontend.
- Backend.
- Database.
- Documentation.

---

## Planned Tech Stack

> The technology stack may be adjusted during the design and implementation phases.

### Frontend

- React.js
- Vite
- JavaScript

### Backend

- Node.js
- Express.js
- RESTful API

### Database

- PostgreSQL or MySQL

### Authentication

- JWT
- Password hashing

### Development Tools

- Git
- GitHub
- Trello
- Figma
- Postman

---

## Planned Project Structure

```text
HRM-Attendance-Management-System/
│
├── frontend/
│   └── React application
│
├── backend/
│   └── Node.js / Express application
│
├── docs/
│   ├── requirements/
│   ├── database/
│   └── diagrams/
│
├── database/
│   ├── schema.sql
│   └── seed.sql
│
├── .gitignore
├── LICENSE
└── README.md
```

The structure may evolve as the project progresses.

---

## Development Workflow

The project follows a basic software development lifecycle:

```text
Requirement Analysis
        ↓
System Design
        ↓
Database Design
        ↓
UI/UX Design
        ↓
Implementation
        ↓
Testing
        ↓
Deployment
        ↓
Maintenance
```

Task management follows a Kanban workflow:

```text
BACKLOG
   ↓
TODO
   ↓
IN PROGRESS
   ↓
REVIEW / TESTING
   ↓
DONE
```

Issues discovered during development are tracked separately as `BUG`.

---

## Git Workflow

The planned Git workflow is:

```text
main
 │
 └── develop
       │
       ├── feature/authentication
       ├── feature/employee-management
       ├── feature/attendance
       └── feature/leave-management
```

Typical development process:

```text
Feature Branch
      ↓
Development
      ↓
Commit
      ↓
Push
      ↓
Pull Request
      ↓
Review / Testing
      ↓
Merge into develop
      ↓
Merge stable version into main
```

### Commit Convention

The project aims to use clear commit messages such as:

```text
feat: add employee management API
fix: prevent duplicate attendance check-in
docs: update system requirements
refactor: improve authentication service
test: add attendance API tests
chore: initialize backend project
```

---

## Development Roadmap

### Phase 1 — Requirement Analysis

- [x] Define project objectives
- [ ] Define system scope
- [ ] Identify system actors
- [ ] Define functional requirements
- [ ] Define non-functional requirements
- [ ] Create use case diagram
- [ ] Create use case specifications
- [ ] Finalize MVP requirements

### Phase 2 — System Design

- [ ] Design database entities
- [ ] Design ERD
- [ ] Design database schema
- [ ] Design application structure
- [ ] Design UI/UX prototype

### Phase 3 — Project Setup

- [ ] Initialize frontend
- [ ] Initialize backend
- [ ] Configure database
- [ ] Configure environment variables
- [ ] Establish Git workflow

### Phase 4 — Core Development

- [ ] Authentication & Authorization
- [ ] Employee Management
- [ ] Department & Position Management
- [ ] Attendance Management
- [ ] Leave Management
- [ ] Dashboard & Reporting

### Phase 5 — Testing

- [ ] API testing
- [ ] Functional testing
- [ ] Authorization testing
- [ ] UI testing
- [ ] Bug fixing
- [ ] Regression testing

### Phase 6 — Deployment & Documentation

- [ ] Prepare production environment
- [ ] Deploy backend
- [ ] Deploy frontend
- [ ] Deploy database
- [ ] Write installation guide
- [ ] Write user guide
- [ ] Complete technical documentation

---

## Documentation

Project documentation will be maintained under:

```text
docs/
├── requirements/
│   ├── project-objective.md
│   ├── system-scope.md
│   ├── actors.md
│   └── functional-requirements.md
│
├── database/
│   └── erd.md
│
└── diagrams/
    └── use-case-diagram.png
```

---

## Project Status

**Current Status:** `Requirement Analysis`

Current focus:

```text
01. Project Objective            ✅ Completed
02. System Scope                 🔨 In Progress
03. System Actors                🔨 In Progress
04. Functional Requirements      🔨 In Progress
```

Implementation has not started yet.

---

## Getting Started

Installation and local development instructions will be added after the frontend, backend, and database environments have been initialized.

---

## Future Development

Potential future improvements include:

- Payroll management.
- Recruitment management.
- KPI and performance evaluation.
- QR-code attendance.
- GPS-based attendance.
- Face recognition.
- Email notifications.
- Advanced analytics.
- Mobile application.
- AI-assisted HR analytics.

---

## License

This project is licensed under the **MIT License**.

---

## Author

**LE DUC ANH**

Information Technology Student  
University of Transport Ho Chi Minh City (UTH)

GitHub: `DuwcsAnh1710`

---

## Project Purpose

This repository is developed as an academic software engineering project focusing on applying the complete software development process to a practical **Human Resource Management and Attendance Management System**.
