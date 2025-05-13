# 📚 FastAPI Manga API

A blazing fast, minimalistic web API built using [FastAPI](https://fastapi.tiangolo.com/).  
This API scrapes data directly from [mangakakalot.gg](https://mangakakalot.gg) to provide access to manga titles, chapters, and images.

> ⚠️ **Disclaimer**: This project is for educational purposes only. It is not affiliated with, endorsed by, or associated with mangakakalot.gg. Use responsibly.

---

## 🚀 Features

- 🔍 Search for manga titles on mangakakalot.gg  
- 📘 Get metadata of a specific manga  
- 📖 Fetch manga chapters and content  
- 🖼️ Retrieve images from manga pages  

---

## 🔌 Endpoints

### `GET /`
Basic root endpoint for testing availability.

---

### `GET /search/{query}`
Searches for manga on **mangakakalot.gg** using a query string.

**Path Parameters:**
- `query` (string): Search keyword

**Responses:**
- `200 OK`: JSON list of matched manga
- `422`: Validation error

---

### `GET /manga/{name}`
Fetches details of a specific manga by its name slug.

**Path Parameters:**
- `name` (string): Manga slug (from URL)

---

### `GET /chapter/{name}/{chapter}`
Fetches chapter images from a manga.

**Path Parameters:**
- `name` (string): Manga slug  
- `chapter` (string): Chapter number or ID

---

### `GET /image?url=...`
Downloads and serves an image from a remote URL (useful for proxying images to avoid hotlinking restrictions).

**Query Parameters:**
- `url` (string): Direct image URL

---
