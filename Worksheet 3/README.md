#Worksheet 3

##Entity-Relationship Diagram

![Entity Relationship Diagram](https://github.com/NecroReindeer/comp110-worksheets/blob/master/Worksheet%203/Entity%20Relationship%20Diagram.png)

##Client-Server Pseudocode
###Display the high score table for the current level
Client
```
Get the name of the current level
Request high score table for current level from server
```
Server
```
Receive request for high score table for the current level
Get a list of the top 10 paired scores and player names for the current level from the database
Encode list into JSON
Respond with encoded list
```
Client
```
Receive encoded list
Decode list from JSON
Display each score and player name pair on the screen
```
