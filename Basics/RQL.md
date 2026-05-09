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
# 📘 Relational Algebra (RA)

*(FAANG + Interview + GitHub Ready Notes)*

---

# 🔥 What is Relational Algebra?

Relational Algebra is a:
# ✅ Procedural Query Language

used in relational databases to:
- retrieve data
- manipulate relations
- perform operations on tables

---

# 🧠 Simple Definition

> Relational Algebra is a set of operations performed on relations (tables).

---

# 🎯 Main Idea

Relational Algebra tells:
# ✅ HOW to retrieve data

step-by-step.

---

# 📌 Example

## Students Table

| StudentID | Name | Marks |
|---|---|---|
| 1 | Riya | 90 |
| 2 | Aman | 70 |
| 3 | Neha | 85 |

---

## SQL Query

```sql
SELECT Name
FROM Students
WHERE Marks > 80;
```

---

## Relational Algebra

```text
π Name (σ Marks > 80 (Students))
```

Meaning:
1. Select rows where Marks > 80
2. Project Name column

---

# 🔥 Why Relational Algebra is Important?

Relational Algebra is:
# ✅ Foundation of SQL

DBMS internally converts SQL queries into relational algebra operations.

---

# 🚀 Used In

- Query optimization
- Execution planning
- SQL processing
- Database engines

---

# 🔥 Characteristics of Relational Algebra

| Feature | Meaning |
|---|---|
| Procedural | Specifies HOW |
| Relation-based | Works on tables |
| Closed System | Output is also relation |
| Mathematical | Based on set theory |
| Foundation of SQL | SQL internally uses RA |

---

# 📌 Closure Property

Very important concept.

---

# 🧠 What is Closure Property?

In relational algebra:

# ✅ Input → Relation
# ✅ Output → Relation

Meaning:
every operation produces another table.

---

# 🧠 Example

```text
σ Marks > 80 (Students)
```

Input:
- Students table

Output:
- another relation

Hence:
# ✅ Closure Property

---

# 🔥 Why Closure Property is Powerful?

Because operations can be chained together.

---

# 🧠 Example

```text
π Name (σ Marks > 80 (Students))
```

Output of selection becomes input for projection.

---

# 🔥 Types of Relational Algebra Operations

There are two categories:

| Type | Operations |
|---|---|
| Basic Operations | Fundamental operations |
| Derived Operations | Built using basic operations |

---

# 1️⃣ Basic Operations (Core Six)

| Operation | Symbol | Purpose |
|---|---|---|
| Selection | σ | Select rows |
| Projection | π | Select columns |
| Union | ∪ | Combine relations |
| Set Difference | − | Subtract relations |
| Cartesian Product | × | Pair tuples |
| Rename | ρ | Rename relation |

---

# 2️⃣ Derived Operations

| Operation | Purpose |
|---|---|
| Join | Combine related tables |
| Intersection | Common tuples |
| Division | Complex queries |

---

# 🔥 Operands in Relational Algebra

Operands are:
# ✅ Relations (Tables)

Examples:

```text
Students
Courses
Enrollment
```

Operations work on these relations.

---

# 🔥 Output of Relational Algebra

Output is always:
# ✅ Relation (Table)

This forms:
# ✅ Closed Algebraic System

---

# 🔥 Set Theory Connection

Relational Algebra is based heavily on:
# ✅ Set Theory

because relations behave like mathematical sets.

---

# 📌 Important Set Properties

Relations:
- avoid duplicate tuples
- are unordered
- support set operations

---

# 🔥 Procedural Nature

Very important interview concept.

---

# 🧠 What Does Procedural Mean?

It means:
# ✅ Specify steps for retrieval

---

# 🧠 Example

```text
1. Select rows
2. Project columns
3. Combine results
```

You define:
# ✅ HOW data is retrieved

---

# 🔥 Relational Algebra vs SQL

| Relational Algebra | SQL |
|---|---|
| Procedural | Declarative |
| Mathematical | User-friendly |
| Internal representation | User query language |

---

# 🧠 Example

## SQL

```sql
SELECT Name
FROM Students
WHERE Marks > 80;
```

---

## Relational Algebra

```text
π Name (σ Marks > 80 (Students))
```

---

# 🔥 Why DBMS Uses Relational Algebra Internally?

Because relational algebra operations:
- can be optimized
- reordered
- combined
- executed efficiently

---

# 🧠 Query Optimization Example

DBMS may:
- perform selection first
- reduce tuples early
- minimize joins

to improve performance.

---

# 🎯 FAANG-Level Insight

Large systems like:
- :contentReference[oaicite:0]{index=0}
- :contentReference[oaicite:1]{index=1}
- :contentReference[oaicite:2]{index=2}

internally optimize queries using relational algebra trees.

