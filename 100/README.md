# 100 - Introduction

APIFlask is a lightweight Python web API framework based on [Flask](https://github.com/pallets/flask) and [marshmallow-code](https://github.com/marshmallow-code) projects. It's easy to use, highly customizable, ORM/ODM-agnostic, and 100% compatible with the Flask ecosystem.

With APIFlask, you will have:

- More sugars for view function (```@app.input()```, ```@app.output()```, ```@app.get()```, ```@app.post()``` and more)
- Automatic request validation and deserialization
- Automatic response formatting and serialization
- Automatic [OpenAPI Specification](https://github.com/OAI/OpenAPI-Specification) (OAS, formerly Swagger Specification) document generation
- Automatic interactive API documentation
- API authentication support (with [Flask-HTTPAuth](https://github.com/miguelgrinberg/flask-httpauth))
- Automatic JSON response for HTTP errors
