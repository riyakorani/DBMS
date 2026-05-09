# 📘 Data Models in DBMS

*(FAANG + Interview + GitHub Ready Notes)*

---

# 🔥 Introduction

A Data Model defines **how data is organized, stored, connected, and manipulated** inside a database.

It provides the blueprint for structuring data.

It tells:

- How data is stored
- How data is related
- How users interact with data
- How constraints are applied

Data models are one of the most fundamental concepts in DBMS.

---

# 📌 Why Data Models are Important?

Data models help in:

✅ Organizing data  
✅ Reducing redundancy  
✅ Defining relationships  
✅ Improving consistency  
✅ Efficient querying  
✅ Better database design  

---

# 📌 Types of Data Models

1️⃣ Hierarchical Model  
2️⃣ Network Model  
3️⃣ Relational Model  
4️⃣ Entity Relationship (ER) Model  
5️⃣ Object-Oriented Model  
6️⃣ Semi-Structured Model  

---

# 1️⃣ Hierarchical Data Model

## Definition

The Hierarchical Model organizes data in a **tree-like structure**.

It follows:

```text
Parent → Child
```

Each child has **only one parent**.

---

# 📌 Structure

```text
College
   ├── Department
   │      ├── Students
   │      └── Teachers
```

---

# 📌 Characteristics

✅ Tree structure  
✅ One-to-many relationship  
✅ Fast traversal  
✅ Easy parent-child representation  

---

# 📌 Real-Life Example

File system directories:

```text
C:
 ├── Users
 │   └── Documents
```

---

# 📌 Advantages

- Simple structure
- Fast access
- Easy implementation

---

# 📌 Disadvantages

- No many-to-many support
- Rigid structure
- Difficult restructuring

---

# 🎯 Interview Question

## Q. Why is hierarchical model limited?

### Answer

Because each child can have only one parent, making many-to-many relationships difficult.

---

# 2️⃣ Network Data Model

## Definition

The Network Model organizes data as a **graph structure**.

A child can have **multiple parents**.

---

# 📌 Structure

```text
Student ↔ Course
```

A student can enroll in multiple courses, and a course can have multiple students.

---

# 📌 Characteristics

✅ Graph structure  
✅ Many-to-many support  
✅ Flexible relationships  
✅ Efficient traversal

---

# 📌 Real-Life Example

Social networks:

```text
User ↔ Friends
```

---

# 📌 Advantages

- Supports complex relationships
- Efficient for connected data
- Better flexibility

---

# 📌 Disadvantages

- Complex design
- Harder maintenance
- Difficult implementation

---

# 🎯 Interview Question

## Q. Why is network model more flexible than hierarchical model?

### Answer

Because a child can have multiple parents, allowing many-to-many relationships.

---

# 3️⃣ Relational Data Model

## Definition

The Relational Model stores data in **tables (relations)**.

It is the most widely used model.

---

# 📌 Structure

| StudentID | Name | Marks |
|---|---|---|
| 101 | Riya | 85 |

---

# 📌 Components

- Rows → Tuples
- Columns → Attributes
- Table → Relation

---

# 📌 Characteristics

✅ Table-based  
✅ Easy querying using SQL  
✅ Data integrity  
✅ Strong relationships via keys

---

# 📌 Examples of DBMS Using Relational Model

- :contentReference[oaicite:0]{index=0}
- :contentReference[oaicite:1]{index=1}
- :contentReference[oaicite:2]{index=2}

---

# 📌 Advantages

- Simple design
- Powerful querying
- Data consistency
- Easy normalization

---

# 📌 Disadvantages

- Complex joins can be expensive
- Less flexible for unstructured data

---

# 🎯 Interview Question

## Q. Why is relational model popular?

### Answer

Because it provides simplicity, strong consistency, SQL support, and efficient structured data management.

---

# 4️⃣ Entity Relationship (ER) Model

## Definition

ER Model represents data using:

- Entities
- Attributes
- Relationships

Used for database design.

---

# 📌 Example

```text
Student --- Enrolls --- Course
```

---

# 📌 Components

## Entity

Real-world object

Examples:
- Student
- Employee

---

## Attribute

Properties of entity

Examples:
- Name
- Age

---

## Relationship

Connection between entities

Example:

Student enrolls in Course

---

# 📌 Advantages

