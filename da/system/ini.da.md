{
  "date": "2021-07-07",
  "keywords": [
"INI",
"udvidelse",
"fil",
"format",
"system",
"Indvielse",
"biblioteksudvidelse",
"programmer",
"computer",
"Ansøgning"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "INI - Initieringsfilformat",
  "description": "Lær om INI-filformat og API'er, der kan oprette og åbne INI-filer.",
  "linktitle": "INI",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-in-dai"
}
},
  "lastmod": "2021-07-07"
}

## Hvad er en INI fil? ##

En INI-fil er et meddelelseskonfigurationsdokument til computerprogrammer, der indeholder offentlige nøgler til karakteristika og sektioner, der organiserer attributterne i en ramme og en grammatik. Disse systemfilformatkonfigurationsdokumenter får deres navn fra MS-DOS-operativsystemets biblioteksudvidelse INI, som står for initiering. Det populariserede denne form for softwareopsætning. Mange programmer på andre softwareapplikationer bruger forskellige filnavne tilføjelser, såsom CONF og [CFG](/system/cfg/), selvom formatet har etableret en uofficiel standard i mange konfigurationssituationer.

## Kort historie om INI-filer##

Til at begynde med var Windows' primære programkonfigurationsteknik et tekstfilformat, der bestod af tekstlinjer med et afgørende par pr. linje, opdelt i sektioner. Enhedsdrivere, skrifttyper og startstartere blev alle gemt i dette format. Individuelle indstillinger blev også almindeligvis gemt i INI-filer af apps.
Indtil Windows 3.1x blev formatet understøttet på 16-bit Microsoft Windows-platforme. Fra og med Windows 95 begyndte Microsoft at opfordre udviklere til at bruge Windows-registreringsdatabasen i stedet for INI-filer til konfiguration.

## INI-fil - Filformatspecifikationer

### Nøgler/egenskaber ###

Nøglen/egenskaben er det mest grundlæggende element i en INI-fil. Et lig-symbol (=) adskiller navnet og værdien af hver nøgle. Til venstre for lighedstegnet er der, hvor navnet vises. Ligesymbolet og semikolon er diskrete bogstaver i Windows-systemet og kan derfor ikke bruges i nøglen. Ethvert tegn kan bruges i værdien.

```
name=value
```

### Afsnit ###

Sektionskommentaren vises i firkantede parenteser ([]) på sin egen linje. Efter sektionsdefinitionen er alle nøgler knyttet til den sektion. Sektioner afsluttes ved den næste sektionsbetegnelse eller dokumentets slutning; der er ingen specifik end of section-separator. Sektioner kan ikke stables; de kan kun navngives én gang og er ikke påkrævet at være sammenkædet.

```
[section]
a=a
b=b
```

### Ændring af funktioner ###

INI-filformatet har ikke en globalt accepteret definition. Mange computerapplikationer indeholder funktioner ud over de allerede nævnte. Listen nedenfor indeholder nogle almindelige karakteristika, som muligvis er inkluderet i et individuelt program.

* Kommentarer

* Escape-karakterer 

* Dublerede navne 



## INI-eksempel ##

Eksempel INI-filen ser ud som følger:

```
[Settings]
 
#======================================================================
 
# Set detailed log for additional debugging info
 
DetailedLog=1
 
RunStatus=1
 
StatusPort=6090
 
StatusRefresh=10
 
Archive=1
 
# Sets the location of the MV_FTP log file
 
LogFile=/opt/ecs/mvuser/MV_IPTel/log/MV_IPTel.log
 
#======================================================================
 
Version=0.9 Build 4 Created July 11 2004 14:00
 
ServerName=Unknown

```

## Reference ##

* [DMP - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)


