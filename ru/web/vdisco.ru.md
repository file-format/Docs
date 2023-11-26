{
  "date" : "2023-01-29",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Файл VDISCO — формат файла документа DISCO Dynamic Discovery",
  "description":"Подробнее о том, что такое файл VDISCO?",
  "linktitle" : "VDISCO",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2023-01-29"
}

## .VDISCO вариант №

Файл VDISCO — это файл обнаружения, используемый Microsoft Visual Studio в своих веб-службах. Он предоставляет информацию о доступных веб-службах, такую как их URL-адреса, пространства имен и методы. Файл VDISCO аналогичен формату файла [DISCO](/ru/web/disco/), но создается во время выполнения. Он хранится в приложении веб-службы и используется Visual Studio для динамического обнаружения и использования веб-служб в проекте. Файлы VDISCO используются в сочетании с файлом [.asmx](/ru/web/asmx/), который содержит фактический код веб-службы.

Вы можете открыть файл VDISCO в любом текстовом редакторе, например Microsoft Notepad, Github Atom и Apple TextEdit. Его также можно открыть с помощью Microsoft Visual Studio 2012 и более поздних версий для работы с ним.

## Формат файла VDISCO

Файл VDISCO сохраняется и размещается в формате файла [XML](/ru/web/xml/), который является универсальным форматом для составления и публикации данных. Он содержит URL-адрес службы, пространства имен и методы в стандартных тегах XML, где каждый тег содержит соответствующее значение своей информации.

## Рекомендации

* [DISCO](https://appsource.microsoft.com/en-us/product/office/WA104381894)
* [Обнаружение веб-служб](https://en.wikipedia.org/wiki/Web_Services_Discovery)
* [Пример класса DiscoveryClient на C#] (https://learn.microsoft.com/en-us/dotnet/api/system.web.services.discovery.discoveryclientprotocol?view=netframework-4.8)

