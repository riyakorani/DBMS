# 📘 Keys in DBMS (Master FAANG Notes)

*(Microsoft + Google + Amazon + Interview + GitHub Ready Notes)*

---

# 🔥 Introduction

Keys are one of the most important concepts in DBMS.

Almost every advanced DBMS topic depends on keys:

* normalization
* joins
* indexing
* relationships
* constraints
* query optimization
* transactions

Without keys:

* duplicate data increases
* relationships break
* integrity is lost
* searching becomes difficult

---

# 📌 What is a Key?

## Definition

A Key is an attribute or set of attributes used to:

✅ uniquely identify tuples (rows) in a table.

---

# 📌 Simple Example

| StudentID | Name | Marks |
| --------- | ---- | ----- |
| 101       | Riya | 85    |
| 102       | Aman | 90    |

Here:

# ✅ StudentID uniquely identifies each student.

So:

```text
StudentID = Key
```

---

# 🔥 Why Keys are Important?

Keys help in:

✅ Unique identification
✅ Preventing duplicate data
✅ Maintaining relationships
✅ Enforcing integrity
✅ Faster searching
✅ Normalization
✅ Efficient joins

---

# 📌 Types of Keys

1️⃣ Super Key
2️⃣ Candidate Key
3️⃣ Primary Key
4️⃣ Alternate Key
5️⃣ Foreign Key
6️⃣ Composite Key
7️⃣ Unique Key
8️⃣ Surrogate Key
9️⃣ Natural Key
10️⃣ Secondary Key

---

# 1️⃣ Super Key

# 📌 Definition

A Super Key is:

> Any attribute or combination of attributes that uniquely identifies a row.

---

# 📌 Example Table

| StudentID | Email                                   | Name |
| --------- | --------------------------------------- | ---- |
| 101       | [riya@gmail.com](mailto:riya@gmail.com) | Riya |
| 102       | [aman@gmail.com](mailto:aman@gmail.com) | Aman |

Possible Super Keys:

```text
StudentID
Email
StudentID + Name
Email + Name
StudentID + Email
```

All of these uniquely identify rows.

---

# 📌 Important Point

A Super Key may contain:

# ❌ unnecessary attributes

Example:

```text
StudentID + Name
```

Name is unnecessary because StudentID alone is enough.

---

# 📌 Characteristics

✅ Uniquely identifies rows
✅ Can contain extra attributes
✅ Parent concept for candidate keys

---

# 🎯 Interview Question

## Q. Why is every Candidate Key a Super Key?

### Answer

Because candidate keys also uniquely identify rows.

---

# 2️⃣ Candidate Key

# 📌 Definition

A Candidate Key is:

> Minimal Super Key.

It uniquely identifies rows without unnecessary attributes.

---

# 📌 Example

| StudentID | Email                                   | Name |
| --------- | --------------------------------------- | ---- |
| 101       | [riya@gmail.com](mailto:riya@gmail.com) | Riya |

Candidate Keys:

```text
StudentID
Email
```

Both uniquely identify rows.

Neither contains unnecessary attributes.

---

# 📌 Important Point

Candidate Key must satisfy:

✅ Unique
✅ Minimal

---

# 📌 Why Minimal Important?

Example:

```text
StudentID + Name
```

Not candidate key because:

StudentID alone already identifies rows.

---

# 🎯 Interview Question

## Q. Difference between Super Key and Candidate Key?

### Answer

| Super Key                    | Candidate Key     |
| ---------------------------- | ----------------- |
| May contain extra attributes | Minimal           |
| Not necessarily minimal      | Minimal super key |

---

# 3️⃣ Primary Key

# 📌 Definition

A Primary Key is:

> The candidate key chosen to uniquely identify rows.

---

# 📌 Example

| StudentID | Email                                   | Name |
| --------- | --------------------------------------- | ---- |
| 101       | [riya@gmail.com](mailto:riya@gmail.com) | Riya |

Candidate Keys:

```text
StudentID
Email
```

Suppose we choose:

```text
StudentID
```

Then:

# ✅ StudentID becomes Primary Key

---

# 📌 Characteristics

✅ Unique
✅ Cannot be NULL
✅ One primary key per table
✅ Main identifier

---

# 📌 Why NOT NULL?

Because every row must be identifiable.

NULL means unknown.

Unknown identifier is invalid.

---

# 📌 Real-Life Examples

