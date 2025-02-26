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
- Orders and Payments → One-to-One: Since two orders cannot have the same details (especially the same ID), each order corresponds to a single payment.
- Clients and Orders → One-to-Many: Users can place multiple orders, but each order must belong to a single customer.
- Reservations and Orders → One-to-One: Each order involves a single reservation for a specific show.
- Seats and Reservations → One-to-Many: A user can reserve multiple seats for the same show, meaning a reservation can include multiple seats.
- Shows and Reservations → One-to-Many: A single show can have multiple reservations.
- Shows and Actors → Many-to-Many: A show can feature multiple actors, and an actor can perform in multiple shows.
