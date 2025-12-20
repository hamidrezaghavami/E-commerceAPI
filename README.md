# E-Commerce API Project

This project involves building a logic-heavy RESTful API for an e-commerce platform. It focuses on complex data models, authentication, and integration with external payment services.

## Tech Stack Requirements
* **Server:** REST API (Node.js/Express.js recommended).
* **Database:** A database capable of handling complex relationships (Products, Carts, Users, Orders).
* **Authentication:** JWT (JSON Web Tokens).
* **External Integration:** Payment Gateway (e.g., Stripe).

## Functional Requirements

### 1. Authentication & Users
* **Sign Up & Log In:** Users must be able to create an account and authenticate.
* **JWT Implementation:** Secure the API using JWT to handle multiple concurrent users.

### 2. Product Management
* **View Products:** Users should be able to browse available products.
* **Search:** Implement search functionality for products.
* **Admin Panel:** A restricted area/role for administrators to:
    * Add new products.
    * Set and update prices.
    * Manage inventory levels.

### 3. Shopping Cart
* **Add to Cart:** Users can add products to their shopping cart.
* **Remove from Cart:** Users can remove items from their cart.

### 4. Checkout & Payment
* **Checkout:** Users can proceed to checkout with the items in their cart.
* **Payment Integration:** Integrate with an external service (like Stripe) to process payments.
* **Order Recording:** Save transaction details and order status in the database.

## Core Concepts to Demonstrate
* **CRUD Operations:** Create, Read, Update, and Delete data efficiently.
* **Complex Data Modeling:** Manage relationships between Users, Products, Carts, and Orders.
* **External Service Interaction:** Handling third-party API calls (Payment Gateway).