# ECE444 F2021 Lab 6

This repository is based off of: https://github.com/mjhea0/flaskr-tdd

This has been deployed on heroku: https://eerie-coffin-73752.herokuapp.com/

# Group Project Test Cases
Cases added to group project:
https://github.com/ECE444-2021Fall/project1-education-pathways-group-7-apollo/blob/feature/better-course-discovery/flask_app/test/api_test.py#L24-L88

# Pros & Cons of TDD
This section will describe the pros and cons of test driven development (TDD)

## Pros of TDD
- Can quickly find errors while developing
- Easy to maintain as when changes are made can easily run the unit tests
- Easy debug/location of bugs because you know which test cases are failing

## Cons of TDD
- Slow to do, need to write unit tests and regression tests for every scenario still
- Doesn't always specify exactly what the bug is, still need to determine from within a test what the bug is (if it's a big test)
- Need to maintain tests if code is changed

# Setup

Setup virtual environment: 
py -3.9 -m venv env  
.\env\Scripts\activate  

Install Packages:
pip install flask==1.1.2  
pip install pytest==6.1.1
pip install gunicorn==20.0.4
pip install Flask-SQLAlchemy==2.5.1
pip install flake8==3.8.4
pip install black==20.8b1

Add heroku postgres:
heroku addons:create heroku-postgresql:hobby-dev

Set environment variable:
$Env:FLASK_APP="project/app.py"

Run app_test:
py -3.9 -m pytest

Run flask app:
py -3.9 -m flask run

Push to heroku and create database:
git push -f heroku master
heroku run python create_db.py
