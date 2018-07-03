## async await
- lets async code look synchronous 

this:
```
beforeAll(
  pCreateAccount()
  .then((mockData) => {

  })
  .catch((err) => {
    
  })
);
```
is now this:
```
beforeAll(async () => {
  startServer();
  try {
    mockData = await pCreateAccountMock(); // this blocks until we have the resolved value
    // mockData will be the returned resolved value of pCreateAccountMock promise
  } catch (err) {
    return console.log(err)
  }
});
```
- if there is a chance tha something could fail, wrap in try catch block
- must have function named async to use await
