{
  "date" : "2022-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CON File – Concept Application Source File Format",
  "description" :"Научете какво е CON файл и API, които могат да създават и отварят CON файлове.",
  "linktitle" : "CON",
  "menu" : {
    "docs" : {
      "identifier":"web-con",
      "parent" : "web"
}
},
  "lastmod" : "2022-08-24"
}

## Какво е CON файл?

CON файлът е файл с изходен код за приложение, разработено за **Concept Application Server**. Използва се за писане на приложения за обмен на данни между сървъра и потребителя. CON файловете, хоствани на сървъра, са достъпни с уеб браузър, при условие че Concept Client е инсталиран от страна на потребителя. Концепция Сървърът на приложения е уеб сървър с език за програмиране в малък мащаб, който може да има [SQL](/bg/database/sql/) поднабор на базата данни (TinDB).

CON файловете могат да се отварят/изпълняват с RadGs Concept Application Server.

## CON файлов формат - повече информация

CON файловете се хостват на сървъра и са достъпни чрез уеб браузър на потребителска машина. Концептуални [URL адреси](/bg/web/url/) са различни от нормалните HTTP URL адреси и започват с **concept://**.

### Пример за URL адрес на CON файл

CON файл, хостван на Concept Application Server, може да бъде достъпен чрез уеб браузър с помощта на URL адреси като:

```
concept://domain.server.com/web_application/main.con.
```
## Препратки

* [Concept Application Server](https://github.com/Devronium/ConceptApplicationServer)

