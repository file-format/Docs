{
  "date" : "2019-10-11",
  "keywords" :[ "rtf-bestand", "rtf-bestandsformaat", "wat is een rtf-bestand", "bestand", "rtf-voorbeeld", "rtf-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RTF - Rich Text-indeling",
  "description":"Meer informatie over RTF-bestandsindeling en API's die RTF-bestanden kunnen maken en openen.",
  "linktitle" : "RTF",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een RTF-bestand?

Het Rich Text Format (**RTF**), geïntroduceerd en gedocumenteerd door Microsoft, vertegenwoordigt een methode voor het coderen van opgemaakte tekst en afbeeldingen voor gebruik in toepassingen. Het formaat vergemakkelijkt de uitwisseling van documenten tussen verschillende platforms met andere Microsoft-producten, en dient zo het doel van interoperabiliteit. Deze mogelijkheid maakt het een standaard voor gegevensoverdracht tussen tekstverwerkingssoftware en daarom kan inhoud worden overgedragen van het ene besturingssysteem naar het andere zonder de documentopmaak te verliezen. De specificaties van de bestandsindeling zijn door Microsoft beschikbaar voor openbare [download](https://interoperability.blob.core.windows.net/files/Archive_References/%5bMSFT-RTF%5d.pdf) en kunnen worden geraadpleegd vanuit het perspectief van de ontwikkelaar.

## Korte geschiedenis van RTF-bestandsindeling ##

Het RTF-bestandsformaat heeft sinds de publicatie verschillende revisies ondergaan. De officiële versie voor lezen/schrijven werd gepubliceerd als onderdeel van Microsoft Word 3.0 voor Macintosh met versie 1.0-specificaties. De definitieve versie van specificaties, 1.9.1, is in maart 2008 door Microsoft gepubliceerd. Hierna worden geen verbeteringen aan de specificaties meer aangebracht. Op dit moment hebben bijna alle besturingssystemen meer functierijke toepassingen die het gebruik van het RTF-bestandsformaat hebben geminimaliseerd/uitgeroeid.

## Specificaties RTF-bestandsindeling ##

RTF dient als een standaard voor gegevensoverdracht tussen tekstverwerkingssoftware en overdracht van inhoud van het ene besturingssysteem naar het andere. Dit wordt bereikt met behulp van besturingswoorden die tot 2007 door Microsoft Office Word zijn geïntroduceerd. Een standaard RTF-bestand bestaat uit ASCII om rich text weer te geven en met niet-ASCII-tekens dat wordt geconverteerd naar de juiste codewaarden. Nieuwere versies van Word kunnen RTF-bestanden lezen die met eerdere versies zijn gegenereerd, terwijl de oudere versies controlewoorden en -groepen negeren die ze niet begrijpen.

### De fundamenten van RTF begrijpen ###

RTF-bestanden gebruiken 7-bits ASCII-platte tekst, bestaande uit:

* controlewoorden
* controle symbolen, en
* groepen.

Deze fungeren als de bouwstenen voor de weergave van RTF-gegevens als begrijpelijke tekst- en tekencodering.

#### Controlewoord ####

Deze vertegenwoordigen een speciaal opgemaakte opdracht die wordt gebruikt om tekens te markeren voor weergave en mogen niet langer zijn dan 32 letters. Een stuurwoord wordt gedefinieerd door:

\<ASCII Letter Sequence> //<//Delimiter//> //

Elk stuurwoord is hoofdlettergevoelig en begint met een backslash. De ASCII-letterreeks kan ASCII-alfabetten bevatten (a tot en met z en A tot en met Z). De<Delimite> markeert het einde van de naam van het stuurwoord en kan een van de volgende zijn:

* Een ruimte. Dit dient alleen om een stuurwoord af te bakenen en wordt bij de volgende verwerking genegeerd.
* Een numeriek cijfer of een ASCII-minteken, dat aangeeft dat een numerieke parameter aan het stuurwoord is gekoppeld. De daaropvolgende digitale reeks wordt dan begrensd door elk ander teken dan een ASCII-cijfer (gewoonlijk een ander stuurwoord dat begint met een backslash). De parameter kan een positief of negatief decimaal getal zijn. Het bereik van de waarden voor het getal is nominaal –32768 tot en met 32767, dwz een 16-bits geheel getal met teken. Een klein aantal stuurwoorden heeft waarden in het bereik‌ −2.147.483.648 tot 2.147.483.647 (32-bits geheel getal met teken). Deze controlewoorden omvatten **\binN**, **\revdttmN//**, **\rsidN** gerelateerde controlewoorden en enkele afbeeldingseigenschappen zoals **\bliptagN**. Hier staat **N** voor de numerieke parameter. Een RTF-parser mag maximaal 10 cijfers bevatten, eventueel voorafgegaan door een minteken. Als het scheidingsteken een spatie is, wordt het weggegooid, dat wil zeggen dat het niet wordt opgenomen in de daaropvolgende verwerking.
* Elk ander teken dan een letter of een cijfer. In dit geval beëindigt het begrenzende teken het stuurwoord en maakt het geen deel uit van het stuurwoord. Zoals een backslash "\", wat betekent dat er een nieuw besturingswoord of een besturingssymbool volgt.

#### Controlesymbool ####

Een besturingssymbool vertegenwoordigt een speciale gebeurtenis die een specifieke betekenis heeft, afhankelijk van de inhoud. Het bestaat uit een backslash gevolgd door een speciaal teken (niet-alfabetisch teken) en heeft geen scheidingstekens.

#### Groep ####

Een groep kan bestaan uit tekst, controlewoorden of controlesymbolen tussen accolades (**{ }**). De openingsaccolade (**{** ) geeft het begin van de groep aan en de sluitingsaccolade ( **}**) geeft het einde van de groep aan. Elke groep specificeert de tekst die door de groep wordt beïnvloed en de verschillende kenmerken van die tekst.

### RTF-bestandsstructuur ###

Een RTF-bestand heeft de volgende standaardsyntaxis:

Het Rich Text Format (**RTF**), geïntroduceerd en gedocumenteerd door Microsoft, vertegenwoordigt een methode voor het coderen van opgemaakte tekst en afbeeldingen voor gebruik in toepassingen. Het formaat vergemakkelijkt de uitwisseling van documenten tussen verschillende platforms met andere Microsoft-producten, en dient zo het doel van interoperabiliteit. Deze mogelijkheid maakt het een standaard voor gegevensoverdracht tussen tekstverwerkingssoftware en daarom kan inhoud worden overgedragen van het ene besturingssysteem naar het andere zonder de documentopmaak te verliezen. De specificaties van de bestandsindeling zijn door Microsoft beschikbaar voor openbare [download](https://interoperability.blob.core.windows.net/files/Archive_References/%5bMSFT-RTF%5d.pdf) en kunnen worden geraadpleegd vanuit het perspectief van de ontwikkelaar.

#### RTF-koptekst ####

Een RTF-header heeft de volgende weergave.

|Veld|Beschrijving
---|---|
|\<header> |**\rtf1\fbidis**? \<character set> \<from> ? \<deffont> \<deflang> \<fonttbl> ? \<filetbl> ? \<colortbl> ? \<stylesheet> ? \<stylerestrictions> ? \<listtables> ? \<revtbl> ? \<rsidtable> ? \<mathprops> ? \<generator> ?

Koptabellen moeten in deze volgorde worden weergegeven als ze bestaan. Het RTF-bestand kan groepen bevatten voor lettertypen, stijlen, schermkleur, afbeeldingen, voetnoten, opmerkingen (annotaties), kop- en voetteksten, samenvattingsinformatie, velden, bladwijzers, document-, sectie-, alinea- en tekenopmaakeigenschappen, wiskunde, afbeeldingen en objecten. Als het lettertype, het bestand, de stijl, de kleur, het revisieteken, de samenvattingsinformatiegroepen en de documentopmaakeigenschappen in het bestand zijn opgenomen, moeten ze voorkomen in de RTF-header, die voorafgaat aan de RTF-body. Als de inhoud van een groep niet wordt gebruikt, kan de groep worden weggelaten. Elke groep die de eigenschappen gebruikt die in een andere groep zijn gedefinieerd, moet worden weergegeven na de groep die deze eigenschappen definieert. Kleur- en lettertype-eigenschappen moeten bijvoorbeeld voorafgaan aan de stijlgroep.

#### RTF-versie ####

Een RTF-document moet beginnen met deze zes tekens:

```
{\rtf1
```
waarbij de 1 het RTF-versienummer toont.

#### Karakterset ####

Na de {\rtf1 moet het document aangeven welke tekenset het gebruikt. De manier om een tekenset te declareren is met een van deze commando's:

`\ansi` - Het document bevindt zich in de ANSI-tekenset, ook bekend als Code Page 1252, de gebruikelijke MSWindows-tekenset.

`\mac` - Het document bevindt zich in de MacAscii-tekenset, de gebruikelijke tekenset onder oude (pre-10) versies van Mac OS.

`\pc` - Het document staat in DOS-codepagina 437, de standaardtekenset voor MS-DOS. Typisten met een goed spiergeheugen zullen opmerken dat dit de tekenset is die nog steeds wordt gebruikt voor het interpreteren van "Alt-numerieke" codes - dwz wanneer u Alt ingedrukt houdt en "130" typt op het numerieke toetsenbord, produceert het een é, omdat teken 130 in CP437 is een é. Dat is ongeveer het enige gebruik dat CP437 tegenwoordig ziet.

`\pca` - Het document staat in DOS Code Page 850, ook wel bekend als de MS-DOS Multilingual Code Page.

#### Lettertypeopdracht ####

De tekensetdefinitie wordt gevolgd door het commando `\deffN`. Dit definieert dat het lettertypenummer N het standaardlettertype voor dit document is. Het lettertypenummer N is afkomstig uit de lettertypetabel. Het commando `\deffN` is technisch optioneel, maar het zou er voor de zekerheid moeten zijn, aangezien een veelvoorkomende proloog, zoals het volgende, lettertype 0 als het standaardlettertype kiest.

`{\rtf1\ansi\deff0`

#### Lettertypetabel ####

Alle lettertypen die in een document kunnen worden gebruikt, worden weergegeven in een lettertypetabel waarin elk lettertype wordt weergegeven door een lettertypenummer. Document moet een lettertypetabel hebben, hoewel sommige programma's ook zonder zullen werken.

De syntaxis voor een lettertypetabel is {\fonttbl //...declarations//...}, waarbij elke declaratie deze basissyntaxis heeft:

`{\fnummer\familiecommando Lettertypenaam;}`

Een lettertypetabel met vier declaraties ziet er als volgt uit:

```
{\fonttbl
{\f0\froman Times;}
{\f1\fswiss Arial;}
{\f2\fmodern Courier New;}
}
```

In een document met die lettertypetabel zou `{\f2 stuff}` "dingen" afdrukken in Courier New. Een lettertype kan pas in een document worden gebruikt als het wordt vermeld in de lettertypetabel.

### Einde van document ###

Elk RTF-document moet eindigen met een }, om de groep te sluiten die wordt geopend door de {, het eerste teken in het document. Niets kan de laatste } volgen, behalve mogelijk een nieuwe regel.

## Referenties ##

* [RTF 1.9.1-specificaties](https://interoperability.blob.core.windows.net/files/Archive_References/%5bMSFT-RTF%5d.pdf)
* [Rich Text Format](https://en.wikipedia.org/wiki/Rich_Text_Format)

