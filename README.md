# Heroku React Deployment
<!-- 
## Create a Separate Repo
If this is a group project, and you weren't the original creator of the repo you will most likely want to have your own version of the app deployed that you can continue to work on post graduation.

1. If you were not the original owner/creator of the project repo, go ahead and make your way to the repo for the project on Github and fork that project to your own Github account.

2. Once you've forked it, clone the repo to your local machine and rename it to something different. This will be your personal version of the repo.
for example.
```bash
git clone git@github.com:myusername/wayfarer-project.git wayfarer-project-personal
```
3. Now you're ready to deploy! -->

## Deployment Steps

To deploy a prodution ready react application to heroku follow the steps below. 
```bash
cd $YOUR_PROJECT_REPO
```

## Login to heroku cli
```bash 
heroku login
```

## Create Heroku app and set the build pack. 
```bash
heroku create $YOUR_REACT_APP_NAME --buildpack mars/create-react-app
```
When you deploy to heroku this buildpack with compile and publish a production ready application. 

##
Now we're ready to make 

## Update Your API Endpoint
You will want to update your API endpoint from `localhost:4000` to the domain for your deployed backend on Heroku. For example, instead of making requests to `http://localhost:4000/cats` you will want to update this to `https://cats-api.herokuapp.com/`.

You may even decide to store this in an environment variable, in which case you will update it in your `.env` file and also include it as a config variable in Heroku.

_When it comes to deployed react apps config variables must say REACT_APP in front of the variable name to run properly._

for example...
```bash
REACT_APP_API_URL = $NODE_SERVER_URL
```

## Commit and Deploy
```bash
git add .
git commit -m "Start with create-react-app"
git push heroku master
```

And that's it! Easy peasy lemon squeezy. 


