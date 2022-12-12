{
  "date" : "2022-04-07",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru HAML - soubor zdrojového kódu Haml",
  "description":"Další informace o formátu souboru HAML a rozhraních API, která mohou vytvořit a otevřít soubor HAML.",
  "linktitle" : "HAML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-07"
}

## Co je soubor HAML?

Soubor HAML je soubor jazyka HTML abstrakce, který obsahuje zdrojový kód napsaný v jazyce [Haml](https://haml.info/). Může být použit jako náhrada za skripty ERB (Ruby template scripts). Soubor HAML obsahuje zdrojový kód šablony pro generování HTML webového dokumentu. Soubory ERB lze nahradit jednoduchým nahrazením těchto souborů ve složce app/views za Haml změnou přípony souboru. Soubory HAML lze otevřít pomocí libovolného textového editoru, jako je Microsoft Notepad, Notepad++, Apple TextEdit,

## Formát souboru HAML

Soubory HAML jsou zdrojové soubory uložené na disk jako soubory prostého textu. Obsahuje kód napsaný v syntaxi HAML. HAML nahrazuje značky **<>** znakem **%**, aby byl kód jednodušší a jednodušší. Soubory ERB jsou vyměnitelné pomocí HAML, jak ukazuje následující jednoduchý příklad.

```
app/views/account/login.html.erb → app/views/account/login.html.haml
```

### Příklad HAML

Následuje příklad Hello World příklad HAML.

```
%p{:class => "sample", :id => "welcome"} Hello, World!
%p.sample#welcome Hello, World!
```
který se vykreslí do následujícího výstupu HTML.

```
<p class="sample" id="welcome">Hello, World!</p>
```

## Reference

* [HAML – Github](https://github.com/haml/haml)

