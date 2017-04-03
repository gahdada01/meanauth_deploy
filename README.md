# Changes from development stage to poduction deployment.

## app.js

Change `const port` from `3000` to `process.env.PORT || 8080`.

## Angular service

Change the service that have `POST` and `GET` to a url like for example `http://localhost:300/users/profile` to `users/profile`.

## Build

You should be in angular-cli to ng build so cd angular-src folder.

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `-prod` flag for a production build.

You can also do the above instructions but I also have choose to do this.

Open angular-src/angular-cli.json and change the `"outDir": "../dist"` in apps object to `"outDir": "../public"`.

When running `ng build`, It will automatically save and make a public folder in the main folder.

## Server Side

In my app, I am using `MongoDB` as a database.

To set up MongoDB database. Go to `https://mlab.com`.

Create an account or if you already have an account just login.

In `https://mlab.com/home` page inline with `MongoDB Deployments`. Create an account.

Below Plan, select `Single-node`. Then below the Standard Line, select `Sandbox`.

Then set `Database Name` below.

Click `Users` then add database user which will have your username and pass.

Then paste this in your database.js and change database set up which will look like this `database: mongodb://<dbuser>:<dbpassword>@ds149820.mlab.com:49820/meanauth`

`<dbuser>` = your user name.
`<dbpassword>` = your password