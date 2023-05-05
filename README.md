# Cinema API

This API service is designed for cinema management and is written in Django Rest Framework. It provides endpoints for managing orders and tickets, creating movies with genres and actors, creating cinema halls, adding movie sessions, and filtering movies and movie sessions.

## Installation via GitHub

To install the Cinema API, you need to follow the below steps:

1. Install PostgresSQL and create a database
2. Clone the repository using `git clone https://github.com/ykopatko/drf-cinema-api.git`
3. Navigate to the repository directory using `cd drf-cinema-api`
4. Create a virtual environment using `python -m venv venv`
5. Activate the virtual environment on Linux/macOS using `source venv/bin/activate` or on Windows using `venv\Scripts\activate`
6. Install the required dependencies using `pip install -r requirements.txt`
7. Set the following environment variables using the values for your database: 
    - `DB_HOST=<your db hostname>`
    - `DB_NAME=<your db name>`
    - `DB_USER=<your db user>`
    - `DB_PASSWORD=<your db password>`
    - `SECRET_KEY=<your secret key>`
8. Apply migrations to the database using `python manage.py migrate`
9. Start the server using `python manage.py runserver`

## Running with Docker

To run the Cinema API with Docker, you need to follow the below steps:

1. Ensure that Docker is installed on your system
2. Clone the repository using `git clone https://github.com/ykopatko/drf-cinema-api.git
3. Add the .env file to the root of the project. In this file you must specify the values of the environment variables. Use the example which is in the .env.sample file.
4. Navigate to the repository directory using `cd drf-cinema-api`
5. Build the Docker image using `docker-compose build`
6. Start the Docker container using `docker-compose up`

## Getting Access

To get access to the Cinema API, you need to create a user by sending a POST request to `/api/user/register/` and passing the required parameters. After creating the user, you can get an access token by sending a POST request to `/api/user/token/` and passing the user's credentials.

## Features

The Cinema API offers the following features:

- JWT authentication
- Admin panel at `/admin/`
- Swagger documentation at `/api/doc/swagger/`
- Managing orders and tickets
- Creating movies with genres and actors
- Creating cinema halls
- Adding movie sessions
- Filtering movies and movie sessions
