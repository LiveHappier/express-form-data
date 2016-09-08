# express-form-data
<<<<<<< HEAD
Module for parsing multiform data. Based on "connect-multiparty"
=======
Module for parsing multiform data. Base on "connect-multiparty"
>>>>>>> parent of 3cef0e8... v1.0.0
# Install 
`npm install express-form-data`
# Example
```js
var formData = require("express-form-data");
var express = require("express");
var app = express();

// parsing data with connect-multiparty. Result set on req.body and req.files
app.use(formData.parse(...connectMultipartyOptions));
<<<<<<< HEAD
// clear all empty files
app.use(formData.format());
// change file objects to node stream.Readable 
=======
// change all request body to json format
app.use(formData.json());
// create node stream.Readable from elements in req.files and add them in req.stream
>>>>>>> parent of 3cef0e8... v1.0.0
app.use(formData.stream());
// union body and files
app.use(formData.union());
```

After this functions we can see in req:
<<<<<<< HEAD
* req.files = {...} all files 
=======
* req.files = {...} all files request data in connect-multiparty object format
* req.stream = {...} all files request data in node stream object format
>>>>>>> parent of 3cef0e8... v1.0.0
* req.body = {...} all request data including files(or streams if you use .stream())
