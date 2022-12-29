## Deploying a Full-Stack App with Heroku
Hello! This GitHub repo is intended to be used with the article [Deploying a Full-Stack App with Heroku](https://www.codecademy.com/articles/deploying-a-back-end-with-heroku).

Make sure to follow the steps as outlined in the article to see how to use Heroku for your deployment needs!

If you're curious about the app itself feel free to poke around. The server files are located in the root folder. The `/build` folder contains the production code that was created from the front-end folder found in `/client`.

You're free to make changes on your own branch, but for the sake of consistency, we will not be merging any external pull requests. Thank you and happy coding!


Procfile - A text file that is used by Heroku to tell it what commands to run on startup. Your Procfile contains a process type: web that lets Heroku know that this app will receive web traffic, and a command to start the process: node app.js which starts the server (just like if you were to type node app.js to start a server on your local host).

app.js - The app’s entry point. This file defines the port for your web server, and contains all of the logic for the app. Express is used to route requests, send and receive data from the front front-end, and render a page. It also uses node-postgres to interface with the PostgreSQL database you will be setting up later on. Specifically the pool constant, where the connection to the Heroku Postgres database is made. Be sure to read over the comments in this file to gain a better understanding of what all of the code does.

/client - Which contains the React front-end to create the views of this full-stack application.

/build - Contains the production ready code that Node is communicating with to establish a back-end to front-end connection.
