## remember
- killall mongod - to kill old mongo servers
- grab the new index.js
- grab new logger.js
- DevOps should be in LinkedIn

## 1 to many
- FB post would be the 1 and the comments would be many

## 1 to 1 relationship
- user to profile
- user - passwords, email
- profile - about me, interests

## many to many
- barcrawl
- user can have many crawls and crawls can have many users

## dijkstra's alg
- go look this up

## new dependencies
- cors
- http-errors

## lecture
```
classroom {
    students []
}
```
- you can not have a student without a classroom (for now)
- documents are new instances on your model (classroom)
- subdocument will be students that map back to the classroom

```
mockdata = {
    classRoom: {
        _id: 12534,
        name: some name,
        students: [3252354236,  325643643],
    },
    student: {
        first: name,
        last: name,
        _id: 3252354236,
        classRoomId: 12534,
    }
}
```
- superagent POST will be followed by a .send(mockData)
- 