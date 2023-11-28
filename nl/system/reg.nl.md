{
"datum": "2023-03-07",
  "keywords": [
"reg-bestand",
"wat is een reg-bestand",
"bestand",
"reg-bestandsextensie",
"verlenging"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title":"REG-bestandsindeling - Windows-registerbestand",
  "description":"Leer meer over REG-indeling en API's waarmee REG-bestanden kunnen worden gemaakt en geopend.",
"linktitle": "REG",
  "menu": {
    "docs": {
      "identifier": "system-reg",
"parent" : "system"
}
},
"laatste mod": "2023-03-07"
}

## Wat is een REG-bestand?

Een REG-bestand is een bestandsindeling die wordt gebruikt om Windows-registergegevens te importeren of exporteren. Het Windows-register is een hiërarchische database waarin configuratie-instellingen en opties voor het Windows-besturingssysteem en geïnstalleerde applicaties worden opgeslagen. Het register bevat informatie zoals gebruikersvoorkeuren, applicatie-instellingen, hardware- en softwareconfiguratiegegevens en meer.

Een REG-bestand heeft doorgaans de bestandsextensie ".reg" en is een tekstbestand dat een reeks registervermeldingen en waarden in een specifiek formaat bevat. Het formaat bestaat uit een headersectie die het bestand identificeert als een registerbestand, gevolgd door een reeks sleutel- en waardeparen die registervermeldingen vertegenwoordigen.

## REG-bestandsindeling - Meer informatie

Hier is een voorbeeld van een reg-bestandsformaat:

```
[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Run]
"Example"="C:\\Example.exe"

[HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Explorer\Advanced]
"Hidden"=dword:00000001
```

De eerste regel van het bestand specificeert de versie van de register-editor. De volgende regels bevatten de registervermeldingen in de indeling van een sleutelpad, gevolgd door een waardenaam en waardegegevens. In dit voorbeeld bevat het reg-bestand twee vermeldingen: een die een programma met de naam "Example.exe" toevoegt aan de opstartlijst van Windows, en een andere die de "Verborgen" waarde in de geavanceerde instellingen van Windows Verkenner instelt op "true".

Reg-bestanden kunnen worden gemaakt en bewerkt met een teksteditor zoals Kladblok. Ze worden vaak gebruikt voor back-up- en hersteldoeleinden, maar ook voor het configureren van meerdere computers met dezelfde registerinstellingen.

## Importeer of exporteer het Windows-register

Een REG-bestand is een type bestand dat wordt gebruikt om gegevens uit het Windows-register te importeren of exporteren. Het Windows-register is een hiërarchische database waarin configuratie-instellingen en opties voor het Windows-besturingssysteem en geïnstalleerde applicaties worden opgeslagen. Het register bevat informatie zoals gebruikersvoorkeuren, applicatie-instellingen, hardware- en softwareconfiguratiegegevens en meer.

Reg-bestanden kunnen worden gebruikt om registervermeldingen te maken of te wijzigen, en worden vaak gebruikt voor back-up- en hersteldoeleinden, maar ook voor het configureren van meerdere computers met dezelfde registerinstellingen. U kunt als volgt een reg-bestand gebruiken om een nieuwe registervermelding aan het Windows-register toe te voegen:

1. Maak een nieuw tekstbestand met een teksteditor zoals Kladblok.
2. Typ de registervermelding in het juiste formaat. Het formaat bestaat uit een headersectie die het bestand identificeert als een registerbestand, gevolgd door een reeks sleutel- en waardeparen die registervermeldingen vertegenwoordigen. Hier is een voorbeeld:

```
Windows Registry Editor Version 5.00

[HKEY_CURRENT_USER\Software\Example]
"Setting1"="Value1"
```

Hiermee wordt een nieuwe sleutel gemaakt met de naam 'Voorbeeld' onder de sleutel 'Software' in de registercomponent van de huidige gebruiker, en wordt de waarde 'Setting1' ingesteld op 'Waarde1'.

3. Sla het bestand op met de bestandsextensie .reg.
4. Dubbelklik op het REG-bestand om de nieuwe registervermelding aan het Windows-register toe te voegen.

U wordt gevraagd te bevestigen dat u de vermelding aan het register wilt toevoegen. Zodra u bevestigt, wordt de nieuwe vermelding aan het register toegevoegd en kunt u deze verifiëren met de Register-editor.

## Referenties
* [Windows-register](https://en.wikipedia.org/wiki/Windows_Registry)

