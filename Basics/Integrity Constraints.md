# 🔥 Integrity Constraints in DBMS — COMPLETE DEEP DIVE

*(FAANG + SQL + Database Reliability + Real Industry Systems)*

---

# 📘 What are Integrity Constraints?

Integrity Constraints are:
# ✅ rules applied on database data to maintain correctness, consistency, and reliability

They ensure:
- invalid data cannot enter database
- relationships remain correct
- duplication is controlled
- business rules are enforced

---

# 🧠 Simple Meaning

Integrity constraints act like:
# 🚀 database protection rules

They prevent:
- wrong entries
- broken references
- inconsistent records

---

# 🔥 Why Integrity Constraints are Important?

Without constraints:

❌ duplicate records  
❌ invalid references  
❌ inconsistent data  
❌ data corruption  
❌ unreliable systems  

With constraints:

✅ accurate data  
✅ consistency  
✅ reliable relationships  
✅ secure transactions  
✅ trustworthy database  

---

# 🔥 Real-World Example

In banking system:

| Invalid Situation | Constraint Preventing It |
|---|---|
| duplicate account number | primary key |
| invalid customer ID | foreign key |
| negative balance | check constraint |
| missing customer name | NOT NULL |

Used heavily in:
- :contentReference[oaicite:0]{index=0}
- :contentReference[oaicite:1]{index=1}
- :contentReference[oaicite:2]{index=2}
- :contentReference[oaicite:3]{index=3} systems

---

# 🔥 TYPES OF INTEGRITY CONSTRAINTS

We will deeply cover:

1️⃣ Domain Constraint  
2️⃣ Key Constraint  
3️⃣ Entity Integrity Constraint  
4️⃣ Referential Integrity Constraint  
5️⃣ NOT NULL Constraint  
6️⃣ UNIQUE Constraint  
7️⃣ CHECK Constraint  
8️⃣ DEFAULT Constraint  

---

# 🔥 OVERALL HIERARCHY

```text
Integrity Constraints
       ↓
Domain Constraints
Key Constraints
Entity Integrity
Referential Integrity
```

---

# 1️⃣ DOMAIN CONSTRAINT ⭐ VERY IMPORTANT

---

# 📘 Definition

Domain Constraint ensures:
# ✅ attribute values must belong to valid domain/range/type

---

# 🧠 Simple Meaning

Column values must:
- follow datatype
- follow allowed range
- follow allowed format

---

# 🧠 Example

## Age Column

Valid:
```text
18
25
40
```

Invalid:
```text
"Hello"
-5
```

---

# 🔥 Domain Includes

| Property | Example |
|---|---|
| Data Type | INT |
| Range | 1–100 |
| Format | Email format |
| Allowed Values | Male/Female |

---

# 🔥 SQL Example

```sql
Age INT CHECK (Age >= 18)
```

---

# 🎯 Interview Question

## Q. What is domain integrity?

✔ ensures values belong to valid domain

---

# 2️⃣ KEY CONSTRAINT ⭐ EXTREMELY IMPORTANT

---

# 📘 Definition

Key Constraint ensures:
# ✅ certain attributes uniquely identify tuples

---

# 🧠 Example

## Students

| StudentID | Name |
|---|---|
| 101 | Riya |
| 102 | Aman |

StudentID must be unique.

---

# 🔥 Why Important?

Without key constraint:

❌ duplicate rows possible

---

# 🔥 Types of Keys Used

| Key | Purpose |
|---|---|
| Primary Key | main unique identifier |
| Candidate Key | possible unique identifier |
| Unique Key | enforce uniqueness |

---

# 🔥 SQL Example

```sql
StudentID INT PRIMARY KEY
```

---

# 🎯 FAANG Insight

Key constraints:
# 🚀 foundation of indexing and relationships

---

# 3️⃣ ENTITY INTEGRITY CONSTRAINT ⭐ VERY IMPORTANT

---

# 📘 Definition

Entity Integrity states:
# ✅ primary key cannot be NULL

---

# 🧠 Why?

Every entity must:
# ✅ be uniquely identifiable

---

# 🧠 Invalid Example

| StudentID | Name |
|---|---|
| NULL | Riya |

Impossible to identify student uniquely.

---

# 🔥 Rule

```text
Primary Key ≠ NULL
```

---

# 🔥 SQL Example

```sql
StudentID INT PRIMARY KEY
```

Automatically:
- UNIQUE
- NOT NULL

---

# 🎯 Interview Question

## Q. Why primary key cannot be NULL?

✔ because entities must be identifiable uniquely

---

# 4️⃣ REFERENTIAL INTEGRITY CONSTRAINT ⭐ MOST IMPORTANT

---

# 📘 Definition

Referential Integrity ensures:
# ✅ foreign key values must match existing primary key values

---

# 🧠 Simple Meaning

You cannot reference:
# ❌ non-existing records

---

# 🧠 Example

## Departments

| DeptID | DeptName |
|---|---|
| D1 | CSE |
| D2 | IT |

---

## Students

| StudentID | DeptID |
|---|---|
| 101 | D1 |

Valid because:
```text
D1 exists
```

---

# 🔴 Invalid Example

| StudentID | DeptID |
|---|---|
| 102 | D100 |

Invalid because:
```text
D100 does not exist
```

---

# 🔥 Purpose

Maintains:
# ✅ relationship consistency

---

# 🔥 SQL Example

```sql
FOREIGN KEY (DeptID)
REFERENCES Departments(DeptID)
```

---

# 🔥 Referential Actions ⭐ IMPORTANT

When referenced row deleted/updated:

