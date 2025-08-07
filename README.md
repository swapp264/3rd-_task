# Book API Express Server

This is a simple Express.js server for managing a collection of books in memory.

## Setup

1. **Install dependencies:**
   ```bash
   npm install
   ```
2. **Start the server:**
   ```bash
   node index.js
   ```
   The server will run on `http://localhost:5000`.

## API Endpoints

### 1. Get all books
- **GET** `/books`
- **Response:**
  ```json
  [
    { "id": 1, "title": "Book Title", "author": "Author Name" }
  ]
  ```

### 2. Add a new book
- **POST** `/books`
- **Body:**
  ```json
  {
    "title": "Book Title",
    "author": "Author Name"
  }
  ```
- **Response:**
  ```json
  { "id": 1, "title": "Book Title", "author": "Author Name" }
  ```

### 3. Update a book by ID
- **PUT** `/books/:id`
- **Body:** (any or both fields)
  ```json
  {
    "title": "New Title",
    "author": "New Author"
  }
  ```
- **Response:**
  ```json
  { "id": 1, "title": "New Title", "author": "New Author" }
  ```

### 4. Delete a book by ID
- **DELETE** `/books/:id`
- **Response:**
  ```json
  { "id": 1, "title": "Book Title", "author": "Author Name" }
  ```

## Notes
- Data is stored in memory and will reset when the server restarts.
- Use tools like Thunder Client, Postman, or curl to test the API.

