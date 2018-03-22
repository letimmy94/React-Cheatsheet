# MERN App

A full-stack application using Mongo, Express, React, and Node.
Full-stack application: backend and frontend deployment.

Assuming both backend application and frontend are completed, they need to be connected.
Two kinds of servers:

* Multi-Server is where our frontend and backend remain completely seperate. This would require CORS to communicate with the backend and frontend.
* Single Server: where everything is located in one place, which means you'll only need the one deployment and don't need to use CORS.

After choosing server, seed the data using the command

```
node db/seed.js
```

Install CORS on the backend so our frontend can request the data.

```
npm install -S CORS
```

Then on the index.js file on the backend add

```
var cors = require("cors")
var app = express()
app.use(cors())
```

## Deploying Backend

setup Heroku using your terminal
Heroku create appName
Configure your Heroku for a database using MLAB
Once you've created a database in mlab use:
heroku config:set MLAB_URL=mongodb://<your_user_login>:<your_user_password>@ds015760.mlab.com:15760/<your_db_name>
This configures the database with heroku

Frontend

```
npm run build
```

Install Surge which can be done by changing out directory to build:

```
cd build
npm i -g Surge
surge
```
