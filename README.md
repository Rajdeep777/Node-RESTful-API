# Node.js, Express.js & MongoDB: CRUD RESTful API
This is a simple Tutorial application. We will build Rest APIs for creating, reading, updating and deleting the tutorial.

We’ll start by building a simple web server and then move on to configuring the database, building the Tutorial model and different routes for handling all the CRUD operations.

Finally, we’ll test our RESTful APIs using Postman.

We’ll heavily use ES6 features like let, const, arrow functions, promises etc.


First, we start with an Express web server. Next, we add configuration for MongoDB database, create Tutorial model with Mongoose, write the controller. Then we define routes for handling all CRUD operations (including custom finder).


## Project setup
```
npm install
```

### Run
```
node server.js
```
## Endpoints:
```sh
GET    /api/tutorials
POST   /api/tutorials
PUT    /api/tutorials/:id
DELETE /api/tutorails/:id
```

### 1. Create a new Tutorial using POST /tutorials Api
This endpoint inserts a document in the `tutorials` collection of the `tutorials` database.  
Send a `POST` request to `api/tutorials`:

Response:
```sh
{
    "title": "Node tutorial",
    "description": "Node.js is an open source, cross platform, JavaScript run time evironment.",
    "published": false,
    "createdAt": "2023-06-20T08:48:54.568Z",
    "updatedAt": "2023-06-20T08:48:54.568Z",
    "id": "649167f6fc27c788bec32e52"
}
```

### 2. Retrieve a single Tutorial by id using GET /tutorials/:id Api
This endpoint retrieves a tutorial given the id.  
Send a `GET` request to `api/tutorials/:id`:

Response:
```sh
{
    "title": "Express tutorial",
    "description": "Express is a minimal and flexible Node.js web application framework that provides a robust set of features for web and mobile applications.",
    "published": false,
    "createdAt": "2023-06-20T08:56:58.853Z",
    "updatedAt": "2023-06-20T08:56:58.853Z",
    "id": "649169dafc27c788bec32e55"
}
```

### 3. Update a Tutorial using PUT /tutorials/:id Api
This endpoint updates the provided fields within the specified document filtered by id.  
Send a `PUT` request to `api/tutorials/:id`:

Response:
```sh
{
    "message": "Tutorial was updated successfully."
}
```

### 4. Delete a Tutorial using DELETE /tutorials/:id Api
This endpoint deletes the tutorial from database given the id.  
Send a `DELETE` request to `api/tutorial/:id`:

Response:
```sh
{
    "message": "Tutorial was deleted successfully!"
}
```
### Delete all Tutorial using DELETE /tutorials Api
This endpoint deletes the tutorial from database given the id.  
Send a `DELETE` request to `api/tutorial`:

Response: 
```sh
{
    "message": "4 Tutorials were deleted successfully!"
}
```