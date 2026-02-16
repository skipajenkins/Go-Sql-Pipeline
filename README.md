
---

# 🐹 Go SQL Pipeline (Go + PostgreSQL)

A simple Go-based SQL pipeline project that demonstrates how to:

* Connect Go applications to a SQL database

* Execute SQL schema creation scripts

* Manage dependencies using Go Modules

* Structure a small production-style backend pipeline

This project is ideal for learning database-driven backend development with Go.

---

## 🎯 Learning Objectives

By working through this project, you will learn:

* How Go interacts with SQL databases

* How to manage SQL schemas using .sql scripts

* How to structure a backend pipeline in Go

* How Go Modules manage dependencies

* How to separate schema logic from application logic

---

## 📁 Project Structure
Go-Sql-Pipeline/
├── create-tables.sql   # SQL schema definition
├── go.mod              # Go module definition
├── go.sum              # Dependency lock file
├── main.go             # Main Go application
└── README.md           # Project documentation

---

## ⚙️ Prerequisites

Make sure you have the following installed:

* Tool	Purpose
* Go	Application runtime
* PostgreSQL / MySQL / SQLite	SQL database
* Git	Version control

---

## 🦫 Installing Go
### Step 1: Check if Go is installed
```bash
go version
```

### Step 2: Install Go (if missing)

Linux / macOS:
```bash
curl -OL https://go.dev/dl/go1.22.0.linux-amd64.tar.gz
sudo tar -C /usr/local -xvf go1.22.0.linux-amd64.tar.gz
export PATH=$PATH:/usr/local/go/bin
```

Windows:
```
👉 https://go.dev/dl/
```

---

## 🚀 Getting Started
### Step 1: Clone the Repository
```bash
git clone https://github.com/skipajenkins/Go-Sql-Pipeline.git
cd Go-Sql-Pipeline
```
----
### Step 2: Install Dependencies
```bash
go mod tidy
```
----
### Step 3: Create Database Tables
```bash
Run the SQL schema file in your database:

psql -U postgres -d your_database -f create-tables.sql
```

Or for SQLite:
```bash
sqlite3 database.db < create-tables.sql
```
---
### Step 4: Run the Application
```bash
go run main.go
```

---

## 🧠 Key Concepts

| Concept | Explanation |
|----------|-------------|
| Go Modules | Dependency management using `go.mod` |
| SQL Pipelines | Structured execution of database operations |
| Schema Scripts | SQL files for table creation |
| Backend Architecture | Separating schema from logic |
| Database Drivers | Go libraries for SQL connectivity |

---

## 🗃️ SQL Schema

The create-tables.sql file defines:

* Database tables

* Column data types

* Primary keys

* Constraints

This allows clean schema versioning and easy database recreation.

---

## 🏗️ How It Works
1️⃣ Go initializes the module

Handled by:
```bash
go.mod
```
2️⃣ SQL schema is loaded

```bash
create-tables.sql
```
---
3️⃣ Go connects to the database

From:
```bash
main.go
```
----
4️⃣ Queries execute through Go logic

```bash
This creates a full pipeline from SQL → Go → Output.
```

---

## 🧩 Example Execution
```bash
go run main.go
```

Output:
```bash
Connected to database...
Tables created successfully.
Pipeline execution complete.
```

(Example output — depends on your implementation)

---

## 🧱 Built With

* Go (Golang)

* SQL

* Go Modules

* PostgreSQL / SQLite / MySQL

---

## 📜 License

This project is licensed under the MIT License — free to use, modify, and distribute.

---