---

# 🔥 Relational Algebra Expression Structure

General format:

```text
Operation (Relation)
```

Example:

```text
σ Marks > 80 (Students)
```

---

# 🔥 Important Symbols

| Symbol | Meaning |
|---|---|
| σ | Selection |
| π | Projection |
| ∪ | Union |
| − | Difference |
| × | Cartesian Product |
| ρ | Rename |
| ⨝ | Join |

---

# 🧠 Real-Life Analogy

Suppose database is a library.

Relational algebra operations are like:
- filtering books
- selecting authors
- combining lists
- removing records

---

# 🔥 Practice Questions

---

## 1️⃣ What is relational algebra?

### ✅ Answer
Procedural query language used to operate on relations.

---

## 2️⃣ Why is relational algebra procedural?

### ✅ Answer
Because it specifies HOW data is retrieved.

---

## 3️⃣ What is closure property?

### ✅ Answer
Operations produce relations as output.

---

## 4️⃣ Why is closure property important?

### ✅ Answer
Because outputs can become inputs for further operations.

---

## 5️⃣ Which mathematical theory is relational algebra based on?

### ✅ Answer
Set Theory

---

## 6️⃣ Difference between SQL and relational algebra?

### ✅ Answer

| SQL | Relational Algebra |
|---|---|
| Declarative | Procedural |

---

# 🎯 Microsoft / Google Interview Questions

---

## Q1. Why is relational algebra important internally?

### ✅ Answer
Because DBMS query optimization depends on algebra operations.

---

## Q2. Why is closure property powerful?

### ✅ Answer
Because complex queries can be built by chaining operations.

---

## Q3. Why are selections usually pushed early in optimization?

### ✅ Answer
To reduce number of tuples processed later.

---

# 🧠 Quick Revision Table

| Concept | Remember |
|---|---|
| Relational Algebra | Procedural query language |
| Works On | Relations |
| Returns | Relations |
| Closure Property | Output is relation |
| Foundation | Set theory |
| SQL Relation | SQL internally uses RA |

---

# 🚀 Next Topic

# 🔥 Six Basic Operations of Relational Algebra

1️⃣ Selection (σ)  \n
2️⃣ Projection (π)  \n
3️⃣ Union (∪)  \n
4️⃣ Set Difference (−)  \n
5️⃣ Cartesian Product (×)  \n
6️⃣ Rename (ρ)  


# 🔥 Selection Operation (σ)

*(FAANG + Interview + GitHub Ready Notes)*

---

# 📘 What is Selection Operation?

Selection operation is used to:
# ✅ Select specific rows (tuples)

from a relation (table)
based on a condition.

---

# 🧠 Simple Definition

> Selection filters rows from a table.

---

# 🎯 Main Purpose

Selection is used when we want:
- only specific records
- filtered data
- conditional retrieval

---

# 🔥 Symbol of Selection

# ✅ Sigma (σ)

```text
σcondition(Relation)
```

---

# 📌 General Syntax

```text
σcondition(Relation)
```

---

# 🧠 Meaning of Syntax

| Part | Meaning |
|---|---|
| σ | Selection |
| condition | Filtering condition |
| Relation | Table name |

---

# 🔥 Example Table

## Students

| StudentID | Name | Marks | City |
|---|---|---|---|
| 1 | Riya | 90 | Bhopal |
| 2 | Aman | 70 | Delhi |
| 3 | Neha | 85 | Bhopal |
| 4 | Kunal | 60 | Mumbai |

---

# 🔥 Example 1 — Basic Selection

## Problem

Find students with marks greater than 80.

---

## Relational Algebra

```text
σMarks>80(Students)
```

---

## Output

| StudentID | Name | Marks | City |
|---|---|---|---|
| 1 | Riya | 90 | Bhopal |
| 3 | Neha | 85 | Bhopal |

---

# 🧠 What Happened?

DBMS:
- scanned rows
- checked condition
- returned matching tuples

---

# 🔥 SQL Equivalent

```sql
SELECT *
FROM Students
WHERE Marks > 80;
```

---

# 🔥 Example 2 — Equality Condition

## Problem

Find students from Bhopal.

---

## Relational Algebra

```text
σCity='Bhopal'(Students)
```

---

## Output

| StudentID | Name | Marks | City |
|---|---|---|---|
| 1 | Riya | 90 | Bhopal |
| 3 | Neha | 85 | Bhopal |

---

# 🔥 Example 3 — Multiple Conditions

## Problem

Find students:
- from Bhopal
- and marks > 80

---

## Relational Algebra

```text
σCity='Bhopal' ∧ Marks>80(Students)
```

---

## Output

