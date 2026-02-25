# Student Management App (Login + CRUD)

This is a school project app with a login page and student CRUD.

## Features

- Modern minimal pastel UI
- Login page + home page
- Create, Read, Update, Delete students
- Static demo mode using localStorage
- API-ready mode for database integration
- Logout

## Project Structure

- `index.html` redirects to login
- `login.html` login form
- `home.html` student management interface
- `styles.css` app styles
- `js/config.js` static/API mode switch
- `js/auth.js` login logic
- `js/home.js` student CRUD logic
- `db/schema.sql` users + students tables
- `db/seed.sql` sample database data
- `BACKEND_INTEGRATION.md` DBeaver + API setup guide

## Sample Login

- Username: `oua-super`
- Password: `Passw0rd`

## How to Run

1. Open the project folder.
2. Double-click `index.html`.
3. Log in and use the CRUD page.

No server setup is required for demo mode.

## Database Integration

To maintain users and student information in DBeaver, follow:

- `BACKEND_INTEGRATION.md`
