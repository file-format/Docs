{
  "date" : "2019-10-11",
  "keywords" :[ "mhtml", "mhtml файл", "mhtml файлов формат", "mhtml тип файл", "файл", "тип", "какво е mhtml файл" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MHTML - MIME HTML файл",
  "description":"Научете за файловия формат MHTML и API, които могат да създават и отварят MHTML файлове.",
  "linktitle" : "MHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Какво е MHTML файл?

Файловете с разширение MHTML представляват архивен формат на уеб страница, който може да бъде създаден от множество различни приложения. Форматът е известен като архивен формат, защото записва уеб **[HTML](/bg/web/html/)** кода и свързаните ресурси в един файл. Тези ресурси включват всичко, свързано с уеб страницата, като изображения, аплети, анимации, аудио файлове и т.н. MHTML файловете могат да се отварят в различни приложения като Internet Explorer и Microsoft Word. Microsoft Windows използва MHTML файлов формат за запис на сценарии на проблеми, наблюдавани по време на използването на всяко приложение в Windows, което повдига проблеми. Файловият формат MHTML кодира съдържанието на страницата подобно на спецификациите, дефинирани в message/rfc822, което е спецификации, свързани с имейл с обикновен текст. Действителните спецификации на формата са описани подробно в [RFC 2557](https://tools.ietf.org/html/rfc2557).

## MHTML файлов формат

MHTML е известен също като MIME капсулиране на съвкупни HTML документи заради способността си да кодира HTML уеб страници заедно със своите ресурси в един уеб архив. Съгласно спецификациите на RFC 2557, обобщеният документ е MIME-кодирано съобщение, което съдържа основен ресурс (обект), както и други ресурси, свързани с него чрез URI. Такива други ресурси могат да бъдат представяне на вградени картини, таблици със стилове, аплети и т.н. В допълнение, те могат да бъдат основата на други мултимедийни документи. Пълните спецификации на документа за файлов формат MHTML са описани подробно в [RFC 2557](https://tools.ietf.org/html/rfc2557) и трябва да се използват за всякакъв вид разработка на приложения за четене/запис на този файлов формат. Стандартът уточнява, че частите на тялото, които трябва да бъдат посочени, могат да бъдат идентифицирани или чрез Content-ID, или чрез Content-Location.

### Заглавки на MIME съдържание

Заглавка на MIME съдържание, Content-Location, е дефинирана за разрешаване на URI препратки към ресурси в други части на тялото. Тази заглавка може да се появи във всяко заглавие на съобщение или съдържание.

### Заглавка на местоположението на съдържанието

Местоположението на съдържанието е представяне на URI, което обозначава съдържанието на част от тялото, където е поставено. Стойността му може да бъде абсолютен или относителен URI. Може да се използва за етикетиране на ресурс, който не може да се извлече от някои или всички получатели на съобщение. Едно съобщение може да има само една заглавка на местоположението на съдържанието. Пример за многочастна/свързана структура, съдържаща части от тялото с етикети Content-Location и Content-ID:

```
Content-Type: multipart/related; boundary#"boundary-example";
                    type#"text/html"

      --boundary-example

      Content-Type: text/html; charset#"US-ASCII"

      ... ... <IMG SRC#"fiction1/fiction2"> ... ...
      ... ... <IMG SRC#"cid:97116092811xyz@foo.bar.net"> ... ...

      --boundary-example
      Content-Type: image/gif
      Content-ID: <97116092511xyz@foo.bar.net>
      Content-Location: fiction1/fiction2

      --boundary-example
      Content-Type: image/gif
      Content-ID: <97116092811xyz@foo.bar.net>
      Content-Location: fiction1/fiction3

      --boundary-example--
```

### URI на MHTML агрегати

URI на MHTML агрегата е различен от този на неговия основен URI. Полето за заглавка на местоположението на съдържанието трябва да се прилага за цялата съвкупност, ако се използва в заглавието на съставно/свързано заглавие. По същия начин, наборът от извлечени ресурси може да бъде различен от набора от ресурси, извлечени с помощта на Content-Locations на неговите части, когато URI, отнасящ се до MHTML агрегата, се използва за извличане на този агрегат. Например, извличането на MHTML агрегат може да върне стара версия, докато извличането на основния URI и неговите вградени свързани обекти може да върне по-нова версия.

## Препратки

* [MIME капсулиране на сборни документи - RFC 2557](https://tools.ietf.org/html/rfc2557)
* [MHTML файлов формат - от Wikipedia](https://en.wikipedia.org/wiki/MHTML)
