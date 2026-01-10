
## **Learning Objectives – PostgreSQL & Supabase**

### **Session Name: CRUD Operations with Relationships (Joins & Relational Queries)**

By the end of this session, students will be able to:

---

## **1. Recall Relationship Concepts from the Previous Session**

- Recall why real-world applications require multiple tables

- Revisit relationship types:

  - One-to-One (1:1)
  - One-to-Many (1:M)
  - Many-to-Many (M:M)

- Relate these concepts to real-world examples like e-commerce systems

---

## **2. Create Related Tables Using Keys**

- Create tables with **primary keys**
- Create tables with **foreign keys**
- Understand how foreign keys reference primary keys
- Understand how relational links are enforced by the database

---

## **3. Insert Data into Related Tables (Relational CRUD – Create)**

- Insert data into parent tables (e.g., users)
- Insert data into child tables (e.g., orders)
- Understand the order of insertion when relationships exist
- Identify common mistakes while inserting relational data

---

## **4. Retrieve Data Across Multiple Tables Using Joins**

- Understand why joins are required to fetch meaningful data

- Use `INNER JOIN` to fetch matching related records

- Use `LEFT JOIN` to fetch parent records even when child records are missing

- Fetch combined data such as:

  - User with their orders
  - Orders with user details

- Understand how joined data is represented in query results

---

## **5. Update and Delete Data in Relational Tables**

- Update records in tables with relationships
- Understand how updates affect related data
- Delete records safely from related tables
- Understand restrictions imposed by foreign keys during delete operations

---

## **6. Understand the Impact of Relationships and Cascading Effects on CRUD Operations**

- Understand how relationships influence all CRUD operations

- Explain what happens when:

  - A parent record is updated
  - A parent record is deleted

- Understand **cascading actions** such as:

  - `ON DELETE CASCADE`
  - `ON UPDATE CASCADE`

- Understand how cascading helps maintain data consistency

- Identify risks of cascading deletes in real-world applications

- Decide when cascading should be enabled and when it should be avoided

- Understand how databases prevent orphan records using cascading rules

---

## **End-of-Session Outcome**

By the end of this session, students will:

- Confidently perform CRUD operations across related tables
- Write join queries to retrieve meaningful relational data
- Understand how primary and foreign keys impact data operations
- Handle real-world multi-table database scenarios
- Be ready to design and implement schemas more intentionally in upcoming sessions

---
