# ECE444 F2021 Lab 6

This repository is based off of: https://github.com/mjhea0/flaskr-tdd

This has been deployed on heroku: https://eerie-coffin-73752.herokuapp.com/


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