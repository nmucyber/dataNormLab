## What is database normalization?

**Database normalization** is a process used to organize a database efficiently by reducing redundancy and improving data integrity. It involves structuring a database into multiple related tables to eliminate duplication and dependency issues.
### Why Normalize a Database?
1. **Reduce Redundancy** - Avoid storing the same data in multiple places
2. **Improve Data Integrity** - Ensures data consistency and accuracy
3. **Make Updates Easier** - Changes, such as adding additional attributes (fields) to data will only need to be made in one place
4. **Enhance Query Performance** - Well-structured databases perform 
## Relational database modeling 101

**Relational database modeling** - Is the process of designing a structured database that organizes data into ***tables*** with will defined relationships.  It ensures data integrity, minimizes redundancy, and allows for efficient retrieval and management of information.
### Key Concepts of Relational Database Modeling
- **Tables**
	- Fundamental building blocks of a relational database
	- Each ***table*** represents an entity (e.g. Customers, Orders, Products)
	- ***ables*** have 
		- ***columns***: also know as fields, or attributes
		- ***rows***: records of data
	- An Excel worksheet is a simple table.  
		- Columns (A,B,C,D) can be named with attributes (FirstName, LastName, Age, Grade)
		- Rows (1,2,3,4) contain a record for each student
- **Primary Key (PK)**
	- A unique identifier for each row in a table.
	- Ensures that no two records have the same identifier.
		- ==When you designate a field as a PK the database will impose a data constraint that enforces the the PK data is unique and will not allow duplicates
		- Most database developers will create a ***sequence*** (range of integers that the PK is created from when a new record is created. )
		- Example: `UserID` in a **Users** table
- **Foreign Key (FK)**
	- A column (or set of columns) that establishes a relationship between two tables
	- ==Always refers to the primary key (PK) of another table ==
	- For example: `UserId` (FK) in the **Playlist** table links to `UserID`(PK) in the **Users** table
- **Realtionships**
	- Define how tables are connected
	- **Types of Relationships**
		- 1. **One-to-One (1:1)** - Each record in *TableA* corresponds to one record in *TableB*
		- 2. **One-to-Many (1:M)** - One record in *TableA* can have multiple records in *TableB*.  For example,  in the **Users** table there is only one `UserID` representing a user because it is a primary key and has a data constraint.  However, in the **Playlist** table a `UserID`(FK) can have multiple records because a user can have multiple playlists.
		- 3. **Many-to-Many (M:N)** - Multiple records in *TableA* can be associated with multiple records in *TableB*, and vice versa.  This requires a third "join" (also called "junction")  table to manage the relationship.   For example, An author can write multiple books, and a book can be written by multiple authors. A join table (e.g., `authors_books`) would store author IDs and book IDs to represent the authorship

### Example of Spotify Entity Relationship Diagram 
An **Entity Relationship Diagram or (ERD)** is a way of visualizing relationships between tables
<img src="Spotify ERD.png">

## Creating Dimension Tables

## Creating a star schema in the data model

## Exploring the model with Power Pivot

## 2nd Normal form (2NF)

## 3rd Normal form (3NF)

## Creating a snowflake schema

## Pros and cons of normalization


