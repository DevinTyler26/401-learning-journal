##NPM - copy paste to save time! Thank you past Devin
npm i -D babel-eslint babel-preset-env babel-register dotenv eslint eslint-config-airbnb-base eslint-plugin-import eslint-plugin-jest eslint-plugin-react jest

##Setting up Travis CI
github fork 
settings
integrations
travis ci
password 
branches 
branch protection rules 
master 
protect this branch
require status checks to pass
save changes
travis-ci.org
profile
sync account
click toggle button for repo you want to test
clone repo
npm init
__test__ 
create test file faketest.test.js
write test
configure .travis.yml from 00-lab-scaffold in the root of the project folder
goto package.json and create test script "jest --coverage"
git checkout -b lab0X
ACP
goto github
goto forked repo and create pull request from branch to master (change the base repo to personal repo not codefellows)
click on travis ci continuous check details 
back to github and see if checks pass
if passed, merge to master

Travis Badge - build - markdown - copy link and put at top of README.md

##Errors
try catch statement: //it is good for you own custom errors
    try { 
        if (params)){
            //with throw a dev cant ignore the error
            throw new Error ('Error message');
    }
    return 'message';
    }catch(err)
        console.log(err);
        //you can put in more logic here to move on if there is an error
        }
        return undefined;
    };

when you're using a 3rd party that already provides an error for you, dont use try catch i.e (err,data)

JSON.parse is when we will use a try catch call. JSON.parse has their own error catching so we wont need an if statement

##Remember
Spread operators (...args)
test": "eslint . && jest --coverage"
"testWatch": "jest --coverage --watchAll"
test('statement', ()=> {
expect(()=>{
        emptyList.map(e=>e);
    }).toThrow();
});

beforeEach(()=>{

});
afterEach(()=>{

});