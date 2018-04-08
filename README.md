# edX - Microsoft: DEV283x
## Introduction to Node.js
[About EdX course](https://courses.edx.org/courses/course-v1:Microsoft+DEV283x+2T2017/course/)

### Module 4 Assignment Lab: REST API with Mongoose

Implemented a persistent Express REST API server with MongoDB and the Mongoose native driver.

Simple application, to handle Accounts, which has the following REST API endpoints:
*  GET and POST /accounts
*  PUT and DELETE /accounts/:id/

Used the next Account Schema:
```javascript
{
    name: {
      type: String
      ,validate: {
        validator: function(v) {
          return v.length > 1;
        },
        message: '{VALUE} is too short as account name!'
      }
      , required: [true, 'Account name is required']
    },
    balance: {
      type: Number
      , required: [true, 'Balance value is required']
    }
}
```

### HOW MAKE A LOCAL INSTALLATION
```sh
$ git clone https://github.com/jomayma/rest-api.git
$ cd rest-api
$ npm install
$ npm start
```

To implement the code I have used: **errorhandler, express, morgan, mongodb, mongoose**

Check the ./test.sh file in order to make some simple tests.

