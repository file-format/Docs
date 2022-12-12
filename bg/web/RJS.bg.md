{
  "date" : "2021-05-24",
  "keywords" :["rjs", "Файл", "Разширение", "Файлов формат", "Файлово разширение", "RJS", "Ruby Javascript файл"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RJS - Ruby Javascript файл",
  "description":"Научете какво е RJS файлов формат и API, които могат да създават и отварят RJS файлове.",
  "linktitle" : "RJS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## Какво е RJS файл?

Файл с разширение .rjs е комбинация от Ruby код и JavsScript, която позволява на разработчиците на Rails да използват Ruby за създаване на динамичен JavaScript код. Ruby кодът е вграден в Java функциите и се компилира на уеб сървъра, който изисква Ruby engine да работи на сървъра. RJS е подобен на [RHTML](/bg/web/rhtml/); единствената разлика е, че страничният съдържа Ruby код в [HTML](/bg/web/html/), докато съдържа Ruby код във функциите на Javascript.

## RJS файлов формат

RJS файловете са кодирани в обикновен текст като всеки друг скриптов или програмен език. Когато такава страница бъде поискана от клиента, Ruby кодът се изпълнява на сървъра и само HTML и Javascript кодът се връщат към браузъра на клиента. Синтаксисът на RJS файла е подобен на този на комбинация от синтаксис на Ruby и JavaScript, така че само кодът на Ruby е вграден във функциите на JavaScript.

### Пример за RJS

Следващият пример показва прост Ruby код независимо и след това вграден в JavaScript функция.

```Ruby
### Default Ruby Functions

def foo
  "bar"
end
```

```JavaScript
# JS style which looks like JS

foo = -> { return "bar" }
```
и следното е RubyJS:
```Ruby
# here you go!

foo = -> { "bar" }
```
## Препратки

* [RJS](https://github.com/makevoid/rjs)

