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

Deploy to Dokku
---------------

	- [Install](http://dokku.viewdocs.io/dokku/installation/) dokku on Host (Amazon EC2)

	- Create a dokku app on Host (Amazon EC2)
	
		dokku apps:create dokku-flask

	- Upload your public ssh key to your host (Amazon EC2). Execute this command on your local machine.

		cat ~/.ssh/id_rsa.pub | ssh abhinay@abhiomkar.in "sudo sshcommand acl-add dokku [description]"


		- "abhinay" is the user on your host with sudo permissions
		- "abhiomkar.in" is the hostname where dokku was installed
		- ~/.ssh/id_rsa.pub is your local machine's public ssh key

	- Clone this repository on your local machine

		git clone https://github.com/abhiomkar/heroku-flask.git

	- Add remote and push it to dokku

		cd heroku-flask
		git remote add dokku dokku@abhiomkar.in:dokku-flask
		git push dokku master

		- where dokku-flask is the name of your application which you'd created on your host.

	- You should see the URL to access your application after successful deployment. :-)

Demo
----

https://heroku-flask.herokuapp.com/
