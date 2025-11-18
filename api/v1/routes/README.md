# api-service

## Overview

This project implements a RESTful API service for managing user data. It provides endpoints for creating, retrieving, updating, and deleting user records.

## Technologies Used

*   **Language:** Python 3.9+
*   **Framework:** FastAPI
*   **Database:** PostgreSQL (using SQLAlchemy)
*   **ORM:** SQLAlchemy
*   **Serialization:** Pydantic
*   **Testing:** Pytest
*   **Linting:** Ruff
*   **Formatting:** Black

## Prerequisites

*   Python 3.9 or higher
*   PostgreSQL database server
*   Poetry for dependency management

## Installation

1.  Clone the repository:

    ```bash
    git clone [repository_url]
    cd api-service
    ```

2.  Install dependencies using Poetry:

    ```bash
    poetry install
    ```

3.  Configure the database connection:

    *   Create a `.env` file in the root directory.
    *   Add the following environment variables:

        ```
        DATABASE_URL="postgresql://user:password@host:port/database"
        ```

    *   Replace `user`, `password`, `host`, `port`, and `database` with your PostgreSQL credentials.

## Running the Application

1.  Run the application using Poetry:

    ```bash
    poetry run uvicorn main:app --reload
    ```

    This will start the API server on `http://127.0.0.1:8000`.

## API Documentation

The API documentation is automatically generated using FastAPI and can be accessed at:

`http://127.0.0.1:8000/docs`

## Testing

1.  Run the tests using Pytest:

    ```bash
    poetry run pytest
    ```

## Linting and Formatting

1.  Lint the code using Ruff:

    ```bash
    poetry run ruff check .
    ```

2.  Format the code using Black:

    ```bash
    poetry run black .
    ```

## Project Structure

```
api-service/
├── .env              # Environment variables
├── pyproject.toml    # Poetry configuration
├── main.py           # Main application file
├── models.py         # Database models
├── schemas.py        # Pydantic schemas
├── routes/           # API routes
│   ├── users.py      # User-related routes
│   └── __init__.py
├── tests/            # Test files
│   ├── conftest.py   # Pytest configuration
│   ├── test_users.py # Tests for user routes
│   └── __init__.py
├── .gitignore        # Git ignore file
└── README.md         # This file
```

## Contributing

Contributions are welcome! Please follow these guidelines:

*   Fork the repository.
*   Create a new branch for your feature or bug fix.
*   Write tests for your changes.
*   Lint and format your code.
*   Submit a pull request.