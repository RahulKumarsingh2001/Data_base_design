# Database Design & Data Modeling

A practical database design and data modeling project covering **database requirements gathering, conceptual modeling, logical modeling, physical modeling, ER diagrams, relationships, keys, normalization, OLTP, OLAP, and dimensional modeling**.

The project also includes a complete **MySQL database schema** based on the designed data model.

---

## 📌 Project Overview

This project demonstrates the process of designing a database from business requirements to an implementable SQL database.

The project covers:

* Database and Data Modeling fundamentals
* Requirement Gathering
* Conceptual Data Modeling
* Logical Data Modeling
* Physical Data Modeling
* Entity Relationship (ER) Modeling
* Primary Keys and Foreign Keys
* Candidate Keys
* Alternate Keys
* Super Keys
* Composite Keys
* Unique Keys
* Database Relationships
* Cardinality
* Crow's Foot Notation
* Normalization

  * 1NF
  * 2NF
  * 3NF
  * BCNF
* OLTP
* OLAP
* Data Warehouse concepts
* Dimensional Modeling
* Fact Tables
* Dimension Tables
* Star Schema
* Snowflake Schema
* MySQL database implementation

---

## 📂 Project Structure

```text
Data_base_design/
│
├── Data Models.drawio
│
├── workflow.excalidraw
│
├── datamodels.sql
│
├── images/
│   ├── 1stNF.png
│   ├── 2ndNF.png
│   ├── 3rdNF.png
│   ├── datamodels.png
│   └── updatedatamodels.png
│
└── README.md
```

---

## 🗂️ Files Description

### `Data Models.drawio`

Contains the **ER/Data Model diagram** created using Draw.io.

This file represents the database entities, attributes, primary keys, foreign keys, and relationships between entities.

You can open this file using:

* Draw.io / diagrams.net
* Draw.io VS Code extension

---

### `workflow.excalidraw`

Contains the project's **database design notes, workflow, concepts, diagrams, and learning material** created using Excalidraw.

It includes topics such as:

* Why data modeling is required
* Data modeling layers
* Requirement gathering
* OLTP and OLAP
* Database keys
* Relationships
* Cardinality
* Normalization
* Dimensional modeling
* Star schema
* Snowflake schema

---

### `datamodels.sql`

Contains the **MySQL database implementation** generated from the database design.

The script:

1. Creates the `raw` schema.
2. Selects the `raw` schema.
3. Creates the required tables.
4. Defines primary keys.
5. Defines foreign keys.
6. Establishes relationships between tables.

---

### `images/`

Contains supporting diagrams for the project, including normalization examples and database model diagrams.

---

# 🛠️ Tools & Technologies

| Tool / Technology | Purpose                                 |
| ----------------- | --------------------------------------- |
| MySQL             | Database implementation                 |
| SQL               | Database schema creation                |
| Draw.io           | ER/Data Model diagrams                  |
| Excalidraw        | Database design notes and diagrams      |
| VS Code           | Project development and file management |
| Git               | Version control                         |
| GitHub            | Repository hosting                      |

---

# 💻 Local Setup

You can work with this project in two different ways:

### Option 1 — VS Code

Recommended if you want to edit the `.drawio`, `.excalidraw`, and `.sql` files locally.

### Option 2 — Browser

Recommended if you only want to view or edit the diagrams without installing VS Code extensions.

---

# 1. Clone the Repository

Open your terminal and run:

```bash
git clone <YOUR_GITHUB_REPOSITORY_URL>
```

Move into the project directory:

```bash
cd Data_base_design
```

Then open the project in VS Code:

```bash
code .
```

> If the `code` command is not available, simply open VS Code and select **File → Open Folder** and choose the project directory.

---

# 2. VS Code Setup

## Install Visual Studio Code

Download and install VS Code from the official website:

https://code.visualstudio.com/

After installation, open this repository in VS Code.

---

# 3. Open the `.drawio` File in VS Code

The project contains:

```text
Data Models.drawio
```

This is a Draw.io diagram file.

### Recommended VS Code Extension

Install:

**Draw.io Integration**

You can install it from the VS Code Extensions marketplace.

### Installation Steps

1. Open VS Code.
2. Open the **Extensions** panel.
3. Search for:

```text
Draw.io Integration
```

4. Install the Draw.io integration extension.
5. Open:

```text
Data Models.drawio
```

The diagram should open inside VS Code.

### Alternative: Browser

You can also open the Draw.io file using:

https://app.diagrams.net/

Then:

1. Open diagrams.net.
2. Select **Open Existing Diagram**.
3. Select `Data Models.drawio`.
4. The ER/data model diagram will open in the browser.

No VS Code extension is required when using this method.

---

# 4. Open the `.excalidraw` File in VS Code

The project contains:

```text
workflow.excalidraw
```

This file was created using Excalidraw.

### Recommended VS Code Extension

Install:

**Excalidraw**

The project file itself references the VS Code Excalidraw editor:

```text
pomdtr.excalidraw-editor
```

### Installation Steps

1. Open VS Code.
2. Open the **Extensions** panel.
3. Search for:

