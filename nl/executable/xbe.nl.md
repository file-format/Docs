{
  "date" : "2021-08-31",
  "keywords" :[ "xbe file", "xbe file format", "wat is een xbe file", "file", "xbe example", "xbe file extension","extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Meer informatie over XBE-bestandsindeling en API's die XBE-bestanden kunnen maken en openen.",
  "title" :"XBE - iOS-toepassingspakketbestand",
  "linktitle" : "XBE",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-31"
}

## Wat is een XBE-bestand?
Een bestand met de extensie .xbe is een uitvoerbare toepassing van een Xbox-videogameschijf. De XBE-bestanden zijn de belangrijkste bestanden die worden uitgevoerd in het Xbox-systeem en die normaal gesproken niet op een computer mogen worden geopend, maar kunnen op een pc worden geopend met behulp van een Xbox-emulatieprogramma. Deze bestanden worden meestal gemaakt door game-ontwikkelaars en vervolgens ondertekend door Microsoft. De bestandsstructuur is vergelijkbaar met de Windows PE-bestanden, maar er zijn enkele belangrijke wijzigingen volgens de XBox-instellingen toegepast om het op XBox te laten werken.

## XBE-bestandsindeling
Het XBE-bestand bestaat uit een afbeeldingskop, een verzameling sectiekoppen, een certificaat, lokale opslaggegevens voor threads, een verzameling bibliotheekversies, Microsoft-bitmap en de secties die de code en bronnen bevatten.

### Afbeeldingskop
De afbeeldingskop bevat de informatie die uitlegt waar de andere componenten van het uitvoerbare bestand zich in het bestand bevinden en hoe het uitvoerbare bestand moet worden behandeld en geladen.

### TLS-tabel
De TLS-tabel bevat alle informatie die de XBE nodig heeft om thread-local storage correct in te stellen. Het is in principe uniek voor de TLS-directory die wordt gevonden in PE32-bestanden en kan van daaruit rechtstreeks worden gekopieerd. Deze tabel kan worden weggelaten als het XBE-bestand geen lokale threadopslag gebruikt en het respectieve veld in de afbeeldingskop op nul wordt gezet.

| Verschuiving | Maat | Naam | Beschrijving |
--------|--------|--------|------------|
| 0x0000 | 0x0004 | Ruwe gegevens starten | Absoluut (dus geen RVA) adres van start van de TLS variabele data in het programmabeeld. |
| 0x0004 | 0x0004 | Einde van onbewerkte gegevens | Absoluut (dwz geen RVA) adres van het einde van de TLS-variabele gegevens in het programmabeeld. |
| 0x0008 | 0x0004 | Adres van Index | Absoluut (dus geen RVA) adres van de TLS Index-variabele. |
| 0x000C | 0x0004 | Adres van terugbelverzoeken | Absoluut (dwz geen RVA) adres van de TLS-callback-functietabel met null-terminated. |
| 0x0010 | 0x0004 | Grootte van nulvulling | Het aantal bytes na de onbewerkte gegevens dat in het geheugen op nul moet worden gezet. |
| 0x0014 | 0x0004 | Kenmerken | Beschrijft uitlijning. |

### Certificaat

Een a-certificaat is verplicht voor elk Xbox-uitvoerbaar bestand dat informatie over de titels bevat:
 


- Tijd en datum waarop het certificaat is gemaakt
- Titel-ID
- Titel
- Alternatieve titel-ID's
- Toegestane soorten media waarvan het uitvoerbare bestand kan worden uitgevoerd (HD, DVD, CD, enz.)
- Spelregio
- Spelbeoordelingen
- Schijfnummer
- Versie
- LAN-sleutel onbewerkte gegevens gebruikt voor System Link
- Signature key ruwe data (gebruikt om savegames te ondertekenen)
- Alternatieve handtekeningsleutels
- Originele grootte van het certificaat
- Online servicenaam (niet aanwezig in vroege uitvoerbare bestanden)
- Runtime-beveiligingsvlaggen (niet aanwezig in vroege uitvoerbare bestanden)
 


### Toegestane mediatypen
Mediatypen waarvan het uitvoerbare bestand mag worden uitgevoerd. De volgende waarden zijn bekend:
| Mediatype | Waarde |
---------------------|------------|
| HARD_DISK | 0x00000001 |
| DVD_X2 | 0x00000002 |
| DVD_CD | 0x00000004 |
| CD | 0x00000008 |
| DVD_5_RO | 0x00000010 |
| DVD_9_RO | 0x00000020 |
| DVD_5_RW | 0x00000040 |
| DVD_9_RW | 0x00000080 |
| DONGLE | 0x00000100 |
| MEDIA_BOARD | 0x00000200 |
| NONSECURE_HARD_DISK | 0x40000000 |
| NONSECURE_MODE | 0x80000000 |
| MEDIA_MASK | 0x00FFFFFF |

### Secties
De secties worden uitgedrukt door de sectiekoppen. De sectiekoppen beginnen direct na het certificaat en bevatten informatie waar in het bestand de daadwerkelijke secties voorkomen. Er zijn altijd ten minste twee secties aanwezig in een uitvoerbaar bestand van Xbox:


- .tekst


- .rdata


## Referenties



* [Xbe - XBox-uitvoerbaar bestand](https://xboxdevwiki.net/Xbe)


