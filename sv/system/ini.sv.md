{
  "date" : "2021-07-07",
  "keywords" :[ "INI", "tillägg", "fil", "format", "system", "Initiering", "katalogtillägg", "program", "dator", "applikation" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"INI - Initieringsfilformat",
  "description":"Läs mer om INI-filformat och API:er som kan skapa och öppna INI-filer.",
  "linktitle" : "INI",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-07"
}

## Vad är en INI fil? ##

En INI-fil är ett meddelandekonfigurationsdokument för datorprogram som innehåller publika nycklar för egenskaper och sektioner som organiserar attributen i ett ramverk och grammatik. Dessa systemfilformatskonfigurationsdokument får sitt namn från MS-DOS-operativsystemets katalogtillägg INI, som står för initiering. Det populariserade denna form av mjukvaruinstallation. Många program i andra program använder olika filnamnstillägg, såsom CONF och [CFG](/sv/system/cfg/), även om formatet har etablerat en inofficiell standard i många konfigurationssituationer.

## Kort historik över INI-filer##

Från början var Windows huvudsakliga programkonfigurationsteknik ett textfilformat som bestod av textrader med ett avgörande par per rad, uppdelat i sektioner. Enhetsdrivrutiner, typsnitt och startprogram lagrades alla i detta format. Individuella inställningar lagrades också vanligtvis i INI-filer av appar.
Fram till Windows 3.1x stöddes formatet på 16-bitars Microsoft Windows-plattformar. Från och med Windows 95 började Microsoft uppmuntra utvecklare att använda Windows-registret istället för INI-filer för konfiguration.

## INI-fil - Filformatspecifikationer

### Nycklar/egenskaper ###

Nyckeln/egenskapen är det mest grundläggande elementet i en INI-fil. En lika symbol (=) skiljer namnet och värdet på varje nyckel åt. Till vänster om likhetstecknet är där namnet visas. Likasymbolen och semikolon är diskreta bokstäver i Windows-systemet och kan därför inte användas i nyckeln. Alla tecken kan användas i värdet.

```
name=value
```

### Avsnitt ###

Sektionskommentaren visas inom hakparenteser ([]) på sin egen rad. Efter sektionsdefinitionen är alla nycklar kopplade till den sektionen. Avsnitt avslutas vid nästa avsnittsbeteckning eller dokumentets slut; det finns ingen specifik "slut på sektion"-avgränsare. Sektioner kan inte staplas; de kan bara namnges en gång och behöver inte länkas.

```
[section]
a=a
b=b
```

### Ändra funktioner ###

INI-filformatet har inte en globalt accepterad definition. Många datorapplikationer innehåller funktioner utöver de som redan nämnts. Listan nedan innehåller några vanliga egenskaper som kan eller inte kan inkluderas i ett enskilt program.

* Kommentarer
* Escape-karaktärer
* Dubblettnamn


## INI Exempel ##

Exempel INI-filen ser ut som följer:

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

## Referens ##

* [DMP - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

