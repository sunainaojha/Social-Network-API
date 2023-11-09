# Social Network API

## Description

This Social Network API provides a backend for a social networking startup. It uses a NoSQL database and can handle large amounts of unstructured data. With this API, it is possible to perform CRUD operations on users, thoughts, reactions and friends.

## Installation

1. Clone the repository to your local machine.
2. Navigate to the directory where the repository was cloned.
3. Run npm install to install all the dependencies.
4. Make sure MongoDB is installed and running on your local machine.

## Usage

This application runs on a local server.

1. To start the server, run npm start in the terminal.
2. This will start the server and will sync the Mongoose models to the MongoDB database.
3. You can use Insomnia to test the API routes.

## API Routes

### Users

- GET all users: /api/users
- GET a single user by its _id: /api/users/:id
- POST a new user: /api/users
- PUT to update a user by its _id: /api/users/:id
- DELETE to remove user by its _id: /api/users/:id
- POST to add a new friend to a user’s friend list: /api/users/:userId/friends/:friendId
- DELETE to remove a friend from a user’s friend list: /api/users/:userId/friends/:friendId

### Thoughts

- GET to get all thoughts: /api/thoughts
- GET to get a single thought by its _id: /api/thoughts/:id
- POST to create a new thought (don't forget to push the created thought's _id to the associated user's thoughts array field): /api/thoughts
- PUT to update a thought by its _id: /api/thoughts/:id
- DELETE to remove a thought by its _id: /api/thoughts/:id

### Reactions

- POST to create a reaction stored in a single thought's reactions array field: /api/thoughts/:thoughtId/reactions
- DELETE to pull and remove a reaction by the reaction's reactionId value: /api/thoughts/:thoughtId/reactions/:reactionId

## Technologies Used

- Node.js
- Express.js
- MongoDB
- Mongoose

## Links 
[Github](https://github.com/sunainaojha/Social-Network-API)

[Demonstration Video](https://drive.google.com/file/d/1Wpj_m6aPJreeMwC16g6EdG8DlvXS2akY/view)