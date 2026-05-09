# 📘 Relational Query Language (RQL)

*(FAANG + Interview + GitHub Ready Notes)*

---

# 🔥 What is Relational Query Language?

Relational Query Language (RQL) is a language used to:
- retrieve data
- manipulate data
- query relations (tables)

from a relational database.

It allows users to:
- search records
- filter data
- combine tables
- perform operations on relations

---

# 🧠 Simple Definition

> Relational Query Language is used to perform operations on relational tables.

---

# 📌 Why RQL is Needed?

Suppose a database contains millions of records.

Without query language:
❌ retrieving useful information becomes difficult.

RQL helps:
- retrieve specific data
- combine tables
- filter records
- perform calculations
- analyze data efficiently

---

# 🔥 Example

## Students Table

| StudentID | Name | Marks |
|---|---|---|
| 1 | Riya | 90 |
| 2 | Aman | 70 |
| 3 | Neha | 85 |

---

## Query

```sql
SELECT Name
FROM Students
WHERE Marks > 80;
```

---

## Output

| Name |
|---|
| Riya |
| Neha |

---

# 🎯 Main Goal of RQL

RQL is used to:
# ✅ Ask questions from database

Examples:
- Which students scored above 80?
- Which employees work in HR?
- Which products cost more than 500?

---

# 🔥 Types of Relational Query Languages

There are mainly 2 types:

| Type | Nature |
|---|---|
| Relational Algebra | Procedural |
| Relational Calculus | Non-Procedural |

---

# 1️⃣ Relational Algebra

Most important topic in DBMS theory.

Used heavily in:
- interviews
- query optimization
- SQL internals
- database engines

---

# 📌 What is Relational Algebra?

Relational Algebra is:
# ✅ Procedural Query Language

Meaning:
It specifies:
# ✅ HOW to retrieve data

step-by-step.

---

# 🧠 Example

SQL Query:

```sql
SELECT Name
FROM Students
WHERE Marks > 80;
```

Relational Algebra:

```text
π Name (σ Marks > 80 (Students))
```

Meaning:
1. Select rows where Marks > 80
2. Project Name column

---

# 📌 Important Point

Relational Algebra works on:
# ✅ Relations (Tables)

And returns:
# ✅ Relations (Tables)

This is called:

# ✅ Closure Property

---

# 🔥 Characteristics of Relational Algebra

| Feature | Meaning |
|---|---|
| Procedural | Specifies HOW |
| Relation-based | Works on tables |
| Closed system | Output is also relation |
| Foundation of SQL | SQL internally uses algebra concepts |

---

# 2️⃣ Relational Calculus

More theoretical compared to algebra.

---

# 📌 What is Relational Calculus?

Relational Calculus is:
# ✅ Non-Procedural Query Language

Meaning:
It specifies:
# ✅ WHAT data is needed

NOT how to retrieve it.

---

# 🧠 Example

Instead of writing steps:

```text
Find students whose marks > 80
```

DBMS decides:
- execution plan
- optimization
- searching method

---

# 🔥 Types of Relational Calculus

| Type | Uses |
|---|---|
| Tuple Relational Calculus (TRC) | Tuples |
| Domain Relational Calculus (DRC) | Attribute values |

---

# 🎯 Relational Algebra vs Relational Calculus

| Relational Algebra | Relational Calculus |
|---|---|
| Procedural | Non-Procedural |
| HOW to retrieve | WHAT to retrieve |
| Operational | Declarative |
| Step-by-step execution | Condition-based |

---

# 🔥 SQL Connection

SQL is based heavily on:
# ✅ Relational Algebra
AND
# ✅ Relational Calculus

---

# 🧠 Example

SQL Query:

```sql
SELECT Name
FROM Students
WHERE Marks > 80;
```

---

## Relational Algebra Representation

```text
π Name (σ Marks > 80 (Students))
```

---

## Relational Calculus Idea

```text
Find all tuples where Marks > 80
```

---

# 🔥 Why Relational Algebra is Important?

It helps understand:
- joins
- filtering
- projections
- query optimization
- SQL execution
- database internals

---

# 🚀 FAANG Interview Importance

Companies like:
- :contentReference[oaicite:0]{index=0}
- :contentReference[oaicite:1]{index=1}
- :contentReference[oaicite:2]{index=2}

may ask:
- relational algebra queries
- query execution
- SQL internals
- optimization logic

especially for:
- backend engineering
- systems roles
- database engineering

---

# 🔥 Important Terms

| Term | Meaning |
|---|---|
| Relation | Table |
| Tuple | Row |
| Attribute | Column |
| Query | Request for data |
| Procedural | HOW |
| Non-Procedural | WHAT |

---

# 🧠 Real-Life Analogy

---

## Procedural (Relational Algebra)

```text
1. Take bread
2. Add butter
3. Toast it
4. Serve
```

You specify:
# ✅ HOW

---

## Non-Procedural (Relational Calculus)

```text
I want a sandwich.
```

You specify:
# ✅ WHAT

Chef decides how.

---

# 🔥 Practice Questions

## 1️⃣ What is Relational Query Language?

### ✅ Answer
Language used to retrieve and manipulate relational data.

---

## 2️⃣ Why is relational algebra procedural?

### ✅ Answer
Because it specifies step-by-step HOW to retrieve data.

---

## 3️⃣ Difference between relational algebra and calculus?

### ✅ Answer

| Relational Algebra | Relational Calculus |
|---|---|
| Procedural | Non-Procedural |
| HOW | WHAT |

---

## 4️⃣ Which language specifies HOW to retrieve data?

### ✅ Answer
Relational Algebra

---

## 5️⃣ Which language specifies WHAT data is needed?

### ✅ Answer
Relational Calculus

---

## 6️⃣ SQL is based on which concepts?

### ✅ Answer
Relational Algebra + Relational Calculus

---

# 🎯 Microsoft-Level Interview Questions

---

## Q1. Why is relational algebra important internally in DBMS?

### ✅ Answer
Because query optimization and execution plans are based on relational algebra operations.

---

## Q2. Why is SQL considered declarative?

### ✅ Answer
Because users specify WHAT data they want, not how DBMS retrieves it.

---

## Q3. What is closure property in relational algebra?

### ✅ Answer
Operations take relations as input and produce relations as output.

---

# 🧠 Quick Revision Table

| Concept | Remember |
|---|---|
| RQL | Query language for relational DB |
| Relational Algebra | Procedural |
| Relational Calculus | Non-Procedural |
| SQL | Based on both |
| Closure Property | Output is relation |

---

# 🚀 Next Topic

# 🔥 Relational Algebra

Including:
- basics
- syntax
- operators
- symbols
- SQL connection
- interview questions

Then:
# 🚀 Six Basic Operations
- Selection (σ)
- Projection (π)
- Union (∪)
- Set Difference (−)
- Cartesian Product (×)
- Rename (ρ)