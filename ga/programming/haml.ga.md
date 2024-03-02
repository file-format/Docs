{
  "date": "2022-04-07",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Formáid Chomhaid HAML - Comhad Cód Foinse Haml",
  "description": "Foghlaim faoi fhormáid comhaid HAML agus APIs ar féidir leo comhad HAML a chruthú agus a oscailt.",
  "linktitle": "HAML",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-ham-gal"
}
},
  "lastmod": "2022-04-07"
}

## Cad is comhad HAML ann?

Is comhad HTML teanga marcála astarraingthe é comhad HAML ina bhfuil cód foinse scríofa i dteanga [Haml](https://haml.info/). Is féidir é a úsáid in ionad an ERB (scripteanna teimpléid Ruby). Tá cód foinse teimpléid i gcomhad HAML chun HTML doiciméad gréasáin a ghiniúint. Is féidir comhaid ERB a athsholáthar ach na comhaid seo a athsholáthar san fhillteán aip/amharc go Haml trí shíneadh an chomhaid a athrú. Is féidir comhaid HAML a oscailt le haon eagarthóir téacs ar nós Microsoft Notepad, Notepad++, Apple TextEdit,

## Formáid Chomhaid HAML

Is comhaid foinse iad comhaid HAML a shábháiltear ar diosca mar chomhaid gnáth-théacs. Tá cód scríofa i gcomhréir HAML ann. Cuireann HAML an comhartha **%** in ionad na gclibeanna **<>** chun an cód a dhéanamh níos simplí agus níos éasca. Is féidir le HAML comhaid buail isteach a athsholáthar mar a thaispeántar sa sampla simplí seo a leanas.

```
app/views/account/login.html.erb → app/views/account/login.html.haml
```

### Sampla HAML

Seo a leanas sampla Hello World de HAML.

```
%p{:class => "sample", :id => "welcome"} Hello, World!
%p.sample#welcome Hello, World!
```
a dhéanann an t-aschur HTML seo a leanas.

```
<p class="sample" id="welcome">Hello, World!</p>
```

## Tagairtí

* [HAML - Github]( https://github.com/haml/haml)


