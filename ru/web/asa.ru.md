{
  "date" : "2021-12-09",
  "keywords" :[ "asa", ".asa", "формат файла", "тип файла", "что такое файл .asa" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASA — файл конфигурации ASP",
  "description" :"Узнайте, что такое файл ASA и API, которые могут создавать и открывать файлы ASA.",
  "linktitle" : "ASA",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-12-09"
}

## .ASA вариант №

Файл ASA — это файл конфигурации, созданный для проектов [ASP](/ru/web/asp/)/ASP.NET. Он содержит объявления переменных, содержит и функции, которые должны быть доступны на глобальном уровне в приложении. Все страницы в проекте могут получить доступ к этим переменным и функциям, что позволяет избежать необходимости их перезаписи. Одним из таких примеров является страница Global.asa, которая хранится в корневом каталоге и доступна для других страниц веб-сайта ASP. Файлы Global.asa необязательны, но если они используются, каждое приложение может иметь только один файл Global.asa.

## Формат файла ASA — дополнительная информация

Файлы ASA представляют собой простые текстовые файлы со следующей информацией.

* События приложения
* Сессионные события
* \<object> декларации
* Объявления TypeLibrary
* директива #include

## Пример файла ASA

Файл Global.asa может выглядеть примерно так.

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

## использованная литература

* [Файл ASP Global.asa — w3schools](https://www.w3schools.com/asp/asp_globalasa.asp)

