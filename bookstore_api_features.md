# ✅ Bookstore API – All Required Features Summary

---

## 🔹 Entities and Relationships

- `Book`, `Author`, `Category`, `User`, `Order`
- Relationships:
  - One-to-Many: Category → Books, Author → Books
  - Many-to-One: Book → Category, Book → Author
  - One-to-Many: User → Orders
  - Many-to-Many (optional): Order ↔ Books

---

## 🔹 CRUD Endpoints

- ✅ `POST /books` – Create a book
- ✅ `GET /books/{id}` – Get book by ID
- ✅ `PUT /books/{id}` – Update book
- ✅ `DELETE /books/{id}` – Soft delete (or hard)
- ✅ `GET /books` – List all books (with pagination)

---

## 🔹 Validation

- Required fields (e.g., title, price)
- Use of `@Valid` + `@NotBlank`, `@Min`, etc.
- Custom error messages

---

## 🔹 Exception Handling

- Centralized via `@ControllerAdvice`
- Custom `ResourceNotFoundException`, `BadRequestException`, etc.
- Return clean JSON error structure

---

## 🔹 Pagination, Sorting, Filtering

- ✅ `GET /books?page=0&size=10&sort=price,asc`
- ✅ Filter by category, author, price range
- ✅ Dynamic query building (optional: JPA Criteria)

---

## 🔹 Search

- ✅ `GET /books/search?keyword=java`
- Using `LIKE` or full-text search (PostgreSQL / custom query)

---

## 🔹 User Authentication (Basic Auth)

- ✅ Simple basic auth secured endpoint
- `/users/login` + basic protection
- Prepared for upgrade to JWT in later weeks

---

## 🔹 Order Management

- ✅ Place order: `POST /orders`
- ✅ Get all orders for a user
- ✅ Order details include books, quantity, total price

---

## 🔹 DTO Layer

- Clear separation between domain models and exposed DTOs
- Examples: `CreateBookRequest`, `BookResponse`, `OrderDto`

---

## 🔹 Swagger Integration

- ✅ Auto-generated API documentation at `/swagger-ui.html`
- Try, test, and document endpoints easily

---

## 🔹 Folder Structure

```
- controller/
- service/
- repository/
- dto/
- model/
- exception/
- config/
```

---

## 🔹 Data Initialization

- Sample data for authors, categories, books
- Using `data.sql` or `CommandLineRunner` or Liquibase

---

## 🔹 Bonus Ideas

- JWT Security with login/signup
- Upload book cover images
- Caching for books or categories
- Role-based access (ADMIN vs USER)
- Tests (unit + integration)