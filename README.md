# Placement Cell Management System

A full-stack web application designed to manage the placement process of students, companies, jobs, applications, approvals, notifications, and placement-related activities through dedicated portals.

## Overview

The **Placement Cell Management System** provides separate interfaces for:

- Students
- Companies
- Placement Officers

The system is organized into a React/Vite frontend and a Node.js/Express backend. It provides authentication, role-based access, job management, applications, company and student approvals, notifications, and placement statistics.

## Features

### Student Portal

- Student registration and login
- Student profile management
- Browse available jobs
- Apply for jobs
- View applied jobs
- Update profile information
- Access student-specific dashboard

### Company Portal

- Company registration and login
- Company profile management
- Post job opportunities
- View applications
- Manage company-related information
- Access company dashboard

### Placement Officer Portal

- Placement officer authentication
- Placement officer dashboard
- Approve companies
- Approve students
- Review job postings
- Manage users
- Send/view notifications
- View placement statistics
- Update officer profile

### Authentication & Security

- User authentication
- Role-based application access
- Protected frontend routes
- Backend authentication middleware
- Separate functionality for students, companies, and placement officers

### Backend

The backend provides API routes and controllers for:

- Authentication
- Students
- Companies
- Jobs
- Applications
- Notifications
- Placement operations
- Placement officers

## Tech Stack

### Frontend

- React
- Vite
- JavaScript
- CSS
- React Router / protected routing

### Backend

- Node.js
- Express.js
- JavaScript

### Database

- SQL-based database schema
- Database initialization and seed data

## Project Structure

```text
Placement-Cell-Project/
│
├── Backend/
│   ├── controller/
│   │   ├── applications.js
│   │   ├── authentication.js
│   │   ├── companies.js
│   │   ├── jobs.js
│   │   ├── notifications.js
│   │   ├── officer.js
│   │   ├── placement.js
│   │   └── students.js
│   │
│   ├── init/
│   │   ├── data.js
│   │   └── index.js
│   │
│   ├── routes/
│   │   ├── applications.js
│   │   ├── authentication.js
│   │   ├── companies.js
│   │   ├── jobs.js
│   │   ├── notifications.js
│   │   ├── officer.js
│   │   ├── placement.js
│   │   └── students.js
│   │
│   ├── public/
│   │   ├── css/
│   │   │   └── style.css
│   │   └── js/
│   │       └── script.js
│   │
│   ├── utilis/
│   │   ├── ExpressError.js
│   │   └── wrapAsync.js
│   │
│   ├── TablesSchema.sql
│   ├── app.js
│   ├── middleware.js
│   ├── package.json
│   └── package-lock.json
│
├── frontent_placement_cell/
│   ├── public/
│   │   └── vite.svg
│   │
│   ├── src/
│   │   ├── Pages/
│   │   │   ├── Auth/
│   │   │   │   ├── Login.jsx
│   │   │   │   ├── SignUp.jsx
│   │   │   │   └── roleRegisteration.jsx
│   │   │   │
│   │   │   ├── CompanyPortal/
│   │   │   │   ├── Application.jsx
│   │   │   │   ├── CompanyLayout.jsx
│   │   │   │   ├── Dashboard.jsx
│   │   │   │   ├── JobPost.jsx
│   │   │   │   └── Profile.jsx
│   │   │   │
│   │   │   ├── PlacementOfficer/
│   │   │   │   ├── CompanyApproval.jsx
│   │   │   │   ├── Dashboard.jsx
│   │   │   │   ├── Notification.jsx
│   │   │   │   ├── OfficerLayout.jsx
│   │   │   │   ├── PlacementStats.jsx
│   │   │   │   ├── Profile.jsx
│   │   │   │   ├── ReviewJob.jsx
│   │   │   │   ├── StudentApproval.jsx
│   │   │   │   ├── UpdateProfile.jsx
│   │   │   │   └── Users.jsx
│   │   │   │
│   │   │   ├── StudentPortal/
│   │   │   │   ├── AppliedJobs.jsx
│   │   │   │   ├── Dashboard.jsx
│   │   │   │   ├── Profil.jsx
│   │   │   │   ├── StudentLayout.jsx
│   │   │   │   └── Updateprofile.jsx
│   │   │   │
│   │   │   └── Home.jsx
│   │   │
│   │   ├── components/
│   │   │   ├── Form/
│   │   │   │   ├── ErrorMessage.jsx
│   │   │   │   ├── InputField.jsx
│   │   │   │   ├── SelectedField.jsx
│   │   │   │   └── SubmitButton.jsx
│   │   │   ├── Layout/
│   │   │   │   ├── Footer.jsx
│   │   │   │   └── Navbar.jsx
│   │   │   ├── Card.jsx
│   │   │   ├── JobCard.jsx
│   │   │   ├── ProtectedRoute.jsx
│   │   │   ├── ReviewCard.jsx
│   │   │   ├── Stat.jsx
│   │   │   └── StatCad.jsx
│   │   │
│   │   ├── App.jsx
│   │   ├── main.jsx
│   │   └── index.css
│   │
│   ├── eslint.config.js
│   ├── index.html
│   ├── package.json
│   ├── package-lock.json
│   └── vite.config.js
│
└── .gitignore
```

