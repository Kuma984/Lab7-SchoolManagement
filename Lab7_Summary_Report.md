# SE Lab 7 Summary Report: ASP.NET Core with Razor & MVC (Database First)

**Author:** Trinh Duc Long  
**Student ID:** 524K0021  
**Course:** Software Engineering – Lab 7  
**Faculty:** Faculty of Information Technology – Ton Duc Thang University (TDTU)  
**Instructor:** MSc. Pham Thai Ky Trung  
**Submission Type:** Individual Work  

---

## 1. Introduction
The objective of Lab 7 is to design and develop a School Management Web Application using both **ASP.NET Core Razor Pages** and **ASP.NET Core MVC** adopting the **Database First** approach with Microsoft Entity Framework Core.

In the Database First pattern, the relational database `SchoolDB` is authored in SQL first. The application schema, entity models, and `DbContext` are mapped directly to this database structure, enabling efficient CRUD operations and statistical reporting.

---

## 2. Exercise Descriptions and Implementation

### 2.1. Database Design (`SchoolDB.sql`)
The database contains 5 core tables with established relationships:
1. `Departments` (DepartmentID, Name, Budget, StartDate)
2. `Instructors` (InstructorID, FirstName, LastName, HireDate)
3. `Courses` (CourseID, Title, Credits, DepartmentID)
4. `Students` (StudentID, FirstName, LastName, EnrollmentDate)
5. `Enrollments` (EnrollmentID, CourseID, StudentID, Grade)

Comprehensive seed data was provided to support development, testing, and report generation.

### 2.2. Exercise 1: ASP.NET Core Razor Pages (`SchoolAppCore`)
- Configured SQL Server connection string in `appsettings.json`.
- Injected `SchoolContext` via Dependency Injection in `Program.cs`.
- Implemented navigational menu in `Pages/Shared/_Layout.cshtml`.
- Created entity listing pages for Departments, Instructors, Courses, Students, and Enrollments.
- Created `Pages/Report.cshtml` computing dynamic statistics:
  - Total counts for all 5 entities.
  - Overall student average grade.
  - Recent enrollment activities with joined student and course information.

### 2.3. Exercise 2: ASP.NET Core MVC (`SchoolAppCoreMVC`)
- Configured MVC controller routing and services in `Program.cs`.
- Implemented controllers with asynchronous query patterns (`async/await`):
  - `DepartmentsController`, `InstructorsController`, `CoursesController`, `StudentsController`, `EnrollmentsController`.
- Created `ReportController` and corresponding `Views/Report/Index.cshtml` displaying comprehensive analytical summaries.

---

## 3. Conclusion
- The Database First methodology offers precise control over database indexing, constraints, and data integrity when integrating existing databases.
- Both Razor Pages and MVC architectures demonstrated seamless integration with EF Core to deliver robust, high-performance web applications.

---

## Appendix
- **GitHub Repository:** [https://github.com/Kuma984/Lab7-SchoolManagement](https://github.com/Kuma984/Lab7-SchoolManagement)
- **Figma Design:** [https://www.figma.com/design/NIElQyBErDa84XBUGDsKF9/Untitled?node-id=1-11&t=Ew0H3XM52ZZFSqMb-1](https://www.figma.com/design/NIElQyBErDa84XBUGDsKF9/Untitled?node-id=1-11&t=Ew0H3XM52ZZFSqMb-1)
