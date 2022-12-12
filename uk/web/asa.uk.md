{
  "date" : "2021-12-09",
  "keywords" :[ "asa", ".asa", "формат файлу", "тип файлу", "що таке файл .asa" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASA - файл конфігурації ASP",
  "description" :"Дізнайтеся, що таке файл ASA та API, які можуть створювати та відкривати файли ASA.",
  "linktitle" : "ASA",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-12-09"
}

## Що таке файл ASA?

Файл ASA — це файл конфігурації, створений для проектів [ASP](/uk/web/asp/)/ASP.NET. Він містить оголошення змінних, містить і функції, які призначені для доступу на глобальному рівні в програмі. Усі сторінки в проекті можуть отримати доступ до цих змінних і функцій, таким чином уникаючи вимоги їх переписування. Одним із таких прикладів є сторінка Global.asa, яка зберігається в кореневому каталозі, щоб бути доступною для інших сторінок веб-сайту ASP. Файли Global.asa необов’язкові, але якщо вони використовуються, кожна програма може мати лише один файл Global.asa.

## Формат файлу ASA – Додаткова інформація

Файли ASA є простими текстовими файлами з такою інформацією.

* Події програми
* Події сесії
* \<object> декларації
* Оголошення TypeLibrary
* директива #include

## Приклад файлу ASA

Файл Global.asa може виглядати приблизно так.

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

## Список літератури

* [Файл ASP Global.asa - w3schools](https://www.w3schools.com/asp/asp_globalasa.asp)

