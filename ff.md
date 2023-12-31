CRUD_EXPRESS API WITH MONGODB


Table of Contents

[Introduction](#introdction)

[Getting Started](#getting-started)

[API Endpoints](#api-endpoints)

[Examples](#examples)

[Error Handling](#error-handling)

[Contributing](#contributing)

[License](#license)

## Introduction

This repository contains a simple Express.js API for managing a collection of people using a MongoDB database. The API supports basic CRUD (Create, Read, Update, Delete) operations for people records.

## Getting Started
Before running this application, make sure you have the following prerequisites installed:

Node.js: JavaScript runtime environment.
MongoDB: A NoSQL database for storing the person records.
Git: Version control system (optional, but recommended for managing codebase).
Clone the Repository
Clone the repository to your local machine (if you haven't already):

bash
Copy code
git clone https://github.com/your-username/express-mongodb-api.git
Navigate to the Project Directory
bash
Copy code
cd express-mongodb-api
Install Project Dependencies
bash
Copy code
npm install
Create a .env File
Create a .env file in the root directory of the project with the following content:

env
Copy code
PORT=3000
mongoURI=mongodb://localhost/your-database-name
Replace your-database-name with the name of your MongoDB database.

Start the Express Server
bash
Copy code
npm start
Your API should now be running at http://localhost:3000.

## API Endpoints
Create a Person

Endpoint: POST /people
Request Body:
json
Copy code
{
  "name": "John Doe",
  "age": 30
}
Description: Create a new person record with a name and age.
Get All People

Endpoint: GET /people
Description: Retrieve a list of all people records.
Get a Person by ID

Endpoint: GET /people/:id
Description: Retrieve a person record by their unique ID.
Update a Person by ID

Endpoint: PUT /people/:id
Request Body:
json
Copy code
{
  "name": "Updated Name",
  "age": 35
}
Description: Update a person's name and age by their unique ID.
Delete a Person by ID

Endpoint: DELETE /people/:id
Description: Delete a person record by their unique ID.
## Examples
Include examples of how to use the API endpoints here.

## Error Handling
If a request results in an error, the API will respond with an appropriate HTTP status code and a JSON response containing an error message.

## Contributing
Contributions are welcome! If you find any issues or have suggestions for improvements, please feel free to open an issue or submit a pull request.

## License
This project is licensed under the MIT License - see the LICENSE file for details.

Acknowledgments
This project was built using Express.js for the API and Mongoose for MongoDB integration. Thanks to the open-source community for their contributions to the development of these technologies.