- Easy visualization
- Better planning
- Clear relationships

---

# 📌 Disadvantages

- Not used for actual storage
- Must be converted to relational schema

---

# 🎯 Interview Question

## Q. Why is ER model important?

### Answer

Because it helps design and visualize database structure before implementation.

---

# 5️⃣ Object-Oriented Data Model

## Definition

Stores data as objects containing:

- data
- methods

Inspired by object-oriented programming.

---

# 📌 Example

```java
class Student {
   int id;
   String name;

   void display(){}
}
```

Database stores complete objects.

---

# 📌 Characteristics

✅ Supports inheritance  
✅ Supports encapsulation  
✅ Handles complex objects  

---

# 📌 Real-Life Use

Used in:
- CAD systems
- Multimedia systems
- Engineering applications

---

# 📌 Advantages

- Handles complex data
- Reusability
- Better for object-oriented apps

---

# 📌 Disadvantages

- Complex implementation
- Less standardization

---

# 🎯 Interview Question

## Q. Why use object-oriented data model?

### Answer

Because it efficiently handles complex real-world objects and integrates well with OOP languages.

---

# 6️⃣ Semi-Structured Data Model

## Definition

Semi-Structured Model stores flexible, schema-less data.

Common formats:

- JSON
- XML
- BSON

---

# 📌 Example

```json
{
 "name": "Riya",
 "marks": 85
}
```

---

# 📌 Characteristics

✅ Flexible schema  
✅ Dynamic structure  
✅ Good for web applications  
✅ Supports nested data

---

# 📌 Examples of DBMS

- :contentReference[oaicite:3]{index=3}
- XML databases

---

# 📌 Advantages

- Highly flexible
- Easy schema evolution
- Handles unstructured data

---

# 📌 Disadvantages

- Harder consistency enforcement
- Less strict validation

---

# 🎯 Interview Question

## Q. Why is semi-structured model useful for modern apps?

### Answer

Because modern applications often deal with dynamic and rapidly changing data structures.

---

# 🔥 Comparison Table

| Model | Structure |
|---|---|
| Hierarchical | Tree |
| Network | Graph |
| Relational | Tables |
| ER | Diagrammatic |
| Object-Oriented | Objects |
| Semi-Structured | JSON/XML |

---

# 🎯 Microsoft / FAANG Interview Questions

---

## Q1. Which data model is most commonly used?

### Answer

Relational Model

---

## Q2. Which model supports many-to-many naturally?

### Answer

Network Model

---

## Q3. Which model is used for DB design?

### Answer

ER Model

---

## Q4. Which model supports flexible schema?

### Answer

Semi-Structured Model

---

## Q5. Which model follows OOP principles?

### Answer

Object-Oriented Model

---

# 🧠 Practice Questions

---

## 1️⃣ Match the Following

| Model | Structure |
|---|---|
| Hierarchical | Tree |
| Network | Graph |
| Relational | Table |
| ER | Entity Relationship |
| OOP | Objects |
| Semi-Structured | JSON/XML |

---

## 2️⃣ True or False

### a) Relational model stores data in graphs

❌ False

---

### b) ER model is mainly used for design

✅ True

---

### c) JSON belongs to semi-structured model

✅ True

---

# 🚀 FAANG-Level Conceptual Questions

---

## Q1. Why did relational model become dominant?

### Answer

Because it offers:
- simplicity
- SQL support
- strong consistency
- easy querying

---

## Q2. Why is semi-structured model important today?

### Answer

Because web-scale applications require flexible schemas and fast schema evolution.

---

## Q3. Why are hierarchical systems less common now?

### Answer

Because they are rigid and poorly support many-to-many relationships.

---

# 📌 Quick Revision

| Model | Remember |
|---|---|
| Hierarchical | Tree |
| Network | Graph |
| Relational | Tables |
| ER | Design |
| OOP | Objects |
| Semi-Structured | Flexible JSON/XML |

---

# 🎯 One-Line Definitions

## Hierarchical Model
> Organizes data in tree structure.

## Network Model
> Organizes data in graph structure.

## Relational Model
> Stores data in tables.

## ER Model
> Represents entities and relationships.

## Object-Oriented Model
> Stores objects with data and methods.

## Semi-Structured Model
> Stores flexible schema-less data.

---

