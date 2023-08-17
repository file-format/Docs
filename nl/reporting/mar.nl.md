{
  "date" : "2021-28-05",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MAR - Microsoft Access Reports-bestand",
  "keywords" :[ "mar", "mar file", "mar file format", "wat is toegangsrapport", "toegangsrapport", "microsoft toegangsrapport"],
  "description":"Meer informatie over de bestandsindeling van Acess Report (MAR) die door Microsoft Access-software wordt gebruikt om een snelkoppeling of koppeling naar Microsoft Access Report te maken.",
  "linktitle" : "MAR",
  "menu" : {
    "docs" : {
    "identifier": "reporting-mar",
      "parent" : "reporting"
}
},
  "lastmod" : "2021-28-05"
}

## Wat is Access Report (MAR-bestand)? ##
Een bestand dat door Microsoft Access is gemaakt als snelkoppeling van het rapport, wordt opgeslagen met de bestandsextensie .mar. Een **Microsoft Access-rapport** biedt een manier om de informatie in de Microsoft Access-database op te maken, weer te geven en samen te vatten. Met deze rapporten kunt u uw gegevens opmaken in een nauwkeurige en informatieve lay-out om ze op het scherm te bekijken of af te drukken. Het rapport geeft alleen de statische gegevens weer, wat betekent dat we de gegevens in tabellen niet kunnen wijzigen wanneer we het Access-rapport bekijken. Het rapport toont de meest recente gegevens wanneer het wordt geopend.

## Microsoft Access Report (MAR) bestandsformaat

De MAR-bestandsindeling wordt door Microsoft Access-software gebruikt om een snelkoppeling of koppeling naar Microsoft Access Report te maken, een databaseobject dat handig wordt wanneer u de informatie in uw database moet presenteren voor een van de volgende doeleinden:

- Geef een samenvatting van de gegevens weer.
- Archiveer snapshots van de gegevens.
- Details over individuele records weergeven.
- Etiketten maken.

## Delen van toegangsrapport
Het ontwerp van een Access-rapport is verdeeld in verschillende secties die kunnen worden bekeken in de ontwerpweergave. In de volgende tabel wordt uitgelegd hoe elke sectie werkt en hoe u rapporten kunt maken.
| Sectie | Hoe de sectie wordt weergegeven wanneer deze wordt afgedrukt | Waar de sectie kan worden gebruikt |
---------|----|------|
| Koptekst rapporteren | Aan het begin van het rapport. | Gebruik de rapportkop voor informatie die normaal op een voorblad zou kunnen verschijnen, zoals een logo, een titel of een datum. Wanneer u een berekend besturingselement plaatst dat gebruikmaakt van de aggregatiefunctie Som in de rapportkop, is de berekende som voor het hele rapport. De rapportkoptekst wordt vóór de paginakoptekst afgedrukt. |
| Paginakoptekst | Bovenaan elke pagina. | Gebruik een paginakoptekst om de rapporttitel op elke pagina te herhalen. |
| Groepskop | Aan het begin van elke nieuwe groep records. | Gebruik de groepskoptekst om de groepsnaam af te drukken. Gebruik bijvoorbeeld in een rapport dat is gegroepeerd op product de groepskop om de productnaam af te drukken. Wanneer u een berekend besturingselement dat gebruikmaakt van de aggregatiefunctie Som in de groepskoptekst plaatst, is de som voor de huidige groep. U kunt meerdere secties voor groepskopteksten in een rapport hebben, afhankelijk van het aantal groeperingsniveaus dat u hebt toegevoegd. Zie de sectie Groepering, sortering of totalen toevoegen voor meer informatie over het maken van kop- en voetteksten voor groepen. |
| Detail | Verschijnt één keer voor elke rij in de recordbron. | Hier plaatst u de besturingselementen die de hoofdtekst van het rapport vormen. |
| Groepsvoettekst | Aan het einde van elke groep records. | Gebruik een groepsvoettekst om samenvattende informatie voor een groep af te drukken. U kunt meerdere groepsvoettekstsecties in een rapport hebben, afhankelijk van het aantal groeperingsniveaus dat u hebt toegevoegd. |
| Paginavoettekst | Aan het einde van elke pagina. | Gebruik een paginavoettekst om paginanummers of informatie per pagina af te drukken. |
| Voettekst rapporteren | Aan het eind van het verslag. Opmerking: In de ontwerpweergave verschijnt de rapportvoettekst onder de paginavoettekst. In alle andere weergaven (bijvoorbeeld de lay-outweergave of wanneer het rapport wordt afgedrukt of als voorbeeld wordt weergegeven), verschijnt de rapportvoettekst boven de paginavoettekst, net na de laatste groepsvoettekst of detailregel op de laatste pagina. | Gebruik de rapportvoettekst om rapporttotalen of andere samenvattende informatie voor het hele rapport af te drukken. |






## Referenties ##

- [Inleiding tot rapporten in Access](https://support.microsoft.com/en-us/office/introduction-to-reports-in-access-e0869f59-7536-4d19-8e05-7158dcd3681c)
- [Rapporten ontwerpen in Access](https://github.com/prijuly2000/DBMS/blob/master/DesigningReportsinAccess2010.pdf)

