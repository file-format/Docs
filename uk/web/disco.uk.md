{
  "date" : "2022-09-17",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Файл DISCO - формат файлу документа DISCO Discovery",
  "description":"Дізнайтеся, що таке файл DISCO та API, які можуть створювати та відкривати файли DISCO.",
  "linktitle" : "DISCO",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-09-17"
}

## Що таке файл DISCO?

Файл DISCO — це формат файлу Microsoft Discovery, який використовується для публікації та виявлення веб-служб. Він зберігається у форматі файлу XML і дозволяє інструментам виявлення веб-служб знаходити або відкривати один або кілька пов’язаних документів для опису доступних служб [XML](/uk/web/xml/). У файлі DISCO зберігається така інформація, як документи виявлення, схеми [XSD](https://docs.fileformat.com/programming/xsd/) і описи послуг. Веб-служби XML використовують цю інформацію, щоб отримати доступ до доступних веб-служб XML за вказаною URL-адресою.

## Формат файлу DISCO - Додаткова інформація

Файли DISCO зберігаються у форматі XML. Інструмент Microsoft Discovery (DISCO.exe), який постачається разом із програмним забезпеченням розробки Microsoft ASP.NET, таким як Microsoft Studio, використовує файли DISCO для виявлення подробиць про веб-служби XML, перелічені в DiscoveryDocument за певною URL-адресою. Microsoft надала підтримку читання файлів виявлення в .NET framework.

## Список літератури

* [DISCO](https://appsource.microsoft.com/en-us/product/office/WA104381894?tab=Overview)
* [Виявлення веб-служб](https://en.wikipedia.org/wiki/Web_Services_Discovery)
* [Приклад C# класу DiscoveryClient](https://learn.microsoft.com/en-us/dotnet/api/system.web.services.discovery.discoveryclientprotocol?view=netframework-4.8)

