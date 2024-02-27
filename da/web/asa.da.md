{
  "date": "2021-12-09",
  "keywords": [
"som en",
".som en",
"filformat",
"filtype",
"hvad er en .asa-fil"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ASA - ASP-konfigurationsfil",
  "description": "Lær om, hvad en ASA-fil og API'er er, der kan oprette og åbne ASA-filer.",
  "linktitle": "ASA",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-as-daa"
}
},
  "lastmod": "2021-12-09"
}

## Hvad er en ASA fil?

En ASA-fil er en konfigurationsfil, der er oprettet til [ASP](/web/asp/)/ASP.NET-projekter. Den indeholder erklæringer af variabler, indeholder og funktioner, der er beregnet til at være tilgængelige på globalt niveau i applikationen. Alle sider i projektet har adgang til disse variabler og funktioner, og undgår dermed kravet om at omskrive disse. Et sådant eksempel er Global.asa-siden, der er gemt i rodmappen for at være tilgængelig for andre ASP-websteder. Global.asa-filer er valgfrie, men hvis de bruges, kan hver applikation kun have én Global.asa-fil.

## ASA-filformat - flere oplysninger

ASA-filer er almindelige tekstfiler med følgende oplysninger.

 * Ansøgningsbegivenheder
 * Session begivenheder
 * \<object> erklæringer
 * TypeLibrary erklæringer
 * #include-direktivet

## Eksempel på ASA-fil

En Global.asa-fil kunne se sådan ud.

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

## Referencer

* [ASP Global.asa-fil - w3schools](https://www.w3schools.com/asp/asp_globalasa.asp)


