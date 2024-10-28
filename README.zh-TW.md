燒瓶-apiflask

# Flask APIFlask

> APIFlask是一個基於Python的輕量級Web API框架[燒瓶](https://github.com/pallets/flask)和[棉花糖代碼](https://github.com/marshmallow-code)專案.它易於使用、高度可自訂、與 ORM/ODM 無關，並且與 Flask 生態系統 100% 相容。

[參考](./REFERENCES.md)

**執行摘要**

運行它：

    $ cd flask_apiflask/src/example
    $ flask run --reload

或在調試模式下運行：

    $ cd flask_apiflask/src/example
    $ flask run --debug

造訪http&#x3A;//localhost:5000即可看到首頁：

    {
      "message": "Hello!"
    }

http&#x3A;//本地主機:5000

現在存取互動式 API 文件 (Swagger UI)：http&#x3A;//localhost:5000/docs：

![image](https://github.com/user-attachments/assets/32bbb227-97fc-4f39-808b-a9f91f917979)

http&#x3A;//localhost:5000/docs

自動產生的 OpenAPI 規範檔案位於 http&#x3A;//localhost:5000/openapi.json。您也可以透過以下方式取得規格[燒瓶規格指令](https://apiflask.com/openapi/#the-flask-spec-command):

    $ flask spec

## 100 - 簡介

看[README.md](./100/README.md)

## 200 - 要求

看[README.md](./200/README.md)

## 300 - 建立我們的應用程式

看[README.md](./300/README.md)

## 400 - 結論

看[README.md](./400/README.md)
