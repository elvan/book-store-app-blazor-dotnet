# BookStoreApp

## Description

BookStoreApp is a comprehensive web application designed to manage books and authors, providing a user-friendly interface for CRUD operations. The project is built using Blazor for the front-end and ASP.NET Core for the back-end, leveraging Entity Framework Core for data management. The application includes features like authentication, authorization, image uploads, and pagination to enhance the user experience.

## Features

- **Authentication and Authorization**:

  - Implement JWT authentication and authorization.
  - Secure API endpoints and Blazor pages with roles and policies.
  - User login, logout, and registration pages for both Blazor Server and WebAssembly.

- **Book and Author Management**:

  - CRUD operations for books and authors with detailed views.
  - Image upload functionality for book covers.
  - Separate components for displaying author and book lists using pagination.

- **Pagination and Virtualization**:

  - Implement pagination for large datasets using `QueryParameters` and `VirtualizeResponse` models.
  - Enhance performance with virtualized lists for authors and books.

- **Repository Pattern**:

  - Refactor API controllers to use repository pattern for better data management.
  - Implement `IAuthorsRepository` and `IBooksRepository` interfaces.

- **User Interface**:

  - Design user-friendly Blazor components for managing authors and books.
  - Create MainLayout and NavMenu components for consistent navigation.
  - Implement detailed course descriptions and examples pages.

- **Configuration and Services**:

  - Configure AutoMapper for DTO mappings.
  - Set up NSwag for API client generation and Swagger documentation.
  - Configure Serilog for logging and Blazored LocalStorage for token management.

#### Technology Stack

- **Languages and Frameworks**:

  - C#
  - ASP.NET Core
  - Blazor (Server and WebAssembly)
  - Entity Framework Core

- **Libraries and Tools**:
  - AutoMapper
  - NSwag
  - Serilog
  - Blazored LocalStorage
  - Newtonsoft.Json
  - System.IdentityModel.Tokens.Jwt

## Installation

### Prerequisites

- .NET 6 SDK
- Node.js (for front-end dependencies)
- SQL Server (or another configured database)

### Environment Setup

1. Clone the repository:

   ```bash
   git clone https://github.com/elvan/BookStoreApp.git
   cd BookStoreApp
   ```

2. Set up the database connection string in `appsettings.json`:
   ```json
   "ConnectionStrings": {
     "DefaultConnection": "Server=your_server;Database=BookStoreDb;Trusted_Connection=True;MultipleActiveResultSets=true"
   }
   ```

### Installation Commands

1. Navigate to the API project and restore dependencies:

   ```bash
   cd BookStoreApp.API
   dotnet restore
   ```

2. Apply database migrations:

   ```bash
   dotnet ef database update
   ```

3. Run the API project:

   ```bash
   dotnet run
   ```

4. Navigate to the Blazor WebAssembly project and restore dependencies:

   ```bash
   cd ../BookStoreApp.Blazor.WebAssembly.UI
   dotnet restore
   ```

5. Run the Blazor WebAssembly project:
   ```bash
   dotnet run
   ```

## Usage

### Running the Application

1. Ensure the API project is running and accessible.
2. Start the Blazor WebAssembly project.

### Using the Application

- **Authentication**:

  - Register a new user or login with existing credentials.
  - Access secure pages based on user roles.

- **Managing Books and Authors**:

  - Navigate to the Authors or Books section via the navigation menu.
  - Perform CRUD operations, including creating new entries, updating existing ones, and deleting entries.
  - Use the pagination controls to browse through large datasets efficiently.

- **Image Upload**:

  - When adding or editing a book, use the image upload feature to include a cover image.

This README provides a comprehensive guide to setting up, using, and understanding the key features of the BookStoreApp project. For more detailed usage instructions and additional features, refer to the in-app documentation and comments within the code.