* Aadhaar Number
* Passport Number
* Employee ID
* Roll Number

---

# 🎯 Interview Question

## Q. Can a table have multiple candidate keys but one primary key?

### Answer

Yes.

One candidate key is selected as primary key.

---

# 4️⃣ Alternate Key

# 📌 Definition

Candidate keys not selected as primary key are called Alternate Keys.

---

# 📌 Example

Candidate Keys:

```text
StudentID
Email
```

If:

```text
StudentID = Primary Key
```

Then:

```text
Email = Alternate Key
```

---

# 📌 Important Point

Alternate keys are still:

✅ Unique
✅ Candidate keys

But not chosen as primary key.

---

# 🎯 Interview Question

## Q. What is Alternate Key?

### Answer

A candidate key not selected as primary key.

---

# 5️⃣ Foreign Key

# 📌 Definition

A Foreign Key is:

> An attribute in one table that references the primary key of another table.

---

# 📌 Purpose

Used to:

✅ Create relationships
✅ Maintain referential integrity

---

# 📌 Example

## Students Table

| StudentID | Name |
| --------- | ---- |
| 101       | Riya |

---

## Orders Table

| OrderID | StudentID |
| ------- | --------- |
| 1       | 101       |

Here:

```text
Orders.StudentID
```

references:

```text
Students.StudentID
```

So:

# ✅ StudentID in Orders table is Foreign Key

---

# 📌 Referential Integrity

Foreign key ensures:

# ❌ No invalid references

Example:

Cannot insert:

```text
StudentID = 999
```

if student 999 does not exist.

---

# 📌 Characteristics

✅ Creates relationships
✅ Maintains integrity
✅ Can contain duplicates
✅ Can contain NULL (sometimes)

---

# 🎯 Interview Question

## Q. Why are Foreign Keys important?

### Answer

Foreign keys maintain referential integrity between related tables.

---

# 6️⃣ Composite Key

# 📌 Definition

A Composite Key is:

> A key formed using multiple attributes together.

---

# 📌 Example

## Enrollment Table

| StudentID | CourseID |
| --------- | -------- |
| 101       | DBMS     |
| 101       | OS       |

Neither StudentID nor CourseID alone is unique.

But together:

```text
StudentID + CourseID
```

becomes unique.

So:

# ✅ Composite Key

---

# 📌 Important Point

Used heavily in:

✅ Junction tables
✅ Many-to-many relationships

---

# 🎯 Interview Question

## Q. Why are Composite Keys used?

### Answer

When a single attribute cannot uniquely identify rows.

---

# 7️⃣ Unique Key

# 📌 Definition

A Unique Key ensures:

# ✅ All values are unique

similar to primary key.

---

# 📌 Difference from Primary Key

| Primary Key    | Unique Key       |
| -------------- | ---------------- |
| Cannot be NULL | May allow NULL   |
| One per table  | Multiple allowed |

---

# 📌 Example

```sql
Email UNIQUE
```

No duplicate emails allowed.

---

# 🎯 Interview Question

## Q. Difference between Primary Key and Unique Key?

### Answer

Primary key cannot contain NULL and only one exists per table.

Unique key allows uniqueness but may allow NULL.

---

# 8️⃣ Surrogate Key

# 📌 Definition

Artificial/system-generated key.

Does not have real-world meaning.

---

# 📌 Example

```text
Auto Increment ID
```

| ID | Name |
| -- | ---- |
| 1  | Riya |
| 2  | Aman |

---

# 📌 Why Used?

Because natural values may:

* change
* become large
* become inefficient

---

# 📌 Examples

* Auto Increment IDs
* UUIDs

---

# 🎯 Interview Question

## Q. Why are surrogate keys preferred in large systems?

### Answer

Because they are stable, efficient, and independent of business data.

---

# 9️⃣ Natural Key

# 📌 Definition

A Natural Key is:

> Real-world meaningful attribute used as key.

---

# 📌 Examples

* Aadhaar Number
* Passport Number
* Email

---

# 📌 Problem with Natural Keys

Real-world values may:

* change
* become large
* violate privacy

---

# 🎯 Interview Question

## Q. Why do companies often avoid natural keys?

### Answer

Because business values can change and create maintenance problems.

---

# 🔟 Secondary Key

# 📌 Definition

A Secondary Key is:

> Attribute used mainly for searching but not unique.

---

# 📌 Example

| ID | Name |
| -- | ---- |
| 1  | Riya |
| 2  | Riya |

