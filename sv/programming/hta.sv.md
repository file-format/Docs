{
  "date" : "2021-09-16", 
  "keywords" :[ "hta", "fil", "tillägg", "filformat", "hta-implementering", "Programmeringsguide", "hta-exempel", "HTML-applikation", "Hypertext Markup Language Application", "HTA-filer", "Microsoft HTML Application"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HTA - HTML Application Files",
  "description":"Läs mer om HTA-filformat och API:er som kan skapa och öppna HTA-filer.",
  "linktitle" : "HTA",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-16"
}

## Vad är en HTA fil?

HTMLA står för **Hypertext Markup Language Application** är ett program som är kompatibelt med Microsoft Windows. Källkoden för detta program innehåller mer än ett skriptspråk som [HTML](/sv/web/html/) och [JavaScript](/sv/web/js/). För användargränssnittet är en HTML-applikation att föredra medan för att uppfylla kravet på programlogik används något annat skriptspråk.

En HTML-applikation är oberoende av webbläsarens säkerhetsmodell och körs som en helt pålitlig applikation. Tillägget som används för filer angående dessa applikationer är HTA. Dessa applikationer inkluderar funktioner i HTML tillsammans med egenskaperna hos andra skriptspråk.


## Kortfattad bakgrund ##

HTA introducerades först 1999 av Microsoft tillsammans med lanseringen av Internet Explorer 5. Den var kompatibel med Internet Explorer och kunde därför endast köras på Windows operativsystem. Denna teknik patenterades 2003. HTA-filerna körs på samma sätt som alla andra .exe-filer. HTA-filerna är också kompatibla med dagens uppdaterade version av Windows 11.


## Teknisk specifikation ##

HTA:er har samma format som vilken annan HTML-sida som helst, medan vissa attribut används för att styra formaten på ramar eller ikoner för program. Dessutom finns det argument för lanseringen av HTA. Dessa applikationer kan köras med ett program som heter mshta.exe. Den kan nås genom att helt enkelt dubbelklicka på filen. Dessa program körs automatiskt tillsammans med Internet Explorer. Förutom andra specifikationer är dessa inte oberoende av Trident-motorns webbläsare utan är oberoende av Internet Explorer. Det betyder att dessa kan köras utan att använda Internet Explorer.

Taggarna används för att anpassa utseendet på dessa applikationer. Konverteringen från Microsoft HTML-applikation till HTA-format är enklare, dvs du behöver bara ändra tillägget. Eftersom vi vet att dessa applikationer är fullt betrodda så innehåller dessa fler funktioner och fördelar jämfört med enkla HTML-filer. Textredigerare kan användas för att skapa HTA. Dessa redigerare kan förvärvas av Microsoft eller någon annan pålitlig källa.


## HTA filformat exempel ##

```
<HTML>
<HEAD>
<HTA:APPLICATION ID="HelloExample" 
   BORDER="bold" 
   BORDERSTYLE="complex"/>
<TITLE>HTA - Hello World</TITLE>
</HEAD>
<BODY>
<H2>HTA - Hello World</H2>
</BODY>
</HTML>

```

## Referens ##

* [HTA - av Wikipedia](https://en.wikipedia.org/wiki/HTML_Application)



