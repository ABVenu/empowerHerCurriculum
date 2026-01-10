## **Learning Objectives – PostgreSQL & Supabase**

### **Session Name: Schema Design Fundamentals – Designing Clean Database Tables**

By the end of this session, students will be able to:

---

## **1. Understand What Schema Design Means in Databases**

- Define **schema design** in the context of relational databases
- Understand schema as the **structure and rules** of stored data
- Identify schema design as a **core backend responsibility**
- Understand how poor schema design leads to:

  - Data inconsistency
  - Maintenance issues
  - Scalability problems

---

## **2. Understand Why Schema Design Comes Before Backend Code**

- Understand that database design should not be driven by UI screens
- Recognize that backend APIs depend on a well-designed schema
- Understand why fixing schema mistakes later is costly
- Identify schema design as a **foundation step** in application development

---

## **3. Identify Ideal Requirements of a Good Table Schema**

- Understand that a table should represent **one clear entity**

- Identify characteristics of a good schema:

  - Clear and meaningful column names
  - Correct and minimal set of columns
  - Avoidance of redundant or derived data

- Understand why unnecessary columns make tables heavy and error-prone

---

## **4. Choose Appropriate Data Types for Columns**

- Understand the importance of choosing correct data types

- Identify commonly used PostgreSQL data types:

  - `TEXT` / `VARCHAR`
  - `INTEGER`
  - `BOOLEAN`
  - `UUID`
  - `TIMESTAMP`

- Understand how data types impact storage, validation, and performance

---

## **5. Apply Constraints to Enforce Data Quality**

- Understand why databases must enforce data rules

- Apply common constraints such as:

  - `PRIMARY KEY`
  - `NOT NULL`
  - `UNIQUE`
  - `DEFAULT`

- Understand how constraints prevent invalid data from entering the system

- Recognize constraints as **database-level validation**

---

## **6. Design and Implement a Single-Table Schema in Supabase**

- Convert a simple business requirement into a table schema
- Design a **single-table schema** without relationships
- Implement the schema using SQL in **Supabase**
- Review and validate the schema design decisions

---

## **End-of-Session Outcome**

By the end of this session, students will:

- Clearly understand what schema design is and why it matters
- Design clean, meaningful database tables
- Choose correct data types and constraints
- Implement production-quality single-table schemas in Supabase
- Be ready to design relational schemas using ER diagrams in the next session