| StudentID | Name | Marks | City |
|---|---|---|---|
| 1 | Riya | 90 | Bhopal |
| 3 | Neha | 85 | Bhopal |

---

# 🔥 Conditional Operators Used

| Operator | Meaning |
|---|---|
| = | Equal |
| ≠ | Not equal |
| > | Greater than |
| < | Less than |
| ≥ | Greater than equal |
| ≤ | Less than equal |

---

# 🔥 Logical Operators

| Operator | Meaning |
|---|---|
| ∧ | AND |
| ∨ | OR |
| ¬ | NOT |

---

# 🧠 Example 4 — OR Condition

## Problem

Find students:
- from Delhi
OR
- marks > 85

---

## Relational Algebra

```text
σCity='Delhi' ∨ Marks>85(Students)
```

---

# 🔥 Example 5 — NOT Operator

## Problem

Find students NOT from Mumbai.

---

## Relational Algebra

```text
σ¬(City='Mumbai')(Students)
```

---

# 🔥 Important Property

Selection operation:
# ✅ does NOT change columns

It only filters:
# ✅ rows

---

# 📌 Input vs Output

| Input | Output |
|---|---|
| Same columns | Same columns |
| All rows | Filtered rows |

---

# 🔥 Real-Life Analogy

Suppose a college database contains 10,000 students.

You want:
# ✅ Only students with marks > 90

Selection operation acts like:
# ✅ applying filters

similar to:
- Amazon filters
- Netflix filters
- search filters

---

# 🔥 Selection Conditions

Selection can use:
- single condition
- multiple conditions
- nested conditions

---

# 🔥 Selection and Query Optimization

Very important FAANG concept.

---

# 🧠 Why DBMS Performs Selection Early?

Because:
# ✅ it reduces tuples quickly

Smaller data means:
- faster joins
- less memory
- better performance

---

# 🎯 Optimization Example

Instead of:

```text
Join huge tables first
```

DBMS may:

```text
Apply selection first
```

to reduce rows.

---

# 🔥 Selection is Unary Operation

Unary means:
# ✅ operates on one relation only

---

# 📌 Example

```text
σMarks>80(Students)
```

Only:
# ✅ Students relation used

---

# 🔥 Important Characteristics

| Feature | Meaning |
|---|---|
| Unary | One table |
| Row filtering | Filters tuples |
| Same attributes | Columns unchanged |
| Conditional | Based on predicates |

---

# 🎯 FAANG Interview Questions

---

## Q1. Does selection change schema?

### ✅ Answer
❌ No.

It changes rows only.

---

## Q2. Why is selection pushed early in optimization?

### ✅ Answer
To reduce number of tuples processed later.

---

## Q3. Is selection unary or binary?

### ✅ Answer
Unary.

---

## Q4. Difference between selection and projection?

### ✅ Answer

| Selection | Projection |
|---|---|
| Filters rows | Filters columns |

---

# 🔥 Practice Questions

---

## 1️⃣ Find students with marks less than 75.

### ✅ Answer

```text
σMarks<75(Students)
```

---

## 2️⃣ Find students from Delhi.

### ✅ Answer

```text
σCity='Delhi'(Students)
```

---

## 3️⃣ Find students:
- from Bhopal
- and marks > 85

### ✅ Answer

```text
σCity='Bhopal' ∧ Marks>85(Students)
```

---

## 4️⃣ Which operator is used for selection?

### ✅ Answer
σ

---

## 5️⃣ Does selection remove columns?

### ✅ Answer
❌ No.

---

# 🧠 Microsoft-Level Scenario

Suppose:
- Employees table contains 10 million rows.

Query:

```sql
SELECT *
FROM Employees
WHERE Department = 'HR';
```

DBMS internally performs:
# ✅ Selection operation first

to reduce rows before:
- joins
- sorting
- grouping

This improves performance significantly.

---

# 🧠 Quick Revision Table

| Concept | Remember |
|---|---|
| Selection | Filters rows |
| Symbol | σ |
| Unary | One relation |
| Output | Same columns |
| Main Use | Conditional retrieval |

---

# 🚀 Next Topic

# 🔥 Projection Operation (π)

Used to:
# ✅ Select specific columns

Important for:
- reducing attributes
- minimizing unnecessary data
- optimization

# 🔥 Projection Operation (π)

*(FAANG + Interview + GitHub Ready Notes)*

---

# 📘 What is Projection Operation?

Projection operation is used to:
# ✅ Select specific columns (attributes)

from a relation (table).

---

# 🧠 Simple Definition

> Projection filters columns from a table.

---

# 🎯 Main Purpose

Projection is used when:
- only required attributes are needed
- unnecessary columns must be removed
- query optimization is required

---

# 🔥 Symbol of Projection

# ✅ Pi (π)

```text
πattributes(Relation)
```

