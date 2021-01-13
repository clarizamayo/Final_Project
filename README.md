This Readme includes:
- About Project
- Languages
- Important changes (by date)
- Preparing for Deployment
- Deployment to Heroku Instructions

# CO2 Emissions Final Project

This repository contains data on carbone dioxyde around the world. The data of two websites are being scrapped to be able to analyze more accurately how a country's population affects the quantity it produces. When only one factor is taken to draw conclusions on 

You can view visualizations of these data on the [my deployed website at: ](https://emissionsproject.herokuapp.com/). Additional data related to CO2 Emissions is available via [List of countries by Carbon Dioxide Emissions](https://en.wikipedia.org/wiki/List_of_countries_by_carbon_dioxide_emissions) and [List of countries by population in 2005](https://en.wikipedia.org/wiki/List_of_countries_by_carbon_dioxide_emissions). 

Data are preliminary and subject to change. My goal is to learn more about how to automate my page so the data gets scrapped and updated live. 

***
## ⚙ This project is built using:

- `HTML/CSS`
- [Python](https://docs.python.org/3.8/whatsnew/3.8.html)
     - [BeautifulSoup](https://www.crummy.com/software/BeautifulSoup/bs4/doc/)
     - [Jinja](https://jinja.palletsprojects.com/en/2.11.x/)
     - [Request](https://www.crummy.com/software/BeautifulSoup/bs4/doc/)  
- [Flask](https://flask.palletsprojects.com/en/1.1.x/)
   - [Flask SQLAlchemy](https://flask-sqlalchemy.palletsprojects.com/en/2.x/)

***
## Important: Changes on December 1, 2020

After finalizing the decision on which sites I was going to scrape I was able to:
- Create a py script that when call will start the scraping process, clean the data and organize it in a presentable way before returning it to my import_script.py to create the database.


## Important: Changes on December 5, 2020

- The class to create my database was created to include the attributes that will generate each column


## Important: Changes on December 7, 2020

- The finalization of my import_script.py completed the database creation. 

## Important: Changes on December 9, 2020

- Once my database was functional, the next step was concentrating in my API

- I created a total of 6 routes that will return the data stored in my database illustrated in different formats.

## Important: Changes on November 9, 2020

- My API was launched to the web using Heroku as my deployment Platform.

***
# Preparing for Deployment
1. Create your virtual env and set it up.
2. Freeze your dependencies
3. Set up .gitignore
4. commit to your git repo

### Creating your env
In your project folder:  
1.`python -m venv env`   
2.`source env/bin/activate`  
3. `pip install` all your dependencies (including `gunicorn`)

### Freeze your dependencies

`pip freeze > requirements.txt`

### Set up .gitignore

In your project folder, create a file called `.gitignore`.

sample .gitignore:
```
# General
.DS_Store

# Environments
.env
.venv
env/
venv/
ENV/

# Python
*.pyc

# Jupyter Notebook
.ipynb_checkpoints
```

python full example: https://github.com/github/gitignore/blob/master/Python.gitignore

***
# Deployment

## Deploying to Heroku

1. Sign up for heroku and log in.
2. Create a `Procfile` and `runtime.txt` and commit them.
3. Push to heroku either by using the heroku cli or by adding your github account to heroku and setting the repo through the web interface.

### Creating a `Procfile` 

In order to run our application properly Heroku requires a special file that tells it what to do.

For our project we'll need the following:

```
release: ./import-script.py
worker: gunicorn -w 4 app:app

```

### Creating a `runtime.txt`

This tells heroku which python version to use.

example runtime.txt

```
python-3.8.6
```

### Pushing to heroku

You'll either need to do `git push heroku master` (if you've installed the heroku cli) or `git push origin master` (if you've connected the git repo to heroku).

### Check your url

Visit `https://{your-project-name}.herokuapp.com/`
