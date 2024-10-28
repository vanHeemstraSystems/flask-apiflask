# 400 - Relationship with marshmallow

APIFlask accepts marshmallow schema as data schema, uses webargs to validate the request data against the schema, and uses apispec to generate the OpenAPI representation from the schema.

You can build marshmallow schemas just like before, but APIFlask also exposes some marshmallow APIs for convenience:

- ```apiflask.Schema```: The base marshmallow schema class.
- ```apiflask.fields```: The marshmallow fields, contain the fields from both marshmallow and Flask-Marshmallow. Beware that the aliases (```Url```, ```Str```, ```Int```, ```Bool```, etc.) were removed.
- ```apiflask.validators```: The marshmallow validators.

```
from apiflask import Schema
from apiflask.fields import Integer, String
from apiflask.validators import Length, OneOf
from marshmallow import pre_load, post_dump, ValidationError
...
```
flask_apiflask/src/example/app.py