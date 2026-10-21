# 📘 Assignment: Persisting FastAPI Data with SQLite

## 🎯 Objective

Extend the FastAPI book API to store its data in SQLite instead of only in memory. Learn how to create a table and use database queries so books remain available after the server restarts.

## 📝 Tasks

### 🛠️ Create the Books Database

#### Description
Create a SQLite database for the book API using Python's built-in `sqlite3` module. Set up a `books` table with columns that match the book data used by the API.

#### Requirements
Completed program should:

- Create or connect to a local SQLite database file
- Create a `books` table with an integer ID, title, author, and publication year
- Initialize the table when the application starts without deleting existing records
- Use parameterized SQL statements when adding values to queries


### 🛠️ Connect API Endpoints to SQLite

#### Description
Replace the in-memory book collection with database operations. Update each CRUD endpoint to read or change records in SQLite while preserving the API's existing request and response behavior.

#### Requirements
Completed program should:

- Use `GET /books` and `GET /books/{book_id}` to retrieve records from the database
- Use `POST /books` to insert a book and return its assigned ID
- Use `PUT /books/{book_id}` and `DELETE /books/{book_id}` to update and remove records
- Continue returning `404 Not Found` for unknown book IDs
- Keep created and updated records available after restarting the server
