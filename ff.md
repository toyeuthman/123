# CRUD_REST API Documentation

## Table of Contents

- [CRUD\_REST API Documentation](#crud_rest-api-documentation)
  - [Table of Contents](#table-of-contents)
  - [Introduction](#introduction)
  - [Getting Started](#getting-started)
    - [Prerequisites](#prerequisites)
  - [Endpoints](#endpoints)
    - [Create a Person](#create-a-person)
      - [Example Request](#example-request)

## Introduction

Welcome to the documentation for the CRUD_REST API. This document provides information on how to use the API, including its endpoints, request/response formats, and examples.

## Getting Started

### Prerequisites

Before using the CRUD_REST API, ensure that you have the following prerequisites:

- Node.js installed on your machine
- MongoDB server running (configured in `.env` as `mongoURI`)
- Clone this repository and run `npm install` to install dependencies.

## Endpoints

### Create a Person

- **URL:** `/people`
- **Method:** `POST`
- **Request Body:**
  - `name` (string, required): The name of the person (between 3 and 50 characters).
  - `age` (number, required): The age of the person (between 18 and 100).

#### Example Request

```json
POST /people

{
  "name": "John Doe",
  "age": 25
}
Example Response (201 Created)
json
Copy code
{
  "message": "Person created successfully",
  "person": {
    "_id": "12345",
    "name": "John Doe",
    "age": 25
  }
}
Get All People
URL: /people
Method: GET
Example Response (200 OK)
json
Copy code
[
  {
    "_id": "12345",
    "name": "John Doe",
    "age": 25
  },
  {
    "_id": "67890",
    "name": "Jane Smith",
    "age": 30
  }
]
Get Person by ID
URL: /people/:id
Method: GET
Example Response (200 OK)
json
Copy code
{
  "_id": "12345",
  "name": "John Doe",
  "age": 25
}
Update a Person
URL: /people/:id
Method: PUT
Request Body:
name (string, required): The updated name of the person.
age (number, required): The updated age of the person.
Example Request
json
Copy code
PUT /people/12345

{
  "name": "Updated Name",
  "age": 30
}
Example Response (200 OK)
json
Copy code
{
  "message": "Person updated"
}
Delete a Person
URL: /people/:id
Method: DELETE
Example Response (200 OK)
json
Copy code
{
  "message": "Person deleted"
}
Examples
You can find example code for using the API in the test.js file. Follow the examples to perform CRUD operations on person records.

Error Handling
If a request fails validation, you will receive a 400 Bad Request response with an error message.
If a requested person is not found, you will receive a 404 Not Found response with an error message.
For server errors or other issues, you will receive a 500 Internal Server Error response with an error message.
Contributing
Explain how others can contribute to your project. Include guidelines for submitting bug reports, feature requests, or pull requests. Mention any coding standards or conventions.

License
Specify the license under which your project is distributed. Include a link to the full license text if applicable.


