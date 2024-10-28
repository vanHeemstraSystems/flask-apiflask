# 200 - Example

Create a file called ```app.py``` inside ```flask_apiflask/src/example/``` directory (following a Hatch directory structure):

```
from apiflask import APIFlask, Schema, abort
from apiflask.fields import Integer, String
from apiflask.validators import Length, OneOf

app = APIFlask(__name__)

pets = [
    {'id': 0, 'name': 'Kitty', 'category': 'cat'},
    {'id': 1, 'name': 'Coco', 'category': 'dog'}
]


class PetIn(Schema):
    name = String(required=True, validate=Length(0, 10))
    category = String(required=True, validate=OneOf(['dog', 'cat']))


class PetOut(Schema):
    id = Integer()
    name = String()
    category = String()


@app.get('/')
def say_hello():
    # returning a dict or list equals to use jsonify()
    return {'message': 'Hello!'}


@app.get('/pets/<int:pet_id>')
@app.output(PetOut)
def get_pet(pet_id):
    if pet_id > len(pets) - 1:
        abort(404)
    # you can also return an ORM/ODM model class instance directly
    # APIFlask will serialize the object into JSON format
    return pets[pet_id]


@app.patch('/pets/<int:pet_id>')
@app.input(PetIn(partial=True))  # -> json_data
@app.output(PetOut)
def update_pet(pet_id, json_data):
    # the validated and parsed input data will
    # be injected into the view function as a dict
    if pet_id > len(pets) - 1:
        abort(404)
    for attr, value in json_data.items():
        pets[pet_id][attr] = value
    return pets[pet_id]
```
flask_apiflask/src/example/app.py

Save this as app.py, then run it with:

```
$ cd flask_apiflask/src/example
$ flask run --reload
```

Or run in debug mode:

```
$ cd flask_apiflask/src/example
$ flask run --debug
```

Visit the web page at http://localhost:5000 to see the home page:

```
{
  "message": "Hello!"
}
```
http://localhost:5000

Now visit the interactive API documentation (Swagger UI) at http://localhost:5000/docs:

![image](https://github.com/user-attachments/assets/32bbb227-97fc-4f39-808b-a9f91f917979)

http://localhost:5000/docs

Or you can change the API documentation UI when creating the APIFlask instance with the ```docs_ui``` parameter:

```
...
app = APIFlask(__name__, docs_ui='redoc')
...
```
flask_apiflask/src/example/app.py

Now http://localhost:5000/docs will render the API documentation with Redoc.

Supported ```docs_ui``` values (UI libraries) include:

- ```swagger-ui``` (default value): [Swagger UI](https://github.com/swagger-api/swagger-ui)
- ```redoc```: [Redoc](https://github.com/Redocly/redoc)
- ```elements```: [Elements](https://github.com/stoplightio/elements)
- ```rapidoc```: [RapiDoc](https://github.com/rapi-doc/RapiDoc)
- ```rapipdf```: [RapiPDF](https://github.com/mrin9/RapiPdf)

The auto-generated OpenAPI spec file is available at http://localhost:5000/openapi.json. You can also get the spec with [the flask spec command](https://apiflask.com/openapi/#the-flask-spec-command):

```
$ flask spec
```

For some complete examples, see [examples](https://github.com/apiflask/apiflask/tree/main/examples)
