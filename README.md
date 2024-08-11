# DevOps Intern Assignment - Flask MongoDB Application

This repository contains a simple Flask application that connects to a MongoDB database. The application is Dockerized to simplify deployment and setup.

## Prerequisites
- Docker installed on your system.
- A running MongoDB Docker container.

## Setup

1. **Clone the Repository**

   ```bash
   git clone https://github.com/MOHANREDDY3766/DevOps-Intern-Assignment.git
   cd DevOps-Intern-Assignment
Build the Docker Image

bash
Copy code
docker build -t flask-mongo-app .
Run the MongoDB Container

Make sure you have a MongoDB container running. You can use the following command to start one:

bash
Copy code
docker run -d -p 27017:27017 --name mongodb mongo
Run the Flask Application Container

bash
Copy code
docker run -d -p 5000:5000 --name flask-mongo-app --link mongodb:mongo flask-mongo-app
Access the Application

The application should now be running on http://localhost:5000. You can interact with it using your browser or tools like curl or Postman.

Troubleshooting
If you encounter any issues, you can check the logs of the Flask application container using:

bash
Copy code
docker logs flask-mongo-app
Ensure that the MongoDB container is running before starting the Flask application container.

License
This project is licensed under the MIT License.
