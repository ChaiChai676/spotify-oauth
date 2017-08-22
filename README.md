# OAuth bridge template

This service logs in to Spotify and redirects the user to a given frontend application with a valid access_token as a parameter in the url.

In development mode, it assumes you are running the frontend on localhost:3000, but the server itself will be running on localhost:8888.

In order to start developing, register a Spotify Application here:
https://developer.spotify.com/my-applications

On that page, add http://localhost:8888 as a callback url (don't forget to hit save at the bottom of the page)

Write the below commands in your terminal (replacing XXXX AND YYYY with your acutal client id and secret from the page where you registered your application)

```
export SPOTIFY_CLIENT_ID=XXXX
export SPOTIFY_CLIENT_SECRET=YYYY
```


This app is made to be deployed on Heroky. Before you do, you need to configure the app with the following commands:

```
heroku config:set CLIENT_ID=XXXXX
heroku config:set CLIENT_SECRET=YYYYY
heroku config:set REDIRECT_URI=http://mybackend.herokuapp.com/callback
heroku config:set FRONTEND_URI=http://myfrontend.herokuapp.com
```
