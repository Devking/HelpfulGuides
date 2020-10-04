# Heroku Setup

Create an account on the [Heroku](https://www.heroku.com/) website.

Install the Heroku CLI using `brew`.

```
brew tap heroku/brew && brew install heroku
```

Some core Heroku CLI commands:

```
# Log in to the Heroku CLI
heroku login

# Create a new Heroku app
heroku create

# Deploy your app on Heroku
git push heroku master
```

# Node Deployment

[Heroku's Instructions](https://devcenter.heroku.com/articles/deploying-nodejs)

Make sure that a `package.json` exists and specifies a Node version.

```
{
  # Dependencies and stuff
  "engines": {
    "node": "14.13.0"
  }
}
```

First Heroku will look for a `PROCFILE`, and if one is not found, it will run the `start` script specified in `package.json`.

Test that it works locally.

```
# Runs the web server on http:/localhost:5000/
heroku local
```
