{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AGI файл – файлов формат на интерфейса на Asterisk Gateway",
  "description":"Научете какво е AGI файлов формат с пример и API, които могат да създават и отварят AGI файлове.",
  "linktitle" : "AGI",
  "menu" : {
    "docs" : {
      "identifier": "programming-agi",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## Какво е AGI файл?

AGI файлът е скриптов файл, използван от системата за телефония с отворен код Asterisk. Той съдържа информация, която може да се използва за автоматизиране на процеси и план за набиране на Asterisk. С помощта на AGI скриптови файлове могат да се установяват връзки с релационни бази данни като PostgreSQL или MySQL. В допълнение, AGI скриптовете могат да се използват и за достъп до други външни ресурси. AGI скриптовете могат да предадат контрола върху диалплана на външен AGI скрипт, което позволява на Asterisk да изпълнява сложни задачи.

## AGI файлов формат - повече информация

AGI скрипт файловете се записват като текстови файлове и могат да се отварят във всеки текстов редактор за извършване на промени.

### Стандартен модел на AGI комуникация

Скриптът AGI зарежда променливите и техните стойности, изпратени му от Asterisk. Общ вид на тези променливи е както следва.

```
agi_request: test.py
agi_channel: Zap/1-1
agi_language: en
agi_callerid:
agi_context: default
agi_extension: 123
agi_priority: 2
```

Тези променливи са последвани от празен ред, изпратен от Asterisk, показващ, че AGI скриптът може да поеме контрола върху диалплана сега.

### Програмен език за AGI скриптови файлове

AGI скриптовете обикновено могат да бъдат написани на Perl, [PHP](/bg/programming/php/), [C](/bg/programming/c/), Pascal или Bourne Shell.

## Препратки

* [Asterisk AGI скрипт](https://www.oreilly.com/library/view/asterisk-the-future/9780596510480/ch09.html)

