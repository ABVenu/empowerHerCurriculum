### **Session Name: ER Diagrams & Designing Relational Database Schemas**

By the end of this session, students will be able to:

---

## **1. Understand the Purpose of ER Diagrams**

- Define an **Entity Relationship (ER) Diagram**

- Understand ER diagrams as a **visual planning tool** for database design

- Recognize ER diagrams as a bridge between:

  - Business requirements
  - Database schemas

- Understand why complex systems cannot be designed mentally or directly in SQL

---

## **2. Identify Core Components of ER Diagrams**

- Identify **entities** as real-world objects (e.g., User, Order, Product)
- Identify **attributes** as properties of entities
- Identify **relationships** between entities
- Understand how cardinality is represented in ER diagrams

---

## **3. Design ER Diagrams for Real-World Use Cases**

- Design ER diagrams for applications such as:

  - E-commerce systems
  - Learning management systems
  - Booking platforms

- Identify which entities should become separate tables

- Decide attributes that belong to each entity

- Avoid overloading a single entity with unrelated data

---

## **4. Convert ER Diagrams into Relational Schemas**

- Translate entities into database tables

- Convert relationships into foreign keys

- Decide table structures based on relationship types:

  - 1:1
  - 1:M
  - M:M (using junction tables)

- Understand how ER decisions affect final database structure

---

## **5. Understand Cascading Rules in Relational Design**

- Understand why cascading rules are required

- Explain cascading actions such as:

  - `ON DELETE CASCADE`
  - `ON UPDATE CASCADE`

- Understand how cascading maintains referential integrity

- Identify scenarios where cascading is useful

- Identify scenarios where cascading is risky and should be avoided

---

## **6. Design a Relational Schema Ready for Implementation**

- Design a complete relational schema from an ER diagram

- Validate schema design for:

  - Data consistency
  - Scalability
  - Maintainability

- Prepare schemas that can be implemented directly in Supabase or any relational database

---

## **End-of-Session Outcome**

By the end of this session, students will:

- Confidently design ER diagrams
- Convert business requirements into relational schemas
- Understand how relationships and cascading rules impact data
- Design scalable and maintainable database structures
- Be fully prepared to implement relational schemas in Supabase and backend systems
