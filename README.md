<<<<<<< HEAD
# pharmacy-database-management-system
=======
#### Pharmacy Database Management System (PDMS)
### Overview

The Pharmacy Database Management System (PDMS) is a backend-driven system designed to manage pharmacy operations such as product inventory, supplier relationships, purchase transactions, and sales records using a centralized SQL Server database.

The system focuses on data integrity, normalization, and accurate transaction tracking, minimizing manual errors and improving operational efficiency. It is implemented as a Node.js backend connected to Microsoft SQL Server, with a well-structured relational database schema.

### Project Scope

This system manages the complete lifecycle of pharmaceutical products, including:

Product classification (Prescribed vs Over-the-Counter)
Supplier and procurement management
Purchase and sales transactions
Real-time stock tracking
Database-level integrity using relationships and constraints

The project emphasizes database design principles, including entity relationships, functional dependencies, and normalization.

### Key Features
## Product Management

Stores detailed product information:
Product name
Dosage and dosage form
Product type (Prescribed / OTC)
Purchase, average, and sale prices
Supports categorization and structured querying

## Supplier Management

Maintains supplier records
Links suppliers to supplied products
Supports purchase transaction traceability

## Purchase Transactions

Records:
Supplier
Product
Quantity purchased
Purchase price
Automatically affects stock levels

## Sales Transactions

Records:
Product sold
Quantity sold
Sale price
Updates stock availability in real time

## Stock Management

Maintains current inventory levels
Tracks stock updates through purchases and sales
Ensures consistency via foreign key relationships

### Technologies Used

Backend: Node.js (Express.js)
Frontend: HTML, CSS, JavaScript
Database: Microsoft SQL Server
Database Driver: mssql (Node.js)
Environment Configuration: dotenv
Authentication: SQL Server Authentication
Version Control: Git & GitHub

### Project Structure
PHARMACY-APP/
│
├── pharmacy-app/
│   ├── configuration/
│   │   └── .env.example
│   ├── database/
│   │   ├── script.sql
│   │   └── ERD of PDMS.jpg
│   ├── node_modules/
│   ├── .env               (NOT committed)
│   ├── index.html
│   ├── styles.css
│   ├── script.js
│   ├── server.js
│   ├── package.json
│   └── package-lock.json
│
├── .gitignore
└── README.md

### Database Setup
## 1️⃣ Create Database
In SQL Server Management Studio (SSMS):

CREATE DATABASE [Pharmacy Database Management System];

## 2️⃣ Create Tables & Data

Open SSMS
Select the database
Pharmacy Database Management System

Open the file:
database/script.sql

Execute the script
(This creates all tables, relationships, and initial structure)

## 3️⃣ ER Diagram

The database ERD is provided here:

database/ERD of PDMS.jpg

## Environment Configuration

Create .env file
Inside pharmacy-app/, create a .env file using the example:

configuration/.env.example

Example:

DB_SERVER=localhost
DB_DATABASE=Pharmacy Database Management System
DB_USER=pharmacy_user
DB_PASSWORD=your_password
DB_PORT=1433
PORT=3000
NODE_ENV=development


Install & Run
## 1️⃣ Install dependencies
npm install

## 2️⃣ Start the server
npm start

## 3️⃣ Server Output (Expected)
Connected to SQL Server successfully
Database connection verified
Server running on http://localhost:3000
Pharmacy Management System Backend Started

## API Health Check

Verify backend & database connection:

GET http://localhost:3000/api/health


## Expected response:

{
  "status": "healthy",
  "database": "connected"
}

## Authentication

User credentials are stored in the Users table.
Roles include:

admin
pharmacist

Passwords are stored as plain text for academic purposes only.

## Backup & Restore

Backup Database
POST /api/database/backup

Creates a .bak file on the local system.

## Restore Database

POST /api/database/restore

Restores from a .bak file.

## Git & Version Control

✔ .env is ignored
✔ node_modules is ignored
✔ Database structure shared via SQL scripts
✔ No credentials committed

This repository is safe to clone and run locally.

## Academic Note

This project is intended for learning and academic evaluation.
Security practices (password hashing, authorization tokens) are simplified.

## Author

Arooj Saleem
Aimen Hafeez
Anara Hayat 
Database Management Systems Project

## License

This project is for educational use only.
>>>>>>> 82fb28a (Initial commit: Pharmacy Database Management System)
