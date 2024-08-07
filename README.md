Online Book Store
An online book store web application built using Java, JDBC, and Generic Servlets.

Table of Contents
Introduction
Features
Technologies Used
Installation and Setup
Usage
Admin Access
User Access
Contributing
License
Introduction
The Online Book Store is a web application that allows users to purchase books online. It provides features for managing books, maintaining sales history, and offering a user-friendly interface. This project is a mini-project developed using Java, JDBC, and Generic Servlets.

Features
For Selling Books Online
Maintaining Books Selling History
Adding and Managing Books
User-Friendly Interface
Implementation of Generic Servlets in Java
Technologies Used
Front-End Development:

HTML
CSS
JavaScript
Back-End Development:

Java (JDK 8+)
JDBC
Servlet
MySQL
Apache Maven
Database:

MySQL
Installation and Setup
Install the following software and tools:

MySQL
Eclipse (Enterprise Edition)
Java (JDK 8+)
Tomcat v8.0+
Apache Maven
Initialize the database:

Open the MySQL command prompt or MySQL Workbench.

Log in as the administrator user: mysql -u <username> -p (enter the password if asked).

Copy and paste the following MySQL commands to create the database and tables:

create database onlinebookstore;  
use onlinebookstore;  
create table books(barcode varchar(100) primary key, name varchar(100), author varchar(100), price int, quantity int);  
create table users(username varchar(100) primary key, password varchar(100), firstname varchar(100), lastname varchar(100), address text, phone varchar(100), mailid varchar(100), usertype int);  
insert into books values('10101', 'C', 'James', 500, 5);  
insert into books values('10102', 'Java', 'Scott', 150, 13);  
insert into books values('10103', 'Database', 'Charles', 124, 360);  
insert into users values('User', 'Password', 'First', 'User', 'My Home', '42502216225', 'User@gmail.com', 2);  
insert into users values('Admin', 'Admin', 'Mr.', 'Admin', 'Haldia WB', '9584552224521', 'admin@gmail.com', 1);  
insert into users values('mgmg', 'mgmg', 'Mgmg', 'u', 'high', '1236547089', 'mgmg@gmail.com', 2);  
commit;  
Import and run the project in Eclipse Enterprise Edition:

Open Eclipse Enterprise Edition.
Click on File > Import > Git > Projects From Git > Clone URI.
Paste the repository URL: https://github.com/Thant998/onlinebookstore.git.
Select the J2EE branch and click Next > Next > Finish.
Go to OnlineBookStore > constants > IDatabase.java and update the USER_NAME and PASSWORD values to match your installed MySQL admin user credentials.
If Tomcat Server is not configured in Eclipse, right-click on the project, select Run As > Run on Server, choose Tomcat v8.0, and follow the on-screen instructions.
In the Server tab, double-click on the Tomcat Server, go to Ports, and change the Http/1.1 port number to 8080. Close and save.
Right-click on the project, select Run As > Run on Server, choose Tomcat v8.0, and click Next > Add All > Finish.
The application should now be running at http://localhost:8080/onlinebookstore/.
Usage
Admin Access
The default username and password for the admin user are:

Username: Admin
Password: Admin
The admin user has the following access:

Add new books
View available books
Remove books
Increase the quantity of books
User Access
The default username and password for a regular user are:

Username: mgmg
Password: mgmg
The user has the following access:

Create a new account or register
Log in
View available books
Select books to buy
Select the quantity of books
Buy books
Get a payment receipt
Contributing
Suggestions and project improvements are welcomed. Please feel free to contribute to the project by submitting issues or pull requests.
 
