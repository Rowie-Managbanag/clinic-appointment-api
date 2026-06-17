# Clinic Appointment API

This project is a simple Clinic Appointment API built using FastAPI and Docker.

## Laboratory Context

This project was developed in an offline Windows 11 laboratory environment.

Python was not installed directly on the computer. The application was executed using Docker and a
prebuilt Docker image named clinic-fastapi-base:1.0.

## Features

- Create clinic appointments

- View all appointments

- View one appointment

- Update appointment details

- Cancel appointments

## Technologies Used

- Python

- FastAPI

- Docker

· Git

## How to Run

docker compose up --build

Open http://localhost:8000/docs.

## Authentication

The API supports two user roles:
- **admin** (username: admin, password: clinic123) - Role: clinic_staff
- **staff** (username: staff, password: staff123) - Role: clinic_assistant

Users must login using the `/login` endpoint to receive a Bearer token, which must be included in the Authorization header for all appointment endpoints.

### About Logout

This API does not include a logout endpoint. In a production token-based authentication system:

1. **Token Invalidation**: Logout is typically handled client-side by discarding the token. The server doesn't need to maintain a logout list.
2. **Token Expiration**: Tokens should have a short expiration time (e.g., 15-30 minutes), after which users must re-authenticate.
3. **Token Blacklist (Optional)**: For immediate logout across all sessions, a production system might maintain a blacklist of invalidated tokens in a cache (Redis) or database.
4. **Refresh Tokens**: A more robust approach uses short-lived access tokens and separate refresh tokens that are stored securely and can be revoked.

Currently, this development API uses a simple static token without expiration for demonstration purposes.

## Step-by-step to Run the API Locally

Step 14: Initialize, Stage, and Commit Locally

git init

git status

git add .

git commit -m "Initial clinic appointment API using FastAPI and Docker"

git log -- oneline
