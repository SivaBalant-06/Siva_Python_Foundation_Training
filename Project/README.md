# CarConnect - A Car Rental Platform

## Overview
CarConnect is a Python-MySQL based vehicle rental management system. It supports admin and customer roles, providing full CRUD operations for vehicles, reservations, and user profiles.

## Features
- Customer and Admin Authentication
- Vehicle Registration & Availability Tracking
- Reservation System with Cost Calculation
- Unit Testing for DAO and Services

## Technologies Used
- Python 3
- MySQL
- MySQL Connector for Python
- unittest for testing

## Project Structure
```
CARCONNECT/
│
├── config/
│   └── db.properties
│
├── dao/
│   ├── __init__.py
│   ├── AdminService.py
│   ├── AuthenticationService.py
│   ├── CustomerService.py
│   ├── IAdminService.py
│   ├── ICustomerService.py
│   ├── IReservationService.py
│   ├── IVehicleService.py
│   ├── ReportService.py
│   ├── ReservationService.py
│   └── VehicleService.py
│
├── db/
│   └── carconnectdb.sql
│
├── entity/
│   ├── __init__.py
│   ├── Admin.py
│   ├── Customer.py
│   ├── Reservation.py
│   └── Vehicle.py
│
├── exception/
│   ├── __init__.py
│   ├── AdminNotFoundException.py
│   ├── AuthenticationException.py
│   ├── DatabaseConnectionException.py
│   ├── InvalidInputException.py
│   ├── ReservationException.py
│   └── VehicleNotFoundException.py
│
├── main/
│   ├── MainModule.py
│   ├── test_config.py
│   └── test_services.py
│
├── test/
│   └── __init__.py (optional if test folder is used)
│
├── util/
│   ├── __init__.py
│   ├── DBConnUtil.py
│   └── DBPropertyUtil.py
│
└── README.md
```
## System Architecture
The CarConnect architecture follows a layered design, enabling clean separation of concerns and improved maintainability.
```
+------------------------+
|     User Interface     | (Future web/mobile interface)
+-----------+------------+
            |
            v
+------------------------+
|  Authentication Layer  |
+-----------+------------+
            |
            v
+------------------------+      +-------------------------+
|    Service Layer       | <--> |   Exception Handling    |
| (Customer, Vehicle...) |      +-------------------------+
+-----------+------------+
            |
            v
+------------------------+
|        DAO Layer       |
+-----------+------------+
            |
            v
+------------------------+
|      MySQL Database    |
+------------------------+
```

## How to Set Up and Run

1. **Install MySQL** and create a schema: `carconnectdb`
2. **Configure database**: Edit `config/db.properties` with your DB credentials.
3. **Install dependencies**:
4. **Run the app**:

## Setup Instructions
1. Clone the repository.
2. Setup the database using provided schema.
3. Update `config/db.properties` with your DB credentials.
4. Run `test_services.py` to validate functionality.

## CONCLUSION
The CarConnect case study successfully demonstrates how a modular and scalable Python backend system can be built to support real-world business operations such as vehicle rental. Through clean architecture, layered components, and reliable database integration, it provides a foundation for expanding into a full-fledged enterprise application. With comprehensive unit tests, exception handling, and separation of concerns, the solution ensures reliability and future maintainability.

## Author
Siva Balan T — Hexaware Case Study Project
