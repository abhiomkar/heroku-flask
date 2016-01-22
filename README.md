Flask starter kit for Heroku
============================

Install
-------

 - Install Heroku
 - Install Pip
 - Install virtualenvwrapper
 - Install [pip-save](https://github.com/abhiomkar/pip-save)
 - Install Flask

Setup
-----

 - Clone this starter kit 

        git clone https://github.com/abhiomkar/heroku-flask.git

 - Login to Heroku

        heroku login

 - Create Heroku App

        heroku create

Development
-----------

 - Create Python virtual enviroment using pip-save tool & install all deps

        pip init
        pip install
 
 - Run app locally

        python app.py
        # or
        heroku local
 
 - Hack! Hack!
  

Deploy
------

 - Deploy to Heroku

        git push heroku master

 - You should see a link to your heroku app after successful deploy.

Demo
----

https://heroku-flask.herokuapp.com/
