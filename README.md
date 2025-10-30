House Rental Management System (ASP.NET Core & MySQL)

Description

This is a full-stack web application built using ASP.NET Core MVC (C#) designed to manage a portfolio of rental properties (Houses) and their associated long-term or short-term bookings (Rentals).

The project implements robust CRUD operations across two related entities: Houses and Rentals. Crucial business logic and validation ensure data integrity for property availability, booking, and tenancy status.

Key Features (Adapted from Vehicle System):

Technology Stack: ASP.NET Core MVC (C#), Entity Framework Core (Code-First), MySQL/MariaDB (via XAMPP), and Tailwind CSS for a professional, responsive frontend.

Property Models: Replaces the Vehicle entity with a House or Property entity.

Status Management: Automatic updating of a House's Status (Available, Rented/Occupied, Maintenance) based on booking and move-out actions.

Validation: Prevents critical actions like deleting a property or editing core details while the property is currently occupied.

Dashboard: Provides a real-time summary of property availability and current tenancies.

🛠️ Installation & Database Setup

This project uses Entity Framework Core with the Pomelo provider to connect to a MySQL database, typically run through XAMPP.

Prerequisites

.NET SDK (v9.0 or later): Used to build and run the ASP.NET Core application.

MySQL/MariaDB: The database server (Ensure XAMPP MySQL service is running).

1. Configure Project and Packages

Navigate to your project root directory in the terminal:

# Restore project dependencies
dotnet restore

# Rebuild the solution to ensure all files are compiled
dotnet build


2. Apply Database Migrations

You will need to ensure your new database context (e.g., HouseRentalContext) and models (House.cs, Rental.cs) are defined, and your connection string in appsettings.json is correct.

# 1. Create the initial migration files for the new models
# NOTE: You will use the new context/models here.
dotnet ef migrations add InitialHouseSetup 

# 2. Apply the migration to your MySQL database (e.g., HouseRentalDb)
dotnet ef database update


How to Run the Project

Start the Web Server: Run the application using the following command:

dotnet run


Access the Website: The console output will display the listening URLs. Copy the HTTPS address (e.g., https://localhost:7001) and paste it into your web browser.

The application will launch to the Dashboard page, where you can begin adding properties and managing bookings.
