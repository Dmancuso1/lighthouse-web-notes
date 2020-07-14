    You are asked to build an API for a photo app.
    You need to create the routes according to REST for the following actions:

### 1 The end-user wants to see a list of photos
* GET /photos

### 2 The end-user wants to see a particular photo
* GET /photos/:id

### 3 The end-user wants to upload a new photo
* GET /photos/new
* POST /photos/:id

### 4 The end-user wants to update an existing photo
* GET /photos/:id/update
* PUT/POST /photos/:id      (form in html cannot use PUT)
         
### 5 The end-user wants to see a list of user profiles

* GET /users

### 6 The end-user wants to see a specific profile
* GET /users/:id

### 7 The end-user wants to see a list of the photos for a specific profile

* GET /users/:id/photos 

<br>

### You need to write the route with a verb and a path. You don't need to implement the functionality.


For example, to get a list of users, you just need to write GET '/users'. No need to write the code to get the actual users.