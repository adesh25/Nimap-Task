Nimap Machine Test


This project is a Spring Boot application that provides RESTful APIs for managing categories and products, implementing CRUD operations with a relational database. The project uses Spring Data JPA and Hibernate for database interaction and supports server-side pagination.

Features
Category Management:

Create, update, delete, and retrieve categories.
Supports server-side pagination.
Product Management:

Create, update, delete, and retrieve products.
Products are associated with categories (one-to-many relationship).
Supports server-side pagination.
One-to-Many Relationship:

One category can have multiple products.
Product details include respective category information.
Technology Stack
Backend: Spring Boot
Database: MySQL (or any other RDBMS)
ORM: JPA & Hibernate
Configuration: Annotation-based (no XML)
Prerequisites
Java 17 or higher
Maven 3.6+
MySQL Server (or another SQL database)
IDE (Eclipse, IntelliJ, etc.)
Setup and Installation
Steps
Follow the following steps to run the program
Import the NimapTasks folder in the Java editor(eclipse).
Change the application.properties file according to your database.
Run the Program.
Access the APIs using "http://localhost:8080".
API Endpoints
Category API
Get All Categories (with Pagination):

Endpoint: GET /api/categories?page=3
Description: Retrieves all categories with pagination support.
Create a New Category:

Endpoint: POST /api/categories
Description: Creates a new category.
Body: json Copy code { "name": "Electronics" }
Get Category by ID:

Endpoint: GET /api/categories/{id}
Description: Retrieves category details by ID.
Update Category by ID:

Endpoint: PUT /api/categories/{id}
Description: Updates category details by ID.
Body: json Copy code { "name": "Updated Category Name" }
Delete Category by ID:

Endpoint: DELETE /api/categories/{id}
Description: Deletes the category with the specified ID.
Product API
Get All Products (with Pagination):

Endpoint: GET /api/products?page=2
Description: Retrieves all products with pagination support.
Create a New Product:

Endpoint: POST /api/products
Description: Creates a new product under a specific category.
Body: json Copy code { "name": "Laptop", "price": 1200.00, "categoryId": 1 }
Get Product by ID:

Endpoint: GET /api/products/{id}
Description: Retrieves product details by ID, including category information.
Update Product by ID:

Endpoint: PUT /api/products/{id}
Description: Updates product details by ID.
Body: json Copy code { "name": "Updated Product Name", "price": 1300.00, "categoryId": 1 }
Delete Product by ID:

Endpoint: DELETE /api/products/{id}
Description: Deletes the product with the specified ID.
Entity Relationships
Category:

Represents the category entity with fields like id and name.
One-to-many relationship with the Product entity.
Product:

Represents the product entity with fields like id, name, price, and a foreign key categoryId.
Each product belongs to one category.
Contact
Author: Adesh Dhumal
GitHub: adesh25
Email: adeshd814@gmail.com
