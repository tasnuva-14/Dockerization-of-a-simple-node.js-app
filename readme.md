# Node.js Dockerized Application

This repository contains a simple Node.js application that has been dockerized for easy deployment and scalability.

## Features
- A lightweight Node.js application.
- Dockerized for seamless containerization.
- Easily deployable on any platform that supports Docker.


## Getting Started

## Dockerfile Details
The `Dockerfile` includes the following steps:
- Use the official Node.js base image.
- Set up the working directory.
- Copy application files.
- Install dependencies.
- Expose port 3000.
- Define the command to run the application.

## Application Structure

.
├── Dockerfile            # Docker configuration file

├── package.json          # Node.js dependencies

├── app.js                # Main application file


### dockerfile

FROM node:16

# Create app directory
WORKDIR /app

# Install dependencies

RUN npm install

# Copy the rest of the application code
COPY . .

# Expose application port
EXPOSE 3000

# Start the application
CMD ["npm", "start"]



### Build the Docker Image

docker build -t node-app .


### Run the Application

docker run -d -p 3001:3000 node-app


### Access the Application
Open your browser and navigate to:

http://localhost:3001





