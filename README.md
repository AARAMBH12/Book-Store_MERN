SchreenShots->
<img width="955" height="419" alt="image" src="https://github.com/user-attachments/assets/9114abac-3e49-46a3-97a8-167ebc5b3a57" />
<img width="960" height="420" alt="image" src="https://github.com/user-attachments/assets/aa99920f-7424-4dab-b9e8-0adbe8fbb5ab" />
<img width="947" height="425" alt="image" src="https://github.com/user-attachments/assets/274c9d40-b82b-437c-a8e1-a212e3ba2bbe" />



# 📚 Bookstore MERN App

A modern full-stack bookstore manager built with **React**, **Vite**, **Express**, **MongoDB**, and **Mongoose**.

It lets you quickly manage books with a simple, responsive interface and a lightweight REST API.

---

## ✨ Features

- View all books in **table** or **card** layout
- Add a new book
- View detailed book information
- Edit existing books
- Delete books
- Toast notifications for success/error feedback
- Client-side routing with React Router
- REST API with full CRUD support

---

## 🧰 Tech Stack

| Frontend | Backend | Database | UI / Utilities |
|---|---|---|---|
| React 19 | Express 5 | MongoDB | Tailwind CSS |
| Vite | Mongoose 9 |  | Axios |
| React Router DOM | Node.js |  | Notistack |
| React Icons |  |  |  |

---

## 📁 Project Structure

```text
bookstore/
├─ backend/
│  ├─ index.js
│  ├─ config.js
│  ├─ models/
│  └─ routes/
├─ frontend/
│  ├─ src/
│  ├─ public/
│  └─ vite.config.js
├─ README.md
└─ .gitignore
```

---

## 🚀 Getting Started

### 1) Clone the repository

```bash
git clone <your-repo-url>
cd bookstore
```

### 2) Install dependencies

Install backend and frontend dependencies separately:

```bash
npm install --prefix backend
npm install --prefix frontend
```

---

## ▶️ Run the App

### Start the backend

```bash
npm --prefix backend start
```

Backend runs on:

```text
http://localhost:5555
```

### Start the frontend

```bash
npm --prefix frontend run dev
```

Frontend runs on:

```text
http://127.0.0.1:5173
```

If needed, you can force the host:

```bash
npm --prefix frontend run dev -- --host 127.0.0.1
```

---

## 🧪 Build for Production

```bash
npm --prefix frontend run build
```

---

## 🔧 Environment Variables

The backend uses the following environment variable:

| Variable | Description | Default |
|---|---|---|
| `MONGO_URL` | MongoDB connection string | `mongodb://127.0.0.1:27017/bookstore` |

Example:

```bash
MONGO_URL=mongodb://127.0.0.1:27017/bookstore
```

---

## 🛠️ Backend API

Base URL:

```text
http://localhost:5555/books
```

### `GET /books`
Get all books.

**Response**
```json
{
  "count": 2,
  "data": []
}
```

---

### `GET /books/:id`
Get a single book by ID.

---

### `POST /books`
Create a new book.

**Request body**
```json
{
  "title": "Atomic Habits",
  "author": "James Clear",
  "publishYear": 2018
}
```

---

### `PUT /books/:id`
Update an existing book.

**Request body**
```json
{
  "title": "Atomic Habits Updated",
  "author": "James Clear",
  "publishYear": 2020
}
```

---

### `DELETE /books/:id`
Delete a book by ID.

---

## 🖥️ Frontend Pages

| Route | Page |
|---|---|
| `/` | Book list |
| `/books/create` | Create book |
| `/books/details/:id` | Book details |
| `/books/edit/:id` | Edit book |
| `/books/delete/:id` | Delete book |

---

## 🎨 UI Highlights

- Clean layout with a toggle between **table** and **card** views
- Icon-based actions for quick book management
- Modal preview for compact book details
- Responsive components for smaller screens

---

## ✅ Verification

This project was verified with:

- `npm --prefix frontend run build`
- `npm --prefix backend start`
- `npm --prefix frontend run dev -- --host 127.0.0.1`

The app was confirmed to load successfully in the browser.

---

## 🧹 Git Ignore

The repository ignores:

- `node_modules/`
- build output
- log files
- environment files
- editor/system artifacts

---

## 📌 Notes

- The frontend uses `react-router-dom` for page routing.
- The frontend uses `notistack` for notifications.
- The backend uses Mongoose timestamps for `createdAt` and `updatedAt`.

---

## 📜 License

This project is provided as-is for learning and development purposes.
