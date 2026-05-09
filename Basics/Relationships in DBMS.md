# 📘 Relational Model Basics & Relationships in DBMS

*(FAANG + Interview + GitHub Ready Notes)*

---

# 🔥 Introduction

The Relational Model is the most important and most widely used data model in DBMS.

Modern relational databases like:
- :contentReference[oaicite:0]{index=0}
- :contentReference[oaicite:1]{index=1}
- :contentReference[oaicite:2]{index=2}
- :contentReference[oaicite:3]{index=3}

are based on this model.

The relational model stores data in the form of:
# ✅ Tables

---

# 📌 Why Relational Model Became Popular?

Because it provides:

✅ Simple table structure  
✅ Easy querying using SQL  
✅ Strong relationships  
✅ Data consistency  
✅ Integrity constraints  
✅ Easy normalization  

---

# 🔥 Basic Concepts of Relational Model

| Concept | Meaning |
|---|---|
| Relation | Table |
| Tuple | Row |
| Attribute | Column |
| Domain | Allowed values |
| Degree | Number of columns |
| Cardinality | Number of rows |

---

# 1️⃣ Relation

## Definition

A Relation is a table in the relational model.

---

# 📌 Example

| StudentID | Name | Marks |
|---|---|---|
| 101 | Riya | 85 |
| 102 | Aman | 90 |

This complete table is called:
# ✅ Relation

---

# 📌 Characteristics

✅ Organized in rows and columns  
✅ Stores related data  
✅ Has unique name  
✅ Represents real-world entity  

---

# 🎯 Interview Question

## Q. What is a Relation in DBMS?

### Answer

A Relation is a table that stores related data in rows and columns.

---

# 2️⃣ Tuple

## Definition

A Tuple is a single row in a relation.

---

# 📌 Example

| StudentID | Name | Marks |
|---|---|---|
| 101 | Riya | 85 |

This row is one tuple.

---

# 📌 Important Point

Each tuple represents:
# ✅ One record

---

# 📌 Characteristics

✅ Represents single entity instance  
✅ Contains attribute values  
✅ Stored as row  

---

# 🎯 Interview Question

## Q. What is a Tuple?

### Answer

A Tuple is a single row or record in a relation.

---

# 3️⃣ Attribute

## Definition

An Attribute is a column in a relation.

---

# 📌 Example

| StudentID | Name | Marks |
|---|---|---|

Here:
- StudentID
- Name
- Marks

are attributes.

---

# 📌 Important Point

Attributes define:
# ✅ Properties of entities

---

# 📌 Characteristics

✅ Column in table  
✅ Defines data type  
✅ Describes entity property  

---

# 🎯 Interview Question

## Q. What is an Attribute in DBMS?

### Answer

An Attribute is a column representing a property of an entity.

---

# 4️⃣ Domain

## Definition

A Domain defines the set of allowed values for an attribute.

---

# 📌 Example

Attribute:

```text
Marks
```

Allowed values:

```text
0 → 100
```

This allowed range is called:
# ✅ Domain

---

# 📌 Another Example

Attribute:

```text
Gender
```

Domain:

```text
Male, Female, Other
```

---

# 📌 Why Important?

Domains help maintain:
- validity
- integrity
- consistency

---

# 🎯 Interview Question

## Q. What is Domain in DBMS?

### Answer

A Domain is the set of permitted values for an attribute.

---

# 5️⃣ Degree

## Definition

Degree is the total number of attributes (columns) in a relation.

---

# 📌 Example

| ID | Name | Marks |
|---|---|---|

Number of columns:
- ID
- Name
- Marks

Degree:
# ✅ 3

---

# 📌 Important Point

```text
Degree = Number of Columns
```

---

# 🎯 Interview Question

## Q. What is Degree of a relation?

### Answer

Degree is the number of attributes (columns) present in a relation.

---

# 6️⃣ Cardinality

## Definition

Cardinality is the total number of tuples (rows) in a relation.

---

# 📌 Example

| ID | Name |
|---|---|
| 101 | Riya |
| 102 | Aman |
| 103 | Priya |

Total rows:
# ✅ 3

So cardinality = 3

---

# 📌 Important Point

```text
Cardinality = Number of Rows
```

---

# 🎯 Interview Question

## Q. What is Cardinality in DBMS?

### Answer

Cardinality is the number of tuples (rows) present in a relation.

---

# 🔥 Relationships in Relational Model

Relationships describe how tables are connected.

---

# 📌 Types of Relationships

1️⃣ One-to-One (1:1)  
2️⃣ One-to-Many (1:N)  
3️⃣ Many-to-Many (M:N)  

---

# 1️⃣ One-to-One Relationship (1:1)

## Definition

One record in Table A is related to only one record in Table B.

---

# 📌 Example

## Person ↔ Passport

| PersonID | PassportID |
|---|---|
| 1 | P101 |

One person has one passport.

One passport belongs to one person.

---

# 📌 Real-Life Examples

