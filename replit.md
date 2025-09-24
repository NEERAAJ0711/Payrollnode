# HR Management System

## Overview
This is a comprehensive Human Resources Management System built with React, Express.js, and PostgreSQL. The application provides a complete suite of HR functionalities including employee management, job posting and applications, department organization, authentication with role-based access control, and advanced features like attendance management with face and location verification, and a full payroll system. It supports multi-tenant operations for different companies and includes a Flutter mobile companion app. The system aims to provide an enterprise-level HR solution ready for deployment.

## User Preferences
Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript
- **Build Tool**: Vite
- **UI Framework**: shadcn/ui components with Radix UI primitives
- **Styling**: Tailwind CSS with custom CSS variables
- **State Management**: TanStack Query (React Query) for server state
- **Routing**: Wouter
- **Form Handling**: React Hook Form with Zod validation

### Backend Architecture
- **Runtime**: Node.js with Express.js
- **Database**: PostgreSQL with Drizzle ORM
- **Authentication**: JWT-based with bcrypt for password hashing
- **Database Provider**: Neon serverless PostgreSQL
- **API Design**: RESTful API with role-based access control

### Database Design
The system uses PostgreSQL with core entities for multi-tenant support:
- **Companies**: For organizational data.
- **Users**: Authentication, role management (system_admin, admin, employee).
- **Employees**: Profiles linked to users and companies, including detailed employment history, KYC, and family info.
- **Departments, Designations, Branches, Locations, Cost Centers, Biometric Machines, Holidays, Leave Policies**: For comprehensive organizational management.
- **Jobs & Job Applications**: For recruitment processes.
- **Attendance**: Tracking daily attendance, face templates, and locations.
- **Permission Requests**: For managing employee access to features.
- **Monthly Payroll & Payroll Records**: For comprehensive payroll processing.

### Mobile Companion App (Flutter)
- **Framework**: Flutter with GetX state management.
- **Architecture**: Modular with 10 core modules (splash, auth, dashboard, attendance, profile, employees, leave, payroll, compliances, permissions, settings).
- **API Integration**: Dio HTTP client with interceptors for authentication.
- **Authentication**: JWT-based with automatic token refresh.
- **UI/UX**: Material Design 3 with custom theming.
- **Core Features**: Attendance check-in/out, leave applications, payroll viewing, employee management, compliance data, and permission requests.
- **Local Storage**: GetStorage for preferences and token management.

### Key Features and Implementations
- **Multi-Role Authentication & Authorization**: System Admin, Admin, and Employee roles with JWT-based, role-based, and company-scoped access control.
- **Employee Management**: Comprehensive profiles, CRUD operations, Aadhar verification for registration and data lookup, and company-based access control.
- **Recruitment Hub**: Job posting, application tracking, interview scheduling, and offer management.
- **Company Management**: Admin onboarding with mandatory company profile setup and system admin approval workflow.
- **Organizational Settings**: Management of departments, designations, branches, locations, cost centers, biometric machines, holidays, and leave policies via a tabbed interface.
- **Attendance Management**: Enterprise-level system with face verification, GPS location tracking, and automated monthly pay day calculations.
- **Payroll Management**: Comprehensive setup with compliance toggles (EPF, ESIC, LWF, OT, VPF, TDS, PT), dynamic salary calculation based on attendance, and monthly payroll processing workflow.
- **Permission Management**: Request-based system for employees, with admin approval/rejection, and a complete permission enforcement system at the page level.

## External Dependencies

### Core Technologies
- **@neondatabase/serverless**: Serverless PostgreSQL database connection.
- **drizzle-orm**: Type-safe ORM for database operations.
- **@tanstack/react-query**: Server state management and caching.
- **react-hook-form**: Form state management and validation.
- **zod**: Runtime type validation and schema definition.
- **jsonwebtoken**: JWT token generation and validation.
- **bcrypt**: Password hashing and comparison.

### UI Components
- **@radix-ui/***: Accessible component primitives.
- **tailwindcss**: Utility-first CSS framework.
- **class-variance-authority**: Component variant management.
- **lucide-react**: Icon library.

### Flutter Specific
- **GetX**: State management for Flutter app.
- **Dio**: HTTP client for API integration in Flutter.
- **GetStorage**: Local storage management in Flutter.