{
"datum": "20-04-2023",
  "keywords": [
"ldb-bestand",
"wat is een ldb-bestand",
"welke informatie ldb bevat",
"Wat is het doel van het LDB-bestand",
"ldb-extensie",
"bestand",
"verlenging"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title":"LDB-bestandsindeling - Microsoft Access Lock-bestand",
  "description":"Leer meer over het LDB-formaat en welke informatie het bevat.",
"linktitle":"LDB",
  "menu": {
    "docs": {
      "identifier": "misc-ldb",
"parent" : "misc"
}
},
"laatste mod": "20-04-2023"
}

## Wat is een LDB-bestand?

Een LDB-bestand is een vergrendelingsbestand dat door Microsoft Access wordt gebruikt om te voorkomen dat meerdere gebruikers tegelijkertijd dezelfde database bewerken. Wanneer de gebruiker een Access-database opent, maakt Access een bijbehorend LDB-bestand in dezelfde map als de database. Dit bestand bevat informatie over wie momenteel de database gebruikt en welke records ze bewerken.

Het LDB-bestand wordt automatisch aangemaakt door Microsoft Access wanneer de database wordt geopend, en wordt verwijderd wanneer de database wordt gesloten. Het is belangrijk op te merken dat het LDB-bestand nooit handmatig mag worden verwijderd, omdat dit problemen met de database kan veroorzaken.

Als u problemen ondervindt met de Microsoft Access-database, is een mogelijke oplossing het verwijderen van het LDB-bestand dat aan die database is gekoppeld. Hiermee worden eventuele vergrendelingen opgeheven die u mogelijk verhinderen toegang te krijgen tot de database. Zorg er echter voor dat u een back-up van de database maakt voordat u dit probeert, omdat het verwijderen van het LDB-bestand gegevensverlies of corruptie kan veroorzaken als dit op de verkeerde manier wordt gedaan.

## LDB-bestandsindeling - Meer informatie

Een LDB-bestand in Microsoft Access bevat informatie over gebruikers die momenteel toegang hebben tot de database, zoals hun gebruikersnaam, computernaam en inlogtijd. Het LDB-bestand bevat ook informatie over eventuele vergrendelingen die in de database zijn geplaatst, zoals welke records door welke gebruiker worden bewerkt.

Hier is een meer gedetailleerde lijst met de soorten informatie die in een LDB-bestand kunnen worden gevonden:

- **Gebruikersnaam** - de naam van de gebruiker die momenteel toegang heeft tot de database
- **Computernaam** - de naam van de computer waarvandaan de gebruiker toegang heeft tot de database
- **Inlogtijd** - het tijdstip waarop de gebruiker de database voor het eerst opende
- **Recordvergrendelingen** - informatie over welke records momenteel door welke gebruiker worden bewerkt
- **Objectvergrendelingen** - informatie over welke databaseobjecten (zoals tabellen, formulieren of rapporten) momenteel door welke gebruiker worden bewerkt
- **Verbindingsinformatie** - informatie over hoe de gebruiker is verbonden met de database (bijvoorbeeld of deze een lokale of netwerkverbinding gebruikt)

De informatie in het LDB-bestand wordt door Microsoft Access gebruikt om te voorkomen dat meerdere gebruikers tegelijkertijd conflicterende wijzigingen in dezelfde database aanbrengen. Wanneer een gebruiker probeert een record of object te bewerken dat al door een andere gebruiker is vergrendeld, geeft Microsoft Access een bericht weer dat aangeeft dat het object al in gebruik is. Het LDB-bestand wordt bijgewerkt wanneer gebruikers de database openen en sluiten en wijzigingen aanbrengen in vergrendelde objecten.

## Referenties
* [Wat is een LDB-bestand?](https://learn.microsoft.com/en-us/office/troubleshoot/access/ldb-file-description)