Searching by Name.

Name is secondary key.

---

# 📌 Purpose

Improves searching and indexing.

---

# 🎯 Interview Question

## Q. Can secondary key contain duplicates?

### Answer

Yes.

It is mainly used for searching.

---

# 🔥 Key Hierarchy (VERY IMPORTANT)

```text
Super Key
   ↓
Candidate Key
   ↓
Primary Key
```

---

# 🔥 Full Comparison Table

| Key Type      | Unique | NULL Allowed | Multiple Allowed | Main Purpose          |
| ------------- | ------ | ------------ | ---------------- | --------------------- |
| Super Key     | Yes    | Possible     | Yes              | Unique identification |
| Candidate Key | Yes    | No           | Yes              | Minimal unique key    |
| Primary Key   | Yes    | No           | No               | Main identifier       |
| Alternate Key | Yes    | No           | Yes              | Backup candidate key  |
| Foreign Key   | No     | Possible     | Yes              | Relationships         |
| Composite Key | Yes    | Depends      | Yes              | Combined uniqueness   |
| Unique Key    | Yes    | Sometimes    | Yes              | Uniqueness            |
| Surrogate Key | Yes    | No           | No               | Artificial identifier |
| Natural Key   | Yes    | Depends      | Depends          | Real-world identifier |
| Secondary Key | No     | Possible     | Yes              | Searching             |

---

# 🔥 Real World FAANG Examples

---

# 🛒 Amazon Example

## Users Table

| UserID | Email                                   |
| ------ | --------------------------------------- |
| 1      | [riya@gmail.com](mailto:riya@gmail.com) |

Primary Key:

```text
UserID
```

Alternate Key:

```text
Email
```

---

# 🎬 Netflix Example

## WatchHistory Table

| UserID | MovieID |
| ------ | ------- |
| 1      | 55      |

Composite Key:

```text
UserID + MovieID
```

---

# 📱 Instagram Example

## Followers Table

| UserID | FollowerID |
| ------ | ---------- |
| 1      | 9          |

Composite key used heavily.

---

# 🔥 SQL Examples

# 📌 Primary Key

```sql
CREATE TABLE Students(
   StudentID INT PRIMARY KEY,
   Name VARCHAR(50)
);
```

---

# 📌 Foreign Key

```sql
CREATE TABLE Orders(
   OrderID INT PRIMARY KEY,
   StudentID INT,
   FOREIGN KEY(StudentID)
   REFERENCES Students(StudentID)
);
```

---

# 📌 Composite Key

```sql
CREATE TABLE Enrollment(
   StudentID INT,
   CourseID INT,
   PRIMARY KEY(StudentID, CourseID)
);
```

---

# 🎯 Microsoft / FAANG Interview Questions

---

## Q1. Difference between Candidate Key and Primary Key?

### Answer

Candidate keys are all possible minimal unique keys.

Primary key is the selected candidate key.

---

## Q2. Can Foreign Key contain duplicate values?

### Answer

Yes.

Multiple rows may reference same parent row.

---

## Q3. Why are Composite Keys important?

### Answer

They uniquely identify rows when single attribute is insufficient.

---

## Q4. Why are surrogate keys preferred at scale?

### Answer

They improve performance and avoid business-data dependency.

---

## Q5. Can a table have multiple primary keys?

### Answer

No.

Only one primary key exists.

---

## Q6. Can a Candidate Key contain NULL?

### Answer

No.

Candidate keys must uniquely identify rows.

---

## Q7. Why is Primary Key indexed by default in most DBMS?

### Answer

Because primary keys are heavily used for searching and joins.

---

## Q8. Difference between Unique Key and Primary Key?

### Answer

Primary key cannot contain NULL.

Unique key may allow NULL.

---

# 🧠 Practice Questions

---

## 1️⃣ Identify the Keys

| StudentID | Email                                   | Name |
| --------- | --------------------------------------- | ---- |
| 101       | [riya@gmail.com](mailto:riya@gmail.com) | Riya |

Questions:

* Super Keys?
* Candidate Keys?
* Primary Key?
* Alternate Key?

---

## 2️⃣ True or False

### a) Every primary key is candidate key.

✅ True

---

### b) Foreign key must always be unique.

❌ False

---

### c) Composite key uses multiple columns.

✅ True

---

### d) Candidate key may contain unnecessary attributes.

❌ False

---

# 🚀 Advanced FAANG Concepts

