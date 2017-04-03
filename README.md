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




