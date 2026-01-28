# 🍽️ Recipe Sharing App – 2 Day Backend Project

## Tech Stack

* Node.js
* Express.js
* Supabase (Postgres + Auth DB)
* bcrypt
* jsonwebtoken
* dotenv

---

# ✅ Features Covered

### Authentication

* Signup (hash password)
* Login (compare password)
* JWT based auth
* Protected routes

---

### Recipe Management

* Create recipe (protected)
* View recipe
* Update recipe (only owner)
* Delete recipe (only owner)
* Assign preparer (another user)

---

### Sharing

* Public link (no auth)
* Private link (JWT required)

---

### Analytics

* My recipes
* Total views of my recipes
* Recipes where I’m preparer
* Increment views on recipe view

---

---

# 🗓 DAY 1 — Core Backend + Auth + Basic Recipes

### Goal

Build foundation: project setup, Supabase, schemas, auth, JWT, first protected routes.

---

## 1️⃣ Project Setup

```bash
npm init -y
npm install express dotenv bcrypt jsonwebtoken @supabase/supabase-js morgan
```

---

## 2️⃣ Folder Structure

```
src/
 ├── controllers/
 ├── routes/
 ├── models/
 ├── middlewares/
 ├── config/
 └── app.js
.env
```

---

## 3️⃣ Basic Express App

### app.js

* express.json()
* logger middleware (morgan)
* undefined routes handler

```js
app.use("*", (req,res)=>{
  res.status(404).json({msg:"Route not found"});
});
```

---

## 4️⃣ Supabase Client

### config/supabase.js

```js
createClient(process.env.SUPABASE_URL, process.env.SUPABASE_KEY)
```

---

## 5️⃣ Database Schemas

---

### users table

| field      | type      |
| ---------- | --------- |
| id         | uuid      |
| name       | text      |
| email      | text      |
| password   | text      |
| created_at | timestamp |

---

### recipes table

| field       | type            |
| ----------- | --------------- |
| id          | uuid            |
| title       | text            |
| description | text            |
| owner_id    | uuid            |
| preparer_id | uuid (nullable) |
| views       | int default 0   |
| is_public   | boolean         |
| created_at  | timestamp       |

---

---

# 🔐 Authentication

---

## Signup

### POST /auth/signup

### Flow:

1. Take name, email, password
2. bcrypt.hash(password)
3. Insert into users

---

## Login

### POST /auth/login

### Flow:

1. Find user by email
2. bcrypt.compare
3. jwt.sign({ userId })

---

---

# 🔐 JWT Middleware

### middlewares/auth.js

* Read token from headers
* jwt.verify
* attach req.userId

---

---

# 🍲 Recipes (DAY 1 scope)

---

## Create Recipe (Protected)

### POST /recipes

Headers:

```
Authorization: Bearer <token>
```

Body:

```
title, description
```

Owner automatically taken from token.

---

---

## Get My Recipes

### GET /recipes/my

Return only recipes where:

```
owner_id = req.userId
```

---

---

### ✅ End of Day 1 Deliverables

* Node + Express setup
* Supabase connected
* Folder architecture
* User & Recipe schema
* Signup + Login
* JWT middleware
* Create recipe
* Get my recipes

---

---

# 🗓 DAY 2 — Advanced CRUD + Sharing + Analytics

---

## ✏️ Update Recipe

### PUT /recipes/:id

Rules:

* Only owner can update

---

## 🗑 Delete Recipe

### DELETE /recipes/:id

Rules:

* Only owner

---

---

## 👨‍🍳 Assign Preparer

### PATCH /recipes/:id/assign

Body:

```
preparerEmail
```

Logic:

* Find user by email
* Update recipe.preparer_id

---

---

# 🔗 Sharing

---

## Public Recipe

### GET /recipes/public/:id

Rules:

* is_public must be true
* no JWT required

---

---

## Private Recipe

### GET /recipes/private/:id

Rules:

* JWT required
* only owner or preparer

---

---

# 👀 Views Increment Logic

Whenever recipe is viewed:

```sql
views = views + 1
```

Applied in:

* public route
* private route

---

---

# 📊 Analytics

---

## My Recipes

### GET /analytics/my-recipes

---

## Total Views of My Recipes

### GET /analytics/my-total-views

SUM(views) where owner_id = userId

---

---

## Recipes Where I’m Preparer

### GET /analytics/preparer-recipes

---

---

# ⚠ Edge Cases Covered

✔ Email already exists
✔ Wrong password
✔ Invalid JWT
✔ Recipe not found
✔ Non-owner update/delete
✔ Preparer email not found
✔ Private recipe access without token
✔ Views increment only on successful fetch
✔ Cannot assign self as preparer
✔ Cannot delete recipe after sharing publicly (optional rule)

---