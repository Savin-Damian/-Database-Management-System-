# Database-Management-System

## Project Description
This project aims to create an application that allows users to book seats for various cultural performances and artistic events. This web application provides an easy-to-use interface, facilitating access to information about available shows for both customers and administrators.

Features:

- Users can search for available shows, view details, and book tickets online.
- Administrators can manage data (add, delete, modify show types).
- Shopping cart management, including viewing and editing its contents.

## Technologies Used
For the development of this application:

- Front-end: HTML, CSS, and JavaScript.
- Back-end: PHP.

## Database Structure and Table Relationships

After analyzing and implementing the project, several types of relationships have been established between tables: one-to-one, one-to-many, and many-to-many.
- Comenzi and Plata → One-to-One: Since two orders cannot have the same details (especially the same ID), each order corresponds to a single payment.
- Client and Comenzi → One-to-Many: Users can place multiple orders, but each order must belong to a single customer.
- Rezervari and Comenzi → One-to-One: Each order involves a single reservation for a specific show.
- Locuri and Rezervari → One-to-Many: A user can reserve multiple seats for the same show, meaning a reservation can include multiple seats.
- Spectacole and Rezervari → One-to-Many: A single show can have multiple reservations.
- Spectacole and Actori → Many-to-Many: A show can feature multiple actors, and an actor can perform in multiple shows.


## Logical Model

![ModelLogic](https://github.com/user-attachments/assets/4ff9e58b-3337-487b-8ae2-5f12b72374cf)

## Relational Model

![ModelRelational](https://github.com/user-attachments/assets/42b4fe08-c59d-4e6a-84cb-b6611d8ee1a9)

## Constraints Description

At the level of each table, there are four types of constraints: primary key (PK), unique (UN), not null (NN), and check (CK), with the last two being the most commonly used.

Primary key constraints are generated by the database through an auto-increment mechanism, providing an automatic way to assign unique values to each record.
The tables Spectacole, Locuri, Actori, Client, Comenzi, Plata, Rezervari all have the ID field as their primary key. The necessity of these primary keys is especially highlighted when forming relationships between tables, where primary foreign keys are created. Moreover, primary keys identify the table, which facilitates data storage in the database, referring to these keys in a unique way in the fields of the data.

Unique constraints are necessary to ensure that there are no clients with the same email address or phone number and to guarantee the uniqueness and integrity of the data for each order.

Not null constraints indicate that certain columns in a table cannot remain unfilled; implicitly, certain data must be known (in their absence, errors will be generated when entering data). Attributes with these constraints include adresa, email, telefon in the Client table, total_pret in the Plata table, rand and numar in the Locuri table, as well as attributes that constitute the calendar data and attributes containing first and last names.

Check constraints are necessary to impose specific conditions on the data entered into a table. These constraints ensure that the data adheres to certain rules or conditions defined by the user. Thanks to these constraints, in our application, we can check if the email address follows a certain format, if the phone number consists of ten digits, if the total price is a positive number, if the type of a show is Opera or Balet, if the number of seats per row is between 1 and 18, or if the number of rows is between the characters ‘A’ and ‘N’.

## Connecting to the database

![Screenshot (30)](https://github.com/user-attachments/assets/0d7b9dd5-ed9c-405e-9633-6794f042b48c)

## Screenshots from the user interface 


![Screenshot (12)](https://github.com/user-attachments/assets/6c131fb0-ccd5-4edc-97d1-3bd390cc11ae)

![Screenshot (38)](https://github.com/user-attachments/assets/6421345c-6518-40c0-b973-61dc588b2669)
![Screenshot (40)](https://github.com/user-attachments/assets/4eb68a21-7e16-441f-a74c-54b75c7df3a4)
