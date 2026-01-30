---
icon: book-open
---

# Data Dictionaries

Databases are used to store structured data in computer systems. Relational Databases are the most common type for structured data storage.

A database organises data in tables with rows (records) and columns (attributes).

## Data Dictionary

A data dictionary provides a comprehensive description of each variable stored or referred to in a system. This commonly includes variable name, data type, format, size in bytes, number of characters to display the item including number of decimal places (if applicable), the purpose of each variable and a relevant example. Any validation rules applicable to the data item can also be included.

<figure><img src="../../.gitbook/assets/image (47).png" alt=""><figcaption><p>Data Dictionary from Course Specifications</p></figcaption></figure>

{% hint style="warning" %}
The above data dictionary is in the **expected format and is examinable.**
{% endhint %}

## Database Schema

To create a Relational Database, a data schema is required. A data schema is a blueprint or framework that outlines how data is organised in a database.

It defines the structure of the database in terms of the tables, columns, relationships, and constraints that make up the database. It acts as a guide for how data is stored, accessed, and managed within the database system.

### Components

* **Tables**: Represent entities (like customers, products, orders) in the database. Each table is a collection of related data entries.
* **Columns**: Define the attributes or properties of the entity. For instance, a 'Customer' table might include columns like CustomerID, Name, Address, etc.
* **Data Types**: Each column in a table is associated with a specific data type (like integer, text, date), which defines the nature of the data that can be stored in the column.
* **Primary Keys**: Unique identifiers for each record in a table. They help to ensure that each record can be uniquely identified.
* **Foreign Keys**: Establish relationships between tables, linking each record in one table to one or more records in another.
* **Constraints**: Rules applied to table columns to enforce data integrity, such as NOT NULL, UNIQUE, CHECK, etc.

<figure><img src="../../.gitbook/assets/image (50).png" alt=""><figcaption><p>Data Schema for a Relational Database</p></figcaption></figure>

### Example of Database Tables

The following is an example of database tables.&#x20;

* Each **ROW** is a **RECORD**
* Each **COLUMN** represents a **FIELD.**&#x20;
  * **Data Dictionaries** provide a **description** of each field, including data types and validation.
* A **RECORD (ROW)** is made up of many **FIELDS (COLUMNS).**

<figure><img src="../../.gitbook/assets/image (51).png" alt=""><figcaption><p>Database Tables</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (52).png" alt=""><figcaption><p>Database Schema</p></figcaption></figure>

{% hint style="warning" %}
**BIG HINT:** Data dictionaries **are** relevant for your first **assessment task**. Data schemas **are not.**&#x20;

**We will revisit databases in more detail in the HSC Course (Year 12).**&#x20;
{% endhint %}

