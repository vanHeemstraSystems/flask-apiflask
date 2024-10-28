flask-apiflask
# Flask APIFlask

> APIFlask is a lightweight Python web API framework based on [Flask](https://github.com/pallets/flask) and [marshmallow-code](https://github.com/marshmallow-code) projects. It's easy to use, highly customizable, ORM/ODM-agnostic, and 100% compatible with the Flask ecosystem.

[References](./REFERENCES.md)

**Executive Summary**

After [installation](./300/100/README.md), run it with:

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

The auto-generated OpenAPI spec file is available at http://localhost:5000/openapi.json. You can also get the spec with [the flask spec command](https://apiflask.com/openapi/#the-flask-spec-command):

```
$ flask spec
```

## 100 - Introduction

See [README.md](./100/README.md)

## 200 - Requirements

See [README.md](./200/README.md)

## 300 - Building Our Application

See [README.md](./300/README.md)

## 400 - Conclusion

See [README.md](./400/README.md)
