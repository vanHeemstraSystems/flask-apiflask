# 300 - Relationship with Flask

APIFlask is a thin wrapper on top of Flask. You only need to remember the following differences (see [Migrating from Flask](https://apiflask.com/migrations/flask/) for more details):

- When creating an application instance, use ```APIFlask``` instead of ```Flask```.
- When creating a blueprint instance, use ```APIBlueprint``` instead of ```Blueprint```.
- The ```abort()``` function from APIFlask (```apiflask.abort```) returns JSON error response.

For a minimal Flask application:

```
from flask import Flask, request
from markupsafe import escape

app = Flask(__name__)

@app.route('/')
def hello():
    name = request.args.get('name', 'Human')
    return f'Hello, {escape(name)}'
```
flask_apiflask/src/example/app.py

Now change to APIFlask:

```
from apiflask import APIFlask  # step one
from flask import request
from markupsafe import escape

app = APIFlask(__name__)  # step two

@app.route('/')
def hello():
    name = request.args.get('name', 'Human')
    return f'Hello, {escape(name)}'
```
flask_apiflask/src/example/app.py

In a word, to make Web API development in Flask more easily, APIFlask provides ```APIFlask``` and ```APIBlueprint``` to extend Flask's ```Flask``` and ```Blueprint``` objects and it also ships with some helpful utilities. Other than that, you are actually using Flask.