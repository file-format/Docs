{
  "date": "2023-06-08",
  "keywords": [
"crx fil",
"hvad er en crx-fil",
"hvordan man installerer crx-fil i google chrome",
"hvordan man åbner crx fil",
"hvad indeholder crx-filen",
"hvad er formatet på crx-filen",
"fil",
"crx filtypenavn",
"udvidelse"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "CRX-filformat - Google Chrome-udvidelse",
  "description": "Lær om CRX-format og API'er, der kan oprette og åbne CRX-filer.",
  "linktitle": "CRX",
  "menu": {
    "docs": {
      "identifier": "misc-crx-da",
      "parent": "misc"
}
},
  "lastmod": "2023-06-08"
}

## Hvad er en CRX fil?

CRX-filformat er forbundet med Google Chrome-browserudvidelser. En CRX-fil er i bund og grund en komprimeret pakke, der indeholder nødvendige filer og metadata til, at en udvidelse kan installeres og køres i Google Chrome. Det forbedrer funktionaliteten eller udseendet af en webbrowser ved at tilbyde en ekstra funktion eller et tema.

Når en CRX-fil downloades og installeres i Google Chrome, verificerer browseren udvidelsens integritet ved hjælp af offentlig nøgle og signatur. Hvis bekræftelsen lykkes, udpakker Chrome indholdet af CRX-filen og installerer udvidelsen, så den er tilgængelig til brug. Brugere kan administrere deres udvidelser via Chrome Extensions-siden, som gør det muligt at aktivere, deaktivere eller fjerne installerede udvidelser.

## Sådan installeres CRX-fil i Google Chrome?

For at installere en CRX-fil i Google Chrome, kan du følge disse trin:

1. Åbn Chrome-browseren.
2. Skriv 'chrome://extensions' i adresselinjen, og tryk på Enter.
3. Aktiver Udviklertilstand-vippekontakten i øverste højre hjørne af udvidelsessiden.
4. Klik på knappen Indlæs udpakket.
5. Find og vælg mappen, der indeholder det udpakkede indhold af CRX-filen (eller vælg blot selve CRX-filen).
6. Klik på Åbn for at installere udvidelsen.

## Hvad indeholder CRX fil?

En CRX-fil indeholder nødvendige filer og metadata, der kræves til Google Chrome-udvidelsen. Her er en oversigt over typisk indhold fundet i en CRX-fil:

- **Manifest file (manifest.json):** This file is a JSON-formatted file that includes information about extension such as its name, version, description, permissions and background scripts. It defines the structure and behavior of extension.
- **JavaScript-filer:** Disse filer indeholder koden, der definerer udvidelsens funktionalitet. De kan omfatte scripts til håndtering af begivenheder, ændring af websider eller interaktion med Chromes API'er.
- **HTML, CSS og billedfiler:** Udvidelser inkluderer ofte brugergrænsefladeelementer, såsom pop op-vinduer eller indstillingssider. HTML-filer definerer strukturen af disse grænseflader, mens CSS-filer styrer deres udseende. Billedfiler bruges til ikoner eller andre grafiske aktiver.
- **Valgfri ressourcefiler:** Udvidelser kan omfatte yderligere ressourcer, såsom lokaliseringsfiler til understøttelse af flere sprog. Disse filer indeholder oversættelser af tekst, der bruges i udvidelsens brugergrænseflade.
- **Baggrundsscripts:** Hvis en udvidelse har baggrundsprocesser eller scripts, der kører uafhængigt af den aktive webside, vil disse scripts blive inkluderet i CRX-filen.
- **Indholdsscripts:** Indholdsscripts er scripts, der kan injiceres på websider for at ændre deres adfærd eller interagere med deres indhold. Hvis udvidelsen bruger indholdsscripts, vil de nødvendige filer til disse scripts være til stede i CRX-filen.
- **Andre aktiver:** Afhængigt af specifikke krav til udvidelse kan yderligere filer såsom lyd- eller videofiler, skrifttyper eller datafiler inkluderes.

CRX-filformatet er i det væsentlige en komprimeret pakke, der indeholder alle disse filer og mapper på en struktureret måde. Når CRX-filen er installeret i Google Chrome, udtrækker browseren indholdet og placerer det på passende steder, så udvidelsen kan indlæses og køres i browseren.

## Hvad er formatet på filen CRX?

CRX-filformatet er specifikt format til pakning og distribution af Google Chrome-udvidelser. Det er i bund og grund et komprimeret ZIP-arkiv med forskellige filtypenavne. Den grundlæggende struktur af CRX-fil er som følger:

- **Filsignatur:** De første 4 bytes af filen indeholder det magiske nummer Cr24 (hexadecimal: 43 72 32 34), der tjener som signatur for at identificere filen som CRX-fil.
- **Versionsnummer:** De næste 4 bytes repræsenterer versionsnummeret af CRX-formatet.
- **Længde på den offentlige nøgle:** De følgende 4 bytes angiver længden af den kodede offentlige nøgle, der bruges til verificering af udvidelsessignatur.
- **Signaturlængde:** De efterfølgende 4 bytes angiver længden på signaturen for udvidelsen.
- **Offentlig nøgle:** Dette afsnit indeholder den kodede offentlige nøgle, der bruges til at verificere integriteten af udvidelsen.
- **Signatur:** Denne sektion indeholder signatur af udvidelse, som genereres ved at signere udvidelsens indhold ved hjælp af en privat nøgle svarende til den offentlige nøgle nævnt ovenfor.
- **ZIP-arkiv:** De resterende bytes af CRX-filen omfatter et komprimeret ZIP-arkiv. Dette arkiv indeholder alle nødvendige filer og mapper med udvidelse, inklusive manifestfil, JavaScript-filer, HTML-filer, CSS-filer, billeder og andre ressourcer.

## Referencer
* [CRX-formatspecifikation](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/K3YIsNL_Et4)


