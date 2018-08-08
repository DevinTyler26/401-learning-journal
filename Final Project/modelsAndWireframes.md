# final project preparation: backend models and frontend wireframes

## models:
 ```
 user {
    firstName: '',
    lastName: '',
    email: '',
    address: ''
    phoneNumber: ''
    type: [staff, teacher, coach]
 }
 ```
 ```   
 student {
    firstName: '',
    lastName: '',
    points: int,
    schoolName: '',
    classes: [],
    grades: [],
    games: [],
    sportsTeams: [],    
    teachers: [],
    goals: [],
    coaches: [],
    familyMembers: [],
 }
```
```
  familyMember {
    firstName: '',
    lastName: '',
    students: [],
 }
```
```
  coach {
    players: [],
    playersMentors: [],
  }
```
```
  teacher {
    students: [],
  }
```
```
  sport {
    sportName: '',
    students: [],
 }
 ```
 ```
  school {
    schoolName: '',
    students: [],
 }
```
```
  authUser {
    name: '',
    students: [],
  }
```
## data modeling relationships

### mentor
- one mentor can have many students

### student
- one student can have one mentor
- one student can have many coaches
- one student can have many teachers

### coach
- one coach can have many players
- one coach can have many mentors (mentors will be their players mentors)

## routes
### /students
  - /students
    - will return all students in the program
  - /students:id
    - with an id query, you can get one student back with all of their info (grades, teachers, classes, sports, points etc...)
  - /students:school
    - with a school query, you can get all the students at one school
  - /students:sports
    - with a school query, you can get all the students in one sport

### /mentor
  - /mentors
    - will return all mentors in the program
  - /mentors:id
    - with an id query, you can get one mentor back
  - /mentors:school
    - with a school query, you can get all the mentors at one school
  - /mentors:sports
    - with a school query, you can get all the mentors in one sport