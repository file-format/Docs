{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PDF/X-filformat",
  "description":"Läs mer om PDF/X-filformat och API:er som kan skapa och öppna PDF/X-filer.",
  "linktitle" : "PDF/X",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

# Vad är PDF/X-fil? #

PDF/X är en ISO 15930-standard publicerad 2001 med en delmängd av PDF-funktioner. Standarden upprättades och publicerades utifrån specifika krav från tryckeri- och förlagsbranschen. Kraven för denna standard utformades enligt de olika behoven hos tryckeri- och förlagsindustrin. PDF/X kräver att de överensstämmande filerna är kompletta, dvs. fristående. Detta kräver att element som typsnitt som används på sidan ska vara en del av dokumentet. Innehåll som 3D eller video kan inte vara en del av PDF/X-dokument. Informationen i PDF/X-dokumentet kräver att den är korrekt.

## PDF/X-standarder och versioner ##

PDF/X-familjen av standarder består av flera versioner, var och en utformad för ett specialiserat resultat. Utvecklingen av dessa standarder syftade till att möta tryckeri- och förlagsindustrins många olika behov.

* `PDF/X-1a` - Även känd som den första standarden för PDF/X-familjen, kräver PDF/X-1a att allt innehåll är en del av PDF-dokumentet för att kunna skrivas ut. Dokumentelement som typsnitt, formulär, lösenordsskydd och synliga kommentarer är inte tillåtna. PDF/X-1a har sina egna specifika krav samt de som gäller transparens och lager är tillåtna. Dessa kräver också att utskriftselement endast använder CMYK, gråskala eller dekorfärger, vilket resulterar i att RGB eller enhetsoberoende färgrymder inte används. är för utbyten där alla filer ska levereras i CMYK (och/eller dekorfärger), utan RGB eller färghanterade data. PDF/X-1a kallas också för komplett utbyte på grund av att informationen är fullständig
* `PDF/X-3` - introducerades 2002 och hävde många restriktioner för PDF/X-1a. Detta gjorde det möjligt för grafik i en PDF/X-3 att använda CMYK, grescale, RGB, Lab och ICC-baserade färgrymder. Den är faktiskt baserad på PDF-standard 1.3 med [ICC-profil](https://en.wikipedia.org/wiki/ICC_Profile). Det kallas också för färghantering på grund av den flexibilitet och regler som det introducerar för färger som ingår i ett PDF-dokument.
* `PDF/X-4` - stöder OH-film, så PDF-X/4 innehåller all data som krävs för utmatning utan att plattas ut.
* `PDF/X-5` - är baserad på PDF/X-4 och lägger till stöd för extern grafik via referens XObjects, såväl som externa n-colorant-profiler för rendering. Använd den för partiellt utbyte av utskriftsdata med PDF-version 1.6

## Referenser ##

* [PDF/X - Av Wikipedia](https://en.wikipedia.org/wiki/PDF/X)

