# back-end

Hi guys! Here is some documentation to help you figure out the API

This is the full url that you will need as a prefix to every request:
    https://bw-bucketlist.herokuapp.com/api

These are the endpoints available to you:

Users

POST /users/register
returns: object
function: adds user to database
Data structure:
  username: "" *required*
  password: "" *required*
  email: "" *optional*

POST /users/login
returns: object
function: verifies user is registered in the database, provides token to allow access to protected material
Data structure:
  username: "" *required*
  password: "" *required*
  email: "" *optional*

GET /users
returns: array
function: shows list of all users in database *must be logged in to view

GET /users/:id
returns: object
function: returns specified user by id *must be logged in to view

PUT /users/:id
returns: object
function: updates specified user information **NOTE: password cannot be changed! *must be logged in to change

DELETE /users/:id
returns: object
function: removes user from database **NOTE: this is irreversible! *must be logged in to remove 


Buckets

GET /users/:id/buckets
returns: array
function: shows buckets belonging to the specified user (right now it just shows all buckets, but I'll fix that)

POST /users/:id/buckets
returns: object
function: adds a new bucket to a specified user
Data structure:
  title: "" *required*
  created_by: "" *optional*

GET /users/:id/buckets/:id
returns: object
function: shows the bucket with the specified id

PUT /users/:id/buckets/:id
returns: object
function: user can update the bucket information
Data structure:
  title: "" *required*
  created_by: "" *optional*

DELETE /users/:id/buckets/:id
returns: object
function: removes bucket from database





