{
  "date" : "2020-11-11",
  "keywords" :[ "ACCDB", "extensie", "bestand", "bestandsindeling", "Databasebestandstype", "Databasebestandsindeling", "Databasebestanden"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Meer informatie over ACCDB-bestandsindelingen en API's die ACCDB-bestanden kunnen maken en openen.",
  "title" :"ACCDB-bestandsindeling - Microsoft Access 2007-databasebestand",
  "linktitle" : "ACCDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-12"
}

## Wat is een ACCDB-bestand?

Een bestand met de extensie .accdb is een Microsoft Access 2007-databasebestand waarin gebruikersgegevens in tabellen worden opgeslagen. Het ondersteunt het opslaan
aangepaste formulieren, SQL-query's en andere gegevens. ACCDB-bestanden vervingen [MDB](/nl/database/mdb/)-bestanden nadat Microsoft was overgestapt op een op XML gebaseerde bestandsstructuur. ACCDB-bestanden kunnen nog steeds worden geconverteerd naar MDB met oude compatibiliteit. De ACCDB is nu echter het veelgebruikte Access-databasebestandsformaat. Microsoft ondersteunde ook extra functies in ACCDB-indeling, zoals de mogelijkheid om bestandsbijlagen, binaire gegevens en meerwaardige veldondersteuning op te slaan.

## ACCDB-bestandsindeling

Net als MDB zijn er geen openbare specificaties beschikbaar voor het ACCDB-bestandsformaat. Microsoft ondersteunt programmatische toegang tot deze bestanden via Open Database Connectivity (ODBC) -standaard en Visual Basic for Applications (VBA).

### Een inzicht

Een hex-dump van een eenvoudig ACCDB-bestand suggereert dat er algemene overeenkomsten in structuur zijn met de nieuwste versies van de voorganger MDB Format Family. Beide bestandsformaten gebruiken vaste paginagroottes van 4096 bytes. Een andere overeenkomst tussen ACCDB en MDB is de vorm van het magische getal, dat de tekenreeks "Standard ACE DB" voor ACCDB bevat. Een versie- of compatibiliteitscode bevindt zich in beide formaten op dezelfde locatie. De mdbtools | HACKING-bestand vermeldt "Offset 0x14 bevat de Jet-versie van deze database" en de onofficiële MDB-gids is het daarmee eens. De informatie in deze bronnen, gecombineerd met Wikipedia-vermelding voor [Microsoft Jet Database Engine](https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine), suggereert dat een waarde van 0x02 ACE 12 (Access 2007) aangeeft en 0x03 ACE aangeeft 14 (Toegang 2010). Een minimale database die is gemaakt in Access 2010 en een vergelijkbare database die is gemaakt in Access 2016, hebben echter beide 0x02 op deze locatie. Een minimale database die in Access 2016 is gemaakt, maar die een kolom definieert met het nieuw geïntroduceerde gegevenstype "groot geheel getal", had een waarde van 0x05. In ACCDB-bestanden lijkt deze indicator de compatibiliteit van het bestand weer te geven in plaats van de versie van de ACE-engine die is gebruikt om het te maken.

## Referenties

* [Access File Format](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41)
* [Access 2016-specificaties](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c?ui=en-us&rs=en-us&ad=us)
* [Microsoft Jet Database Engine](https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine)
* [Welke Access-bestandsindeling moet ik gebruiken?](https://support.microsoft.com/en-us/office/who-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41?ui=nl-nl&rs=nl-nl&ad=ons)