| Action | Meaning |
|---|---|
| CASCADE | automatic changes |
| SET NULL | foreign key becomes NULL |
| RESTRICT | prevent deletion |
| NO ACTION | reject operation |

---

# 🧠 Example

```sql
ON DELETE CASCADE
```

If department deleted:
- related students deleted automatically

---

# 🎯 FAANG Interview Question

## Q. Why referential integrity important?

✔ prevents broken relationships

---

# 5️⃣ NOT NULL CONSTRAINT

---

# 📘 Definition

NOT NULL ensures:
# ✅ attribute cannot contain NULL value

---

# 🧠 Example

Customer name mandatory.

---

# 🔥 SQL Example

```sql
Name VARCHAR(50) NOT NULL
```

---

# 🔥 Used For

| Example |
|---|
| Name |
| Email |
| Aadhaar |
| AccountNumber |

---

# 6️⃣ UNIQUE CONSTRAINT ⭐ IMPORTANT

---

# 📘 Definition

UNIQUE ensures:
# ✅ all values are unique

---

# 🧠 Example

Email IDs:
```text
must not repeat
```

---

# 🔥 Difference from Primary Key

| Feature | Primary Key | UNIQUE |
|---|---|---|
| Duplicate | ❌ | ❌ |
| NULL Allowed | ❌ | ✔ (depends DBMS) |

---

# 🔥 SQL Example

```sql
Email VARCHAR(100) UNIQUE
```

---

# 7️⃣ CHECK CONSTRAINT ⭐ VERY IMPORTANT

---

# 📘 Definition

CHECK ensures:
# ✅ condition must be true before insertion/update

---

# 🧠 Example

Salary must be positive.

---

# 🔥 SQL Example

```sql
Salary INT CHECK (Salary > 0)
```

---

# 🧠 Another Example

```sql
Age INT CHECK (Age >= 18)
```

---

# 🔥 Used For

| Rule |
|---|
| Marks ≤ 100 |
| Balance ≥ 0 |
| Age ≥ 18 |

---

# 🎯 Interview Question

## Q. Why CHECK constraint useful?

✔ enforces business rules

---

# 8️⃣ DEFAULT CONSTRAINT

---

# 📘 Definition

DEFAULT provides:
# ✅ automatic value if user does not provide one

---

# 🧠 Example

Default country:
```text
India
```

---

# 🔥 SQL Example

```sql
Country VARCHAR(50) DEFAULT 'India'
```

---

# 🧠 Insert Example

```sql
INSERT INTO Students(Name)
VALUES ('Riya');
```

Country automatically:
```text
India
```

---

# 🔥 COMPLETE SQL EXAMPLE ⭐ IMPORTANT

```sql
CREATE TABLE Students(
    StudentID INT PRIMARY KEY,
    Name VARCHAR(50) NOT NULL,
    Email VARCHAR(100) UNIQUE,
    Age INT CHECK (Age >= 18),
    Country VARCHAR(50) DEFAULT 'India',
    DeptID VARCHAR(10),
    
    FOREIGN KEY (DeptID)
    REFERENCES Departments(DeptID)
);
```

---

# 🔥 REAL-WORLD CONSTRAINT EXAMPLES

| System | Constraint |
|---|---|
| Banking | balance ≥ 0 |
| Ecommerce | stock ≥ 0 |
| College | marks ≤ 100 |
| Social Media | unique email |

---

# 🔥 Advantages of Integrity Constraints

| Advantage | Meaning |
|---|---|
| Data Accuracy | prevents invalid data |
| Consistency | maintains correctness |
| Reliability | trusted database |
| Automation | DB enforces rules |
| Security | prevents misuse |

---

# 🔥 Disadvantages

| Disadvantage | Meaning |
|---|---|
| Slight performance overhead | validation cost |
| Complex schema design | more planning needed |

---

# 🔥 Integrity Constraints vs Validation

| Application Validation | DB Constraints |
|---|---|
| frontend/backend checks | DB-level enforcement |
| can be bypassed | harder to bypass |

---

# 🎯 FAANG INTERVIEW QUESTIONS

---

## Q1. What are integrity constraints?

✔ rules ensuring correctness and consistency of data

---

## Q2. Difference between entity integrity and referential integrity?

✔ entity integrity → PK not NULL  
✔ referential integrity → FK references valid PK

---

## Q3. Why primary key cannot be NULL?

✔ entity must be uniquely identifiable

---

## Q4. Difference between UNIQUE and PRIMARY KEY?

✔ primary key cannot contain NULL

---

## Q5. What is CHECK constraint?

✔ enforces conditional rules

---

## Q6. Why referential integrity important?

✔ prevents invalid relationships

---

## Q7. What happens if referential integrity absent?

✔ orphan records may occur

---

# 🔥 ORPHAN RECORD ⭐ IMPORTANT

Child record without valid parent.

---

# 🧠 Example

Student references:
```text
DeptID = D100
```

but D100 absent.

This creates:
# ❌ orphan record

---

# 🔥 FINAL INTUITION TABLE

| Constraint | Think Like |
|---|---|
| Domain Constraint | valid value range |
| Key Constraint | uniqueness |
| Entity Integrity | PK cannot be NULL |
| Referential Integrity | valid references |
| CHECK | rule enforcement |
| UNIQUE | no duplicates |
| DEFAULT | automatic value |

---

# 🚀 FINAL SUMMARY

Integrity Constraints:
# ✅ ensure database correctness and reliability

They prevent:
- invalid data
- duplicate records
- broken relationships
- inconsistent states

Foundation for:
- enterprise databases
- secure systems
- reliable transactions
- scalable applications