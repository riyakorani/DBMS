# 📘 Schema vs Instance in DBMS

*(FAANG + Interview + GitHub Ready Notes)*

---

# 🔥 What is Schema?

A **Schema** is the **structure or design of the database**.

It defines:

- Table names
- Column names
- Data types
- Constraints
- Relationships

👉 Schema tells us:

> “How the database is organized.”

---

# 📌 Example of Schema

```sql
Student(
    ID INT,
    Name VARCHAR(50),
    Marks INT
)
```

This only defines:

- columns
- structure
- format

❌ No actual data is stored here.

---

# 🔥 What is Instance?

An **Instance** is the **actual data stored in the database at a particular time**.

👉 Instance tells us:

> “What data is currently stored inside the database.”

---

# 📌 Example of Instance

| ID | Name | Marks |
|----|------|------|
| 101 | Riya | 85 |
| 102 | Aman | 90 |

This is the actual stored data.

---

# 🧠 Easy Analogy

## Schema = Blueprint of House 🏠
Defines:
- number of rooms
- design
- structure

## Instance = People living inside the house 👨‍👩‍👧
Actual content at a specific time.

---

# 🔥 Key Difference Between Schema and Instance

| Feature | Schema | Instance |
|---|---|---|
| Meaning | Structure of database | Actual data stored |
| Changes Frequently? | Rarely | Frequently |
| Contains | Table definitions | Actual records |
| Example | Student(ID, Name, Marks) | 101, Riya, 85 |
| Also Called | Intension | Extension |

---

# 📌 Important Point

## Schema changes rarely

Example:

```sql
ALTER TABLE Student
ADD Email VARCHAR(50);
```

Now schema changes because:
- new column added

---

## Instance changes frequently

Example:

```sql
INSERT INTO Student
VALUES(103, 'Rahul', 88);
```

Only data changes.

---

# 🔥 Real Interview-Level Understanding

## Example 1

### Schema

```sql
Employee(
    EmpID,
    Name,
    Salary
)
```

### Instance

| EmpID | Name | Salary |
|---|---|---|
| 1 | Riya | 50000 |
| 2 | Aman | 60000 |

---

# 🔥 What Happens in Different Cases?

---

# Case 1 → Adding New Row

```sql
INSERT INTO Student
VALUES(104, 'Karan', 91);
```

## What changes?

✅ Instance changes  
❌ Schema does NOT change

Reason:
- Structure same
- Only data added

---

# Case 2 → Adding New Column

```sql
ALTER TABLE Student
ADD Phone VARCHAR(15);
```

## What changes?

✅ Schema changes  
✅ Instance changes

Reason:
- Structure changed
- Existing records updated with new column

---

# 🧠 Important Terms

## Intension
Another name for Schema.

## Extension
Another name for Instance.

FAANG interviewers sometimes ask this directly.

---

# 🎯 Microsoft / FAANG Interview Questions

---

## Q1. What is the difference between schema and instance?

### Answer

Schema is the structure/design of the database, while instance is the actual data stored in the database at a particular time.

---

## Q2. Does inserting new data change schema?

### Answer

No.  
Inserting data changes only the instance because structure remains same.

---

## Q3. Does adding a new column affect schema?

### Answer

Yes.  
Adding a column changes schema because database structure changes.

---

## Q4. Which changes more frequently: schema or instance?

### Answer

Instance changes frequently because records are continuously inserted, updated, or deleted.

---

## Q5. Why is schema important?

### Answer

Schema provides:
- database structure
- organization
- consistency
- data relationships
- constraints

---

# 🧠 Practice Questions

---

## 1️⃣ Identify Schema vs Instance

### A)

```sql
Student(ID, Name, Marks)
```

### B)

| ID | Name | Marks |
|---|---|---|
| 101 | Riya | 85 |

### Answer

A → Schema  
B → Instance

---

## 2️⃣ What changes here?

```sql
INSERT INTO Student
VALUES(105, 'Aman', 95);
```

### Answer

✅ Instance changes

---

## 3️⃣ What changes here?

```sql
ALTER TABLE Student
ADD Address VARCHAR(100);
```

### Answer

✅ Schema changes  
✅ Instance affected

---

## 4️⃣ True or False

### a) Schema changes frequently

❌ False

### b) Instance contains actual data

✅ True

### c) Schema contains rows

❌ False

---

# 🚀 FAANG-Level Conceptual Question

## Question

Why is schema usually stable while instance changes continuously?

### Answer

Schema defines the structure of the database, which is designed carefully and rarely modified.

Instance changes continuously because users keep inserting, updating, and deleting records during normal database operations.

---

# 📌 Super Important Revision

| Concept | Remember |
|---|---|
| Schema | Structure |
| Instance | Actual Data |
| Schema | Rarely changes |
| Instance | Frequently changes |
| Schema | Blueprint |
| Instance | Real records |

---

# 🎯 Final One-Line Definitions

## Schema
> The overall logical structure/design of a database.

## Instance
> The actual data stored in the database at a particular time.

---

