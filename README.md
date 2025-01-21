# Laravel Standard REST API

This project demonstrates the development of a **standard REST API** using **Laravel**. Below are the best practices and standards followed in this project.

## 🧑‍💻 Service Repository Pattern
- Follow the service repository pattern to separate the logic of data access and business logic, promoting clean code and maintainability.

## 📜 Grouped Routes with Prefixes
- Organize routes into groups and apply prefixes to manage different API versions and improve readability.

## ✅ Centralized Validation
- Implement centralized validation logic to ensure consistency and reusability across the application.

## 🛠️ Eloquent ORM with Relationships
- Utilize Eloquent ORM for managing database interactions and define proper relationships between models (e.g., One-to-Many, Many-to-Many).

## 🌐 Centralized API Response
- Standardize API responses in a central location to ensure consistency and improve error handling across all endpoints.

## 💡 Database Transaction Management
- Handle database transactions effectively to ensure data integrity and rollback in case of failures.

## 🔧 Eloquent Accessors and Mutators
- Use Eloquent accessors and mutators for proper manipulation of model attributes (e.g., formatting data before storing or retrieving).

## 📝 Adherence to PSR Coding Standards
- Follow PHP-FIG's PSR standards (such as PSR-1, PSR-2, and PSR-4) for clean and maintainable code.

## 🚀 REST API Standards & Response Format
- Structure API responses according to REST conventions, ensuring consistent success and error response formats (e.g., HTTP status codes, message structure).

## 🔐 Secure Token Authentication with Expiry
- Implement secure token-based authentication (e.g., JWT) with token expiration for enhanced security.

## 📡 Laravel Resources for Response Structure
- Use Laravel's resource classes to structure the API response and ensure consistent data formatting.

## 🔒 Data Encryption and Decryption
- Implement proper encryption and decryption mechanisms for sensitive data to ensure security.

This project is a Library Management System developed using Laravel 10, PHP 8.2, and MySQL 8.35. The application provides features for users to borrow and return books, and for administrators to manage books and users effectively. Laravel Sanctum is used for authentication.

## Table of Contents
1. [Features](#features)
2. [Technologies Used](#technologies-used)
3. [Installation](#installation)
4. [Configuration](#configuration)
5. [Usage](#usage)


## Features

### User Features
1. **User Registration and Login**
   - **Register**: Users can sign up with details such as name, email, password, and an optional mobile number.
   - **Login**: Users can log in using their email and password.

2. **View Books**
   - Browse a list of books with details such as title, author, description, publish date, and availability status.

3. **Borrow Books**
   - Request to borrow an available book.
   - System sets a configurable due date (e.g., 14 days).

4. **Return Books**
   - Return borrowed books.
   - Calculate fine for late returns.

5. **View Borrowed Books**
   - View currently borrowed books and their respective due dates.

6. **Pay Fines**
   - Pay fines online for late book returns.

### Admin Features
1. **Manage Books**
   - Add new books with details (title, author, description, publish date, and availability status).
   - Update book details.
   - Soft delete books.

2. **Manage Users**
   - View a list of all registered users.
   - Delete user accounts (only if they have no borrowed books or outstanding fines).

3. **View Books with Status**
   - View all books with their current status:
     - Available: Not currently borrowed.
     - Borrowed: Currently issued to a user (with borrower details and due date).

4. **Track Borrowers**
   - View all users who have borrowed books, along with details of the borrowed books.

5. **Configure Fine Settings**
   - Configure the fine amount per day for late returns via the `.env` file.

## Technologies Used
- **Backend**: Laravel 10
- **Language**: PHP 8.2
- **Database**: MySQL 8.35
- **Authentication**: Laravel Sanctum

## Installation

### Prerequisites
- PHP >= 8.2
- Composer
- MySQL >= 8.35


### Steps
1. Clone the repository:
   ```bash
   git clone <https://github.com/Karvendhannagaraj/laravel-standard-rest-api>
   cd library_management
   ```

2. Install dependencies:
   ```bash
   composer install
   ```

3. Create a `.env` file:
   ```bash
   cp .env.example .env
   ```

4. Configure the database and other settings in the `.env` file.

5. Run migrations and seed the database:
   ```bash
   php artisan migrate --seed
   ```

6. Start the server:
   ```bash
   php artisan serve
   ```

## Configuration

### Fine Settings
- Configure the fine amount per day in the `.env` file:
  ```env
  FINE_AMOUNT_PER_DAY=10
  BORROW_DUE_DAYS=14
  ```

### Authentication
- Laravel Sanctum is used for API authentication. Ensure Sanctum is properly configured in the `.env` file.




