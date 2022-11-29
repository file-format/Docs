{
  "date" : "2021-09-08",
  "keywords" :[ "rel fil", "rel filformat", "vad är en rel fil", "fil", "rel exempel", "rel filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Läs mer om REL-filformat och API:er som kan skapa och öppna REL-filer.",
  "title" :"REL - Relocatable Module File",
  "linktitle" : "REL",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## Vad är REL fil?
En fil med filändelsen .rel kan användas för flera olika ändamål. När det gäller spelklassificering är den därför känd som en flyttbar modulfil som används av vissa Nintendo Wii-spel, som Brawl, Super Smash Bros och Mario Kart Wii. Den omfattar speldata, inklusive karaktärsmodeller och stadier. REL-filer fungerar på samma sätt som .DLL-filerna som används av Microsoft Windows.

## REL filformat
I ett REL-filformat är filen uppdelad i flera sektioner, grupperade efter liknande åtkomst, t.ex. läsbara data i en sektion, all körbar kod placeras i en annan, etc. Filen börjar med en rubriksektion, följt av:
- Tabell med avsnittsinformation.
- Sektionsdata.
- Flyttinformation.

### Filhuvud
Filen börjar med en rubrik på upp till 0x4C byte:
| Offset | Storlek | Fältnamn | Beskrivning |
--------------------|---------------|-------------------|---------------------------------|
| 0x00 | 4 | id | Godtyckligt identifikationsnummer. Måste vara unik bland alla RELs som används av ett spel. Får inte vara 0. |
| 0x04 | 4 | nästa | Pekare till nästa modul, fylld vid körning. |
| 0x08 | 4 | föregående | Pekare till föregående modul, fylld vid körning. |
| 0x0c | 4 | numSektioner | Antal avsnitt i filen. |
| 0x10 | 4 | sectionInfoOffset | Offset till början av sektionstabellen. |
| 0x14 | 4 | namnOffset | Offset till ASCII-sträng som innehåller modulens namn. Kan vara NULL. I förhållande till början av REL-fil. |
| 0x18 | 4 | namnStorlek | Storleken på modulnamnet i byte. |
| 0x1c | 4 | version | Versionsnummer för REL-filformatet. |
| 0x20 | 4 | bssStorlek | Storleken på avsnittet '.bss'. |
| 0x24 | 4 | relOffset | Offset till flytttabellen. |
| 0x28 | 4 | impOffset | Offset till imp-tabell. |
| 0x2c | 4 | impSize | Storlek på imp-tabellen i byte. |
| 0x30 | 1 | prologSektion | Indexera i sektionstabell vilken prolog är relativ till. Hoppa över om detta fält är 0. |
| 0x31 | 1 | epilogSektion | Indexera i sektionstabell vilken epilog är relativ till. Hoppa över om detta fält är 0. |
| 0x32 | 1 | olöstAvsnitt | Indexera till sektionstabell som olöst är relativt. Hoppa över om detta fält är 0. |
| 0x33 | 1 | bssSektion | Indexera i sektionstabell som bss är relativ till. Fylld vid körning! |
| 0x34 | 4 | prolog | Offset till specificerad del av _prolog-funktionen. |
| 0x38 | 4 | epilog | Offset till specificerad sektion av _epilog-funktionen. |
| 0x3c | 4 | olöst | Offset till specificerad sektion av _unresolved-funktionen. |
| 0x40 | 4 | justera | Endast version ≥ 2. Justeringsbegränsning på alla sektioner, uttryckt som potens av 2. |
| 0x44 | 4 | bssAlign | Endast version ≥ 2. Justeringsbegränsning på alla '.bss'-sektioner, uttryckt som potens av 2. |
| 0x48 | 4 | fixSize | Endast version ≥ 3. Om REL är länkad till OSLinkFixed (istället för OSLink), kan utrymmet efter denna adress användas för andra ändamål (som BSS). |

### Sektionsinformationstabell
Sektionsinformationstabellen innehåller **numSections**-poster var och en 0x8 byte lång:
| Offset | Storlek | Beskrivning |
-------|------------|-------------|
| 0x0 | 30 bitar | Offset från början av REL till sektionen. Om detta är noll är avsnittet ett oinitierat avsnitt (dvs. .bss). |
| 0x3,6 | 1 bit | Okänd. |
| 0x3,7 | 1 bit | Körbar flagga; om detta är 1 är avsnittet körbart. |
| 0x4 | 4 | Längd i byte av sektionen. Om detta är noll, hoppas denna post över. |
| 0x8 | Nästa inlägg | Nästa inlägg |

### Flyttdata
Omlokaliseringsdata är en eller flera listor med 0x8 bytestrukturer. Slutet på varje lista markeras med den speciella typkoden 203:
| Offset | Namn | Storlek | Beskrivning |
-------|------------|------------|-----|
| 0x0 | offset | 2 | Offset i byte från föregående flytt till denna. Om detta är den första omplaceringen i sektionen är detta i förhållande till sektionsstarten. |
| 0x2 | typ | 1 | Omplaceringstypen. Beskrivet nedan. |
| 0x3 | avsnitt | 1 | Den del av symbolen som ska flyttas mot. För den särskilda flytttypen 202 är detta istället numret på den sektion i denna fil som följande flyttningsposter gäller. |
| 0x4 | addend | 4 | Offset i byte av symbolen att flytta mot, i förhållande till början av dess sektion. Detta är en absolut adress istället för omplaceringar mot main.dol. |
| 0x8 | Nästa inlägg | Nästa inlägg | Nästa inlägg |


 




## Referenser


* [Relocatable Object Module Format](https://en.wikipedia.org/wiki/Relocatable_Object_Module_Format)


