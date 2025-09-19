# 🐞 Bug Tracking

A **role-based web application** for managing and tracking bugs across multiple projects in an organization.  
Provides a single-dashboard view of projects, currently open bugs, and total resolved bugs to help teams stay organized and ship higher-quality software.

---

## 🚀 Tech Stack

- **Framework:** .NET 6 (ASP.NET Core / Razor Pages)  
- **Language:** C# (Razor)  
- **ORM:** Entity Framework Core  
- **Auth:** ASP.NET Core Identity (Role-based)  
- **Database:** MySQL

---

## ✨ Key Features

- Centralized **project dashboard** showing open & resolved bug counts  
- Full **bug lifecycle**: create, edit, resolve, delete  
- **Role-based access**: Admin, Manager, Developer  
- User management and secure authentication via Identity Core  
- EF Core migrations for database versioning and portability

---

## 👥 Roles & Permissions

- **Admin**
  - Manage roles
  - Create and manage Manager users
  - Full system access

- **Manager**
  - All Developer permissions
  - Create and manage projects

- **Developer**
  - View projects and bugs
  - Add / Edit / Resolve / Delete bugs

---

## ⚙️ Prerequisites

- [.NET 6 SDK](https://dotnet.microsoft.com/download/dotnet/6.0)  
- [MySQL Server](https://dev.mysql.com/downloads/) (or Docker MySQL image)  
- EF Core CLI tools (optional but recommended):  

---

## ⚙️ How to Run This Project Locally

Follow these steps to set up and run the application on your local machine:

### 1️⃣ Clone the Project

Clone the repository and open it in your preferred code editor (Visual Studio, Rider, or VS Code).

Example: git clone https://github.com/your-username/bug-tracking-app.git

Then navigate into the project folder: 
```
cd bug-tracking-app
```

### 2️⃣ Restore Dependencies

Run: 
```
dotnet restore
```

### 3️⃣ Build the Project

Compile the solution with: 
```
dotnet build
```
Or simply press `Fn + 5` in your IDE to launch the project directly in the browser.

You should now see the login screen.

### 4️⃣ Create Database & Tables

Create the initial migration: 
```
dotnet ef migrations add Init
```

Apply the migration to generate tables: 
```
dotnet ef database update
```

### 5️⃣ Seed Users & Roles

Run the provided `seedData.sql` script to insert default roles (Admin, Manager, Developer) and a default test user.
Example (MySQL CLI): 
```
mysql -u root -p BugTrackingDB < scripts/seedData.sql
```

Alternatively, you can sign up directly in the app. New accounts are assigned the Developer role by default.

#### ✅ At this point, the application should be running and accessible at:
```
https://localhost:5001
```

---
## 🎥 Project Demo

[Demo](https://user-images.githubusercontent.com/30929093/215810141-67dc03de-800d-4c8e-a42a-c3a28a4a91a9.mp4)
