## 2. Example


## Status

Proposed

## Context

John the Claim Inspector is out in the field assessing a car crash involving Adam, who has PDR Insurance. John pulls out his iPhone and opens up the PDR Insurance handy dandy mobile application to search for Adam’s profile. Behind the scenes, the application is performing an HTTP GET request using one of the API endpoints developed by Turnberry Solutions. This endpoint processes the HTTP request and sends Adam’s information from the database to the front end to be displayed. John then adds a new claim to Adam’s profile and fills in the relevant information for this claim. Adam then presses the save button which performs an HTTP PUT request to add the new information to Adam’s table in the database. 