## Getting Started

### Prerequisites

Install the following before running the project:

- Node.js
- npm
- Git

You can verify Node.js and npm with:

```bash
node --version
npm --version
```

## Installation

### 1. Clone the repository

```bash
git clone https://github.com/musaib-bhat/Placement-Cell-Project.git
cd Placement-Cell-Project
```

### 2. Install backend dependencies

```bash
cd Backend
npm install
```

### 3. Install frontend dependencies

Open another terminal and run:

```bash
cd frontent_placement_cell
npm install
```

## Running the Application

### Start the Backend

From the `Backend` directory:

```bash
node app.js
```

If a start script is configured in `Backend/package.json`, you can alternatively use:

```bash
npm start
```

### Start the Frontend

From the `frontent_placement_cell` directory:

```bash
npm run dev
```

Vite will display the local development URL in the terminal, normally similar to:

```text
http://localhost:5173
```

## Database

The project includes the database schema in:

```text
Backend/TablesSchema.sql
```

Initial/sample data and database initialization logic are located in:

```text
Backend/init/
├── data.js
└── index.js
```

Follow the database setup used by the backend code before starting the application if a local database has not already been initialized.

## Backend Architecture

The backend follows a modular structure:

```text
Routes
   ↓
Controllers
   ↓
Database / Application Logic
```

### Controllers

Controllers contain the application logic for:

- Authentication
- Students
- Companies
- Jobs
- Applications
- Notifications
- Placement officers
- Placement operations

### Routes

Routes expose API endpoints for the different modules of the application.

### Middleware

`Backend/middleware.js` contains backend middleware used by the application.

### Utilities

Reusable backend utilities are located in:

```text
Backend/utilis/
```

including error handling and asynchronous request helpers.

## Frontend Architecture

The frontend is built using React and Vite.

The application is divided into role-specific pages:

```text
Authentication
      │
      ├── Student Portal
      │
      ├── Company Portal
      │
      └── Placement Officer Portal
```

Reusable UI components are stored in:

```text
frontent_placement_cell/src/components/
```

Protected pages use:

```text
ProtectedRoute.jsx
```

to control access to authenticated areas of the application.

## Main Workflow

A typical placement workflow can be represented as:

```text
Student registers
      ↓
Student approval
      ↓
Student accesses portal
      ↓
Company registers
      ↓
Company approval
      ↓
Company posts a job
      ↓
Placement officer reviews job
      ↓
Approved job becomes available
      ↓
Student applies
      ↓
Company manages applications
      ↓
Placement statistics are updated
```

## Git Workflow

After making changes to the project:

```bash
git add .
git commit -m "Describe your changes"
git push
```

For example:

```bash
git add .
git commit -m "Updated student dashboard"
git push
```

## Future Improvements

Possible future improvements include:

- Advanced search and filtering for jobs
- Application status tracking
- Email notifications
- Resume upload and management
- More detailed placement analytics
- Improved role-based authorization
- Automated testing
- Production deployment
- Cloud database integration
- Improved validation and error handling

## Repository

GitHub repository:

https://github.com/musaib-bhat/Placement-Cell-Project

## License

This project is intended for educational and development purposes.
