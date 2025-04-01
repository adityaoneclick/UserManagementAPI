# User Management API

## Project Overview
This is a RESTful API for managing user data, built with ASP.NET Core. The API provides endpoints for creating, reading, updating, and deleting user information.

## Features
- **CRUD Operations**: Complete set of endpoints for user management
- **Data Validation**: Input validation for user data (required fields, email format, etc.)
- **Request Logging**: Custom middleware for logging all incoming requests
- **Swagger Documentation**: API documentation and testing interface

## Technologies Used
- **ASP.NET Core 9.0**
- **C#**
- **RESTful API principles**
- **Middleware for request logging**

## API Endpoints

| Method | Endpoint           | Description                   |
|--------|-------------------|-------------------------------|
| GET    | `/api/user`       | Get all users                 |
| GET    | `/api/user/{id}`  | Get a specific user by ID     |
| POST   | `/api/user`       | Create a new user             |
| PUT    | `/api/user/{id}`  | Update an existing user       |
| DELETE | `/api/user/{id}`  | Delete a user                 |

## Getting Started

### Prerequisites
- .NET SDK 9.0 or later

### Installation

Clone the repository:
```sh
git clone https://github.com/yourusername/UserManagementAPI.git
```

Navigate to the project directory:
```sh
cd UserManagementAPI
```

Build the project:
```sh
dotnet build
```

Run the application:
```sh
dotnet run
```

The API will be available at:
- `https://localhost:5001`
- `http://localhost:5000`

## Usage Examples

### Create a User
#### Request
```http
POST /api/user
Content-Type: application/json

{
  "id": 1,
  "name": "John Doe",
  "email": "john@example.com"
}
```

### Get All Users
#### Request
```http
GET /api/user
```

### Update a User
#### Request
```http
PUT /api/user/1
Content-Type: application/json

{
  "id": 1,
  "name": "John Updated",
  "email": "john.updated@example.com"
}
```

### Delete a User
#### Request
```http
DELETE /api/user/1
```

## Project Structure
- **`Controllers/`**: Contains API controllers
- **`Models/`**: Data models including `User` class
- **`Middleware/`**: Custom middleware components

## License
This project is licensed under the MIT License - see the `LICENSE` file for details.

