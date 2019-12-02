1. What is responsible for defining the routes of the games resource?

In the server folder, the server.js file creates a router using the helper file "create router". This helper file defines the restful routes that can be used, but it is the creation specifically of the games router that sets the api base url.

2. What do you notice about the folder structure? Whats the client responsible for? Whats the server responsible for?

Two overarching folders - client and server. The client folder supports the visualisation of the app, and the server deals with the data.

3. What are the the responsibilities of server.js?

Server defines the db being used and connects it with the restful routes and points things to the right direction for the app to work.

4. What are the responsibilities of the gamesRouter?
gamesRouter is set up using the create_router helper. In it, the routes are defined by finding the data, formatting them so they are in the correct format, then returning them, as well as any errors that may have arisen.

5. What process does the the client (front-end) use to communicate with the server?

Most of the clientside functionality operates using the games service.js. This acts as a go between the app the client sees and the data that needs to be manipulated and presented.

6. What optional second argument does the fetch method take? And what is it used for in this application? Hint: See Using Fetch on the MDN docs

It takes an optional init option - containing custom settings that you might also want to apply to the request. i.e. methods (get, put, post etc.) or other headers. Here, it is used for example int he postGame function to make the request post the appropriate json verison of the string sent to it.


7. Which of the games API routes does the front-end application consume (i.e. make requests to)?
Front end uses getGames to display the cards in the grid.
It also posts requests to add games to this list and deletes them by id.


8. What are we using the MongoDB Driver for?
..allows us to build the api...?

Extension
9. Why do we need to use ObjectId from the MongoDB driver?
to produce and work with a complex hex string? 
