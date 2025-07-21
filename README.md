# Flask User Management API

This project is a simple RESTful API built with Flask for managing user data in-memory. It provides endpoints to create, read, update, and delete users.

## Features
- Get all users
- Get a single user by ID
- Create a new user
- Update an existing user
- Delete a user

## Endpoints

### Get all users
- **GET** `/users`
- Returns a JSON object containing all users.

### Get a user by ID
- **GET** `/users/<user_id>`
- Returns the user data for the specified ID.

### Create a new user
- **POST** `/users`
- Expects JSON body: `{ "id": int, "name": str, "email": str }`
- Returns a success message or error if user already exists.

### Update a user
- **PUT** `/users/<user_id>`
- Expects JSON body with fields to update (e.g., `{ "name": str, "email": str }`)
- Returns a success message or error if user not found.

### Delete a user
- **DELETE** `/users/<user_id>`
- Deletes the user with the specified ID.
- Returns a success message or error if user not found.

## How to Run
1. Install Flask:
   ```powershell
   pip install flask
   ```
2. Run the app:
   ```powershell
   python app.py
   ```
3. The API will be available at `http://127.0.0.1:5000/`

## Notes
- User data is stored in-memory and will be lost when the server restarts.
- This project is for demonstration and testing purposes only.

## Example Request
```
POST /users
{
  "id": 1,
  "name": "John Doe",
  "email": "john@example.com"
}
```

## License
This project is open source and free to use.
