matraz-apiflask

# Matraz APIFlasco

> APIFlask es un marco API web ligero de Python basado en[Matraz](https://github.com/pallets/flask)y[código de malvavisco](https://github.com/marshmallow-code) projects. It's easy to use, highly customizable, ORM/ODM-agnostic, and 100% compatible with the Flask ecosystem.

[Referencias](./REFERENCES.md)

**Resumen ejecutivo**

Después[instalación](./300/100/README.md), ejecútelo con:

    $ cd flask_apiflask/src/example
    $ flask run --reload

O ejecutar en modo de depuración:

    $ cd flask_apiflask/src/example
    $ flask run --debug

Visite la página web en http&#x3A;//localhost:5000 para ver la página de inicio:

    {
      "message": "Hello!"
    }

http&#x3A;//localhost:5000

Ahora visite la documentación de la API interactiva (Swagger UI) en http&#x3A;//localhost:5000/docs:

![image](https://github.com/user-attachments/assets/32bbb227-97fc-4f39-808b-a9f91f917979)

http&#x3A;//localhost:5000/docs

El archivo de especificaciones OpenAPI generado automáticamente está disponible en http&#x3A;//localhost:5000/openapi.json. También puedes obtener las especificaciones con[el comando de especificación del matraz](https://apiflask.com/openapi/#the-flask-spec-command):

    $ flask spec

## 100 - Introducción

Ver[README.md](./100/README.md)

## 200 - Requisitos

Ver[README.md](./200/README.md)

## 300 - Construyendo nuestra aplicación

See [README.md](./300/README.md)

## 400 - Conclusión

Ver[README.md](./400/README.md)
