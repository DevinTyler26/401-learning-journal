## DSA Scaffold
- DS is updated - add index.js and every other file that is missing

## Lab Scaffold
- mongodb is now in travis.yml - lecture code will have all the new changes
- devLogger and productionLogger
- test-nolint is updated as well with new flags
- babel cli

## REST
- CRUD - Create Read Update Destroy

## lab
- index.js will always be written in ES5 because heroku cant read es6 (dont use import in index.js)
- have a jest in your package.json file
- Car.remove({}) passing in {} removes all objects 
- superagent calls are promises - so you can use a .then() after them
- comment out afterEach Car.remove({}) to see whats in the GUI after some tests
- JSON parser is only used fir PUT or POST
- response.status.(400).send('string') OR response.sendStatus(400);
- Cars.init() needs to be on PUT and POST requests then you can put a .then() to run more functionality
- every property that is flagged unique gets auto indexed by mongoose
- don't forget to turn on mongo server
- remember to string the ID because the ID from mongo is an object