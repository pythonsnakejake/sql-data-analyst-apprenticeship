# What Is a Database?

In this lesson, we explore the fundamental question, **'What Is a Database and Why Do we Need One?'**

We began with some of the benefits of using a database in place of a spreadsheet, examining problems we would expect to emerge as a spreadsheet scales, and how a relational database can solves these problems. Some of the problems we highlighted included:

| **Problem** | **Spreadsheet Reality** | **Database Solution** |
| :--- | :--- | :--- |
| **Inconsistent values** | Anything goes in any cell | **Constraints** enforce allowed values |
| **Wrong data types** | "fifteen" in a number column | **Data types** reject invalid entries |
| **Duplicate data** | Copy everything everywhere | **Normalization**: store once, reference many times |
| **Concurrent editing** | Last save wins, data lost | **Transactions** manage simultaneous access |
| **Referential chaos** | Delete a customer, orders reference nothing | **Foreign keys** maintain relationships |

## The relational model in one paragraph
Data is organised into tables, each having columns and rows. Each column has a defined data type which only accepts that specific data type. Each row represents one instance of whatever that table tracks (one customer, one order, one product etc). Every row has a **primary key**, such as an ID, which is a unique identifier that is used to refer to that specific row. Tables relate to each other through **foreign keys**: the orders table doesn't copy the customers name and address - it only stores the customer's ID, pointing to the one authoritative row in the customers table.
