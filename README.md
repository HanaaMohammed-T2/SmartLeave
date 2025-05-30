# SmartLeave – Leave Management System

## 📌 Overview

**SmartLeave** is a real-world assignment project designed to evaluate your full understanding of building enterprise-level web applications using **ASP.NET Core** with **layered architecture**. You will develop:

- A **Web API** (ASP.NET Core API)
- A **Razor MVC web app** (ASP.NET Core MVC)

The MVC application must **only communicate with the API** using `HttpClient`. There should be **no direct DB access** in the MVC project.

---

## 🧠 Project Goals

You are expected to demonstrate:

- Layered architecture separation
- Authentication & authorization
- Business workflows beyond CRUD
- API-first design and documentation
- Frontend-backend communication via HTTP
- Clean code and developer discipline

---

## 🏗️ Architecture Overview

SmartLeave.sln

│

├── SmartLeave.API → ASP.NET Core Web API (no Razor)

├── SmartLeave.MVC → Razor frontend (no direct DB access)

├── SmartLeave.BLL → Business logic (interfaces + services)

├── SmartLeave.DAL → EF Core entities, DbContext, repositories

└── SmartLeave.Common → Shared validators, helpers, constants


---

## 📦 Technologies Required

| Area                 | Technology                         |
|----------------------|-------------------------------------|
| Backend              | ASP.NET Core 6 Web API             |
| Frontend             | ASP.NET Core 6 MVC (Razor)         |
| DB                   | EF Core 6 with SQL Server          |
| Auth (API)           | JWT Bearer                         |
| Auth (MVC)           | Cookie                             |
| Identity             | ASP.NET Identity                   |
| Validation           | FluentValidation                   |
| Mapping              | AutoMapper                         |
| Docs                 | Swagger (Swashbuckle)              |
| Misc                 | File Upload, Email, Business Logic |
| Deployment           | GitHub-ready structure             |

---

## 👥 Roles & Permissions

Implement the following roles with proper access restrictions:

- **Admin**: Manage users, approve/reject leaves
- **Manager**: View team leaves, approve/reject
- **Employee**: Apply for leave, view history

---

## 📑 Functional Requirements

### ✅ API Features (SmartLeave.API)

- [ ] Register/Login/Logout with JWT (ASP.NET Identity)
- [ ] Role-based authorization
- [ ] Manage Leave Types (CRUD)
- [ ] Submit Leave Requests
- [ ] Approve/Reject Leave Requests (based on role)
- [ ] Upload attachments with leave requests
- [ ] Send email notifications (on submit/approve)
- [ ] Swagger documentation for all endpoints

### ✅ MVC Features (SmartLeave.MVC)

- [ ] Login/Register using API
- [ ] Cookie-based auth
- [ ] Submit leave form (with file upload)
- [ ] View own leave history
- [ ] Approve/reject leave (for Managers/Admins)
- [ ] Role-based dashboard & access
- [ ] UI validation + error messages

---

## ⚙️ How to Run

### 1. Requirements

- [.NET 6 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/6.0)
- SQL Server instance
- Visual Studio or VS Code

### 2. Clone the Repo

```bash
git clone https://github.com/HanaaMohammed-T2/SmartLeave.git
cd SmartLeave
```
### 3. Setup DB

- Update connection string in SmartLeave.API/appsettings.json
- Run migrations using EF Core or:
```bash
dotnet ef database update --project SmartLeave.DAL
```

### 4. Run the API

```bash
cd SmartLeave.API
dotnet run
```

### 5. Run the MVC App
```bash
cd SmartLeave.MVC
dotnet run
```

## 📝 Evaluation Criteria (100 Points)

| Area                                | Points |
| ----------------------------------- | ------ |
| Functional API                      | 15     |
| Working MVC frontend                | 15     |
| Authentication & Role Handling      | 15     |
| EF Core + Identity + DB             | 10     |
| HttpClient usage (API calls only)   | 10     |
| AutoMapper + FluentValidation       | 10     |
| File Uploads + Email notifications  | 10     |
| Swagger Documentation               | 5      |
| UI & UX (basic but clear)           | 5      |
| GitHub discipline (commits, README) | 5      |

## ⭐ Bonus Points

| Extra Feature                       | Bonus |
| ----------------------------------- | ----- |
| Refresh Token Support               | +5    |
| Unit Tests (at least 2 services)    | +5    |
| Background Jobs (e.g., email queue) | +5    |
| Creative AI Usage                   | +5    |

## 📅 Deadline

**Complete the project in 12/6.**

You will be evaluated based on:
- Completion
- Functionality
- Code structure
- Azure Devops hygiene
- Clean and maintainable code
