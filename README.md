# microblog
The first portion of the flask microblog assesment is a simpled helloworld application. When the program is run it will display "Hello World!" on two endpoints, "/" and "/index".
THe second portion 
of the assesment is aimed at teaching you how to use templates to use templates to easily render html.
In using templates you are afforded more options, including conditionals and loops in your html.

The third portion requires the developer to create a config.py with a config class inside to be used later. Also must include a login form class in the forms.py file. The login form needs to have username password and a remeber me as its attributes. Base .html needs to have the anchor tag for the /login endpoint and logic for errors, and the routes.py should be updated with the logic to handle login data

The fourth portion of the flask assessment is centered around databases. First you are given a walkthrough of the creation of databases, and you may use sql migration sql alchemy to update the database. In order to use them you must change your app.__init__.py file and config.py. Add     "SQLALCHEMY_DATABASE_URI = os.environ.get('DATABASE_URL') or \
        'sqlite:///' + os.path.join(basedir, 'app.db')
    SQLALCHEMY_TRACK_MODIFICATIONS = False" to your config.py
    You will also need a models.py file with the following content:"from app import db

class User(db.Model):
    id = db.Column(db.Integer, primary_key=True)
    username = db.Column(db.String(64), index=True, unique=True)
    email = db.Column(db.String(120), index=True, unique=True)
    password_hash = db.Column(db.String(128))

    def __repr__(self):
        return '<User {}>'.format(self.username) 
        
        " and "
        class Post(db.Model):
    id = db.Column(db.Integer, primary_key=True)
    body = db.Column(db.String(140))
    timestamp = db.Column(db.DateTime, index=True, default=datetime.utcnow)
    user_id = db.Column(db.Integer, db.ForeignKey('user.id'))

    def __repr__(self):
        return '<Post {}>'.format(self.body)"

        The two preceding blocks of code set class variables for the User and Post classes, both of which inherit from db model.


Getting started
To get a copy of this project you must clone the repo by running
"git@github.com:wharris64/microblog.git" in your terminal

prerequisites
Pipenv

flask sql alchemy
flask migrate

Installing
to install pip env on your machine
"brew install pipenv"
"pipenv install flask-migrate"
"pipenv install flask-sqlalchemy"


To run the program run 
$: export flask=microblog.py
$: flask run
Then go to "localhost:5000/", "loalhost:5000/index", or hold command and click http://127.0.0.1:5000/ as it appears in the command line below.

Output

* Serving Flask app "microblog.py"
 * Environment: development
 * Debug mode: off
 * Running on http://127.0.0.1:5000/ (Press CTRL+C to quit)
