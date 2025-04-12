# [Finals-Lab-Task-2](https://github.com/user-attachments/files/19719375/FajardoFLT2.docx)

This portfolio showcases my proficiency in creating MySQL databases through the development of a basic student assignment submission system. It outlines the step-by-step process of building tables for students, assignments, and submissions. The task demonstrates the application of proper data types, table relationships, and constraints such as primary keys, foreign keys, and composite keys to establish a functional relational database structure.

# Step-by-Step Process

### 1. Creating the `student` table:
- Define `username` as `VARCHAR(50)`.
- Set `username` as the table’s **Primary Key**.

### 2. Creating the `assignment` table:
- Define `shortname` as `VARCHAR(50)` and assign it as the **Primary Key**.
- Define `due_date` as a `DATE` that **cannot be null**.
- Define `url` as a `VARCHAR(255)`, which is **nullable**.

### 3. Creating the `submission` table:
- Include `username` and `shortname` as `VARCHAR(50)`.
- Define `version` as an `INT`.
- Set `submit_date` as a `DATE NOT NULL`.
- Include `data` as `TEXT`.
- Assign a **composite primary key** consisting of (`username`, `shortname`, `version`).
- Add **foreign key constraints** linking to the `student` and `assignment` tables.

# Table Relationships

### 1. **`student` Table**
- **Primary Key:** `username`
- **Relationship:**
  - **One-to-Many** with `submission`: A single student (`username`) can have multiple submission entries.

### 2. **`assignment` Table**
- **Primary Key:** `shortname`
- **Relationship:**
  - **One-to-Many** with `submission`: A single assignment (`shortname`) may receive several submissions from different students or multiple versions from the same student.

### 3. **`submission` Table**
- **Composite Primary Key:** (`username`, `shortname`, `version`)
- **Relationships:**
  - **Many-to-One** with `student`: Each submission is tied to one student.
  - **Many-to-One** with `assignment`: Each submission pertains to a single assignment.
  - Collectively, the `submission` table bridges a **many-to-many relationship** between students and assignments, while tracking submission versions.

## SQL Query Statements

1. **Student Table**
- ![Image](https://github.com/user-attachments/assets/cf3b630b-ed7a-40ae-905c-761d14a865b3)

2. **Assignment Table**
- ![Image](https://github.com/user-attachments/assets/94587c19-ade7-4cdd-a858-d5f8a017a86c)


3. **Submission Table**
- ![Image](https://github.com/user-attachments/assets/625e919a-71b8-4bfe-93c1-7583b3ddde10)

## Table Structures

1. **Student Table Structure**
- ![Image](https://github.com/user-attachments/assets/0c46bb9f-b104-4513-a624-2f8e57f85062)

2. **Assignment Table Structure**
- ![Image](https://github.com/user-attachments/assets/366a8cc3-bb11-49e4-bbd9-795eb6fb6393)

3. **Submission Table Structure**
- ![Image](https://github.com/user-attachments/assets/a134ed4b-e825-4ed2-a354-68a5c9667143)

## Enhanced Entity-Relationship (EER) Diagram

- ![Image](https://github.com/user-attachments/assets/be86d660-a18d-4e61-b987-b15c37126861)
- ![Image](https://github.com/user-attachments/assets/58591056-7f2c-4e5a-a9d7-c89b91a1532d)



Let me know if you’d like this adapted into a presentation format or if you need help summarizing it further!
