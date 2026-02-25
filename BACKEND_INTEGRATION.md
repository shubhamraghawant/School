# Backend + DBeaver Integration Guide

This frontend is already prepared for backend mode through `js/config.js`.

## 1) Database setup in DBeaver

1. Open DBeaver.
2. Create a new database connection (SQLite, MySQL, or PostgreSQL).
3. Open SQL Editor.
4. Run:
   - `db/schema.sql`
   - then `db/seed.sql`

You can now maintain data in:
- `users` table (for login)
- `students` table (for student information)

## 2) Frontend switch to backend mode

Edit `js/config.js`:

```js
window.APP_CONFIG = {
  useApi: true,
  apiBaseUrl: "http://localhost:4000/api",
};
```

## 3) Required backend API endpoints

### Login
- `POST /api/login`
- Body:
  ```json
  { "username": "oua-super", "password": "Passw0rd" }
  ```
- Success response:
  ```json
  { "userId": 1, "username": "oua-super" }
  ```

### Students list
- `GET /api/students?userId=1`
- Response:
  ```json
  [
    { "id": 1, "name": "Ava Sharma", "grade": "10-A", "email": "ava.sharma@example.com" }
  ]
  ```

### Add student
- `POST /api/students`
- Body:
  ```json
  { "userId": 1, "name": "Noah Roy", "grade": "11-A", "email": "noah.roy@example.com" }
  ```

### Update student
- `PUT /api/students/:id`
- Body:
  ```json
  { "userId": 1, "name": "Noah Roy", "grade": "11-B", "email": "noah.roy@example.com" }
  ```

### Delete student
- `DELETE /api/students/:id`

## Important

- This current project runs in static mode by default (no server required).
- For real login security, store hashed passwords in `users.password`.
