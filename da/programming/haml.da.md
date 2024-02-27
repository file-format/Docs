{
  "date": "2022-04-07",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "HAML filformat - Haml kildekodefil",
  "description": "Lær om HAML filformat og API'er, der kan oprette og åbne HAML fil.",
  "linktitle": "HAML",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-ham-dal"
}
},
  "lastmod": "2022-04-07"
}

## Hvad er en HAML fil?

En HAML-fil er en HTML-abstraktion markup-sprogfil, der indeholder kildekode skrevet på [Haml](https://haml.info/) sprog. Det kan bruges som en erstatning for ERB (Ruby template scripts). HAML-filen indeholder skabelonkildekode, der bruges til at generere HTML-koden til et webdokument. ERB-filer kan erstattes ved blot at erstatte disse filer i app/view-mappen til Haml ved at ændre filtypenavnet. HAML-filer kan åbnes med en hvilken som helst teksteditor, såsom Microsoft Notepad, Notepad++, Apple TextEdit,

## HAML filformat

HAML-filer er kildefiler, der er gemt på disken som almindelige tekstfiler. Den indeholder kode skrevet i HAML-syntaks. HAML erstatter **<>** tags med **%** tegnet for at gøre koden enklere og nemmere. ERB-filer er drop-in-udskiftelige af HAML som vist i følgende enkle eksempel.

```
app/views/account/login.html.erb → app/views/account/login.html.haml
```

### HAML Eksempel

Følgende er et eksempel på Hello World på HAML.

```
%p{:class => "sample", :id => "welcome"} Hello, World!
%p.sample#welcome Hello, World!
```
som gengiver til følgende HTML-output.

```
<p class="sample" id="welcome">Hello, World!</p>
```

## Referencer

* [HAML - Github](https://github.com/haml/haml)


