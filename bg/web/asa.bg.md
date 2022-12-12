{
  "date" : "2021-12-09",
  "keywords" :[ "asa", ".asa", "файлов формат", "тип файл", "какво е .asa файл" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASA - ASP конфигурационен файл",
  "description" :"Научете какво е ASA файл и API, които могат да създават и отварят ASA файлове.",
  "linktitle" : "ASA",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-12-09"
}

## Какво е ASA файл?

ASA файлът е конфигурационен файл, създаден за [ASP](/bg/web/asp/)/ASP.NET проекти. Той съдържа декларации на променливи, съдържа и функции, които са предназначени да бъдат достъпни на глобално ниво в приложението. Всички страници в проекта имат достъп до тези променливи и функции, като по този начин се избягва изискването за тяхното пренаписване. Един такъв пример е страницата Global.asa, която се съхранява в главната директория, за да бъде достъпна от други страници на уебсайт на ASP. Файловете Global.asa не са задължителни, но ако се използват, всяко приложение може да има само един файл Global.asa.

## ASA файлов формат - повече информация

ASA файловете са обикновени текстови файлове със следната информация.

* Събития на приложението
* Сесионни събития
* \<object> декларации
* Декларации на TypeLibrary
* директивата #include

## Пример за ASA файл

Файлът Global.asa може да изглежда по следния начин.

```
<script language="vbscript" runat="server">

sub Application_OnStart
'some code
end sub

sub Application_OnEnd
'some code
end sub

sub Session_OnStart
'some code
end sub

sub Session_OnEnd
'some code
end sub

</script>
```

## Препратки

* [Файл ASP Global.asa - w3schools](https://www.w3schools.com/asp/asp_globalasa.asp)

