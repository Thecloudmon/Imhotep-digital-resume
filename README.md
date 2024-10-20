# Digital Searchable Resume - Imhotep Harnett
This repository contains digital resumes that are searchable by various technical keywords. 

## Getting Started
These instructions will help you set up the project on your local machine for development and testing purposes.

## Prerequisites
You will need the following to get started:
- Docker
- Git

## Installing
To install and run the project:
1. Clone this repository:
    ```sh
    git clone [https://github.com/yourusername/digital-resumes.git](https://github.com/Thecloudmon/Imhotep-digital-resume/edit/main/README.md)
    cd digital-resumes
    ```
2. Build and run the Docker container:
    ```sh
    docker build -t digital-resumes .
    docker run -d -p 8080:80 digital-resumes
    ```

## Adding Resumes
To add a new resume, simply upload the document and ensure it includes relevant searchable keywords in the metadata or content. These keywords will be indexed for search purposes.

## Search Functionality
Resumes can be searched using the following fields:
- Name
- Skills
- Experience
- Education

## Dockerfile
The provided Dockerfile ensures that the project can be built and deployed with ease.

## Keywords
Ensure that each resume has searchable field keywords to optimize the search functionality. 

## Comments
The repository is designed to be user-friendly and self-explanatory, with comments included in the code to detail why certain decisions were made.
Step 4: Create the Dockerfile

Here’s a simple Dockerfile:
dockerfile
Copy
# Use an official Node.js runtime as a parent image
FROM node:14

# Set the working directory
WORKDIR /usr/src/app

# Copy the package.json and package-lock.json files
COPY package*.json ./

# Install the application dependencies
RUN npm install

# Copy the rest of the application code
COPY . .

# Expose the port the app runs on
EXPOSE 8080

# Run the application
CMD ["node", "app.js"]
