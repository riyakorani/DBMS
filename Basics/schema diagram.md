# 📘 Schema Diagram in DBMS

*(FAANG + Interview + GitHub Ready Notes)*

---

# 🔥 What is a Schema Diagram?

A Schema Diagram is a visual representation of:
- tables
- attributes
- keys
- relationships

inside a database.

It helps developers understand:
- database structure
- table connections
- foreign key relationships
- overall database design

---

# 📌 Purpose of Schema Diagram

Schema diagrams are used for:

✅ Database design  \n
✅ Understanding relationships  \n
✅ Normalization planning  \n
✅ Query writing  \n
✅ Backend development  \n
✅ System architecture  \n

---

# 🔥 Example Schema Diagram

```text
+------------------+
|     Students     |
+------------------+
| PK StudentID     |
| Name             |
| Email            |
+------------------+
          |
          | FK StudentID
          ↓
+------------------+
|    Enrollment    |
+------------------+
| PK StudentID     |
| PK CourseID      |
+------------------+
          ↑
          | FK CourseID
          |
+------------------+
|      Courses     |
+------------------+
| PK CourseID      |
| CourseName       |
+------------------+
```

---

# 🧠 Understanding the Diagram

---

# 1️⃣ Students Table

Stores student information.

## Attributes

| Attribute | Meaning |
|---|---|
| StudentID | Unique student identifier |
| Name | Student name |
| Email | Student email |

---

## Primary Key

```text
StudentID
```

Used to uniquely identify each student.

---

# 2️⃣ Courses Table

Stores course information.

## Attributes

| Attribute | Meaning |
|---|---|
| CourseID | Unique course identifier |
| CourseName | Name of course |

---

## Primary Key

```text
CourseID
```

Uniquely identifies each course.

---

# 3️⃣ Enrollment Table

Acts as:
# ✅ Junction Table

Used to connect:
- Students
- Courses

---

# 🔥 Why Enrollment Table Exists?

Because:

# ✅ One student can enroll in many courses
AND
# ✅ One course can contain many students

This creates:

# ✅ Many-to-Many Relationship (M:N)

---

# 🔥 Relationship Explanation

## Student ↔ Course

Relationship Type:

# ✅ Many-to-Many (M:N)

Implemented using:
# ✅ Enrollment Table

---

# 🔥 Composite Key

Enrollment table uses:

```text
StudentID + CourseID
```

as:
# ✅ Composite Primary Key

---

# 📌 Why Composite Key Needed?

Because:

```text
StudentID alone → NOT unique
CourseID alone → NOT unique
```

But together:

```text
StudentID + CourseID
```

becomes unique.

---

# 🔥 Foreign Keys

| Foreign Key | References |
|---|---|
| Enrollment.StudentID | Students.StudentID |
| Enrollment.CourseID | Courses.CourseID |

---

# 📌 Purpose of Foreign Keys

Foreign Keys help:
- create relationships
- maintain referential integrity
- prevent invalid references

---

# 🔥 Referential Integrity Example

Suppose:

```text
StudentID = 999
```

does not exist in Students table.

Then:

❌ DBMS will reject insertion into Enrollment table.

---

# 🔥 Important Terms

| Symbol | Meaning |
|---|---|
| PK | Primary Key |
| FK | Foreign Key |

---

# 🔥 Types of Relationships

| Relationship | Meaning |
|---|---|
| One-to-One | One record maps to one record |
| One-to-Many | One record maps to many records |
| Many-to-Many | Many records map to many records |

---

# 📌 Relationship Used Here

```text
Students ↔ Courses
```

is:

# ✅ Many-to-Many

---

# 🔥 Real-World Examples

| Application | Junction Table Example |
|---|---|
| Netflix | UserMovies |
| Amazon | OrdersProducts |
| Instagram | Followers |
| Spotify | PlaylistSongs |
| College System | Enrollment |

---

# 🔥 SQL Example

## Students Table

```sql
CREATE TABLE Students(
   StudentID INT PRIMARY KEY,
   Name VARCHAR(50),
   Email VARCHAR(100)
);
```

---

## Courses Table

```sql
CREATE TABLE Courses(
   CourseID INT PRIMARY KEY,
   CourseName VARCHAR(100)
);
```

---

## Enrollment Table

```sql
CREATE TABLE Enrollment(
   StudentID INT,
   CourseID INT,
   PRIMARY KEY(StudentID, CourseID),
   FOREIGN KEY(StudentID)
   REFERENCES Students(StudentID),
   FOREIGN KEY(CourseID)
   REFERENCES Courses(CourseID)
);
```

---

# 🎯 Microsoft / FAANG Interview Questions

---

## Q1. What is a Schema Diagram?

### ✅ Answer

A schema diagram visually represents database structure and relationships.

---

## Q2. Why are schema diagrams important?

### ✅ Answer

They help in:
- database design
- understanding relationships
- writing queries
- backend architecture

---

## Q3. Why is Enrollment table needed?

### ✅ Answer

To implement many-to-many relationship.

---

## Q4. Why is composite key used in Enrollment table?

### ✅ Answer

Because single column cannot uniquely identify rows.

---

## Q5. What happens if junction table is removed?

### ✅ Answer

Many-to-many relationship cannot be represented properly.

---

## Q6. Difference between PK and FK?

### ✅ Answer

| Primary Key | Foreign Key |
|---|---|
| Uniquely identifies row | References another table |
| Unique | May contain duplicates |
| Cannot be NULL | Can sometimes be NULL |

---

# 🧠 Practice Questions

---

## 1️⃣ Identify the Primary Keys

### Students

| StudentID | Name |
|---|---|

### Courses

| CourseID | CourseName |
|---|---|

### Enrollment

| StudentID | CourseID |
|---|---|

---

## 2️⃣ What relationship exists between Students and Courses?

### ✅ Answer
Many-to-Many

---

## 3️⃣ Why are foreign keys important?

### ✅ Answer
To maintain referential integrity.

---

## 4️⃣ Why is StudentID alone insufficient in Enrollment table?

### ✅ Answer
Because one student can enroll in multiple courses.

---

# 🚀 Advanced FAANG Concepts

---

# 📌 Why Schema Design Matters

Bad schema design causes:
- redundancy
- inconsistency
- slow queries
- poor scalability

Good schema design improves:
- normalization
- indexing
- performance
- maintainability

---

# 📌 Why Large Systems Use Schema Diagrams

Companies like:
- :contentReference[oaicite:0]{index=0}
- :contentReference[oaicite:1]{index=1}
- :contentReference[oaicite:2]{index=2}
- :contentReference[oaicite:3]{index=3}

use schema diagrams heavily for:
- distributed databases
- microservices
- backend systems
- query optimization

---

# 📌 Why Composite Keys Can Be Expensive

Large composite keys:
- increase index size
- slow joins
- consume more storage

So large systems often prefer:
# ✅ Surrogate Keys

---

# 🧠 Quick Revision Table

| Concept | Remember |
|---|---|
| Schema Diagram | Visual DB structure |
| PK | Unique identifier |
| FK | Creates relationship |
| Junction Table | Handles M:N |
| Composite Key | Multiple columns together |

---

# 🎯 One-Line Definitions

## Schema Diagram
> Visual representation of database structure.

## Primary Key
> Uniquely identifies rows.

## Foreign Key
> References another table.

## Junction Table
> Table used to implement many-to-many relationship.

## Composite Key
> Multiple columns together form unique key.

---

