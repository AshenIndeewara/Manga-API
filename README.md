# 📚 FastAPI Manga API

A simple and fast web API built using [FastAPI](https://fastapi.tiangolo.com/), designed to provide endpoints for searching and accessing manga information, chapters, and images.

## 🚀 Features

- 🔍 Search for manga titles  
- 📘 Get details of a specific manga  
- 📖 Fetch specific manga chapters  
- 🖼️ Retrieve images via URL  

## 🛠️ Endpoints

### `GET /`
Returns a basic welcome or root response.

---

### `GET /search/{query}`
Searches for manga using a query string.

**Path Parameters:**
- `query` (string): The search keyword.

**Responses:**
- `200 OK`: List of matching manga.
- `422 Unprocessable Entity`: Validation error.

---

### `GET /manga/{name}`
Fetches information for a specific manga.

**Path Parameters:**
- `name` (string): Name of the manga.

**Responses:**
- `200 OK`: Manga details.
- `422 Unprocessable Entity`: Validation error.

---

### `GET /chapter/{name}/{chapter}`
Retrieves a specific chapter of a manga.

**Path Parameters:**
- `name` (string): Manga name.  
- `chapter` (string): Chapter number or ID.

**Responses:**
- `200 OK`: Chapter data.
- `422 Unprocessable Entity`: Validation error.

---

### `GET /image?url=...`
Fetches and serves an image from a given URL.

**Query Parameters:**
- `url` (string): Direct image URL.

**Responses:**
- `200 OK`: Returns image metadata or proxy.
- `422 Unprocessable Entity`: Validation error.

---
