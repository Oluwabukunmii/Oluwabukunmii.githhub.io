# Oluwabukunmii.githhub.io
My portfolio site showcasing my C# and ASP.NET Core projects.
# 👋 Hi, I'm Oluwabukunmi Ogunlana

I am a Backend Developer who blends her network perspective with backend engineering. I am all for building systems that are clean, efficient, and optimized for performance, with a deep appreciation for how applications interact with networks and infrastructure.

---

## 🚀 Featured Projects

---

### ✅ Todo List API
A focused CRUD API for managing personal tasks, built for clarity and extensibility.

**Core functionality**
- Full **CRUD** for tasks/todos with user ownership.
- **Authentication** using JWT tokens.
- **Role-based authorization** (user vs admin).
- **Pagination**, sorting and filtering endpoints for list endpoints.
- **Input validation** using Data Annotations (and FluentValidation where applicable).
- **DTOs** + AutoMapper for clear separation between domain models and public API.
- **Centralized error handling** (global exception middleware that returns consistent error responses).
- **Swagger / OpenAPI** documentation for easy exploration.

**Quality & tooling**
- Unit tests and integration tests around controllers and services.
- Seed data for development, and migration scripts for reproducible DB state.
- Swagger for  testing.

**Tech:** C#, ASP.NET Core, Entity Framework Core, SQL Server, AutoMapper, JWT, FluentValidation.  
🔗 https://github.com/Oluwabukunmii/TodoListapp

---

### 🌍 9JA NGWalks API
An API that catalogs scenic walking routes, regions, and difficulty levels — built with versioning, strong validation, and production-ready observability.

**API design & stability**
- **API Versioning** implemented (URL or header versioning) so v1, v2, etc. can coexist safely.  

**Modeling & validation**
- **Rich domain model**: `Region`, `Walk`, `DifficultyLevel` with normalized relations.  
- **Model validation** using Data Annotations and FluentValidation — all DTOs are validated before business logic runs (clean error messages returned).
- Strong use of **DTOs** to prevent over-posting / leaking internal fields.

**Observability & resilience**
- **Structured logging** via `ILogger<T>` across controllers, services, and data layers (useful log scopes for traceability).
- Error handling middleware returns standardized validation and error responses.

**Developer ergonomics**
- Automapper mapping profiles .
- API includes **pagination**, filtering, and sorting for list endpoints.
- **Role-based security** for admin operations .
- **OpenAPI / Swagger** docs that list both v1 and v2 endpoints.

**Tech:** C#, ASP.NET Core, EF Core, AutoMapper, Validation, API Versioning, SQL Server, ILogger.  
🔗 https://github.com/Oluwabukunmii/9JA-NGWALKS

---

### 🏨 Hotel Listing API
A production-minded hotel & booking management API showcasing clean architecture, EF Core relationships, and a consistent result pattern.

**Domain & relationships**
- Entities: `Country` ←→ `Hotel` ←→ `Booking`  
  - `Country` has many `Hotels` (one-to-many).  
  - `Hotel` has many `Bookings` (one-to-many).  
  - Proper **navigation properties** (`Country.Hotels`, `Hotel.Country`, `Hotel.Bookings`, `Booking.Hotel`) to enable expressive LINQ queries and eager loading.
- **EF Core** code-first migrations and fluent model configuration to express keys, constraints, and cascading behavior.

**API patterns & consistency**
- **Result Pattern** (e.g., `Result<T>` or `OperationResult`) used across services and controllers:
  - Returns a consistent shape for success, not-found, validation errors, and conflicts.
  - Separates domain errors from HTTP translation (controller maps `Result` → appropriate `IActionResult`).
- **Repository / service** layers with dependency injection to keep controllers thin and testable.

**Data access & performance**
- Use of `Include(...)` / `ThenInclude(...)` for controlled eager loading when returning nested resources.
- Paginated listing endpoints for hotels and bookings to avoid large payloads.
- Query optimization (select only DTO fields when needed) to reduce load.



**Tech:** C#, ASP.NET Core, EF Core (Code-First), SQL Server, AutoMapper, JWT.  
🔗 https://github.com/Oluwabukunmii/HotelListingApi

---

## 🧰 Tech Stack & Practices
- **Languages:** C#, SQL  
- **Frameworks:** ASP.NET Core, Entity Framework Core  
- **Design:** DTOs, Result Pattern, Dependency Injection, Clean Separation  
- **Validation:** DataAnnotations, FluentValidation  
- **Logging:** `ILogger<T>` with structured logs and scopes  
- **Security:** JWT Authentication, Role-Based Authorization  
- **Documentation:** Swagger / OpenAPI  
- **Versioning:** API versioning (URL/header) for NGWalks to support evolution  

---

## 📫 Get in Touch
- 📧 **Email:** oluwabukunmiogunlana@gmail.com  
- 💻 **GitHub:** https://github.com/Oluwabukunmii


