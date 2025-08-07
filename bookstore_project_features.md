# 🎓 Technical Skills Gained – Bookstore API Project

---

## ✅ Java + Spring Boot Fundamentals

- Developed RESTful APIs using **Spring Boot Framework**
- Applied **OOP principles**: encapsulation, abstraction, inheritance
- Designed **clean architecture**: Controller → Service → Repository

---

## ✅ Entity Modeling with JPA

- Mapped relational entities using **JPA annotations**:
    - `@Entity`, `@Id`, `@GeneratedValue`
    - `@OneToMany`, `@ManyToOne`, `@JoinColumn`
- Handled bidirectional relationships and avoided infinite loops

---

## ✅ DTO and Mapper Patterns

- Built custom **DTO classes** for API input/output
- Used **ModelMapper / manual mapping** to convert between Entities and DTOs
- Separated domain models from exposed API contracts

---

## ✅ Validation & Exception Handling

- Applied bean validation via:
    - `@Valid`, `@NotBlank`, `@Size`, `@Min`
- Implemented global error handler using `@ControllerAdvice`
- Designed reusable exception types with clean JSON error format

---

## ✅ Pagination, Sorting, and Filtering

- Implemented `Pageable` and `Sort` in endpoints
- Filtered resources by category, price, and search keyword
- Applied clean query design using Spring Data JPA

---

## ✅ Basic Security (Authentication)

- Secured sensitive endpoints using **Basic Auth**
- Defined `User` entity with roles (optional)
- Prepared backend for advanced JWT implementation

---

## ✅ Swagger Documentation

- Auto-generated and tested APIs using **Swagger UI**
- Clearly documented all endpoints, inputs, and outputs

---

## ✅ Data Initialization & Bootstrapping

- Created initial dataset using:
    - `CommandLineRunner`
    - or structured migration via **Liquibase**
- Bootstrapped database with authors, categories, and books

---

## ✅ Error-Free REST API Design

- Followed best practices:
    - Clean URL naming (e.g. `/api/books`, `/api/orders`)
    - Proper HTTP status codes: `201`, `404`, `400`, `200`
    - Clear separation between read/write models

---

## ✅ Deployment-Ready Folder Structure

```
📁 controller/
📁 service/
📁 repository/
📁 dto/
📁 model/
📁 exception/
📁 config/
```