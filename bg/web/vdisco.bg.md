{
  "date" : "2023-01-29",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VDISCO File – DISCO Dynamic Discovery Document File Format",
  "description":"Научете какво е VDISCO файл?",
  "linktitle" : "VDISCO",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2023-01-29"
}

## Какво е VDISCO файл?

VDISCO файл е файл за откриване, използван от Microsoft Visual Studio в неговите уеб услуги. Той предоставя информация за наличните уеб услуги, като техните URL адреси, пространства от имена и методи. Файлът VDISCO е подобен на файловия формат [DISCO](/bg/web/disco/), но се генерира по време на изпълнение. Той се съхранява в приложението за уеб услуга и се използва от Visual Studio за динамично откриване и използване на уеб услуги в проект. Файловете VDISCO се използват в комбинация с файла [.asmx](/bg/web/asmx/), който съдържа действителния код на уеб услугата.

Можете да отворите VDISCO файл във всеки текстов редактор като Microsoft Notepad, Github Atom и Apple TextEdit. Може да се отвори и с Microsoft Visual Studio 2012 и по-нови за работа с него.

## Файлов формат VDISCO

VDISCO файл се записва и хоства във файлов формат [XML](/bg/web/xml/), който е универсален формат за съставяне и публикуване на данни. Той съдържа URL адреса на услугата, пространства от имена и методи в стандартни XML тагове, където всеки таг съдържа съответната стойност на своята информация.

## Препратки

* [ДИСКО](https://appsource.microsoft.com/en-us/product/office/WA104381894)
* [Откриване на уеб услуги](https://en.wikipedia.org/wiki/Web_Services_Discovery)
* [C# пример за клас DiscoveryClient](https://learn.microsoft.com/en-us/dotnet/api/system.web.services.discovery.discoveryclientprotocol?view=netframework-4.8)

