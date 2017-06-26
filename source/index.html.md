---
title: DocmanPro API Reference
language_tabs:
  - javascript
toc_footers:
  - <span>&copy; Ignatius Ukwuoma</span>
includes:
  - users
  - documents
  - roles
  - search
search: true
---
# Introduction
DocmanPro API contains restful API endpoints that allow users to create, read, update and delete documents, users and roles. It also offers a way to ensure that only authorized users can perform certain operations.
## Development
DocmanPro is a [NodeJs](http://nodejs.org/) application and [Express](http://expressjs.com/) is used for routing. [Sequelize](http://docs.sequelizejs.com/) is used as the Object Relational Mapper with [Postgres](http://postgresql.com/) as database.
## Installation
Follow the steps below to setup a local development environment. First ensure you have [Postgresql](https://www.postgresql.org/) installed, and a version of [Node.js](http://nodejs.org/) greater than or equal to v6.8.0.
1. Clone the repository from a terminal with `git clone https://github.com/andela-iukwuoma/docman.git`.
2. Move into the project directory with `cd docman`
3. Create a `.env` file and add your database URL as the key name `DATABASE URL`.
4. Install project dependencies with `npm install`
5. Start the express server with  `npm start`.
## API Summary
### Users
EndPoint                      |   Functionality
------------------------------|------------------------
POST /users/login         |   Logs in a user
POST /users/logout        |   Logs out a user
POST /users/              |   Creates a new user
GET /users/               |   Gets all users (available only to Admins)
GET /users/:id           |   Retrieves a particular user by the id specified
PUT /users/:id           |   Updates a user's details by the id specified (available only to the user and SuperAdmin)
DELETE /users/:id        |   Deletes a user by the id specified (available only to the user and SuperAdmin)
GET /users/:id/documents   | Gets all documents for a particular user by the id specified
GET /users/?limit={integer}&offset={integer} | Get users by limit and/or offset for pagination
### Documents
EndPoint                      |   Functionality
------------------------------|------------------------
POST /documents/          |   Creates a new document.
GET /documents/           |   Gets all documents.
GET /documents/:id       |   Find document by id.
PUT /documents/:id       |   Updates a document's details. (available only to the author and Admins)
DELETE /documents/:id    |   Delete document. (available only to the author and Admins)
GET /documents/?limit={integer}&offset={integer} | Get documents by limit and/or offset for pagination
### Roles (available only to the SuperAdmin)
EndPoint                      |   Functionality
------------------------------|------------------------
GET /roles/               |   Get all Roles.
POST /roles/               |   Create a Role.
PUT /roles/:id               |   Edit a Role by the id specified.
DELETE /roles/:id               |   Delete a Role by the id specified.
### Search
EndPoint                      |   Functionality
------------------------------|------------------------
GET /search/documents/?q=query | Get all documents with title containing the search query
GET /search/users/?q=query | Get all users whose name, username or email matches the search query (available only to Admins)