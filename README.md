# Masterblog API

A simple RESTful API built with Flask to manage blog posts.

---

## Features

* Get all posts
* Add new posts
* Delete posts
* Update posts
* Search posts (by title or content)
* Sort posts (by title or content, ascending or descending)

---

## Tech Stack

* Python (Flask)
* Flask-CORS
* HTML / CSS
* JavaScript (Fetch API)

---

## Project Structure

```
Masterblog_API/
├── backend/
│   └── backend_app.py
├── frontend/
│   ├── frontend_app.py
│   ├── templates/
│   │   └── index.html
│   └── static/
│       ├── main.js
│       └── styles.css
```

---

## How to Run

### Backend

```bash
cd backend
python backend_app.py
```

Runs on:
http://127.0.0.1:5002

---

### Frontend

```bash
cd frontend
python frontend_app.py
```

Runs on:
http://127.0.0.1:5001

---

## API Endpoints

### Get all posts

GET /api/posts

Optional sorting:

* /api/posts?sort=title&direction=asc
* /api/posts?sort=content&direction=desc

---

### Add post

POST /api/posts

Body:

```json
{
  "title": "Post title",
  "content": "Post content"
}
```

---

### Delete post

DELETE /api/posts/<id>

---

### Update post

PUT /api/posts/<id>

Body (optional):

```json
{
  "title": "New title",
  "content": "New content"
}
```

---

### Search posts

GET /api/posts/search?title=keyword
GET /api/posts/search?content=keyword
GET /api/posts/search?title=keyword&content=keyword

---

## Notes

* Data is stored in memory (no database)
* Data resets when the server restarts
* Frontend supports:

    * Load posts
    * Add posts
    * Delete posts
* Update, search and sorting are tested via Postman

---

## Author

Nick Steinmann
