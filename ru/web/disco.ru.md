{
  "date" : "2022-09-17",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Файл DISCO — формат файла документа DISCO Discovery",
  "description":"Узнайте, что такое файл DISCO и API, которые могут создавать и открывать файлы DISCO.",
  "linktitle" : "DISCO",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-09-17"
}

## .DISCO вариант №

Файл DISCO — это формат файла Microsoft Discovery, который используется для публикации и обнаружения веб-служб. Он хранится в формате файла XML и позволяет инструментам обнаружения веб-служб находить или обнаруживать один или несколько связанных документов для описания доступных служб [XML](/ru/web/xml/). В файле DISCO хранится такая информация, как документы обнаружения, схемы [XSD](/programming/xsd/) и описания служб. Веб-службы XML используют эту информацию для доступа к доступным веб-службам XML по заданному URL-адресу.

## Формат файла DISCO — дополнительная информация

Файлы DISCO сохраняются в формате XML. Инструмент обнаружения Microsoft (DISCO.exe), поставляемый в комплекте с программным обеспечением для разработки Microsoft ASP.NET, таким как Microsoft Studio, использует файлы DISCO для обнаружения сведений о веб-службах XML, перечисленных в DiscoveryDocument по определенному URL-адресу. Microsoft предоставила поддержку чтения файлов обнаружения в .NET framework.

## использованная литература

* [ДИСКО](https://appsource.microsoft.com/en-us/product/office/WA104381894)
* [Обнаружение веб-служб](https://en.wikipedia.org/wiki/Web_Services_Discovery)
* [Пример C# класса DiscoveryClient](https://learn.microsoft.com/en-us/dotnet/api/system.web.services.discovery.discoveryclientprotocol?view=netframework-4.8)

