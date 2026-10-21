# 📘 Assignment: Building REST APIs with FastAPI

## 🎯 Objective

Build a REST API for managing a small book collection using FastAPI. Practice defining routes, validating request data, and returning appropriate HTTP status codes.

## 📝 Tasks

### 🛠️ Create the Books API

#### Description
Create a FastAPI application that stores books in memory and lets clients retrieve them. Each book should have an integer ID, a title, an author, and a publication year.

#### Requirements
Completed program should:

- Start a FastAPI application that can be run locally with Uvicorn
- Provide `GET /books` to return the collection of books
- Provide `GET /books/{book_id}` to return one book by ID
- Return a `404 Not Found` response when the requested book ID does not exist


### 🛠️ Add and Validate Books

#### Description
Add an endpoint for creating books. Define a Pydantic request model so FastAPI can validate incoming data.

#### Requirements
Completed program should:

- Provide `POST /books` to create a book from a JSON request body
- Require a non-empty title and author and a valid integer publication year
- Assign each new book a unique ID and return the created book with a `201 Created` status
- Return a validation error for requests with missing or invalid fields


### 🛠️ Update and Delete Books

#### Description
Complete the API by allowing clients to replace or remove a book, and verify the endpoints using FastAPI's interactive documentation.

#### Requirements
Completed program should:

- Provide `PUT /books/{book_id}` to replace an existing book's title, author, and publication year
- Provide `DELETE /books/{book_id}` to remove an existing book and return a `204 No Content` status
- Return a `404 Not Found` response when an update or delete request uses an unknown ID
- Make the endpoints available and testable through FastAPI's `/docs` page
