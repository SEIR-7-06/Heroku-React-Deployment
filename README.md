# Heroku React Deployment

To deploy a prodution ready react application to heroku follow the steps below. 

## Login to heroku cli
```bash 
heroku login
```

## Create Heroku app and set the build pack. 
```bash
heroku create $APP_NAME --buildpack mars/create-react-app
```
When you deploy to heroku this buildpack with compile and publish a production ready application. 

## Commit and Deploy
```bash
git add .
git commit -m "Start with create-react-app"
git push heroku master
```

And that's it! Easy peasy lemon squeezy. 

### notes:
You will need to update your configuration variables to connect to your deployed remote URL. Your can find them in your heroku dashboard. 
Settings -> configuration variables. 

```
REACT_APP_API_URL = $NODE_SERVER_URL
```
_When it comes to deployed react apps config variables must say REACT_APP in front of the variable name to run properly._