---

# 📌 General Syntax

```text
πA1, A2, A3...(Relation)
```

---

# 🧠 Meaning of Syntax

| Part | Meaning |
|---|---|
| π | Projection |
| Attributes | Required columns |
| Relation | Table name |

---

# 🔥 Example Table

## Students

| StudentID | Name | Marks | City |
|---|---|---|---|
| 1 | Riya | 90 | Bhopal |
| 2 | Aman | 70 | Delhi |
| 3 | Neha | 85 | Bhopal |
| 4 | Kunal | 60 | Mumbai |

---

# 🔥 Example 1 — Single Column

## Problem

Show only student names.

---

## Relational Algebra

```text
πName(Students)
```

---

## Output

| Name |
|---|
| Riya |
| Aman |
| Neha |
| Kunal |

---

# 🔥 SQL Equivalent

```sql
SELECT Name
FROM Students;
```

---

# 🔥 Example 2 — Multiple Columns

## Problem

Show Name and Marks.

---

## Relational Algebra

```text
πName, Marks(Students)
```

---

## Output

| Name | Marks |
|---|---|
| Riya | 90 |
| Aman | 70 |
| Neha | 85 |
| Kunal | 60 |

---

# 🔥 Important Property

Projection:
# ✅ changes columns (schema changes)

---

# 🧠 Duplicate Removal Rule

Projection in relational algebra:
# ✅ removes duplicate tuples automatically

Because:
- relations follow set theory
- sets do not allow duplicates

---

# 🔥 Example 3 — Duplicate Case

## Problem

Show only City.

---

## Relational Algebra

```text
πCity(Students)
```

---

## Raw Data

| City |
|---|
| Bhopal |
| Delhi |
| Bhopal |
| Mumbai |

---

## Final Output

| City |
|---|
| Bhopal |
| Delhi |
| Mumbai |

---

# 🔥 Projection is Unary Operation

Unary means:
# ✅ operates on one relation only

---

# 📌 Example

```text
πName(Students)
```

Only one table involved → Students

---

# 🔥 Projection vs Selection

| Projection (π) | Selection (σ) |
|---|---|
| Filters columns | Filters rows |
| Changes schema | Does not change schema |
| Attribute-based | Condition-based |
| Unary | Unary |

---

# 🧠 Example Difference

## Selection

```text
σMarks > 80(Students)
```

👉 Filters rows

---

## Projection

```text
πName(Students)
```

👉 Filters columns

---

# 🔥 Combined Operation (Very Important)

## Example

Find names of students with Marks > 80

```text
πName(σMarks > 80(Students))
```

---

# 🧠 Execution Order

1. Selection (filter rows)
2. Projection (select columns)

---

# 🔥 Why Projection is Important?

✔ Reduces data size  
✔ Improves performance  
✔ Reduces memory usage  
✔ Optimizes query execution  

---

# 🔥 Real-Life Analogy

Database = big Excel sheet

Projection = selecting only needed columns like:
- Name only
- Marks only

instead of full sheet.

---

# 🎯 FAANG Interview Questions

---

## Q1. What does projection do?

### ✅ Answer
It selects specific columns from a relation.

---

## Q2. Does projection change schema?

### ✅ Answer
Yes, it changes schema because columns are reduced.

---

## Q3. Does projection remove duplicates?

### ✅ Answer
Yes, in relational algebra it removes duplicate tuples.

---

## Q4. Is projection unary or binary?

### ✅ Answer
Unary operation.

---

## Q5. Difference between selection and projection?

### ✅ Answer

| Selection | Projection |
|---|---|
| Filters rows | Filters columns |

---

# 🔥 Practice Questions

---

## 1️⃣ Get names of all students

```text
πName(Students)
```

---

## 2️⃣ Get Name and City

```text
πName, City(Students)
```

---

## 3️⃣ Which operation removes columns?

### ✅ Answer
Projection (π)

---

## 4️⃣ Which operation removes duplicates?

### ✅ Answer
Projection (π)

---

## 5️⃣ What is output of projection?

### ✅ Answer
A relation (table)

---

# 🧠 Microsoft-Level Insight

In real DBMS systems:
- projection reduces disk I/O
- improves query speed
- reduces network transfer in distributed databases

Example:

Instead of fetching:
- 10 columns

DBMS fetches:
- only 1 or 2 needed columns

---

# 🧠 Quick Revision Table

| Concept | Remember |
|---|---|
| Projection | Selects columns |
| Symbol | π |
| Unary | Yes |
| Schema change | Yes |
| Duplicate removal | Yes |
| Main use | Reduce attributes |

---

# 🚀 Next Topic

# 🔥 Union Operation (∪)

Used to:
- combine two relations
- merge datasets
- perform set-based queries


