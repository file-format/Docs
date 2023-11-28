{
"datum": "2023-06-08",
  "keywords": [
"crx-bestand",
"wat is een crx-bestand",
"hoe crx-bestand te installeren in Google Chrome",
"hoe crx-bestand te openen",
"wat bevat het crx-bestand",
"wat is het formaat van het crx-bestand",
"bestand",
"crx bestandsextensie",
"verlenging"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title":"CRX-bestandsindeling - Google Chrome-extensie",
  "description":"Leer meer over het CRX-formaat en API's waarmee CRX-bestanden kunnen worden gemaakt en geopend.",
"linktitle": "CRX",
  "menu": {
    "docs": {
      "identifier": "misc-crx",
"parent" : "misc"
}
},
"laatste mod": "2023-06-08"
}

## Wat is een CRX-bestand?

CRX-bestandsindeling is gekoppeld aan Google Chrome-browserextensies. Een CRX-bestand is in wezen een gecomprimeerd pakket dat de benodigde bestanden en metagegevens bevat om een extensie te installeren en uit te voeren in Google Chrome. Het verbetert de functionaliteit of het uiterlijk van een webbrowser door een extra functie of thema te bieden.

Wanneer een CRX-bestand wordt gedownload en geïnstalleerd in Google Chrome, verifieert de browser de integriteit van de extensie met behulp van de openbare sleutel en handtekening. Als de verificatie succesvol is, extraheert Chrome de inhoud van het CRX-bestand en installeert de extensie, zodat deze beschikbaar wordt voor gebruik. Gebruikers kunnen hun extensies beheren via de Chrome-extensiespagina, waarmee geïnstalleerde extensies kunnen worden ingeschakeld, uitgeschakeld of verwijderd.

## Hoe CRX-bestand in Google Chrome installeren?

Om een CRX-bestand in Google Chrome te installeren, kunt u deze stappen volgen:

1. Open de Chrome-browser.
2. Typ `chrome://extensions` in de adresbalk en druk op Enter.
3. Schakel de tuimelschakelaar voor de "Ontwikkelaarsmodus" in de rechterbovenhoek van de pagina Extensies in.
4. Klik op de knop "Uitgepakt laden".
5. Zoek en selecteer de map met de uitgepakte inhoud van het CRX-bestand (of selecteer eenvoudigweg het CRX-bestand zelf).
6. Klik op "Openen" om de extensie te installeren.

## Wat bevat het CRX-bestand?

Een CRX-bestand bevat de noodzakelijke bestanden en metagegevens die vereist zijn voor de Google Chrome-extensie. Hier volgt een overzicht van de typische inhoud van een CRX-bestand:

- **Manifestbestand (manifest.json):** Dit bestand is een JSON-geformatteerd bestand dat informatie bevat over de extensie, zoals de naam, versie, beschrijving, machtigingen en achtergrondscripts. Het definieert de structuur en het gedrag van de extensie.
- **JavaScript-bestanden:** Deze bestanden bevatten de code die de functionaliteit van de extensie definieert. Ze kunnen scripts bevatten voor het afhandelen van gebeurtenissen, het aanpassen van webpagina's of de interactie met de API's van Chrome.
- **HTML-, CSS- en afbeeldingsbestanden:** Extensies bevatten vaak elementen van de gebruikersinterface, zoals pop-upvensters of optiepagina's. HTML-bestanden definiëren de structuur van deze interfaces, terwijl CSS-bestanden hun uiterlijk bepalen. Afbeeldingsbestanden worden gebruikt voor pictogrammen of andere grafische elementen.
- **Optionele bronbestanden:** Extensies kunnen extra bronnen bevatten, zoals lokalisatiebestanden voor de ondersteuning van meerdere talen. Deze bestanden bevatten vertalingen van tekst die wordt gebruikt in de gebruikersinterface van de extensie.
- **Achtergrondscripts:** Als een extensie achtergrondprocessen of scripts heeft die onafhankelijk van de actieve webpagina worden uitgevoerd, worden deze scripts opgenomen in het CRX-bestand.
- **Inhoudsscripts:** Inhoudsscripts zijn scripts die in webpagina's kunnen worden geïnjecteerd om hun gedrag te wijzigen of om met hun inhoud te communiceren. Als de extensie inhoudsscripts gebruikt, zullen de benodigde bestanden voor die scripts aanwezig zijn in het CRX-bestand.
- **Andere middelen:** Afhankelijk van de specifieke vereisten van de extensie kunnen extra bestanden, zoals audio- of videobestanden, lettertypen of gegevensbestanden, worden opgenomen.

Het CRX-bestandsformaat is in wezen een gecomprimeerd pakket dat al deze bestanden en mappen op een gestructureerde manier bevat. Wanneer het CRX-bestand in Google Chrome wordt geïnstalleerd, extraheert de browser de inhoud en plaatst deze op de juiste locaties, waardoor de extensie kan worden geladen en uitgevoerd in de browser.

## Wat is het formaat van een CRX-bestand?

Het CRX-bestandsformaat is een specifiek formaat voor het verpakken en distribueren van Google Chrome-extensies. Het is in wezen een gecomprimeerd ZIP-archief met verschillende bestandsextensies. De basisstructuur van het CRX-bestand is als volgt:

- **Bestandshandtekening:** De eerste 4 bytes van het bestand bevatten het magische getal "Cr24" (hexadecimaal: 43 72 32 34) dat dient als handtekening om het bestand te identificeren als CRX-bestand.
- **Versienummer:** De volgende 4 bytes vertegenwoordigen het versienummer van het CRX-formaat.
- **Lengte openbare sleutel:** De volgende 4 bytes geven de lengte aan van de gecodeerde openbare sleutel die wordt gebruikt voor verificatie van de handtekening van de extensie.
- **Handtekeninglengte:** De volgende 4 bytes specificeren de lengte van de handtekening van de extensie.
- **Openbare sleutel:** Deze sectie bevat de gecodeerde openbare sleutel die wordt gebruikt voor het verifiëren van de integriteit van de extensie.
- **Handtekening:** Deze sectie bevat de handtekening van de extensie, die wordt gegenereerd door de inhoud van de extensie te ondertekenen met een privésleutel die overeenkomt met de hierboven genoemde openbare sleutel.
- **ZIP-archief:** De resterende bytes van het CRX-bestand vormen een gecomprimeerd ZIP-archief. Dit archief bevat alle benodigde bestanden en extensiemappen, inclusief manifestbestanden, JavaScript-bestanden, HTML-bestanden, CSS-bestanden, afbeeldingen en andere bronnen.

## Referenties
* [CRX-formaatspecificatie](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/K3YIsNL_Et4)