---

# 📌 Why Primary Keys Matter for Indexing

Most databases automatically create indexes on primary keys.

Benefits:

✅ Faster searching
✅ Faster joins
✅ Efficient retrieval

---

# 📌 Why Composite Keys Can Become Expensive

Large composite keys:

* increase index size
* slow joins
* increase storage

FAANG companies often use:

✅ surrogate integer IDs

for performance.

---

# 📌 Why Foreign Keys Sometimes Removed at Scale

Some distributed systems avoid strict foreign keys because:

* distributed validation becomes expensive
* scaling becomes harder
* microservices become loosely coupled

But integrity is then handled at application level.

---

# 📌 Why UUIDs Used in Distributed Systems

UUIDs allow:

✅ globally unique identifiers
✅ distributed ID generation
✅ reduced collision risk

Used heavily in:

* distributed databases
* microservices
* cloud systems

---

# 🧠 Extra Practice Questions (FAANG Level)

---

# 1️⃣ Identify All Possible Keys

## Table

| EmployeeID | Email                                   | Phone | Name |
| ---------- | --------------------------------------- | ----- | ---- |
| 1          | [riya@gmail.com](mailto:riya@gmail.com) | 9999  | Riya |
| 2          | [aman@gmail.com](mailto:aman@gmail.com) | 8888  | Aman |

### Questions

1. Identify all Super Keys
2. Identify Candidate Keys
3. Choose a possible Primary Key
4. Identify Alternate Keys

---

# 2️⃣ Find the Relationship

## Tables

### Students

| StudentID | Name |
| --------- | ---- |
| 1         | Riya |

### Courses

| CourseID | Course |
| -------- | ------ |
| 101      | DBMS   |

### Enrollment

| StudentID | CourseID |
| --------- | -------- |
| 1         | 101      |

### Questions

1. What type of relationship exists?
2. Why is Enrollment table needed?
3. Which key is usually used in Enrollment table?

---

# 3️⃣ True or False

### a) Every Candidate Key is Super Key.

✅ True

---

### b) Primary Key can contain NULL.

❌ False

---

### c) Foreign Key creates relationships.

✅ True

---

### d) Composite Key always uses one column.

❌ False

---

### e) Surrogate Keys are system generated.

✅ True

---

# 4️⃣ Fill in the Blanks

1. A __________ uniquely identifies tuples in a table.

✅ Key

---

2. A minimal super key is called __________.

✅ Candidate Key

---

3. Candidate key selected for identification becomes __________.

✅ Primary Key

---

4. A key referencing another table is called __________.

✅ Foreign Key

---

5. Multiple columns together forming uniqueness create __________.

✅ Composite Key

---

# 5️⃣ Scenario Based Questions

---

## Q1.

A university stores:

* StudentID
* Email
* AadhaarNumber

All are unique.

### Questions

1. Which are candidate keys?
2. Which should ideally become primary key and why?

---

## Q2.

A company uses:

```text
Email as Primary Key
```

Later employees change emails frequently.

### Question

Why is this a bad design?

### Expected Answer

Because natural/business values may change frequently.
Surrogate keys are more stable.

---

## Q3.

Why might large companies avoid very large composite primary keys?

### Expected Answer

Because they:

* increase index size
* slow joins
* increase storage overhead

---

# 6️⃣ SQL Practice Questions

---

## Create a table with Primary Key

```sql
CREATE TABLE Students(
   StudentID INT PRIMARY KEY,
   Name VARCHAR(50)
);
```

---

## Create a table with Composite Key

```sql
CREATE TABLE Enrollment(
   StudentID INT,
   CourseID INT,
   PRIMARY KEY(StudentID, CourseID)
);
```

---

## Create a table with Foreign Key

```sql
CREATE TABLE Orders(
   OrderID INT PRIMARY KEY,
   StudentID INT,
   FOREIGN KEY(StudentID)
   REFERENCES Students(StudentID)
);
```

---

# 7️⃣ Microsoft / Google / Amazon Interview Questions

---

## Q1. Why are primary keys indexed automatically?

### Answer

Because primary keys are heavily used in:

* searching
* joins
* relationships

Indexing improves retrieval speed.

---

## Q2. Why are surrogate keys preferred in distributed systems?

### Answer

Because they:

* remain stable
* avoid business dependency
* improve scalability

---

## Q3. Why are foreign keys expensive in distributed databases?

### Answer

