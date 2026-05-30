# Bookstore MERN App

A simple bookstore management app built with:

- React + Vite on the frontend
- Express + MongoDB on the backend

Users can:

- View all books
- Switch between table and card layouts
- Create a book
- View book details
- Edit a book
- Delete a book

## Project structure

```text
bookstore/
├─ backend/
└─ frontend/
```

## Requirements

- Node.js 18+
- MongoDB running locally, or a MongoDB connection string
- npm

## Backend setup

The backend listens on port `5555`.

### Install dependencies

```bash
npm install --prefix backend
```

### Run the backend

```bash
npm --prefix backend start
```

### Optional development mode

```bash
npm --prefix backend run dev
```

### Environment variables

The backend reads:

- `MONGO_URL` — MongoDB connection string

If `MONGO_URL` is not set, it defaults to:

```text
mongodb://127.0.0.1:27017/bookstore
```

## Frontend setup

The frontend uses Vite and runs on port `5173` by default.

### Install dependencies

```bash
npm install --prefix frontend
```

### Run the frontend

```bash
npm --prefix frontend run dev
```

If you want to force the host used during development:

```bash
npm --prefix frontend run dev -- --host 127.0.0.1
```

### Build for production

```bash
npm --prefix frontend run build
```

## API routes

Base URL:

```text
http://localhost:5555/books
```

### `GET /books`

Returns all books.

### `GET /books/:id`

Returns a single book by ID.

### `POST /books`

Creates a new book.

Required body fields:

```json
{
  "title": "Atomic Habits",
  "author": "James Clear",
  "publishYear": 2018
}
```

### `PUT /books/:id`

Updates an existing book.

### `DELETE /books/:id`

Deletes a book.

## Frontend pages

- `/` — books list
- `/books/create` — create book form
- `/books/details/:id` — book details
- `/books/edit/:id` — edit book form
- `/books/delete/:id` — delete confirmation

## Notes

- The frontend uses `react-router-dom` for routing.
- The app uses `notistack` for toast notifications.
- The backend uses Mongoose timestamps, so created and updated times are available on book records.

## Troubleshooting

### Frontend says dependencies are missing

Make sure the frontend dependencies are installed:

```bash
npm install --prefix frontend
```

### Backend cannot connect to MongoDB

Check that MongoDB is running locally, or set `MONGO_URL` to a valid connection string.

### Pages fail on refresh

The frontend must be served through Vite or a compatible static server because it uses client-side routing.
