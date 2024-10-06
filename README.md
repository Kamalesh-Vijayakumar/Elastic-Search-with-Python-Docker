# Elastic Search with Python and Docker

## Overview

This project integrates Elasticsearch with a Python Flask backend and a React frontend, all containerized using Docker. It demonstrates a simple employee management system where Elasticsearch is used as the search backend.

## Features

- **Elasticsearch for Searching**: Leverage Elasticsearch's powerful full-text searching capabilities.
- **Flask Backend**: A RESTful API to interact with the Elasticsearch engine.
- **React Frontend**: A user interface to interact with the Flask backend.
- **Docker Compose**: Simplifies deployment by using Docker containers for each part of the stack.

## Project Structure

```plaintext
.
├── backend
│   ├── data
│   │   └── Employee_Sample_Data_1.csv  # Sample data for Elasticsearch
│   ├── Dockerfile
│   ├── app.py
│   ├── .env
│   └── requirements.txt
├── frontend
│   ├── build
│   ├── public
│   ├── src
│   ├── Dockerfile
│   ├── package.json
│   └── .gitignore
├── .gitignore
└── docker-compose.yml
```


## Prerequisites

**Docker**<br>
**Docker Compose**<br>
**Node.js and npm (for building the frontend)**

## Setup and Running 
<br>

**1. Clone the Repository**
<br>
**bash**
**Copy code**
**git clone https://github.com/Kamalesh-Vijayakumar/Elastic-Search-with-Python-Docker.git
cd Elastic-Search-with-Python-Docker**
<br>
**2. Build and Run with Docker Compose**
bash
Copy code
```docker-compose up --build
This command builds the Docker images if they don't exist and starts the containers.
```
<br>

**3. Accessing the Application**
<br>
Frontend: Open http://localhost:3000 in your browser to access the frontend.<br>
Backend API: The Flask API is available at http://localhost:5000.<br>
APIs
<br>
GET /api/employees - Retrieves all employees
<br>
POST /api/employees - Adds a new employee
<br>
PUT /api/employees/{id} - Updates an existing employee
<br>
DELETE /api/employees/{id} - Deletes an employee
<br>
Environment Variables
<br>
Ensure the .env file in the backend directory is configured correctly:

<br>
env
<br>
Copy code :
<br>
ELASTICSEARCH_HOST=elasticsearch ,ELASTICSEARCH_PORT=9200 <br>
EMPLOYEE_DATA_FILE=/data/Employee_Sample_Data_1.csv <br>
Contributions are welcome! Please fork the repository and open a pull request with your changes.
