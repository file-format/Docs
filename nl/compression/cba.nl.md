{
"datum": "24-05-2023",
  "keywords": [
"cba-bestand",
"wat is een cba-bestand",
"hoe een CBA-bestand te maken",
"wat bevat het CBA-bestand",
"wat is het formaat van het cba-bestand",
"bestand",
"cba bestandsextensie",
"verlenging"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title":"CBA Bestandsformaat - Stripboekenarchief",
  "description":"Leer meer over het CBA-formaat en API's waarmee CBA-bestanden kunnen worden gemaakt en geopend.",
"linktitle":"CBA",
  "menu": {
    "docs": {
      "identifier": "compression-cba",
"parent":"compressie"
}
},
"laatste mod": "24-05-2023"
}

## Wat is een CBA-bestand?

Een Comic Book Archive-bestand (CBA), ook wel Comic Book Archive of Comic Book Reader-bestand genoemd, is een populair formaat dat wordt gebruikt voor het opslaan en distribueren van digitale stripboeken. Het bevat doorgaans een verzameling afzonderlijke stripboekpagina's of afbeeldingen die in één bestand zijn gebundeld voor eenvoudige organisatie en lezen.

Een van de gebruikelijke formaten voor het maken van stripboekarchiefbestanden is het TAR-formaat (Tape Archive). TAR is een bestandsarchiveringsformaat dat wordt gebruikt in Unix- en Linux-omgevingen. Het combineert meerdere bestanden in één bestand dat vaak wordt gebruikt voor back-updoeleinden.

## Hoe maak ik een CBA-bestand?

Om een Comic Book Archive-bestand te maken met behulp van de TAR-archiveringstool, volgt u doorgaans deze stappen:

1. Verzamel alle stripboekpagina's of afbeeldingen die u in het archief wilt opnemen.
2. Open een opdrachtprompt of terminalvenster.
3. Navigeer naar de map waar stripboekpagina's/afbeeldingen zich bevinden.
4. Gebruik de TAR-opdracht met de juiste opties om het archief te maken. De opdracht kan er bijvoorbeeld als volgt uitzien:

```
tar -cf comicbook.cbt page1.jpg page2.jpg page3.jpg
```

In dit voorbeeld vertelt de optie -c aan TAR om een nieuw archief te maken en specificeert de optie -f de naam van het uitvoerbestand (in dit geval comicbook.cbt). Nadat u de opties heeft opgegeven, geeft u de namen op van de bestanden die u in het archief wilt opnemen (pagina1.jpg, pagina2.jpg, pagina3.jpg).

5. Na het uitvoeren van de opdracht maakt de TAR-tool het Comic Book Archive-bestand (stripbook.cbt in dit voorbeeld) in de huidige map.

Zodra u een Comic Book Archive-bestand heeft, kunt u verschillende stripboeklezersoftware of -applicaties gebruiken om stripboeken op uw computer of apparaat te openen en te lezen. Deze toepassingen bieden doorgaans functies zoals paginanavigatie, zoomen en bladwijzers om de leeservaring te verbeteren.

## Wat bevat het CBA-bestand?

Een Comic Book Archive-bestand (CBA) dat is gemaakt met de TAR-archiveringstool, bevat een verzameling afzonderlijke stripboekpagina's of afbeeldingen, samengebundeld in één bestand. De specifieke inhoud van het archief is afhankelijk van het stripboek dat wordt verpakt.

Normaal gesproken bevat een stripboekarchiefbestand het volgende:

- **Stripboekpagina's:** De belangrijkste inhoud van het archief zijn de stripboekpagina's zelf. Deze pagina's worden meestal opgeslagen als afzonderlijke afbeeldingsbestanden, zoals JPEG of PNG, die elke pagina van het stripboek vertegenwoordigen. De pagina's zijn in een specifieke volgorde gerangschikt om de verhaalstroom van de strip te behouden.
- **Metadata:** Sommige stripboekarchiefformaten kunnen metadata over het stripboek bevatten, zoals de titel, auteur, uitgever, publicatiedatum en beschrijving. Deze informatie helpt bij het identificeren en categoriseren van het stripboek.
- **Extra bestanden:** Naast de stripboekpagina's en metadata kan het archief andere aanvullende bestanden bevatten die verband houden met het stripboek. Deze bestanden kunnen albumhoezen, promotieafbeeldingen, bonusinhoud of tekstbestanden bevatten met aanvullende informatie of commentaar.

## Wat is het formaat van een CBA-bestand?

Het Comic Book Archive (CBA)-bestandsformaat dat is gemaakt met de TAR-archiveringstool, heeft doorgaans de TAR-indeling. TAR, een afkorting van Tape Archive, is een bestandsarchiveringsformaat dat veel wordt gebruikt in Unix- en Linux-systemen. Het is niet specifiek voor stripboeken, maar is een archiveringsformaat voor algemene doeleinden.

Het TAR-formaat is een eenvoudige manier om meerdere bestanden in één archiefbestand te bundelen. Het biedt zelf geen compressie, dus het resulterende TAR-bestand kan groot zijn in vergelijking met andere gecomprimeerde formaten zoals ZIP of RAR. TAR-bestanden kunnen echter worden gecomprimeerd met behulp van aanvullende tools of worden gecombineerd met compressie-algoritmen zoals gzip of bzip2 om de bestandsgrootte te verkleinen.

Het TAR-formaat behoudt de bestandsstructuur, bestandsrechten en tijdstempels van de opgenomen bestanden. Het slaat bestanden opeenvolgend op in het archief, waardoor eenvoudige extractie van individuele bestanden of het hele archief mogelijk is.

## Referenties
* [Stripboekenarchief](https://en.wikipedia.org/wiki/Comic_book_archive)

