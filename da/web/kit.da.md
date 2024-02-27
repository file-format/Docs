{
  "date" : "2022-07-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Lær om KIT-filformat og API'er, der kan oprette og åbne KIT-filer.",
  "title" : "KIT-filformat - CodeKit-fil",
  "linktitle" : "KIT",
  "menu" : {
    "docs" : {
      "identifier":"web-kit-da",
      "parent" : "web"
}
},
  "lastmod" : "2022-07-04"
}

## Hvad er en KIT fil?

En fil med filtypenavnet .kit er en HTML-fil, der er oprettet med programmeringssproget [CodeKit](https://codekitapp.com/). Den indeholder importer og variabler ud over eksisterende [HTML](/web/html/) filer, hvilket gør den ideel til statiske websteder. CodeKit kompilerer KIT-filer til HTML, der let kan bruges som statiske webstedsfiler.

## KIT filformat

KIT-filer er HTML-filer, der desuden inkluderer importer og variabler. Disse gemmes som almindelige tekstfiler og kan åbnes med enhver teksteditor eller webfileditor.

### KIT-filimport

Næsten enhver filtype kan importeres til en Kit-fil. Følgende er importsyntaksen, der bruges til at importere filer til en .kit-fil.

```
<!-- @import "someFile.kit" -->
<!-- @import "file.html" -->
```

Når en import tilføjes til en KIT-fil og gemmes, erstattes den med teksten i den fil, der importeres. Du kan også bruge @include i stedet for @import.

### Flere importer i en KIT-fil

Du kan også importere mere end én fil ad gangen ved at bruge en kommasepareret liste:

```
<!-- @import someFile, otherFile.html, ../thirdFile.kit -->
```

## Referencer

* [Hvad er Kit?](https://codekitapp.com/help/kit/)


