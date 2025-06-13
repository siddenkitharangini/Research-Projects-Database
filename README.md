# 🎓 University Examination System – Database Project

## 📌 Description

This project presents a robust **University Examination System** designed using **SQL** and **ER modeling**. It effectively manages academic entities such as departments, courses, students, faculty members, and examinations within a university setup.

The system captures:
- Department-wise course offerings and heads
- Faculty responsibilities like teaching, coordinating, and exam creation
- Student enrollments, attendance tracking, and exam attempts
- Exam metadata such as type, date, duration, and subject association

---

## 🧱 ER Diagram Structure

### 🧾 Entities and Attributes:

- **Department**: `Dept_ID`, `Name`, `Head_EmpID`
- **Faculty**: `Emp_ID`, `Name`, `Designation`
- **Course**: `Course_Code`, `Title`, `Dept_ID`, `Coordinator_ID`
- **Student**: `Roll_No`, `Name`, `Dept_ID`
- **Exam**: `Exam_ID`, `Title`, `Subject_Name`, `Duration`, `Date`, `Type`, `Course_Code`, `Created_By`
- **Enrollment** (relation): `Roll_No`, `Course_Code`, `Attendance_Percentage`
- **Course_Teaching** (relation): `Emp_ID`, `Course_Code`
- **Exam_Attempt** (relation): `Exam_ID`, `Roll_No`, `Attempt_No`, `Marks`, `Attempt_Date`

---

## 🔗 Relationships

- One **department** offers many **courses** and has many **students**
- A **faculty** can:
  - Teach and coordinate multiple **courses**
  - Be the **head** of a department
  - **Create** exams
- A **student**:
  - Belongs to one department
  - Enrolls in multiple **courses**
  - Attempts **exams** (multiple attempts allowed)
- **Exams** are linked to specific **courses** and created by **faculty**

---

## 🗃️ SQL Implementation

The project includes:
- **Table creation scripts** with appropriate primary/foreign keys
- **Data insertion statements** for demo records
- **Support for referential integrity** and role mapping

Tables:
1. `Department`
2. `Faculty`
3. `Course`
4. `Student`
5. `Enrollment`
6. `Course_Teaching`
7. `Exam`
8. `Exam_Attempt`

---

## 📊 Sample Features

- Track which faculty teaches or coordinates which courses
- View student enrollments with attendance per course
- Monitor exam results per student with multiple attempt support
- Analyze department-level academic structures

---

## ✅ Summary

- 📁 8 core relational tables
- 🔑 Proper use of **primary/foreign keys**
- 🔄 Many-to-many relationships implemented via junction tables
- 📌 Practical design for real-world academic use

---

## 🖼️ ER Diagram

*(Include your ER Diagram image here if available)*

---

## 🚀 Getting Started

To run this project:
1. Use any SQL-compatible RDBMS (e.g., MySQL, PostgreSQL)
2. Run the table creation scripts
3. Insert the sample data provided
4. Execute queries to test the relationships and data integrity

---

## 📧 Contact

For questions or suggestions, feel free to raise an issue or contact the maintainer.

