# microblog
The first portion of the flask microblog assesment is a simpled helloworld application. When the program is run it will display "Hello World!" on two endpoints, "/" and "/index".
THe second portion 
of the assesment is aimed at teaching you how to use templates to use templates to easily render html.
In using templates you are afforded more options, including conditionals and loops in your html.

The third portion requires the developer to create a config.py with a config class inside to be used later. Also must include a login form class in the forms.py file. The login form needs to have username password and a remeber me as its attributes. Base .html needs to have the anchor tag for the /login endpoint and logic for errors, and the routes.py should be updated with the logic to handle login data
Getting started
To get a copy of this project you must clone the repo by running
"git@github.com:wharris64/microblog.git" in your terminal

prerequisites
Pipenv

Installing
to install pip env on your machine
"brew install pipenv"



To run the program run 
$: export flask=microblog.py
$: flask run
Then go to "localhost:5000/", "loalhost:5000/index", or hold command and click http://127.0.0.1:5000/ as it appears in the command line below.

Output

* Serving Flask app "microblog.py"
 * Environment: development
 * Debug mode: off
 * Running on http://127.0.0.1:5000/ (Press CTRL+C to quit)
