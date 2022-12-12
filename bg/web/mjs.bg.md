{
  "date" : "2021-07-20",
  "keywords" :["MJS", "Файл", "Разширение", "Файлов формат", "Файлово разширение", "Node.js ES модулен файл"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MJS – Node.js ES модул Javascript файл",
  "description" :"Научете какво е MJS файл и API, които могат да създават и отварят MJS файл.",
  "linktitle" : "MJS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-20"
}

## Какво е MJS файл?

Файл с разширение .mjs е файл с изходен код на JavaScript, който се използва като ECMA модул (ECMAScript модул) в приложения Node.js. Модулната система natvie на Node.js е CommonJS, която се използва за разделяне на кода в различни файлове, за да се поддържа [JS](/bg/web/js/) кодът организиран. MJS е единственият начин, използван от Node.js за идентифициране дали модулът е CommonJS или ES6. ECMAScript модулите са стандартна форма за опаковане на JavaScript код за повторна употреба. MJS файловете могат да се отварят в текстови редактори като Atom, Vim, Apple xCode, Microsoft Visual Studio и Notepad.

## MJS файлов формат - повече информация

MJS файловете се записват на диск като обикновен текстов формат в синтаксиса на JavaScript. Те могат да бъдат отворени във всеки текстов редактор и са четими от хора. От 2018 г. почти всички основни браузъри вече поддържат ES модули.

## Разлики между ES модулите и CommonJS

И така, какво прави MJS файловете различни от обикновените JS файлове? Разликата между ES модулите и CommonJS може да бъде обобщена, както следва:

* Без изискване, износ или module.exports
* Няма \__име на файл или \__dirname
* Няма зареждане на JSON модул
* Няма зареждане на собствен модул
* Няма изискване.разрешаване
* Няма NODE_PATH
* Без изискване на разширения
* Няма require.cache

## Препратки

* [Node.js ESM](https://nodejs.org/docs/latest/api/esm.html)
* [Разлика между JS и MJS](https://nodejs.org/docs/latest/api/esm.html#esm_differences_between_es_modules_and_commonjs)

