{
  "date" : "2022-05-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Meer informatie over de PYC-bestandsindeling en API's die PYC-bestanden kunnen maken en openen.",
  "title" :"PYC-bestandsindeling - door Python gecompileerd bestand",
  "linktitle" : "PYC",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2022-05-09"
}

## Wat is een PYC-bestand?

Een PYC-bestand is een gecompileerd uitvoerbestand dat is gegenereerd op basis van broncode die is geschreven in de programmeertaal Python. Wanneer het PY-bestand wordt uitgevoerd met behulp van de Python-interpreter, wordt het geconverteerd naar bytecode voor uitvoering. Tegelijkertijd wordt de gecompileerde bytecode ook opgeslagen als .pyc-bestand om op een later tijdstip opnieuw uit de cache te kunnen gebruiken, indien van toepassing.

## Structuur van PYC-bestandsindeling

PYC-bestanden zijn in bytecode en hun specificaties voor bestandsindelingen zijn niet openbaar beschikbaar. Uit onderzoek door sommige bronnen blijkt echter dat de [structuur van een PYC-bestand](https://nedbatchelder.com/blog/200804/the_structure_of_pyc_files.html#:~:text=pyc%20file%20is%20a%20binary,A% 20marshalled%20code%20object.) bestaat uit:

* `Een magisch getal van vier bytes` - Gewoon twee bytes die veranderen bij elke wijziging in de rangeercode, en dan twee bytes van 0d0a.
* `Een vier-byte wijzigingstijdstempel` - Unix wijzigingstijdstempel van het bronbestand dat de .pyc heeft gegenereerd, zodat het opnieuw kan worden gecompileerd als de broncode verandert.
* `Een gemarshalld code-object' - de uitvoer van marshal.dump van het code-object dat het resultaat is van het compileren van het bronbestand.

## Referenties

* [De structuur van .pyc-bestanden](https://nedbatchelder.com/blog/200804/the_structure_of_pyc_files.html#:~:text=pyc%20file%20is%20a%20binary,A%20marshalled%20code%20object.)

