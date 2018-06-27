## lab 12 deployment 
- pull down from 11 into 12
- set up travis
- goto heroku
- create new app
- mongodb-express-test-something
- resources
- add ons
- mlab
- click provision - probably have to put in CC
- deplopy
- choose github
- search for forked repo
- enable auto deploys
- go to build on heroku after merging to master
- copy link from build
- http POST https://mongodb-exp-test.herokuapp.com/api/cars/ make=audi model=rs4

- if I run into trouble heroku app (app name)

## code review
- app.use is basically middleware

## lab
- return next(); - is expected
- import loggerMiddleware in server.js
- 