Because referential checks across distributed nodes increase coordination cost.

---

## Q4. Why can composite keys hurt performance?

### Answer

Because larger keys create:

* bigger indexes
* slower joins
* more memory usage

---

## Q5. Can a table have multiple unique keys?

### Answer

Yes.

But only one primary key.

---

# 8️⃣ Advanced Conceptual Questions

---

## Q1.

Why is minimality important in candidate keys?

### Answer

Because unnecessary attributes:

* waste storage
* increase index size
* reduce efficiency

---

## Q2.

Why do NoSQL databases sometimes avoid strict foreign keys?

### Answer

To improve:

* scalability
* distributed performance
* loose coupling

---

## Q3.

Why are UUIDs useful in cloud systems?

### Answer

Because globally unique IDs can be generated independently across distributed servers.

---

# 🔥 Quick Revision Table

| Key           | Remember                             |
| ------------- | ------------------------------------ |
| Super Key     | Unique but may have extra attributes |
| Candidate Key | Minimal unique key                   |
| Primary Key   | Selected candidate key               |
| Alternate Key | Remaining candidate key              |
| Foreign Key   | References another table             |
| Composite Key | Multiple columns together            |
| Unique Key    | Uniqueness enforced                  |
| Surrogate Key | Artificial ID                        |
| Natural Key   | Real-world value                     |
| Secondary Key | Search attribute                     |

---

# 🎯 One-Line Definitions

## Super Key

> Attribute set uniquely identifying rows.

## Candidate Key

> Minimal super key.

## Primary Key

> Selected candidate key.

## Alternate Key

> Candidate key not chosen as primary.

## Foreign Key

> Attribute referencing another table.

## Composite Key

> Multiple attributes together form key.

## Unique Key

> Ensures uniqueness.

## Surrogate Key

> Artificial system-generated identifier.

## Natural Key

> Real-world meaningful identifier.

## Secondary Key

> Attribute used mainly for searching.

---
# 🔥 DBMS Keys — Practice Questions with Answers (FAANG Level)

---

# 🧠 Basic Concept Questions

## 1️⃣ What is a key in DBMS?

### ✅ Answer
A key is an attribute or set of attributes used to uniquely identify rows in a table.

---

## 2️⃣ Why are keys important in relational databases?

### ✅ Answer
Keys help in:
- unique identification
- relationships
- integrity
- faster searching
- normalization

---

## 3️⃣ What is the difference between a row and a key?

### ✅ Answer

| Row | Key |
|---|---|
| Complete record | Identifier |
| Stores data | Identifies data |

---

## 4️⃣ Can two rows have the same primary key?

### ✅ Answer
❌ No.

Primary key values must always be unique.

---

## 5️⃣ Why can primary key never be NULL?

### ✅ Answer
Because every row must be uniquely identifiable.

NULL means unknown.

---

# 🔥 Super Key Questions

## 6️⃣ Define Super Key.

### ✅ Answer
A super key is any attribute or combination of attributes that uniquely identifies rows.

---

## 7️⃣ Can a Super Key contain unnecessary attributes?

### ✅ Answer
✅ Yes.

Example:

```text
StudentID + Name
```

Here Name may be unnecessary.

---

## 8️⃣ Identify all possible super keys.

| StudentID | Email | Name |
|---|---|---|
| 101 | riya@gmail.com | Riya |

### ✅ Answer

```text
StudentID
Email
StudentID + Name
Email + Name
StudentID + Email
StudentID + Email + Name
```

---

## 9️⃣ Is this a valid super key?

```text
StudentID + Name
```

### ✅ Answer
✅ Yes.

Because it still uniquely identifies rows.

---

# 🔥 Candidate Key Questions

## 🔟 Define Candidate Key.

### ✅ Answer
A candidate key is a minimal super key.

---

## 1️⃣1️⃣ Why is Candidate Key called minimal super key?

### ✅ Answer
Because it contains no unnecessary attributes.

---

## 1️⃣2️⃣ Find candidate keys.

| EmployeeID | Email | Phone |
|---|---|---|
| 1 | a@gmail.com | 9999 |

### ✅ Answer

```text
EmployeeID
Email
Phone
```

---

## 1️⃣3️⃣ Which is NOT a candidate key?

```text
A) EmployeeID
B) Email
C) EmployeeID + Email
```

### ✅ Answer
✅ C

Because it contains unnecessary attributes.

---

