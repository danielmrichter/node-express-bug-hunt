# Node & Express Bug Hunt!

**READ ALL INSTRUCTIONS BEFORE STARTING**

There are 10 bugs in total, can you find them all? There are hints throughout (???), you should only need to make minor modifcations to 10 lines of code.

**Don't race through the files looking for the issues!** They should all have a console log or error that help you identify them. Read the console so that you know what error will cause each bug. The last one is tricky since it doesn't throw any errors. Document the error, line number and your fix in this README for each of the bugs.

## Setup
```
npm install
npm start
```

> NOTE: A couple of bugs prevent the server from starting.

## Error List

TODO: Add the error here followed by the line of code you fixed.

### Bug 0

`ReferenceError: app is not defined`

Fixed `quote.router.js` line 28: switch `app` to `router`. _This is the solution to the first bug._

### Bug 1

`Router.use() requires a middleware function but got an object`

Fixed quote.router.js, adding in module.exports to export the router into the server.js file.

Look, I'm bad at recording stuff. I notice bugs and I fix them.
### Bug 2
While I was there, changed the quoteList from an object into an array, which it is supposed to be.

### Bug 3
Fixed a typo somewhere as well, I don't even remember where. Think it was in the getQuotes function server side

### Bug 4
Static files weren't being delivered because express wasn't pointed in the correct spot to get deliver them from. Changed `static('/public')` on line 17 to `static('server/public')`

### Bug 5
The GET request from client side was getting a 404. Changed the route in the quote.router.js file on the router.get to not be `/quotes` but to just be `/`. Because that's how it works... for some reason.
### Bug 6
POST request was getting an error. This wasn't because of the POST request, but a typo in the function call for `getQuotes()`.

### Bug 7
For some reason there was an `i+= 1` in the for of loop in the getQuotes() function. Deleted, though it doesn't actually do anything. Along with the i that was being tracked above it.
## Extra Practice (Optional)

Complete the JS debugging exercises at:

- https://education.launchcode.org/intro-to-professional-web-dev/chapters/errors-and-debugging/exercises.html
