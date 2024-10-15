Microservices - Spring Boot Application
Overview
This project is a microservice-based application built with Spring Boot. It provides basic functionality for managing an online shopping cart, including operations on items and users. The application demonstrates key Spring features such as dependency injection, service layers, repositories, and security configurations.

Features
Cart Management: Add, remove, and manage items within a user's shopping cart.
Item Service: Manage item information and inventory.
User Authentication: Secure access to the cart via user-based authentication.
Database Integration: Leverages a database for storing cart, item, and user data.
RESTful Endpoints: Expose endpoints for managing the shopping cart and items.
Project Structure
The key components of this project are as follows:

Cart.java: Represents the shopping cart for a user.
CartItem.java: Represents individual items in the shopping cart.
CartRepository.java: Interface for managing cart data persistence.
CartService.java: Business logic for handling shopping cart operations.
Item.java: Entity representing an item in the store.
ItemRepository.java: Interface for managing item data persistence.
ItemService.java: Business logic for handling item operations.
User.java: Represents a user in the system.
UserRepository.java: Interface for managing user data persistence.
SecurityConfig.java: Spring Security configuration for securing endpoints.
HomeController.java: Controller that manages home-related endpoints.
MicroSpringApplication.java: The main application entry point.
DatabaseLoader.java: Preloads data into the database on application startup.
Prerequisites
Java 8+
Maven 3.6+
A running database (e.g., H2, MySQL) or in-memory database configuration
Running the Application
Clone the repository.

git clone https://github.com/yourusername/microservices.git
cd microservices
Build the project using Maven:

./mvnw clean install
Run the Spring Boot application:

./mvnw spring-boot:run

Endpoints
GET /cart/{userId}: Fetch the user's shopping cart.
POST /cart/{userId}/add: Add an item to the user's cart.
POST /cart/{userId}/remove: Remove an item from the user's cart.
GET /items: Fetch all available items.
GET /items/{itemId}: Fetch details of a specific item.
Security
The application uses Spring Security to secure certain endpoints. User authentication is required to access cart-related endpoints. You can configure user roles and permissions in SecurityConfig.java.
