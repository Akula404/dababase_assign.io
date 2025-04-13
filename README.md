# dababase_assign.io
**BookStore Database Project**
**Project Overview**
This project involves the creation of a BookStore Database using MySQL, designed to manage and store information related to the operations of a bookstore. The database includes tables for books, authors, customers, orders, shipping, and more. It allows for efficient management of inventory, customer information, and order processing, while enforcing referential integrity between tables.

The system also includes user roles and permissions to ensure that different users have appropriate access to various parts of the database, based on their responsibilities.

**Features**
Book Management: Includes information about books such as title, price, publisher, language, and publication year.
Author-Book Relationship: A many-to-many relationship between books and authors, allowing books to have multiple authors and vice versa.
Customer Management: Tracks customer information such as name, email, and phone number.
Order Management: Allows for the creation and tracking of customer orders, including order lines (books ordered) and order statuses (pending, shipped, delivered).
Shipping Management: Supports various shipping methods to ensure timely delivery of orders.
Address Management: Customers can have multiple addresses, which can be marked with different statuses (e.g., current, old).
User Roles and Permissions: The database supports roles like Admin and other specific roles (Wonder, Enock, Metrine), with tailored permissions for each role to restrict access to specific tables.

**Technology Stack**
MySQL: The relational database management system used for creating and managing the database.
SQL: Used for defining the database schema, tables, and relationships.
Draw.io for Entity relationship visualization

**Setup Instructions**
1. Clone the Repository
bash
git clone https://github.com/Akula404/dababase_assign.io.git
cd bookstore-database
2. Install MySQL
Make sure MySQL is installed on your system. If it is not installed, you can download and install MySQL from the official website:

Download MySQL

3. Create the Database
Log into MySQL:

bash
mysql -u root -p
Once you're in MySQL, create the BookStore database and use it:

sql
CREATE DATABASE BookStore;
USE BookStore;
4. Execute the SQL Script
Execute the provided SQL script to create all the necessary tables and relationships.

sql
-- Paste the full SQL script provided here
5. Set Up User Roles and Permissions
The script includes roles and permissions. Ensure that the roles are correctly set and permissions are granted to the appropriate roles.

6. Create Users and Assign Roles
The script will also create users (Carlos, Wonder, Enock, Metrine) and assign them roles. You can test the permissions by logging in with each user:
sql
-- Admin User (Carlos with full access)
CREATE USER 'Carlos'@'localhost' IDENTIFIED BY '1234';
GRANT ALL PRIVILEGES ON BookStore.* TO 'Carlos'@'localhost';

-- Wonder User
CREATE USER 'Wonder'@'localhost' IDENTIFIED BY '4321';
GRANT 'role_wonder' TO 'Wonder'@'localhost';

-- Enock User
CREATE USER 'Enock'@'localhost' IDENTIFIED BY '5678';
GRANT 'role_enock' TO 'Enock'@'localhost';

-- Metrine User
CREATE USER 'Metrine'@'localhost' IDENTIFIED BY '8765';
GRANT 'role_metrine' TO 'Metrine'@'localhost';

7. Test the Database
Test the functionality by running some queries to verify that all the tables have been created and that the relationships between tables (foreign keys) are working properly.

Example Query:
sql
SELECT * FROM book;
Usage
Once the database is set up, you can use it to perform operations related to the bookstore's business logic, such as:

Managing Books: Add new books to the book table.
Managing Authors: Add new authors and link them to books through the book_author table.
Managing Customers: Add customer information and store multiple addresses in the customer_address table.
Managing Orders: Create new orders and track their status in the cust_order and order_history tables.
Shipping Management: Add and update shipping methods for customer orders.

**Database Schema**
Here is an overview of the key tables and their relationships:

book: Stores information about books (book_id, title, price, publication year).
book_author: Many-to-many relationship between books and authors.
author: Stores author information.
book_language: Stores available languages for books.
publisher: Stores information about book publishers.
customer: Stores customer details like name, email, and phone number.
customer_address: Tracks customer addresses and their status.
address_status: Defines the status of addresses (e.g., current, old).
address: Stores address details for customers.
country: Stores country information for addresses.
cust_order: Tracks customer orders.
order_line: Associates books with customer orders.
shipping_method: Stores shipping methods available for orders.
order_history: Tracks changes to the order status (e.g., pending, shipped, delivered).
order_status: Stores order status types (e.g., pending, shipped).

**User Interface Design**
This project is currently a backend database with no front-end interface. However, you can easily integrate this database with a web application built using frameworks like Django or Flask. The web interface would allow:

Admin Interface: For managing books, authors, customers, and orders.
Customer Dashboard: For managing customer orders and addresses.

**Contributing**
Contributions to the project are welcome! If you wish to enhance or improve the database schema or functionality, feel free to fork the repository and submit a pull request.

Authors:
Carlos Oyanda
Wonder Munga
Enock Bosire
Metrine Regina

