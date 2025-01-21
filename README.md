# laravel Standard Rest Api 

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




