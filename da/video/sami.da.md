{
  "date": "2023-05-16",
  "keywords": [
"samisk fil",
"hvad er en samisk fil",
"eksempel på sami fil",
"fil",
"sami filtypenavn",
"udvidelse"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "SAMI filformat - undertekster og metadataudvekslingsfil",
  "description": "Lær om SAMI-format og API'er, der kan oprette og åbne SAMI-filer.",
  "linktitle": "SAMI",
  "menu": {
    "docs": {
      "identifier": "video-sami-da",
      "parent": "video"
}
},
  "lastmod": "2023-05-16"
}

## Hvad er SAMI fil?

En fil med filtypenavnet .sami refererer typisk til en SAMI-fil (Subtitles And Metadata Interchange). SAMI er et undertekstformat, der bruges til at vise undertekster eller lukkede undertekster i videoer. Det blev oprindeligt udviklet af Microsoft til deres Windows Media Player.

SAMI-filer indeholder timinginformation og tekstindhold til undertekster eller lukkede billedtekster, så de kan synkroniseres med en videoafspilning. Formatet understøtter grundlæggende formateringsmuligheder såsom skrifttype, farve og placering af underteksterne på skærmen.

SAMI-filer er normalt almindelige tekstfiler og kan åbnes og redigeres ved hjælp af en teksteditor. Indholdet af en SAMI-fil inkluderer typisk en overskriftssektion, der giver information om filen, efterfulgt af individuelle undertekstposter med deres respektive timing og tekst.

Her er et eksempel på, hvordan en SAMI-fil kan se ud:

```
<SAMI>
<HEAD>
<TITLE>Example Subtitles</TITLE>
</HEAD>
<BODY>
<SYNC Start=100><P Class=ENCC>Subtitle 1</P></SYNC>
<SYNC Start=500><P Class=ENCC>Subtitle 2</P></SYNC>
<SYNC Start=1000><P Class=ENCC>Subtitle 3</P></SYNC>
</BODY>
</SAMI>
```

SAMI-filer bruges almindeligvis i forbindelse med videoafspillere eller medieafspillere, der understøtter undertekstvisning, såsom Windows Media Player eller VLC Media Player. Afspilleren læser SAMI-filen og synkroniserer underteksterne med videoindholdet, så seerne kan læse billedteksterne, mens de ser videoen.

## Understøttede HTML-tags

SAMI (Subtitles And Metadata Interchange) files support a limited set of HTML-like tags for formatting and styling the subtitles. Here are some of the commonly used tags supported by SAMI:

- ``<SAMI> :`` Rodelementet, der indkapsler hele SAMI-filen.
- ``<HEAD> :`` Indeholder headerinformation for SAMI-filen.
- ``<TITLE>:`` Specifies the title of the SAMI file.
- ``<BODY>:`` Encloses the subtitle entries and their timing information.
- ``<SYNC>:`` Represents a synchronization point for a subtitle entry. It specifies the timing at which the subtitle should be displayed.
- ``<P>:`` Encloses the actual text content of a subtitle. It is typically used within a <SYNC> block.
- `` <FONT>:`` Definerer skrifttypeegenskaber for den vedlagte tekst. Attributter som farve, ansigt, størrelse og stil kan bruges til at ændre skrifttypens udseende.</font>
- ``<BR>:`` Inserts a line break within a subtitle.
- `` <B>:`` Gengiver den vedlagte tekst med fed skrift.</b>
- `` <I>:`` Gengiver den vedlagte tekst i kursiv.</i>
- `` <U>:`` Gør den vedlagte tekst understreget.</u>
- ``<C>:`` Specifies the position or alignment of the subtitle text on the screen. It supports attributes like Center, Middle, Left, Right, Top, Bottom, and their combinations.
- ``<LANG>:`` Specifies the language code for the subtitle text. It helps in identifying the language of the subtitles.

Dette er nogle af de grundlæggende tags, der understøttes af SAMI-filer. Det er vigtigt at bemærke, at SAMI ikke understøtter hele spektret af HTML-tags og attributter. De understøttede tags er primært fokuseret på styling og placering af underteksterne frem for at give omfattende dokumentstrukturering eller interaktivitet.

## Referencer
* [SAMI](https://en.wikipedia.org/wiki/SAMI)


