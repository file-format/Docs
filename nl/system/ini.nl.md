{
  "date" : "2021-07-07",
  "keywords" :[ "INI", "extensie", "bestand", "format", "systeem", "Initiatie", "directory-extensie", "programma's", "computer", "toepassing"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"INI - Initiatiebestandsformaat",
  "description":"Meer informatie over INI-bestandsindelingen en API's die INI-bestanden kunnen maken en openen.",
  "linktitle" : "INI",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-07"
}

## Wat is een INI-bestand? ##

Een INI-bestand is een berichtconfiguratiedocument voor computerprogramma's die openbare sleutels bevatten voor kenmerken en secties die de attributen in een raamwerk en grammatica organiseren. Deze configuratiedocumenten voor systeembestandsindelingen ontlenen hun naam aan de directory-extensie INI van het MS-DOS-besturingssysteem, wat staat voor initiatie. Het maakte deze vorm van software-installatie populair. Veel programma's in andere softwaretoepassingen gebruiken verschillende toevoegingen aan bestandsnamen, zoals CONF en [CFG](/nl/system/cfg/), hoewel het formaat in veel configuratiesituaties een onofficiële standaard heeft vastgesteld.

## Korte geschiedenis van INI-bestanden##

Aanvankelijk was de belangrijkste programmaconfiguratietechniek van Windows een tekstbestandsformaat dat bestond uit tekstregels met één cruciaal paar per regel, verdeeld in secties. Apparaatstuurprogramma's, lettertypen en opstartprogramma's werden allemaal in dit formaat opgeslagen. Individuele instellingen werden ook vaak opgeslagen in INI-bestanden door apps.
Tot Windows 3.1x werd het formaat ondersteund op 16-bits Microsoft Windows-platforms. Vanaf Windows 95 begon Microsoft ontwikkelaars aan te moedigen om het Windows-register te gebruiken in plaats van INI-bestanden voor configuratie.

## INI-bestand - Specificaties bestandsindeling

### Sleutels/Eigenschappen ###

De sleutel/eigenschap is het meest elementaire element van een INI-bestand. Een gelijkteken (=) scheidt de naam en waarde van elke sleutel. Links van het isgelijkteken staat de naam. Het gelijkteken en de puntkomma zijn discrete letters in het Windows-systeem en kunnen daarom niet in de sleutel worden gebruikt. Elk teken kan in de waarde worden gebruikt.

```
name=value
```

### Secties ###

De sectieopmerking verschijnt tussen vierkante haken ([]) op een eigen regel. Na de sectiedefinitie worden alle sleutels aan die sectie gekoppeld. Secties eindigen bij de eerstvolgende sectie-aanduiding of het einde van het document; er is geen specifiek "einde van sectie"-scheidingsteken. Secties kunnen niet worden gestapeld; ze kunnen maar één keer worden genoemd en hoeven niet te worden gekoppeld.

```
[section]
a=a
b=b
```

### Functies wijzigen ###

Het INI-bestandsformaat heeft geen wereldwijd geaccepteerde definitie. Veel computertoepassingen bevatten functies naast de reeds genoemde. De onderstaande lijst bevat enkele gemeenschappelijke kenmerken die al dan niet in een individueel programma zijn opgenomen.

* Opmerkingen
* Escape-tekens
* Dubbele namen


## INI Voorbeeld ##

Het voorbeeld-INI-bestand ziet er als volgt uit:

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

## Referentie ##

* [DMP - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

