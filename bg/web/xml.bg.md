{
  "date" : "2019-10-11",
  "keywords" :["xml", "Файл", "Разширение", "Файлов формат", "Разширение на файл", "разширяем език за маркиране"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XML файлов формат",
  "description":"Научете повече за XML файловия формат и API, които могат да създават и отварят XML файлове.",
  "linktitle" : "XML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Какво е XML файл?

XML означава Extensible Markup Language, който е подобен на **[HTML](/bg/web/html/)**, но е различен в използването на тагове за дефиниране на обекти. Цялата идея зад създаването на XML файлов формат беше да съхранява и транспортира данни, без да зависи от софтуерни или хардуерни инструменти. Популярността му се дължи на това, че е както човек, така и машинно четим. Това му позволява да създава общи протоколи за данни под формата на обекти, които да се съхраняват и споделят в мрежа като World Wide Web (WWW). „X“ в XML е за разширяем, което означава, че езикът може да бъде разширен до произволен брой символи според изискванията на потребителя. Именно за тези функции го използват много стандартни файлови формати като Microsoft Open XML, LibreOffice OpenDocument, **[XHTML](/bg/web/xhtml/)** и **[SVG](/bg/page-description-language/svg/)**.

## XML файлов формат

XML файловият формат се основава на XML Document Object Model (DOM), който е API за програмиране за HTML и XML документи. XML DOM дефинира стандартен метод за достъп и манипулиране на елементите на XML документа. Той прави изглед на дървовидна структура на XML документ, който може да се използва за достъп до всички елементи през DOM дървото. Съществуващите елементи могат да се променят/изтриват, както и да се създават нови елементи в XML дървото. Всеки елемент от XML документ се нарича възел. XML DOM е както е показано на следното изображение.

{{< figure src="../XML DOM.png" alt="XML DOM" >}}

### Универсален подход на XML

Силата на XML го прави универсален език за комуникация на данни по мрежата, като прави транспорта на данни и промените в платформата опростени. Това също гарантира възможен обмен на данни между несъвместими системи чрез съхраняване на данни в обикновен текстов формат. HTML е за представяне на данни в мрежата, докато XML е за обмен на данни. Двойките тагове за маркиране, използвани в XML, дефинират ключовите елементи на структурата, които да се използват от приложения за четене.

## Пример за XML

Следното е опростен пример за CD каталог, където всеки запис съдържа информация за компактдискове като изпълнител, държава, компания, цена и година на производство.

```
<CATALOG>
  <CD>
    <TITLE>Empire Burlesque</TITLE>
    <ARTIST>Bob Dylan</ARTIST>
    <COUNTRY>USA</COUNTRY>
    <COMPANY>Columbia</COMPANY>
    <PRICE>10.90</PRICE>
    <YEAR>1985</YEAR>
  </CD>
  <CD>
    <TITLE>Hide your heart</TITLE>
    <ARTIST>Bonnie Tyler</ARTIST>
    <COUNTRY>UK</COUNTRY>
    <COMPANY>CBS Records</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1988</YEAR>
  </CD>
  <CD>
    <TITLE>Greatest Hits</TITLE>
    <ARTIST>Dolly Parton</ARTIST>
    <COUNTRY>USA</COUNTRY>
    <COMPANY>RCA</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1982</YEAR>
  </CD>
  <CD>
    <TITLE>Still got the blues</TITLE>
    <ARTIST>Gary Moore</ARTIST>
    <COUNTRY>UK</COUNTRY>
    <COMPANY>Virgin records</COMPANY>
    <PRICE>10.20</PRICE>
    <YEAR>1990</YEAR>
  </CD>
  <CD>
    <TITLE>Eros</TITLE>
    <ARTIST>Eros Ramazzotti</ARTIST>
    <COUNTRY>EU</COUNTRY>
    <COMPANY>BMG</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1997</YEAR>
  </CD>
  <CD>
</CATALOG>
```

## Препратки

* [XML – от Wikipedia](https://en.wikipedia.org/wiki/XML)

