# Files Manager

## Introduction

**Files Manager** is a back-end project developed using **JavaScript (ES6)** and built with **Node.js**, **ExpressJS**, **MongoDB**, **Redis**, and **Kue**. This project is designed to help users upload, manage, and view files via a simple platform. The project focuses on several key back-end concepts, including authentication, background processing, pagination, and file management.

This platform includes features like user authentication, listing files, uploading files, changing file permissions, viewing files, and generating image thumbnails. It's developed for educational purposes, aiming to combine different technologies and tools in a full-stack product simulation.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Configuration](#configuration)
- [API Endpoints](#api-endpoints)
- [Background Processing](#background-processing)
- [Troubleshooting](#troubleshooting)
- [Contributors](#contributors)
- [License](#license)

## Features

- **User Authentication:** Token-based authentication for secure access.
- **List Files:** Retrieve a list of all uploaded files.
- **Upload File:** Upload new files to the platform.
- **Change File Permissions:** Modify the access permissions for files.
- **View File:** View and download files.
- **Thumbnail Generation:** Automatically create thumbnails for image files.

## Technologies Used

- **Node.js**: JavaScript runtime for building scalable server-side applications.
- **Express.js**: Web framework for Node.js, used for building RESTful APIs.
- **MongoDB**: NoSQL database for storing file information.
- **Redis**: In-memory data structure store, used for temporary data and caching.
- **Kue**: Priority job queue backed by Redis, used for background processing.
- **ES6**: Modern JavaScript syntax.
- **Mocha**: Testing framework.
- **Bull**: Queue system for handling background jobs.
- **Image Thumbnail**: For creating thumbnails of uploaded images.

## Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/files-manager.git

## Usage
## Authentication

1.Generate a token via the authentication route to access the API endpoints.

2.File Management

Upload files, list all uploaded files, and view specific files using the API endpoints.

3.Background Tasks

Generate thumbnails for uploaded images automatically in the background.

## Configuration
Ensure you configure the following environment variables in your .env file:

`MONGO_URL`: The MongoDB connection string.

`REDIS_URL`: The Redis connection URL.

`TOKEN_SECRET`: Secret key used for JWT authentication.
`API Endpoints

`POST /auth/login`: Login a user and retrieve an authentication token.

`POST /files`: Upload a new file.

`GET /files`: List all uploaded files.

`GET /files/`: Retrieve a specific file.


## Background Processing
Kue is used for handling background tasks, such as generating image thumbnails after a file is uploaded. Jobs are processed using Redis as the message broker.

To view the status of jobs, you can navigate to the Kue dashboard by running the following command:

```
npm run kue-dashboard
```

## Troubleshooting
MongoDB Connection Issues: Ensure MongoDB is running and properly configured.
Redis Connection Issues: Verify that Redis is up and running on the correct port.
Thumbnail Generation Issues: Check the logs for any errors related to the image processing utility.

## Contributors
Khalif Noor - GitHub

## License
This project is licensed under the MIT License.


