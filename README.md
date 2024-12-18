# Adstack-Media

# TASK 1 and 2 : Backend Development & Database Management

# Django App Management API
   This project provides a RESTful API for managing application details. The API is built using Django and includes endpoints to add, retrieve, and delete app details from an SQLite database.

# Features
   . Add application details (name, version, and description).
   . Retrieve application details by ID.
   . Delete an application by ID.

# API Endpoints

1. Add App
Endpoint: POST /add-app/
Description: Adds app details to the database.
Request Payload:
{
    "app_name": "MyApp",
    "version": "1.0.0",
    "description": "A sample app description"
}
Response (on success):
{
    "id": 1,
    "app_name": "MyApp",
    "version": "1.0.0",
    "description": "A sample app description"
}

2. Get App Details
Endpoint: GET /get-app/{id}/
Description: Retrieves app details by ID.

Response (if the app exists):

{
    "id": 1,
    "app_name": "MyApp",
    "version": "1.0.0",
    "description": "A sample app description"
}
Response (if the app does not exist):

{
    "error": "App with the given ID does not exist."
}
3. Delete App
Endpoint: DELETE /delete-app/{id}/

Description: Deletes an app from the database by ID.

Response (on success):

{
    "message": "App deleted successfully."
}
Response (if the app does not exist):

{
    "error": "App with the given ID does not exist."
}

# Project Setup
Prerequisites
1.Python (>= 3.8).
2.Django (>= 4.0).
3.SQLite (bundled with Python).


# Installation

1. Apply Makemigration

   cmd : python manage.py Makemigration

2. Apply Migrations

   cmd : python manage.py migrate

3. Run the Development Server
    cmd : python manage.py runserver

4. Access the API

   API Base URL: http://127.0.0.1:8000

# API Testing Using Postman
 # Testing Endpoints

1. Add App (POST /add-app)
. Steps:
    1. Open Postman and create a new request.
    2. Set the method to POST.
    3. Enter the URL: http://127.0.0.1:8000/add-app/.
    4. In the Body tab, select raw and choose JSON.
    5. Enter the following payload:
{
    "app_name": "MyApp",
    "version": "1.0.0",
    "description": "A sample app description"
}
    6. Click Send.

. Expected Respose :
{
    "id": 1,
    "app_name": "MyApp",
    "version": "1.0.0",
    "description": "A sample app description"
}

2. Get App Details (GET /get-app/{id})
. Steps:
    1. Create a new request in Postman.
    2. Set the method to GET.
    3. Enter the URL: http://127.0.0.1:8000/get-app/1/ (replace 1 with the desired app ID).
    4. Click Send.

. Expected Response (if app exists) :
{
    "id": 1,
    "app_name": "MyApp",
    "version": "1.0.0",
    "description": "A sample app description"
}

3. Delete App (DELETE /delete-app/{id})
. Steps:
    1. Create a new request in Postman.
    2. Set the method to DELETE.
    3. Enter the URL: http://127.0.0.1:8000/delete-app/1/ (replace 1 with the desired app ID).
    4. Click Send.

Expected Response:

{
    "message": "App deleted successfully."
}

# Django App Management API with SQLite Integration

This project provides a RESTful API for managing application details (app_name, version, description) using a simple SQLite database. The API allows users to add, retrieve, and delete application data.

# Features
    1.Add application details such as app name, version, and description.
    2.Retrieve application details by ID.
    3.Delete application details by ID.
    4.SQLite database integration for storing app data.

# Directory Structure

project/
├── app_management/    # Contains the main app logic
│   ├── migrations/    # Database migration files
│   ├── models.py      # Database models
│   ├── serializers.py # DRF serializers for API
│   ├── views.py       # API views
│   ├── urls.py        # URL routing
├── db.sqlite3         # SQLite database file
├── manage.py          # Django management script
├── requirements.txt   # List of dependencies
└── README.md          # Documentation

# Task 3: Virtual Android System Simulation

Learning Phase Overview:
I am currently in the learning phase for simulating a virtual Android system using Python. The goal of this task is to understand how to create and manage an Android environment programmatically.

# Task 4: Basic Networking

Learning Phase Overview:
Currently, I am in the learning phase for basic networking concepts, particularly focused on building a simple server-client communication system. This task allows me to explore key concepts such as sockets, data exchange, and network communication protocols
