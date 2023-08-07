{
  "date" : "2022-09-17",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DISCO File – DISCO Discovery Document File Format",
  "description":"Научете какво е DISCO файл и API, които могат да създават и отварят DISCO файлове.",
  "linktitle" : "DISCO",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-09-17"
}

## Какво е DISCO файл?

DISCO файлът е файлов формат на Microsoft Discovery, който се използва за публикуване и откриване на уеб услуги. Той се съхранява в XML файлов формат и позволява на инструментите за откриване на уеб услуги да намерят или открият един или повече свързани документи за описание на наличните [XML](/bg/web/xml/) услуги. Файлът DISCO съхранява информация като документи за откриване, [XSD](https://docs.fileformat.com/programming/xsd/) схеми и описания на услуги. XML уеб услугите използват тази информация, за да стигнат до наличните XML уеб услуги на даден URL адрес.

## DISCO файлов формат - повече информация

DISCO файловете се записват в XML файлов формат. Microsoft Discovery Tool (DISCO.exe), който идва в комплект със софтуера за разработка на Microsoft ASP.NET, като Microsoft Studio, използва DISCO файловете, за да открие подробностите за XML уеб услугите, изброени в DiscoveryDocument на конкретен URL адрес. Microsoft предостави поддръжка за четене на файлове за откриване в .NET framework.

## Препратки

* [ДИСКО](https://appsource.microsoft.com/en-us/product/office/WA104381894)
* [Откриване на уеб услуги](https://en.wikipedia.org/wiki/Web_Services_Discovery)
* [C# пример за клас DiscoveryClient](https://learn.microsoft.com/en-us/dotnet/api/system.web.services.discovery.discoveryclientprotocol?view=netframework-4.8)