```text
Excalidraw
```

4. Install the Excalidraw editor extension.
5. Open:

```text
workflow.excalidraw
```

The diagram and notes should open inside VS Code.

---

# 5. Open Excalidraw in the Browser

You do not need VS Code to view the Excalidraw file.

You can use the Excalidraw web application:

https://excalidraw.com/

If you need to work with the `.excalidraw` file directly:

1. Open Excalidraw in your browser.
2. Use the application's file/open/import functionality.
3. Select:

```text
workflow.excalidraw
```

The diagram can then be viewed and edited in the browser.

---

# 6. SQL Database Setup

The project contains:

```text
datamodels.sql
```

This script is designed for **MySQL**.

You can execute it using:

* MySQL Server + MySQL Workbench
* MySQL CLI
* VS Code with a MySQL extension
* Another MySQL-compatible SQL client

---

## Install MySQL

Download MySQL from:

https://dev.mysql.com/downloads/

You can install:

* MySQL Server
* MySQL Workbench

MySQL Workbench provides a graphical interface for creating and managing MySQL databases.

---

# 7. Run the SQL Script Using MySQL Workbench

### Step 1

Open MySQL Workbench.

### Step 2

Connect to your local MySQL server.

### Step 3

Open:

```text
datamodels.sql
```

### Step 4

Copy or open the SQL script in MySQL Workbench.

### Step 5

Execute the script.

The script will create the schema:

```sql
raw
```

and then create the required tables.

---

# 8. Run the SQL Script Using MySQL CLI

If MySQL is installed and available from your terminal, you can run:

```bash
mysql -u root -p < datamodels.sql
```

Enter your MySQL password when prompted.

---

# 🗄️ Database Schema

The SQL script creates the following schema:

```text
raw
```

The main tables are:

```text
customers
store_branch
products
orders
orders_items
payments
shipments
```

---

# 🔗 Database Relationships

The main relationships in the database are:

```text
customers
    │
    │ 1 : M
    ▼
orders
    │
    ├──────────────► payments
    │
    ├──────────────► shipments
    │
    ▼
orders_items
    │
    ▼
products

store_branch
    │
    │ 1 : M
    ▼
orders
```

### Customer → Orders

One customer can place multiple orders.

```text
Customer 1 ──────── M Orders
```

The relationship is implemented using:

```text
orders.customer_id
        ↓
customers.customer_id
```

---

### Store Branch → Orders

One store branch can process multiple orders.

```text
Store Branch 1 ──────── M Orders
```

The relationship is implemented using:

```text
orders.store_branch_id
        ↓
store_branch.store_branch_id
```

---

### Orders → Order Items

An order can contain multiple order items.

```text
Order 1 ──────── M Order Items
```

---

### Products → Order Items

A product can appear in multiple order items.

```text
Product 1 ──────── M Order Items
```

The `orders_items` table therefore acts as an associative table for the many-to-many relationship between orders and products.

Conceptually:

```text
Orders M ──────── M Products
```

becomes:

```text
Orders 1 ─── M Orders_Items M ─── 1 Products
```

---

### Orders → Payments

An order can have one or more payment records.

```text
Order 1 ──────── M Payments
```

---

### Orders → Shipments

An order can have one or more shipment records.

```text
Order 1 ──────── M Shipments
```

---

# 🧱 Data Modeling Layers

The project demonstrates three major layers of data modeling.

## 1. Conceptual Layer

The conceptual layer focuses on understanding business requirements.

The main activities include:

* Requirement gathering
* Identifying business entities
* Understanding business processes
* Identifying relationships

Example:

```text
Customer
Product
Order
Payment
Shipment
Store Branch
```

---

## 2. Logical Layer

The logical layer converts business requirements into a logical database structure.

It includes:

* Entities
* Attributes
* Primary keys
* Foreign keys
* Relationships
* Cardinality

The ER diagram belongs primarily to this stage.

---

## 3. Physical Layer

The physical layer implements the logical design in an actual database.

For this project, the physical implementation uses:

```text
MySQL
```

The implementation is provided in:

```text
datamodels.sql
```

---

# 🔑 Database Keys Covered

The project explains several database keys.

### Primary Key

Uniquely identifies each record in a table.

Example:

```sql
customer_id INT AUTO_INCREMENT PRIMARY KEY
```

---

### Foreign Key

Connects records between related tables.

Example:

```sql
FOREIGN KEY (customer_id)
REFERENCES customers(customer_id)
```

---

### Candidate Key

A column or minimal combination of columns that can uniquely identify a record and could be selected as a primary key.

---

### Alternate Key

A candidate key that was not selected as the primary key.

---

### Super Key

A set of one or more attributes that can uniquely identify a record.

---

### Composite Key

A key consisting of multiple columns.

---

### Unique Key

Ensures that values in a column or column combination are unique, subject to the database engine's handling of `NULL`.

---

# 🔄 Normalization

The project contains examples of database normalization.

Normalization is used to organize database data and reduce unnecessary duplication and data anomalies.

The project covers:

