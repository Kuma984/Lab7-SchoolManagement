# School Management System - Lab 7 (ASP.NET Core Database First)

**Author:** Trinh Duc Long (Student ID: 524K0021)  
**Course:** Software Engineering – Lab 7  
**Faculty:** Faculty of Information Technology – Ton Duc Thang University (TDTU)  
**Instructor:** MSc. Pham Thai Ky Trung  

---

## 📌 Project Overview
This repository contains the complete solution for **Lab 7: ASP.NET Core with Razor Pages & MVC – Database First Approach**.
In this project, the database `SchoolDB` is designed and created first via SQL script (`SchoolDB.sql`), after which Entity Framework Core (EF Core) models and `DbContext` are mapped to query and manage the data.

Two web applications have been fully implemented and tested:
1. **`SchoolAppCore`**: ASP.NET Core Web Application built with **Razor Pages**.
2. **`SchoolAppCoreMVC`**: ASP.NET Core Web Application built with the **Model-View-Controller (MVC)** architectural pattern.

Both applications feature comprehensive management pages for all 5 core entities, along with an integrated **Summary Report Page**:
- **Departments** (DepartmentID, Name, Budget, StartDate)
- **Courses** (CourseID, Title, Credits, DepartmentID)
- **Instructors** (InstructorID, FirstName, LastName, HireDate)
- **Students** (StudentID, FirstName, LastName, EnrollmentDate)
- **Enrollments** (EnrollmentID, CourseID, StudentID, Grade)
- **Report Dashboard (`/Report` and `/Report/Index`)**: Aggregated metrics including total students, courses, instructors, departments, enrollments, GPA average, and recent enrollments list.

---

## 🔗 Project Links
- **GitHub Repository:** [https://github.com/Kuma984/Lab7-SchoolManagement](https://github.com/Kuma984/Lab7-SchoolManagement)

---

## 🚀 Getting Started

### Prerequisites
- [.NET 8.0 SDK](https://dotnet.microsoft.com/)
- Microsoft SQL Server (LocalDB or SQL Server Express)

### 1. Database Setup
Execute `SchoolDB.sql` using SQL Server Management Studio (SSMS) or the command line:
```bash
sqlcmd -S "(localdb)\MSSQLLocalDB" -i SchoolDB.sql
```

### 2. Running the Razor Pages Application (`SchoolAppCore`)
```bash
cd SchoolAppCore
dotnet run
```
Open your browser and navigate to:
- Home: `http://localhost:5000`
- Report Page: `http://localhost:5000/Report`

### 3. Running the MVC Application (`SchoolAppCoreMVC`)
```bash
cd SchoolAppCoreMVC
dotnet run
```
Open your browser and navigate to:
- Home: `http://localhost:5119`
- Report Page: `http://localhost:5119/Report/Index`

---

## 🏗 Architecture & Key Highlights
- **Database First Workflow:** Pre-defined relational database schema with primary keys, foreign key constraints, and seed data.
- **Asynchronous Execution:** Async EF Core queries (`ToListAsync`, `CountAsync`, `AverageAsync`) for responsive performance.
- **Clean Separation of Concerns:** Organized folder hierarchy following Microsoft ASP.NET Core enterprise standards.
