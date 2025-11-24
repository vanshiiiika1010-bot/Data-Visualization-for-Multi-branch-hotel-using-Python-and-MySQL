# Multi-Branch Hotel Booking & Data Visualization

## Project Overview
This project is a Python + MySQL based application designed to manage hotel customers, rooms and bookings across multiple branches.  
It also generates simple bar charts for data visualization.  
The project focuses on problem solving, modular programming, algorithms, and connecting theory with a real-world domain.

## Objectives
- Identify a real-world problem (hotel data management)
- Apply Python programming concepts
- Use modular design and top-down approach
- Perform CRUD operations using MySQL
- Generate analytics and visualizations
- Connect concepts of data structures, loops, functions, and file/database handling


## Features
### Customer Module
- Add Customer  
- View Customers  

### Room Module
- Add Room  
- View Rooms  

### Booking Module
- Create Booking (auto transaction ID)  
- View Bookings  

### Data Visualization
- Customer Age Distribution Chart  
- Other plots can be added


## Installation & Setup

### Install Python
Download Python 3.10+  
https://www.python.org/downloads/

### Install MySQL
Download MySQL Server + Workbench  
https://dev.mysql.com/downloads/installer/

Use:
- Username: **root**
- Password: (your password)
- Port: **3306**

### Install Required Libraries
Open VS Code terminal:
pip install -r requirements.txt

## Create MySQL Database

Run these commands inside MySQL Workbench:
REATE DATABASE hotel_project;
USE hotel_project;

CREATE TABLE customer (
customerid INT PRIMARY KEY,
name VARCHAR(30),
email VARCHAR(40),
address VARCHAR(100),
age INT
);

CREATE TABLE room (
roomno INT PRIMARY KEY,
price INT,
branch VARCHAR(30),
type VARCHAR(20)
);

CREATE TABLE booking (
customerid INT,
roomno INT,
days INT,
transactionid INT,
FOREIGN KEY (customerid) REFERENCES customer(customerid),
FOREIGN KEY (roomno) REFERENCES room(roomno)
);


## How to Run the Project
In VS Code terminal:
python main.py

You will see the menu:

HOTEL PROJECT MENU

Add Customer

View Customers

Add Room

Create Booking

View Chart

Exit