- Person ↔ Passport
- Employee ↔ Locker
- User ↔ Aadhaar

---

# 🎯 Interview Question

## Q. What is One-to-One relationship?

### Answer

A relationship where one record in one table is associated with only one record in another table.

---

# 2️⃣ One-to-Many Relationship (1:N)

## Definition

One record in Table A can relate to many records in Table B.

But one record in Table B relates to only one record in Table A.

---

# 📌 Example

## Department ↔ Students

| Department | Student |
|---|---|
| CS | Riya |
| CS | Aman |

One department has many students.

Each student belongs to one department.

---

# 📌 Real-Life Examples

- Department → Employees
- Teacher → Students
- Customer → Orders

---

# 🎯 Interview Question

## Q. What is One-to-Many relationship?

### Answer

A relationship where one record can be associated with multiple records in another table.

---

# 3️⃣ Many-to-Many Relationship (M:N)

## Definition

Multiple records in Table A can relate to multiple records in Table B.

---

# 📌 Example

## Students ↔ Courses

| Student | Course |
|---|---|
| Riya | DBMS |
| Riya | OS |
| Aman | DBMS |

One student can enroll in many courses.

One course can have many students.

---

# 📌 Real-Life Examples

- Students ↔ Courses
- Actors ↔ Movies
- Customers ↔ Products

---

# 🎯 Interview Question

## Q. Why is Many-to-Many relationship complex?

### Answer

Because both tables can contain multiple matching records, requiring an intermediate mapping mechanism.

---

# 🔥 Junction Table Concept

Many-to-Many relationships are implemented using:
# ✅ Junction Table

Also called:
- Bridge Table
- Mapping Table

---

# 📌 Example

## Students Table

| StudentID | Name |
|---|---|
| 1 | Riya |

---

## Courses Table

| CourseID | Course |
|---|---|
| 101 | DBMS |

---

## Enrollment Table (Junction Table)

| StudentID | CourseID |
|---|---|
| 1 | 101 |

This table connects:
- students
- courses

---

# 📌 Why Junction Table Needed?

Because relational databases cannot directly store many-to-many relationships efficiently.

---

# 🎯 Interview Question

## Q. What is a Junction Table?

### Answer

A Junction Table is an intermediate table used to implement many-to-many relationships.

---

# 🔥 Relationship Comparison

| Relationship | Meaning |
|---|---|
| 1:1 | One ↔ One |
| 1:N | One ↔ Many |
| M:N | Many ↔ Many |

---

# 🎯 Microsoft / FAANG Interview Questions

---

## Q1. What is the difference between Degree and Cardinality?

### Answer

- Degree = Number of columns
- Cardinality = Number of rows

---

## Q2. What is a Tuple?

### Answer

A Tuple is a row in a relation.

---

## Q3. Why are Domains important?

### Answer

Domains enforce valid and meaningful values for attributes.

---

## Q4. Which relationship requires a junction table?

### Answer

Many-to-Many relationship.

---

## Q5. Why is relational model widely used?

### Answer

Because it provides:
- simplicity
- SQL support
- integrity
- structured data management

---

# 🧠 Practice Questions

---

## 1️⃣ Match the Following

| Concept | Meaning |
|---|---|
| Relation | Table |
| Tuple | Row |
| Attribute | Column |
| Domain | Allowed values |
| Degree | Number of columns |
| Cardinality | Number of rows |

---

## 2️⃣ True or False

### a) Tuple means row.

✅ True

---

### b) Degree means number of rows.

❌ False

---

### c) Many-to-Many uses junction table.

✅ True

---

## 3️⃣ Identify the Relationship

### A)

One customer → many orders

✅ One-to-Many

---

### B)

Students ↔ Courses

✅ Many-to-Many

---

### C)

Person ↔ Passport

✅ One-to-One

---

# 🚀 FAANG-Level Conceptual Questions

---

## Q1. Why are relational databases so successful?

### Answer

Because they provide:
- structured organization
- strong consistency
- SQL querying
- integrity constraints
- normalization support

---

## Q2. Why are many-to-many relationships difficult?

### Answer

Because relational systems require separate mapping tables to efficiently manage multiple associations.

---

## Q3. Why are domains important in enterprise systems?

### Answer

Domains prevent invalid data and maintain consistency across applications.

---

# 📌 Quick Revision

| Concept | Remember |
|---|---|
| Relation | Table |
| Tuple | Row |
| Attribute | Column |
| Domain | Allowed values |
| Degree | Columns |
| Cardinality | Rows |
| 1:1 | One ↔ One |
| 1:N | One ↔ Many |
| M:N | Many ↔ Many |

---

# 🎯 One-Line Definitions

## Relation
> Table storing related data.

## Tuple
> Single row in a table.

## Attribute
> Column representing property.

## Domain
> Allowed set of values.

## Degree
> Number of columns.

## Cardinality
> Number of rows.

## Junction Table
> Intermediate table for many-to-many relationships.

---

