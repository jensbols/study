# BACKEND
---

##  ORM

>**Object-Relational Mapping** is a technique for storing, retrieving, updating and deleting from an object-oriented program in a relational database.

* Maakt gebruik van een datalaag om te vertalen tussen tussen je klassen en methoden en de database. 
* De datalaag is typisch een library geschreven in de OO taal (java, etc..) dat deel uitmaakt of samenwerkt met je web framework.

De datalaag ontvangt een object van een klasse en vormt deze om zodat het object opgeslagen kan worden in de databank. Bij het ophalen van data wordt een object gecreeërd met data uit de databank.

---
## ACID

**Transaction** = a single unit of work, can be one or multiple queries.

> **Atomicity, Consistency, Isolation, Durability** are 4 properties in a database system that help making sure we are able to perform the transactions in a reliable manner.


**Atomicity** = Entire transaction must finish or revert the database to old state.


**Consistency** = Helps ensure the data to be in Correct state. Data integrity constraints must be followed. (Constraints / Cascades / Triggers)

**Isolation** = Concurrent execution safe. How the database should perform when there concurrent executions. (Optimistic vs Pessimistic Concurrency Control)

**Durability** = Committed transactions to be persisted in non-volatile memory. Safe in case of crashes.

---

