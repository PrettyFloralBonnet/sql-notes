# SQL and databases

## Database

A **database** is a set of data structured in a certain way to scale with organizations that store and manage massive amounts of data.

## Database Management Software (DBMS)

Software used to manage the database (CRUD operations, ensuring that the data stays secure, transaction management etc.). This is what people actually mean when they drop names like MySQL, PostreSQL, Cassandra, RabbitMQ etc. Most of them are compatible with SQL.

A subset of DBMS that uses a relational database model is referred to as RDBMS (relational database management software).

The rules enforced by the RDBMS on users when interacting with databases through it are known as the **13 Rules of Codd** (named after the IBM programmer who first came up with the relational database model).

## Structured Query Language (SQL)

A declarative way to communicate and interact with the DBMS.

## Five main types of database models

* **relational**
* document (good scalability)
* key value (e.g. Redis)
* graph (e.g. AWS Neptune)
* wide columnar

## Legacy database models

Those are not in wide use anymore today, but are important for historical and methodology related reasons.

* hierarchical
* networking

The **hierarchical model** has been used by IBM in the 60s and 70s and has since fallen out of favour due to its inefficiencies. It stores and organizes data in a tree like structure of one-to-many relationships, where a parent node can have multiple children, but every child can only have a single parent. The data stored in the nodes is **tightly coupled** (if we delete the parent node, the child information goes away with it). A modern day example would be something like XML.

The **networking model** expanded on the hierarchical model, allowing many-to-many relationships, which made it more complicated for the software to manage them. This eventually led to the development of the relational model that is the standard today.

## The relational model

This model has done away with the parent-child structure, instead choosing to organize data in **tables**, or, in other words, relations. Every entity stored in a table structure is an individual piece of data, with a unique identifier, and can be tied together with other entities (stored in different tables that exist within the structure) thanks to relations that exist between them.

The logic of how the relationships are linked is managed by the **database management software**.

## Tables

A **table** is a representation of an object, an entity, a concept - some kind of data. Each table has a **name** (which relates to the concept of the data we're going to store), **columns** (that store specific types of data) and **rows** (each representing a single piece of data for that table).

## Columns

One single column is simply a column, a part of the table that stores specific types of data. However, all of the table's columns (or **attribures**) together are that table's **degree of the relation**.

When we talk about what a column can store, we call that the **domain** or the **constraint** of the column/attribute. E.g. in a column "date of birth", only put dates (in a specific format).

## Rows

Another word for "rows" is **tuples**. One tuple is a singular row of data. Each tuple follows the column constraints.

All of the tuples in the table is referred to as the **cardinality** of the table.

## Primary and foreign keys

The **primary key** is what uniquely identifies every row of data in the table.

The **foreign key** is the identifier that **relates** a row in one table to a different row in another table by **referencing its primary key**. This is what allows for the relational database model to work.

## Query

A **query**, or an **SQL statement**, is an instruction to interact with the database, composed from parts called **clauses** that make use of **keywords**, **identifiers**, **expressions** and **conditions**.

Quick side note: SQL comments looks like this: `--` and `/* */`

## OLTP vs. OLAP

OLTP stands for **On-Line Transaction Processing**, operations (using relational databases) that aim to support the day to day work in an organization (e.g. by storing data on users, orders, purchases etc.).

OLAP stands for **On-Line Analytical Processing**, where you take the data from OLTP and try to analyze it, figure out what decisions can be made based on the existing information.
