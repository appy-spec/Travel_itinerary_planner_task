# Travel_itinerary_planner_task
Triplify helps users plan their travel itineraries, including adding destinations, start/end date, number of guests and activities. The app utilizes google map APIs to display the map with popular activities of various types for users to select and add to itinerary. The app also uses openAI API to suggest travel itineraries, answer questions and provide recommendations. A full user interface with user signup, login, update profile, logout is implemented. The user state is maintained across all pages with an Express session.

Link: https://triplify-5a9d21c42868.herokuapp.com/
The purpose of the project is to learn and practice concepts:
Buildiing a full stack website
Practice Vanilla JS, HTML/CSS and sql
MVC Architectural Pattern.
Following technologies and framework were used:
Node/Express for backend
Vanilla JS for front-end
Jaws DB for CRUD operations
Session for maintaining state
APIs: Google Map & Marker, Google Places (new), Google Places (legacy), openAI API
Bcrypt for hashing passwords
DB Schema:
Users
userId INT (PK) Unique identifier for each user
password VARCHAR Hashed password for security
email VARCHAR Email address of the user
firstName VARCHAR User's first name
lastName VARCHAR User's last name
subscribed TINYINT User subscription to newsletter
mobilePhone VARCHAR User’s phone number
addressLine VARCHAR User’s address line of residency
postalCode VARCHAR User’s postal code of residency
country VARCHAR User’s country of residency
state VARCHAR User’s state of residency
Itineraries
itineraryId INT (PK) Unique identifier for each user
userId INT (FK) Username of the user
destination VARCHAR Location
startDate DATE Start date of the trip
endDate DATE End date of the trip
duration INT Trip duration
guests INT Number of guests
Activities
activityId INT (PK) Unique identifier for each activity
itineraryId INT (FK) ID of the related itinerary
name VARCHAR Name of the activity
dayId VARCHAR Date of the activity in the itinerary
placeId VARCHAR Google’s Place Id retrieved from Places API
address VARCHAR Location of activity
