# Node.js + PostgreSQL Starter Project (From Scratch)

## Step 1 — Create project

```bash
mkdir node-postgres-basic
cd node-postgres-basic
npm init -y
```

---

## Step 2 — Install dependencies

```bash
npm install express pg dotenv
npm install --save-dev nodemon
```

---

## Step 3 — Create project files

```bash
touch server.js
touch db.js
touch .env
touch README.md
```

---

## Step 4 — Setup `.env`

```
PORT=3002

DB_HOST=localhost
DB_USER=postgres
DB_PASSWORD=yourpassword
DB_NAME=testdb
DB_PORT=5432
```

---

## Step 5 — Create database

```bash
psql -U postgres
```

```sql
CREATE DATABASE testdb;
```

---

## Step 6 — Create table

```bash
psql -U postgres -d testdb
```

```sql
CREATE TABLE users (
  id SERIAL PRIMARY KEY,
  name VARCHAR(100),
  email VARCHAR(100)
);

INSERT INTO users(name,email)
VALUES ('John Doe','john@gmail.com');
```

---

## Step 7 — Add scripts to `package.json`

```json
"scripts": {
  "start": "node server.js",
  "dev": "nodemon server.js"
}
```

---

## Step 8 — Run project

```bash
npm run dev
```

Open:

```
http://localhost:3002/users
```

---

## Step 9 — Project structure

```
node-postgres-basic
│── server.js
│── db.js
│── .env
│── package.json
│── README.md
```
