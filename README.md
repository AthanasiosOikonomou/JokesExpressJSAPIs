# Jokes ExpressJS API

Welcome to the Jokes ExpressJS API! This simple project provides a RESTful API for managing jokes. It supports various operations, including retrieving random jokes, fetching specific jokes by ID, filtering jokes by type, posting new jokes, updating existing jokes, and deleting jokes.

## Start

- You need to open your index.js and write npm i to install all dependencies/ modules.
- After you need to cd to the same folder as the index.js
- Finally you can use node index.js or nodemon index.js to start your localhost. 

## Routes

1) GET /random
  -Retrieve a random joke.

2) GET /jokes/:id
  - Retrieve a specific joke by ID.

3) GET /filter
  - Filter jokes by type and retrieve all matching jokes.

4) POST /jokes
  -Post a new joke. Make sure to include the required parameters in the request body:
    --text: Text of the joke (length > 0).
    --type: Type of the joke (length > 0).

5) PUT /jokes/:id
  - Update an existing joke by ID. Make sure to include the required parameters in the request body:
    --text: Text of the joke (length > 0).
    --type: Type of the joke (length > 0).

6) PATCH /jokes/:id
  - Update a specific value of an existing joke by ID. Include the parameters you want to update.

7) DELETE /jokes/:id
  - Delete a specific joke by ID.

8) DELETE /all
  - Delete all jokes. Note: Authentication is required using the master key stored in index.js.

## Authentication

To delete all jokes (using the DELETE /all route), you need to include the correct authentication key. The master key is stored in index.js.

## Validation

The API includes a validation function that checks the inputs of the user during POST and PUT requests. The following criteria must be met:
  - The length of the joke text should be more than 0.
  - The length of the joke type should be more than 0.
    
## Status Codes and Response Messages

The API returns the following HTTP status codes:
  -- 200: Success.
  -- 400: Bad request (invalid input or missing parameters).
  -- 404: Not found (resource not available).

Custom response messages provide additional information about the operation's outcome.

## Jokes Array

Inside the index.js a jokes array exists with various jokes for your testing.

## Postman

You can use the following collection to run your tests:

[JokeAPI.postman_collection.json](https://github.com/AthanasiosOikonomou/expressApis/files/13835198/JokeAPI.postman_collection.json)

I would like to thank Dr. Angela Yu and her course 'The Complete 2023 Web Development Bootcamp' for this project.
