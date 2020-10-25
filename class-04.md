# Advanced Mongo/Mongoose

### Why would a developer choose to make data models?
- Ensures that all data objects required by the database are accurately represented. The omission of data will lead to the creation of faulty reports and produce incorrect results.
- A data model helps design the database at the conceptual, physical, and logical levels.
- Data Model structure helps to define the relational tables, primary and foreign keys, and stored procedures.
- It provides a clear picture of the base data and can be used by database developers to create a physical database.
- It is also helpful to identify missing and redundant data.
- Though the initial creation of the data model is labor and time consuming, in the long run, it makes your IT infrastructure upgrade and maintenance cheaper and faster.

### What purpose do CRUD operations serve?
performing these methods Create, Read, Update, and Delete

### What kind of database is Postgres? What kind of database is MongoDB?
**MongoDB:** open-source software that is used for non-relational database management systems<br />
**Postgres:** is used for the relational database management system

### What is Mongoose and why do we need it?
Helps the developer to work with dynamic data collection that has no structure defined, it implements validation, It also creates Model abstraction which makes it easier to work with, so it looks like you are working with just objects rather than pure data.

### Describe how NoSQL Databases scale horizontally
1. Horizontal scaling means that you scale by adding more machines into your pool of resources whereas Vertical scaling means that you scale by adding more power (CPU, RAM) to an existing machine.<br />
2. because its easier to scale dynamically by adding more machines into the existing pool

## Vocabulary Terms

**database:**  organized collection of structured information, or data, typically stored electronically in a computer system<br />
**data model:**  is the act of exploring data-oriented structures. Like other modeling artifacts, data models can be used for a variety of purposes, from high-level conceptual models to physical data models. From the point of view of an object-oriented developer, data modeling is conceptually similar to class modeling. With data modeling, you identify entity types whereas with class modeling you identify classes. Data attributes are assigned to entity types just as you would assign attributes and operations to classes<br />
**CRUD:** performing these methods, Read, Update, and Delete<br />
**schema:** is an abstraction used to represent the storage of data in a database. It not only describes the organization of data but also represents the relationship between various tables in a database.<be />
**sanitize:**  checked by software to see if it contains any information that might be harmful to the system. <br />
**Structured Query Language (SQL)** is a programming nomenclature used to do set operations (like union, intersect, and minus) to organize and retrieve information in relational databases <br />
**Non-SQL (NoSQL):** non-tabular, and store data differently than relational tables. NoSQL databases come in a variety of types based on their data model. <br />
**MongoDB:**  a cross-platform document-oriented database program. Classified as a NoSQL database program, MongoDB uses JSON-like documents with schema<br />
**Mongoose:** Object Data Modeling (ODM) library for MongoDB and Node.js. It manages relationships between data, provides schema validation, and is used to translate between objects in code and the representation of those objects in MongoDB.<br />
**record:**  composed of fields and contains all the data about one particular person, company, or item in a database.<br />
**document:**  is a type of nonrelational database that is designed to store and query data as JSON-like documents. Document databases make it easier for developers to store and query data in a database by using the same document-model format they use in their application code<br />
**Object Relation Mapping (ORM):**  a programming technique for converting data between incompatible type systems using object-oriented programming languages