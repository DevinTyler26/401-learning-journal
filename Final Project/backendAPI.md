# Rainier Athletes Backend API

## Routes

### POST
  - /api/v1/accounts
  - /api/v1/profiles
  - /api/v1/pointstracker

### GET
  - /api/v1/login
  - /api/v1/profiles?id=mongoose._id
  - /api/v1/profiles/me
  - /api/v1/pointstracker?[id=mongoose._id | student=mongoose._id | date=tracker-date]
    - We'll need to experiment with the date query to be sure date is formatted correctly. And that it's a valid report date (a Friday).

### PUT
  - /api/v1/profiles?id=mongoose._id
  - /api/v1/pointstracker?id=mongoose._id

### DELETE
  - /api/v1/accounts?id=mongoose._id
  - /api/v1/profiles?id=mongoose._id
  - /api/v1/pointstracker?id=mongoose._id
  
## Mock JSON

### GET /api/v1/pointstracker?student=1EF12348902093DECBA908 JSON
```
{
  "_id": "1EF12348902093DECBA908", 
	"date": 1533761272724,
	"studentId": "1EF12348902093DECBA908",
	"subjects": [{
		"subjectName": "Social Studies",
		"teacher": "1EF12348902093DECBA910",
		"scoring": {
			"excusedDays": 1,
			"stamps": 14,
			"x": 3,
			"tutorials": 1
		}
	}, {
		"subjectName": "Math",
		"teacher": "1EF12348902093DECBA912",
		"scoring": {
			"excusedDays": 1,
			"stamps": 12,
			"x": 6,
			"tutorials": 0
		}
	}, {
		"subjectName": "Biology",
		"teacher": "1EF12348902093DECBA914",
		"scoring": {
			"excusedDays": 1,
			"stamps": 16,
			"x": 1,
			"tutorials": 2
		}
	}],
	"surveyQuestions": {
		"attendedCheckin": true,
		"metFaceToFace": true,
		"hadOtherCommunication": false,
		"scoreSheetTurnedIn": true
	},
	"synopsisComments": {
		"extraPlayingTime": "Jamie is working hard toward his goals. We agreed that if he achieved a small improvement this week he would get extra playing time.",
		"studentActionItems": "Jamie agreed to attend 1 more tutorial in each of his classes this coming week",
		"sportsUpdate": "Last week Jamie had a great game against the Cardinals. Had two hits and caught three fly balls!",
		"additionalComments": ""
	}
}
```

### Student Profile: GET /api/v1/profiles?id=1EF12348902093DECBA908
```
{
  "_id": "1EF12348902093DECBA908",
	"firstName": "Jamie",
	"lastName": "McPheters",
	"email": "jamiemcp@gmail.com",
	"address": {
		"street": "615 6th St",
		"apt": "Apt 202",
		"city": "Bellevue",
		"state": "WA",
		"zip": "98007"
	},
	"phone": "425-643-5178",
	"role": "student",
	"studentData": {
		"scoringReports": ["1EF12348902093DECBA914", "1EF12348902093DECBA916", "1EF12348902093DECBA914"],
		"coaches": ["1EF12348902093DECBA920"],
		"school": "Odle Middle School",
		"mentor": "1EF12348902093DECBA914",
		"teachers": ["1EF12348902093DECBA914", "1EF12348902093DECBA916", "1EF12348902093DECBA914", "1EF12348902093DECBA914", "1EF12348902093DECBA916", "1EF12348902093DECBA914", "1EF12348902093DECBA914"],
		"family": ["1EF12348902093DECBA914", "1EF12348902093DECBA916"]
	},
	"mentorData": {}
}
```

### Mentor Profile: GET /api/v1/profiles?id=1EF12348902093DECBA908
```
{
  "_id": "1EF12348902093DECBA908",
	"firstName": "Ryan",
	"lastName": "Smithers",
	"email": "ryan@rainierathletes.com",
	"address": {
		"street": "1714 147th Ave SE",
		"apt": "",
		"city": "Bellevue",
		"state": "WA",
		"zip": "98007"
	},
	"phone": "425-648-2212",
	"role": "mentor",
	"studentData": {},
	"mentorData": {
		"students": ["1EF12348902093DECBA914", "1EF12348902093DECBA916"]
	}
}
```

### Teacher/Family/Staff profile (everybody else): GET /api/v1/profiles?id=1EF12348902093DECBA908
```
{
  "_id": "1EF12348902093DECBA908",
	"firstName": "Generic",
	"lastName": "Person",
	"email": "anybody@gmail.com",
	"address": {
		"street": "12345 67th St NW",
		"apt": "",
		"city": "Bellevue",
		"state": "WA",
		"zip": "98007"
	},
	"phone": "425-648-5555",
	"role": "teacher",
	"studentData": {},
	"mentorData": {}
}
```