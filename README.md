1. Introduction
1.1 Purpose
The purpose of this SRS is to describe all functional and non-functional requirements of the Gym Management System. This document ensures a clear understanding among developers, students, supervisors, and evaluators regarding the system design, scope, and functionalities.
          1.2 Project Overview
The Gym Management System is a web-based application developed to simplify and automate daily gym operations. The system enables the administrator to manage members, trainers, attendance, payments, and membership plans through a centralized digital platform. The application runs on a local server using PHP and MySQL.
1.3 Intended Audience
    • Supervisors and evaluators
    • Software developers
    • QA/testing team
    • Documentation reviewers
               1.4 Definitions and Abbreviations
    • Admin: Authorized user managing system operations
    • CRUD: Create, Read, Update, Delete
    • DBMS: Database Management System

2. Overall Description
2.1 Product Perspective
The Gym Management System is a standalone web application that stores all data on a local MySQL server. It aims to completely replace manual registers and spreadsheets used in gyms.
2.2 Product Features
    • Member record management
    • Trainer management
    • Attendance tracking
    • Payment and membership plan management
    • Report generation
    • Secure login system
2.3 User Classes and Characteristics
User Type	Description
Admin	Can access all modules including member, trainer, attendance, and payment management
(Only one user role is included in this project scope.)
2.4 Operating Environment
    • Backend: PHP 7+
    • Database: MySQL (phpMyAdmin)
    • Server: Apache (XAMPP/WAMP)
    • Frontend: HTML, CSS, JavaScript
    • Browser: Chrome, Edge, Firefox
2.5 Design & Implementation Constraints
    • System must run offline on local server
    • Database must be normalized and secure
    • PHP and Apache environment required
    • Proper form validation mandatory
2.6 Assumptions & Dependencies
    • Admin has basic computer and internet usage knowledge
    • XAMPP/WAMP properly installed
    • Local server remains active during usage

3. Specific Requirements
3.1 Functional Requirements
3.1.1 Login System
    • The system shall provide a secure login page for admin access.
    • The system shall validate admin credentials.
    • The system shall prevent unauthorized access.
3.1.2 Member Management
    • The system shall allow admin to add new members.
    • The system shall allow viewing member details.
    • The system shall allow editing or deleting member records.
    • The system shall categorize members based on membership plan.
3.1.3 Trainer Management
    • The system shall allow admin to add trainer details.
    • The system shall allow managing trainer schedules.
    • The system shall allow updating and removing trainer data.
3.1.4 Attendance Management
    • The system shall allow admin to mark daily attendance for members.
    • The system shall display attendance reports for selected dates.
    • The system shall store attendance history in the database.
3.1.5 Payment Management
    • The system shall allow admin to record payments from members.
    • The system shall generate dues or pending payment notifications.
    • The system shall show membership validity dates.
3.1.6 Reports Module
    • The system shall generate member reports.
    • The system shall generate trainer reports.
    • The system shall generate payment and attendance summaries.

4. Non-Functional Requirements
4.1 Usability Requirements
    • The system interface must be simple and user-friendly.
    • Navigation menus must be clear and consistent.
4.2 Reliability Requirements
    • The system must ensure no data loss during CRUD operations.
    • The database must support daily backups (manual for now).
4.3 Performance Requirements
    • Pages must load within 2–3 seconds on a local server.
    • The system must support up to 1,000 records without performance issues.
4.4 Security Requirements
    • Passwords must be encrypted in the database.
    • Only authenticated users can access admin panel.
    • Input fields must use validation to prevent SQL injection.
4.5 Maintainability Requirements
    • The codebase must be modular and properly commented.
    • Database schema should support future enhancements.
4.6 Portability Requirements
    • The system must run on any Windows machine with XAMPP/WAMP installed.
    • Browser-independent functionality required.

5. System Models
5.1 Use Case Descriptions
Primary Use Cases:
    • Login
    • Manage Members
    • Manage Trainers
    • Mark Attendance
    • Record Payments
    • Generate Reports
5.2 Entity-Relationship Model (Conceptual Description)
Entities:
    • Member
    • Trainer
    • Attendance
    • Payment
    • Membership Plan
Relationships:
    • A member has one membership plan
    • A member has many attendance records
    • A member has many payments

6. Technology Stack
Component	Technology
Frontend	HTML, CSS, JavaScript
Backend	PHP
Database	MySQL
Server	Apache (Localhost)
Version Control	Git & GitHub

7. Expected Outcomes
    • A complete working Gym Management System running on localhost
    • Centralized storage of member and trainer data
    • Easy attendance and payment tracking
    • Reduced manual paperwork and improved accuracy
    • Faster decision-making through reports

8. Future Enhancements
    • Online member registration and payments
    • Mobile-friendly responsive UI
    • Automated backup and recovery system
    • Analytics dashboards (charts & insights)

9. Conclusion
This SRS defines the complete requirements for the Gym Management System. The system aims to streamline gym operations by offering easy management of members, trainers, attendance, and payments. It improves efficiency, accuracy, and decision-making while providing a foundation for future enhancements such as online payments and analytics integration.
