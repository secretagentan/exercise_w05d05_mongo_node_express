# 🏋️ Working with Mongo in Node with Express

## Directory Structure

Let's practice issuing commands to our MongoDb server via HTTP!

## 👷 Setup

- [ ] Fork and clone this repo. 
- [ ] Install your dependencies with `npm install` and start up your server.
- [ ] Start up a mongoDB server!

## 🔬 Getting started

- [ ] Look through `routes/index.js` to see how we're connecting to MongoDB
- [ ] Check out `views/layouts/main.hbs` what scripts are being loaded on the client side?
- [ ] This app will connect to a mongoDB called "TESTER"

### 🤰 Crud
- [ ] Visit '/' and try adding data. 
- [ ] Connect to the MongoDB via the mongoshell to ensure data is making its way there!

## Implement the following user stories

### 📖 cRud

When a user visits '/'

- [ ] they should see a button "Get Data"

When a user visits '/data'

- [ ] The server should respond with JSON of all the inserted data

When a user visits '/' and clicks "Get Data"
    - the client should perform an XHR GET request to '/data'
    - the server should retrieve all the data from MongoDB
    - the server should return a JSON response of the data

When a user visits '/comments'
    - the server should retrieve all the data from MongoDB
    - the server should render an HTML response using a Handlebars template
>>>>>>> update to readme

When a user visits '/data/[objectId]'

- [ ] The server should respond with JSON of that inserted data with that objectId

When a user visits '/comments/[objectId]'
    - the server should retrieve that data from MongoDB
    - the server should render an HTML response using a Handlebars template

### 💀 cruD

Update the rendered list of data to include a "DELETE" button next to each item in the list

When a user clicks on "DELETE" for an item

- [ ] the client should send an XHR POST request '/data/[objectId]/delete'
- [ ] the server should remove the data with that objectId from the server
- [ ] the server should return a JSON response of `{status: 200}`
- [ ] the client should remove that item from the list

### 💅 crUd

Update the rendered list of data to include a "UPDATE" button next to each item in the list

When a user clicks "UPDATE" for an item

- [ ] the client should send an HTTP POST request to '/data/[objectId]'
- [ ] the server should modify the data with that objectId and change the author to "Shakespeare"
- [ ] the server should send back a JSON response of `{status: 200}`
- [ ] the client should change the name in the list

# 🚀 Bonus

When a user visits "/" and clicks "GET DATA"
    - render the JSON response with a client side templating language - handlebars or ejs, check "main.hbs" for Handlebars or Underscore
    
When a user visits '/comments/[objectId]/edit'
    - the server should render an HTML response using a Handlebars template
    - the response should include an HTML form
    - the form fields should be pre-populated with the values from the data

When a user visits '/comments/[objectId]/edit' and changes the data and clicks "Update"
    - the client should send an HTTP POST request with the data to '/data/[objectId]'
    - the server should update the data with that objectId with the data from the body of the post request
    - the server should send back a 302 response and redirect the browser to '/'

Add a nav bar to the `main.hbs` layout template to provide links to 'Home' and 'Data'

## 🤷‍♀️Resources

- [Handlebars Documentation](http://handlebarsjs.com/)
- [Templating Engine set-up](https://webapplog.com/jade-handlebars-express/)
- [Express Error Handling](https://expressjs.com/en/guide/error-handling.html)
- [Express Router Docs](https://expressjs.com/en/4x/api.html#router)
- [Express Router](https://scotch.io/tutorials/learn-to-use-the-new-router-in-expressjs-4)
- [MongoClient](https://mongodb.github.io/node-mongodb-native/driver-articles/mongoclient.html)
- [Node Assert](https://nodejs.org/api/assert.html)
- [Client Side EJS](http://underscorejs.org/#template)
