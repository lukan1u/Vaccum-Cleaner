---
Date: 2023-10-03T10:59:00
Summary:
---
# Introduction to databases
---
#settings
Table of contents >>> 
Previous page >>> 
Next Page >>>

## Database terminology
---
- Database is collectino of data
- Data is information that is processed which could be anything like user_ids, passwords, text, images etc
- Data needs to be given a meaning

## Types of databases
---
- Multimedia databases
- Geographic information systems (gis)
- Biological and genome databases
- Data warehouses

## Database (DBMS)
---
- Database management system (DBMS) is a software that enables users to  create and maintain a database. It handles storage, retrieval and modification of data in a computer system.
- is a single repo to maintain data defined once and accessed by various users and applications.
![[Pasted image 20231003112123.png]]

## File system processing system vs DBMS
---
- Data redundancy
- data inconsistency
- unsecure data

## Why do we need the databases
---
- Data independence and efficient access
- Data intergrity
- Security
- uniform data administration
- Concurrent access
- Data recovery and backup
## Operations of DBMS
---
- Faster Development of New Applications ➢ A well-designed DB is always modular and helps in developing new applications as most of the data can be retrieved by using queries
• Better Data Accessibility ➢ Query Language support allows any user to get data required anytime. 
• More Control of Concurrency ➢ Simultaneous access by two or more users is allowed. 
• Better Backup and Recovery Procedures ➢ Simple backup. Imagine backing up all the files of all the departments.

## Operations of DBMS … 
---
• Support for different types of operations on data ➢ CRUD –create, read, update, delete 
• ACID: Atomicity –transactions are all or nothing; consistency –valid consistent data is saved; isolation –transactions do not affect each other; durability –written data will not be lost. 
• Views: a subset of the database visible to users (e.g., a level of security, customized appearance of database, can present a consistent, unchanging picture of the structure of database despite underlying changes to schema)


## Actors on the Scene
---
• Database Administrators - The DBA is responsible for authorizing access to the database, coordinating and monitoring its use, and acquiring software and hardware resources as needed. 
• Database Designers - responsible for identifying the data to be stored in the database and for choosing appropriate structures to represent and store this data.
• End Users - the people whose jobs require access to the database for querying, updating, and generating reports; the database primarily exists for their use.

## Nature of Database Systems
---

• A typical database (relational) has a complete definition or description of the database structure and constraints. • The definition is stored in the DBMS catalog, which contains information such as the structure of each file, the type and storage format of each data item, and various constraints on the data. This information is called metadata. • Relational databases have a schema • Newer database system called NoSQL systems do not require a meta-data • Rather the data is stored as self-describing data that includes the data item names and data values together in one structure • NoSQL databases do not have a schema or are schemaless


![[Pasted image 20231003112820.png]]