# 🔥 Primary Key Questions

## 1️⃣4️⃣ Define Primary Key.

### ✅ Answer
Primary key is the candidate key selected to uniquely identify rows.

---

## 1️⃣5️⃣ Can a table have multiple primary keys?

### ✅ Answer
❌ No.

Only one primary key exists per table.

---

## 1️⃣6️⃣ Can a primary key contain duplicate values?

### ✅ Answer
❌ No.

Primary keys must be unique.

---

## 1️⃣7️⃣ Why is primary key important?

### ✅ Answer
Because it:
- uniquely identifies rows
- prevents duplicates
- supports relationships

---

## 1️⃣8️⃣ Which candidate key should become primary key and why?

```text
Email
AadhaarNumber
StudentID
```

### ✅ Answer
Usually:

```text
StudentID
```

Because surrogate/system-generated IDs are stable and efficient.

---

# 🔥 Alternate Key Questions

## 1️⃣9️⃣ Define Alternate Key.

### ✅ Answer
Candidate key not selected as primary key.

---

## 2️⃣0️⃣ If Email is candidate key but StudentID is selected as primary key, then Email becomes what?

### ✅ Answer
Alternate Key.

---

# 🔥 Foreign Key Questions

## 2️⃣1️⃣ Define Foreign Key.

### ✅ Answer
A foreign key is an attribute referencing the primary key of another table.

---

## 2️⃣2️⃣ Why are foreign keys used?

### ✅ Answer
To create relationships and maintain referential integrity.

---

## 2️⃣3️⃣ Can foreign key contain duplicate values?

### ✅ Answer
✅ Yes.

Many rows may reference same parent row.

---

## 2️⃣4️⃣ Can foreign key contain NULL?

### ✅ Answer
✅ Yes (sometimes).

Depends on constraints.

---

## 2️⃣5️⃣ Identify foreign key.

### Orders

| OrderID | StudentID |
|---|---|
| 101 | 1 |

### ✅ Answer

```text
StudentID
```

---

## 2️⃣6️⃣ What happens if foreign key references non-existing value?

### ✅ Answer
DBMS throws integrity constraint error.

---

# 🔥 Composite Key Questions

## 2️⃣7️⃣ Define Composite Key.

### ✅ Answer
A key formed using multiple attributes together.

---

## 2️⃣8️⃣ Why are composite keys used?

### ✅ Answer
When single column cannot uniquely identify rows.

---

## 2️⃣9️⃣ Identify composite key.

| StudentID | CourseID |
|---|---|
| 1 | DBMS |

### ✅ Answer

```text
StudentID + CourseID
```

---

## 3️⃣0️⃣ Why is StudentID alone insufficient here?

### ✅ Answer
Because one student can enroll in multiple courses.

---

# 🔥 Unique Key Questions

## 3️⃣1️⃣ Difference between Unique Key and Primary Key.

### ✅ Answer

| Primary Key | Unique Key |
|---|---|
| No NULL | May allow NULL |
| One per table | Multiple allowed |

---

## 3️⃣2️⃣ Can Unique Key contain NULL?

### ✅ Answer
✅ Yes (DBMS dependent).

---

## 3️⃣3️⃣ Can a table have multiple unique keys?

### ✅ Answer
✅ Yes.

---

# 🔥 Surrogate Key Questions

## 3️⃣4️⃣ What is Surrogate Key?

### ✅ Answer
Artificial/system-generated identifier.

---

## 3️⃣5️⃣ Why do companies prefer surrogate keys?

### ✅ Answer
Because they:
- are stable
- improve performance
- avoid business dependency

---

## 3️⃣6️⃣ Give examples of surrogate keys.

### ✅ Answer

```text
Auto Increment ID
UUID
Generated IDs
```

---

# 🔥 Natural Key Questions

## 3️⃣7️⃣ What is Natural Key?

### ✅ Answer
Real-world meaningful attribute used as key.

---

## 3️⃣8️⃣ Why can natural keys become problematic?

### ✅ Answer
Because business values may:
- change
- become large
- create maintenance issues

---

## 3️⃣9️⃣ Which is better for large systems?

```text
Natural Key OR Surrogate Key
```

### ✅ Answer
Usually:
✅ Surrogate Key

Because it is stable and efficient.

---

# 🔥 Secondary Key Questions

## 4️⃣0️⃣ What is Secondary Key?

### ✅ Answer
Attribute mainly used for searching.

---

