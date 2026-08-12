
1. Title

Abi Mart – Online Grocery & Daily Essentials Shopping Platform

2. Domain

E-Commerce / Online Grocery & Retail Management

3. Who is the User?
Customer – Browses products, searches for items, adds products to cart, places orders, and tracks order status.
Store Admin – Manages products, categories, prices, inventory, customers, and orders.
Delivery Staff – Views assigned orders and updates delivery status.
4. What Problem Are We Solving?

Small grocery stores often manage product inventory and customer orders manually, which can lead to stock errors, delayed order processing, and difficulty tracking sales. Customers may also have to visit the store physically or contact the shop to check product availability and place orders. Abi Mart provides a centralized online platform where customers can view available products, place orders, and track their purchases. For example, a customer who needs groceries such as rice, vegetables, snacks, and household items can select them through Abi Mart, place one order, and receive updates without visiting the store.

5. Proposed Solution

Abi Mart will provide the following features:

User registration and login
Customer profile management
Product browsing and search
Product categories
Product details with price and availability
Add/remove products from cart
Quantity management
Order placement and order history
Order status tracking
Inventory/stock management
Admin product management (add, update, delete)
Admin category management
Admin order management
Delivery assignment and status updates
Basic sales and order reports
Payment status management
6. Core Entities / Database Tables
Users – Stores customer, admin, and delivery staff information.
Roles – Defines system roles and permissions.
Products – Stores product name, description, price, quantity, and availability.
Categories – Organizes products into categories.
Cart – Stores products selected by customers before checkout.
Cart_Items – Stores individual products and quantities in a cart.
Orders – Stores customer order details and order status.
Order_Items – Stores products, quantities, and prices belonging to an order.
Payments – Stores payment method and payment status.
Deliveries – Stores delivery assignment and delivery status.
Addresses – Stores customer delivery addresses.
7. User Roles & Permissions
Role	Permissions
Admin	Manage users, products, categories, inventory, orders, payments, and reports
Customer	Register/login, browse products, manage cart, place orders, view order history, and track orders
Delivery Staff	View assigned orders and update delivery status
8. Success Criteria
A customer should be able to register and log in within 1 minute.
A customer should be able to find a product within 30 seconds.
A customer should be able to add products to the cart and place an order within 2 minutes.
Customers should be able to view their current and previous orders.
Admin should be able to add or update a product in under 1 minute.
Inventory should automatically update when an order is successfully placed.
Delivery staff should be able to update an order's delivery status easily.
The system should prevent customers from ordering products that are out of stock.
9. Out of Scope

To keep the project manageable, the following will not be included in the initial version:

Multi-vendor marketplace functionality
International shipping
AI-based product recommendations
Advanced warehouse management
Real-time GPS delivery tracking
Subscription-based grocery deliveries
Voice-based shopping
Cryptocurrency payments
Complex accounting and taxation systems
Mobile application development (the initial project will focus on the web application)
10. Chosen Track

Java – Spring Boot

Technology Stack:

Backend: Java + Spring Boot
Database: MySQL
API: REST API
Security: Spring Security + JWT
ORM: Spring Data JPA / Hibernate
Frontend: HTML, CSS, JavaScript / React (depending on project requirements)
