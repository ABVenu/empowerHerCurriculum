## **Learning Objectives – PostgreSQL & Supabase**

By the end of this session, students will be able to:

---

## **1. Reinforce and Extend CRUD Operations Using SQL**

* Recall basic CRUD operations from the previous session

* Perform advanced read operations using:

  * `WHERE`
  * `ORDER BY`
  * `LIMIT`

* Understand how filtering and sorting improve data retrieval

* Identify real-world use cases for controlled data reads

---

## **2. Use Commonly Used SQL Built-in Functions**

* Understand why databases provide built-in functions

* Use frequently used SQL aggregate functions:

  * `COUNT`
  * `SUM`
  * `AVG`
  * `MIN`
  * `MAX`

* Use `GROUP BY` to summarise data

* Interpret aggregated results correctly

* Relate aggregate queries to dashboards and reports

---

## **3. Understand Why Single-Table Design Does Not Scale (Real-World Example)**

* Understand problems with putting all data into one table

* Use an **e-commerce application** as a reference example

* Understand that in a `users` table:

  * Only user-specific data should exist (name, email, phone)
  * Orders, refunds, cancellations, saved addresses **should NOT** be stored in the same table

* Recognize that mixing all data in one table makes it:

  * Heavy
  * Hard to maintain
  * Difficult to scale

---

## **4. Understand the Need for Separating Data into Multiple Tables**

* Understand why related data must be stored in separate tables such as:

  * `users`
  * `orders`
  * `refunds`
  * `addresses`

* Understand that separating data avoids:

  * Repetition
  * Inconsistency
  * Unnecessary null values

* Identify separation of tables as a **core database design principle**

---

## **5. Understand Relationship Types (Theory Only)**

* Explain **One-to-One (1:1)** relationships
* Explain **One-to-Many (1:M)** relationships
* Explain **Many-to-Many (M:M)** relationships
* Map each relationship type to the e-commerce example:

  * User → Orders (1:M)
  * User → Address (1:M)
  * Orders ↔ Products (M:M)

---

## **6. Understand How Relationships Are Maintained in Databases (Theory Only)**

* Understand the role of a **Primary Key**
* Understand the role of a **Foreign Key**
* Recognize foreign keys as references between tables
* Understand how databases maintain links between related data
* Understand that relationships are enforced at the database level

---

## **End-of-Session Outcome**

By the end of this session, students will:

* Perform advanced SQL queries confidently
* Use aggregate functions for meaningful insights
* Understand why real-world applications require multiple tables
* Clearly explain why data must be separated into related tables
* Understand how relationships are maintained using keys
* Be conceptually ready to implement relational CRUD in the next session

