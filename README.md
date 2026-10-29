# Restaurant Management System – ER Diagram

## Objective

To design and develop an Entity Relationship (ER) Diagram for a Restaurant Management System to manage customers, waiters, tables, food orders, chefs, supervisors, and billing efficiently.

## Purpose

The purpose of this project is to understand database design concepts by identifying entities, attributes, primary keys, foreign keys, relationships, and constraints in a real-world restaurant management application.

## Business Context

A restaurant requires an efficient database management system to handle daily operations such as customer service, table allocation, food ordering, food preparation, staff management, and payment processing.

The Restaurant Management System helps maintain accurate records and improves coordination between customers, waiters, chefs, and supervisors.

## Requirements

- Store customer information and contact details.
- Maintain waiter details and assign waiters to customers.
- Manage restaurant tables and their availability.
- Record customer orders with date, time, amount, and status.
- Maintain food menu items with categories and prices.
- Track ordered food items and quantities.
- Assign chefs to prepare food orders.
- Allow supervisors to manage order items.
- Generate customer bills and track payment status.

## ER Diagram

<img width="4512" height="2226" alt="restorent" src="https://github.com/user-attachments/assets/e48d2a38-49e2-49aa-be3b-93efe3a3260e" />

## Entities and Attributes

| Entity | Attributes | Description |
|---|---|---|
| Customer | CustomerID (PK), Name, ContactDetails, TableNo | Stores customer information |
| Waiter | WaiterID (PK), Name, ContactDetails | Stores waiter information |
| Table | TableID (PK), Location, Status | Maintains restaurant table details |
| Order | OrderID (PK), DateTime, TotalAmount, Status | Stores customer order information |
| Order Item | OrderItemID (PK), OrderID (FK), FoodItemID (FK), Quantity, Status | Maintains individual ordered food items |
| Food Item | FoodID (PK), Name, Category, Description, Price | Stores food menu details |
| Chef | ChefID (PK), Name, ContactDetails | Stores chef information |
| Supervisor | SupervisorID (PK), Name, ContactDetails | Maintains supervisor details |
| Bill | BillID (PK), OrderID (FK), TotalAmount, PaymentStatus | Stores billing and payment information |

## Relationships and Constraints

| Relationship | Cardinality | Description |
|---|---|---|
| Waiter – Customer | 1:M | One waiter can serve multiple customers |
| Customer – Table | M:1 | Multiple customers can be associated with one table |
| Waiter – Order | 1:M | One waiter can create multiple orders |
| Table – Order | 1:M | One table can have multiple orders over time |
| Order – Order Item | 1:M | One order contains multiple order items |
| Order Item – Food Item | M:1 | Multiple order items can refer to the same food item |
| Chef – Order Item | 1:M | One chef can prepare multiple order items |
| Supervisor – Order Item | 1:M | One supervisor can manage multiple order items |
| Order – Bill | 1:1 | Each completed order generates one bill |

## Assumptions

1. Every customer has a unique CustomerID.
2. A waiter can serve multiple customers and handle multiple orders.
3. Each restaurant table has a unique TableID.
4. One order may contain multiple food items.
5. Every food item has a unique FoodID.
6. A chef can prepare multiple order items.
7. A supervisor can manage multiple order items.
8. Each completed order generates one bill.
9. Payment status is maintained for every bill.

## Conclusion

The Restaurant Management System ER Diagram represents the database structure required for efficient restaurant operations.

It establishes relationships between customers, waiters, tables, orders, food items, chefs, supervisors, and bills.

This database design helps reduce data redundancy, improve data consistency, and simplify restaurant management operations.

## Tools Used

- Draw.io / diagrams.net
- GitHub
- Entity Relationship Modeling

## Project

**Project Title:** Restaurant Management System – ER Diagram

**Project Type:** Database Management System (DBMS)

**Diagram Type:** Entity Relationship Diagram (ERD)
