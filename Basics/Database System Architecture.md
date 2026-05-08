# Database System Architecture

## Overview
Database System Architecture explains how users, query processors, and storage managers interact within a DBMS.

---

# 1. Types of Users

## Naive Users
Examples:
- Tellers
- Agents
- Web users

### Role
- Use application interfaces
- Perform predefined operations

---

## Application Programmers
### Role
- Write application programs
- Interact with DBMS using programming languages

---

## Sophisticated Users
Examples:
- Analysts

### Role
- Use query tools
- Execute complex database queries

---

## Database Administrators (DBA)
### Role
- Manage the database system
- Handle security, backup, and maintenance

---

# 2. Query Processor Components

## Application Interfaces
- Interfaces used by users to interact with applications

---

## Application Programs
- Programs developed to access databases

---

## Compiler and Linker
### Functions
- Convert source code into executable code
- Link required libraries

---

## DML Queries
DML = Data Manipulation Language

### Commands
- INSERT
- UPDATE
- DELETE
- SELECT

---

## DML Compiler and Organizer
### Functions
- Parses DML queries
- Optimizes query execution

---

## Query Evaluation Engine
### Functions
- Executes database queries
- Retrieves required data efficiently

---

## DDL Interpreter
DDL = Data Definition Language

### Commands
- CREATE
- ALTER
- DROP

### Functions
- Interprets schema definitions
- Stores metadata in data dictionary

---

# 3. Storage Manager Components

## Buffer Manager
### Functions
- Manages data transfer between memory and disk
- Improves database performance

---

## File Manager
### Functions
- Manages database files
- Organizes storage on disk

---

## Authorization & Integrity Manager
### Functions
- Checks user permissions
- Maintains data integrity

---

## Transaction Manager
### Functions
- Ensures ACID properties
- Handles concurrency and recovery

---

# 4. Disk Storage Components

## Data
- Stores actual database records

---

## Indices
### Purpose
- Speed up data retrieval

---

## Statistical Data
### Purpose
- Helps in query optimization

---

## Data Dictionary
### Purpose
- Stores metadata about database structure

---

# Working Flow of DBMS

1. Users interact through interfaces or query tools.
2. Query processor processes user queries.
3. Storage manager accesses data from disk.
4. Results are returned to users.

---

# Summary Table

| Component | Function |
|-----------|-----------|
| Query Processor | Processes and optimizes queries |
| Storage Manager | Manages stored data |
| Buffer Manager | Handles memory and disk transfer |
| Transaction Manager | Maintains transaction consistency |
| Data Dictionary | Stores metadata |