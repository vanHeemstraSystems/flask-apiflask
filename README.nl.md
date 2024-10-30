kolf-apiflas

# Kolf APIFlask

> APIFlask is een lichtgewicht Python-web-API-framework gebaseerd op[Kolf](https://github.com/pallets/flask)En[marshmallow-code](https://github.com/marshmallow-code)projecten. Het is gemakkelijk te gebruiken, zeer aanpasbaar, ORM/ODM-agnostisch en 100% compatibel met het Flask-ecosysteem.

[Referenties](./REFERENCES.md)

**Samenvatting**

Na[installatie](./300/100/README.md), voer het uit met:

    $ cd flask_apiflask/src/example
    $ flask run --reload

Of voer het uit in debug-modus:

    $ cd flask_apiflask/src/example
    $ flask run --debug

Bezoek de webpagina op http&#x3A;//localhost:5000 om de startpagina te bekijken:

    {
      "message": "Hello!"
    }

http&#x3A;//localhost:5000

Bezoek nu de interactieve API-documentatie (Swagger UI) op http&#x3A;//localhost:5000/docs:

![image](https://github.com/user-attachments/assets/32bbb227-97fc-4f39-808b-a9f91f917979)

http&#x3A;//localhost:5000/docs

Het automatisch gegenereerde OpenAPI-specificatiebestand is beschikbaar op http&#x3A;//localhost:5000/openapi.json. Je kunt de specificatie ook verkrijgen met[het kolfspecificatiecommando](https://apiflask.com/openapi/#the-flask-spec-command):

    $ flask spec

## 100 - Inleiding

Zien[README.md](./100/README.md)

## 200 - Requirements

Zien[README.md](./200/README.md)

## 300 - Onze applicatie bouwen

Zien[README.md](./300/README.md)

## 400 - Conclusie

Zien[README.md](./400/README.md)
