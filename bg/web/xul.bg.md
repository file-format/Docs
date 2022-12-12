{
  "date" : "2021-05-24",
  "keywords" :["xul", "Файл", "Разширение", "Файлов формат", "Разширение на файл", "Език на потребителския интерфейс на XML"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XUL - езиков файл на XML потребителски интерфейс",
  "description":"Научете за файловия формат XUL и API, които могат да създават и отварят XUL файлове.",
  "linktitle" : "XUL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## Какво е XUL файл?

Файл с разширение .xul ([XUL](https://wiki.mozilla.org/XUL:Home_Page) означава XML потребителски интерфейсен език) е базиран на [XML](/bg/web/xml/) езиков файл за маркиране за създаване на потребителски интерфейси. Той е разработен от Mozilla за разработчици за създаване на елементи на графичен потребителски интерфейс, подобни на други езици за маркиране, използвани за създаване на уеб страници. XUL се използва широко от Mozilla в нейния браузър Firefox, където използва кодовата база на Mozilla. XUL изобразяването се извършва с помощта на
[Gecko engine](https://en.wikipedia.org/wiki/Gecko_(software)). Разклоненията на Firefox като Pale Moon, Basilisk и Waterfox поддържат поддръжка за XUL добавки. XUL файловете се идентифицират с MIME тип: application/vnd.mozilla.xul+xml.

## XUL файлов формат

XUL файловете са написани в обикновен текст въз основа на XML файлов формат и се изобразяват с помощта на Gecko двигателя. Трите основни части на XUL структурата са:

* `Съдържание` - Това включва декларациите на прозореца и елементите на потребителския интерфейс, съдържащи се в тях.
* `Кожа` - Включва всички стилови таблици, изображения и други файлове, свързани с теми. Появата на прозорец е описана в листовете със стилове.
* `Locale` - Текстът, показван в рамките на прозорец, се съхранява отделно и множество набори от езикови файлове могат да се използват от потребителите.

### Пример за XUL

Следващият пример създава три бутона, които са подредени един върху друг във вертикална посока.

```
<?xml version="1.0"?>
<?xml-stylesheet href="chrome://global/skin/" type="text/css"?>

<window id="vbox example" title="Example 3...."
xmlns="http://www.mozilla.org/keymaster/gatekeeper/there.is.only.xul">
  <layout>
    <button id="yes1" label="Yes"/>
    <button id="no1" label="No"/>
    <button id="maybe1" label="Maybe"/>
  </layout>
</window>
```

## Препратки

* [XUL – от Wikipedia](https://en.wikipedia.org/wiki/XUL)
* [XUL архивирана документация - от Mozilla](https://wiki.mozilla.org/XUL:Home_Page)

