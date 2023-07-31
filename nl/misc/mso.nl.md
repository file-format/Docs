{
  "date" : "2022-03-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MSO - Microsoft Office-macroreferentiebestand",
  "description":"Meer informatie over MSO-bestanden en API's die MSO-bestanden kunnen maken en openen.",
  "linktitle" : "MSO",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-03-12"
}

## Wat is een MSO-bestand?

Een MSO-bestand is een gegevenscontainerbestandsindeling die wordt gemaakt wanneer een HTML-bericht wordt verzonden met Microsoft Outlook. Dit gebeurt meestal met Microsoft Office 2000-toepassingen. In de meeste gevallen wordt het e-mailbericht als bijlage bijgevoegd met de naam **Oledata.mso** bestand. De e-mailontvanger kan bij het openen van een dergelijke e-mail het bestand correct bekijken, zelfs als niet dezelfde software is geïnstalleerd. MSO-bestanden verwijzen naar [Microsoft Compound Document File Format (MCDF)](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/53989ce4-7b05-4f8d-829b-d08d6148375b).

## Microsoft MSO-bestandsindeling

MSO-bestanden worden opgeslagen in Microsoft Compound Document File Format (MCDF), ook bekend als de binaire bestandsindeling Object Linking and Embedding (OLE) of Component Object Model (COM).

### Structuur van MSO-bestandsindeling

De interne bestandsindelingsstructuur van de MSO-bestandsindeling is goed gedefinieerd in de [Structures](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/28488197-8193-49d7-84d8-dfd692418ccd ) sectie van de MCDF-documentatie. De File Allocation Table (FAT) beheert de sectorverdeling en sectorketens. Het bevat een array van 32-bits sectornummers. Elke index in de array vertegenwoordigt een sectornummer, terwijl de waarde de volgende sector in de keten of een speciale waarde vertegenwoordigt.

## Referenties

* [COM gestructureerde opslag](https://en.wikipedia.org/wiki/COM_Structured_Storage)
* [Microsoft Compound Document File Format (MCDF)](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/53989ce4-7b05-4f8d-829b-d08d6148375b)

