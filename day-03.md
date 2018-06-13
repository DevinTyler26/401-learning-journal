##NPM - copy paste to save time! Thank you past Devin
npm i -D babel-eslint babel-preset-env babel-register dotenv eslint eslint-config-airbnb-base eslint-plugin-import eslint-plugin-jest eslint-plugin-react jest winston@next

copy package.json from day 2 and then do "npm i" this will download all of the dependencies needed in your package.json

##Error first
to have successful callback make sure you put undefined (null) as first argument in your callback. data will be second arg

##fs
__dirname goes back to your absolute path  const file = `${__dirname}/../assests/1.txt`;
npm i -D winston@next
logger.INFO
logger.ERROR
always toString your data from incomingData logger OR
pass in utf-8 as an arg if you dont want to use toString
ENOENT so such file or path - bad path names - messed up file name
callback hell - nested callbacks to make your files comeback in the the order you want

testing will have the expect statement inside of the callback statement of the test
expect(err).toBeNull();
test.skip will skip a test
