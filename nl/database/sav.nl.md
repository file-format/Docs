{
  "date" : "2021-06-14",
  "keywords" :[ "SAV", "extensie", "sav-bestand", "sav-bestandsindeling", "Databasebestandstype", "Databasebestandsindeling", "wat is een sav-bestand"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Meer informatie over SAV-bestandsindelingen en API's die SAV-bestanden kunnen maken en openen.",
  "title" :"SAV - SPSS-gegevensbestand",
  "linktitle" : "SAV",
  "menu" : {
    "docs" : {
      "identifier":"database-sav",
      "parent" : "database"
}
},
  "lastmod" : "2021-06-14"
}

## Wat is een SAV-bestand?
SAV-bestand is een gegevensbestand gemaakt door het Statistical Package for the Social Sciences (SPSS), een applicatie die veel wordt gebruikt door marktonderzoekers, gezondheidsonderzoekers, enquêtebedrijven, overheid, onderwijsonderzoekers, marketingorganisaties, dataminers voor statistische analyse. De SAV is opgeslagen in een eigen binair formaat en bestaat uit een gegevensset en een woordenboek die de gegevensset vertegenwoordigen, slaat gegevens op in rijen en kolommen.

## SAV-bestandsindeling
Het SAV-bestandsformaat is relatief stabiel geworden, maar we kunnen het niet statisch noemen. Achterwaartse en voorwaartse compatibiliteit is optioneel beschikbaar waar nodig, maar wordt niet goed onderhouden. De gegevens in een SAV-bestand zijn onderverdeeld in de volgende secties:

### Bestandskop
Het bestaat uit 176 bytes. De eerste 4 bytes geven de tekenreeks **$FL2** of **$FL3** aan in de tekencodering die voor het bestand is gebruikt. De laatste drie bytes geven aan dat de gegevens in het bestand zijn gecomprimeerd met **ZLIB**. De volgende tekenreeks van 60 bytes begint met **@(#) SPSS DATA FILE** en bepaalt ook het besturingssysteem en de SPSS-versie waarmee het bestand is gemaakt. De header gaat dan verder met velden van zes cijfers, die het aantal variabelen per waarneming en een cijfercode voor compressie bevatten, en eindigt met karaktergegevens die de aanmaakdatum en -tijd en een bestandslabel aangeven.
### Variabele descriptorrecords
Het record bevat een vaste volgorde van velden, die het type en de naam van de variabele classificeren samen met opmaakinformatie die door SPSS wordt gebruikt. Elke variabele record kan optioneel een variabel label van maximaal 120 tekens en maximaal drie ontbrekende-waardespecificaties bevatten.
### Waardelabels
De waardelabels zijn optioneel en worden opgeslagen in paren records met integer tags 3 en 4. Het eerste record dat tag 3 is, heeft een reeks paren velden, waarbij elk paar een waarde en het bijbehorende waardelabel bevat. Het tweede record, dat tag 4 is, geeft aan op welke variabelen de set waarden/labels van toepassing is.
### Documenten
Enkele of meerdere records met integer-tag 6. Optionele documentatie. bevat regels van 80 tekens.
### Extensierecords
Enkele of meerdere records met integer-tag 7. Extensierecords bieden informatie die veilig kan worden genegeerd, maar die in veel situaties behouden blijft, waardoor bestanden die door nieuwere software zijn geschreven, achterwaartse compatibiliteit behouden. Extensierecords hebben tags van het gehele subtype.
### Woordenboekterminator
Neem alleen op met integer-tag 999. Het scheidt woordenboek van gegevensobservaties.
### Gegevenswaarnemingen
Het wordt beschouwd als gegevens in volgorde van waarneming, bijvoorbeeld alle variabele waarden voor de eerste waarneming, gevolgd door alle waarden voor de tweede waarneming, enz. Het formaat van het gegevensrecord varieert afhankelijk van de compressiecode in het bestandskoprecord. Het gegevensgedeelte van een .sav-bestand kan worden gedecomprimeerd:
- **code 0**: gecomprimeerd door bytecode
- **code 1**: gecomprimeerd met ZLIB-compressie
 







## Referenties ##

* [SPSS System Data File Format Family (.sav)](https://www.loc.gov/preservation/digital/formats/fdd/fdd000469.shtml)

