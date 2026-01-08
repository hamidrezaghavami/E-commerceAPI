# E-commerce API (Node.js/Express)

[﻿github.com/hamidrezaghavami/E-commerceAPI.git](https://github.com/hamidrezaghavami/E-commerceAPI.git) 

**Architecture Overview:** Generate a detailed system architecture for a RESTful API named **"e-commerceapi"**. Use a **Layered Architecture** pattern:

1. **Client Layer:** Mobile/Web apps.
2. **API Gateway/Server:** Node.js with Express.js.
3. **Middleware Layer:** JWT Authentication, Request Validation, and Admin Authorization.
4. **Service Layer:** Business logic for Cart calculation, Inventory management, and Stripe Payment processing.
5. **Data Access Layer:** SQL-based database for relational data modeling.
**Detailed Database Schema (ERD):** Create a relational database schema including:

- **Users:** id, email, password (hashed), role (User/Admin).
- **Products:** id, name, description, price, stock_quantity, category_id.
- **Carts & Cart_Items:** Relationship between Users and Products (1:N, N:M).
- **Orders:** id, user_id, total_amount, status (Pending, Paid, Failed), stripe_payment_intent_id.
- **Order_Items:** Snapshot of products at the time of purchase (id, order_id, product_id, price_at_purchase, quantity).
**API Endpoints Structure:** Visualize the following RESTful routes:

- **Auth (**`**/api/auth**` **):** `POST /register` , `POST /login` .
- **Products (**`**/api/products**` **):** `GET /`  (list/search), `GET /:id` .
- **Admin (**`**/api/admin**` **):** `POST /products` , `PUT /products/:id` , `PATCH /inventory`  (Protected by Admin Role).
- **Cart (**`**/api/cart**` **):** `GET /` , `POST /add` , `DELETE /remove/:id` .
- **Checkout (**`**/api/checkout**` **):** `POST /`  (Triggers Stripe Payment and creates Order).
**Key Data Flows to Diagram:**

1. **Secure Access Flow:** User logs in → JWT Issued → Client includes JWT in header → Server validates for `/cart`  and `/admin`  routes.
2. **Transaction Flow:** User clicks Checkout → Server calculates total → Calls **Stripe API** → On success, updates **Inventory** and records **Order** in DB → Clears **Cart**.
**Visual Style:** Professional technical diagram with clear separation between Internal Services and External Integrations (Stripe ( Test Mode)).