```text
1NF
2NF
3NF
BCNF
```

Supporting diagrams are available inside:

```text
images/
```

For example:

```text
images/1stNF.png
images/2ndNF.png
images/3rdNF.png
```

---

# ⚡ OLTP

**OLTP — Online Transaction Processing**

OLTP systems are designed to handle frequent operational transactions.

Examples include:

* Creating an order
* Cancelling an order
* Updating customer information
* Recording a payment
* Updating inventory

The project uses an OLTP-style relational database design for the operational database.

---

# 📊 OLAP

**OLAP — Online Analytical Processing**

OLAP focuses on analyzing large amounts of data for reporting and decision-making.

Typical users include:

* Managers
* Business teams
* Analysts
* Leadership teams

The project also introduces:

* Data Warehouses
* Fact Tables
* Dimension Tables
* Dimensional Modeling
* Star Schema
* Snowflake Schema

---

# ⭐ Dimensional Modeling

The project introduces two common dimensional models.

## Star Schema

A central fact table connects directly to multiple dimension tables.

```text
             Dimension
                 │
                 │
Dimension ─── Fact ─── Dimension
                 │
                 │
             Dimension
```

---

## Snowflake Schema

A snowflake schema further normalizes dimension tables.

```text
Dimension
    │
    ▼
Sub-Dimension
    │
    ▼
    Fact
```

---

# 📚 Learning Material

The `workflow.excalidraw` file contains the detailed learning notes and explanations used while building this project.

It includes topics such as:

* Data Modeling
* Data Modeling Layers
* Requirement Gathering
* OLTP
* OLAP
* Database Keys
* Cardinality
* Relationships
* Crow's Foot Notation
* Normalization
* Data Types
* Dimensional Modeling
* Star Schema
* Snowflake Schema

---

# 🖼️ Diagrams

The project contains supporting diagrams in the `images` directory.

```text
images/
├── 1stNF.png
├── 2ndNF.png
├── 3rdNF.png
├── datamodels.png
└── updatedatamodels.png
```

These images can be viewed directly from GitHub without installing any additional software.

---

# 🚀 Quick Start

If you only want to explore the project quickly:

### View the ER Diagram

Open:

```text
Data Models.drawio
```

using:

* Draw.io / diagrams.net
* VS Code + Draw.io extension

### View the database design notes

Open:

```text
workflow.excalidraw
```

using:

* VS Code + Excalidraw extension
* Excalidraw web application

### Create the MySQL database

Run:

```bash
mysql -u root -p < datamodels.sql
```

---

# 🧰 Recommended VS Code Extensions

For the best local development experience, install:

### Draw.io

Used for:

```text
Data Models.drawio
```

### Excalidraw

Used for:

```text
workflow.excalidraw
```

### SQL / MySQL Extension

Optional, but useful for editing and running SQL directly from VS Code.

> Extension names and marketplace publishers can change over time. If an extension does not appear under the exact name above, search the VS Code Marketplace for **Draw.io**, **Excalidraw**, or **MySQL** and verify that the extension supports the relevant file type/database workflow.

---

# 🌐 Browser-Only Setup

You do not need to install VS Code if you only want to inspect the diagrams.

Use:

### Draw.io

https://app.diagrams.net/

Open:

```text
Data Models.drawio
```

### Excalidraw

https://excalidraw.com/

Open:

```text
workflow.excalidraw
```

### MySQL

For executing `datamodels.sql`, you still need access to a MySQL-compatible database environment.

You can use:

* MySQL installed locally
* MySQL Workbench
* A cloud MySQL environment
* Another MySQL-compatible database client

---

# 🔧 Requirements

To work with the complete project locally, you should have:

```text
Git
VS Code
MySQL
MySQL Workbench (optional)
Draw.io support
Excalidraw support
```

For diagram-only viewing, a modern web browser is sufficient.

---

# 📝 Important Notes

* `Data Models.drawio` is a diagram source file, not a normal text document.
* `workflow.excalidraw` is an Excalidraw source file containing the project's visual notes and diagrams.
* `datamodels.sql` is intended for MySQL.
* The SQL script creates the `raw` schema automatically if it does not already exist.
* The project does not require Node.js, Python, or a frontend framework to run.
* GitHub can display the Markdown, SQL, and image files directly, while diagram source files generally require their respective editors/viewers.

---

# 🎯 Project Objective

The main objective of this project is to demonstrate the complete flow from:

```text
Business Requirements
        ↓
Requirement Gathering
        ↓
Conceptual Model
        ↓
Logical Data Model
        ↓
ER Diagram
        ↓
Normalization
        ↓
Physical Data Model
        ↓
MySQL Database
```

This project can be used as a reference for understanding how a real-world relational database can be designed from business requirements and then implemented using SQL.

---

# 👨‍💻 Author

**Rahul Kumar Singh**

Computer Science & Engineering

Interested in:

* Software Development
* Backend Development
* Full Stack Development
* Database Design
* Data Modeling
* AI / Generative AI

---

# 📄 License

This project is intended primarily for learning, practice, and educational purposes.