## 4️⃣1️⃣ Can secondary key contain duplicates?

### ✅ Answer
✅ Yes.

---

## 4️⃣2️⃣ Why are secondary keys useful?

### ✅ Answer
They improve searching and indexing.

---

# 🔥 Relationship + Keys Questions

## 4️⃣3️⃣ Which key creates relationships between tables?

### ✅ Answer
Foreign Key.

---

## 4️⃣4️⃣ Which relationship usually uses composite key heavily?

### ✅ Answer
Many-to-Many relationship.

---

## 4️⃣5️⃣ Why are junction tables important?

### ✅ Answer
They implement many-to-many relationships.

---

# 🔥 SQL Practice Questions

## 4️⃣6️⃣ SQL to create primary key

```sql
CREATE TABLE Students(
   StudentID INT PRIMARY KEY,
   Name VARCHAR(50)
);
```

---

## 4️⃣7️⃣ SQL to create foreign key

```sql
CREATE TABLE Orders(
   OrderID INT PRIMARY KEY,
   StudentID INT,
   FOREIGN KEY(StudentID)
   REFERENCES Students(StudentID)
);
```

---

## 4️⃣8️⃣ SQL for composite key

```sql
CREATE TABLE Enrollment(
   StudentID INT,
   CourseID INT,
   PRIMARY KEY(StudentID, CourseID)
);
```

---

## 4️⃣9️⃣ SQL for unique key

```sql
CREATE TABLE Users(
   Email VARCHAR(100) UNIQUE
);
```

---

# 🔥 True / False

## 5️⃣0️⃣ Every primary key is candidate key.

### ✅ True

---

## 5️⃣1️⃣ Every candidate key is super key.

### ✅ True

---

## 5️⃣2️⃣ Foreign key must always be unique.

### ❌ False

---

## 5️⃣3️⃣ Composite key uses multiple columns.

### ✅ True

---

## 5️⃣4️⃣ Primary key may contain NULL.

### ❌ False

---

## 5️⃣5️⃣ Candidate key can contain unnecessary attributes.

### ❌ False

---

# 🔥 Fill in the Blanks

## 5️⃣6️⃣ A __________ uniquely identifies tuples.

### ✅ Key

---

## 5️⃣7️⃣ Minimal super key is called __________.

### ✅ Candidate Key

---

## 5️⃣8️⃣ Candidate key selected for identification becomes __________.

### ✅ Primary Key

---

## 5️⃣9️⃣ A key referencing another table is called __________.

### ✅ Foreign Key

---

## 6️⃣0️⃣ Multiple attributes together form __________ key.

### ✅ Composite Key

---

# 🔥 Scenario-Based FAANG Questions

## 6️⃣1️⃣ Why might a huge composite primary key reduce performance?

### ✅ Answer
Because it:
- increases index size
- slows joins
- increases memory usage

---

## 6️⃣2️⃣ Why do distributed systems often use UUIDs?

### ✅ Answer
Because UUIDs provide globally unique identifiers across distributed servers.

---

## 6️⃣3️⃣ Why might some NoSQL systems avoid foreign keys?

### ✅ Answer
To improve scalability and distributed performance.

---

## 6️⃣4️⃣ Why is indexing important for primary keys?

### ✅ Answer
Because primary keys are heavily used in searching and joins.

---

## 6️⃣5️⃣ Why are surrogate keys preferred in microservices?

### ✅ Answer
Because they avoid dependency on business data.

---

# 🔥 Microsoft / Google Interview Questions

## 6️⃣6️⃣ Difference between Super Key and Candidate Key?

### ✅ Answer

| Super Key | Candidate Key |
|---|---|
| May contain extra attributes | Minimal |
| Unique | Unique |

---

## 6️⃣7️⃣ Difference between Candidate Key and Primary Key?

### ✅ Answer

| Candidate Key | Primary Key |
|---|---|
| Possible identifier | Selected identifier |

---

## 6️⃣8️⃣ Difference between Primary Key and Unique Key?

### ✅ Answer

| Primary Key | Unique Key |
|---|---|
| No NULL | May allow NULL |
| One only | Multiple allowed |

---

## 6️⃣9️⃣ Why are foreign keys important for integrity?

### ✅ Answer
They prevent invalid references between tables.

---

## 7️⃣0️⃣ Why are keys important for normalization?

### ✅ Answer
Because normalization depends heavily on identifying dependencies and uniqueness.