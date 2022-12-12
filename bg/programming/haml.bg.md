{
  "date" : "2022-04-07",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HAML файлов формат – Haml файл с изходен код",
  "description":"Научете за HAML файловия формат и API, които могат да създават и отварят HAML файл.",
  "linktitle" : "HAML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-07"
}

## Какво е HAML файл?

HAML файлът е файл на език за маркиране на HTML абстракция, който съдържа изходен код, написан на езика [Haml](https://haml.info/). Може да се използва като заместител на ERB (скриптове за шаблон на Ruby). HAML файлът съдържа изходен код на шаблон за генериране на HTML на уеб документ. ERB файловете могат да бъдат заменени, като просто замените тези файлове в папката app/views с Haml, като промените разширението на файла. HAML файловете могат да се отварят с всеки текстов редактор като Microsoft Notepad, Notepad++, Apple TextEdit,

## HAML файлов формат

HAML файловете са изходни файлове, записани на диск като обикновени текстови файлове. Той съдържа код, написан в HAML синтаксис. HAML заменя етикетите **<>** със знака **%**, за да направи кода по-опростен и лесен. ERB файловете могат да се заменят чрез пускане с HAML, както е показано в следващия прост пример.

```
app/views/account/login.html.erb → app/views/account/login.html.haml
```

### Пример за HAML

Следното е примерен Hello World пример на HAML.

```
%p{:class => "sample", :id => "welcome"} Hello, World!
%p.sample#welcome Hello, World!
```
който се изобразява на следния HTML изход.

```
<p class="sample" id="welcome">Hello, World!</p>
```

## Препратки

* [HAML - Github](https://github.com/haml/haml)

