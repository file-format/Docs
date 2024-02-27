{
  "date": "2021-08-31",
  "keywords": [
"xbe fil",
"xbe filformat",
"hvad er en xbe fil",
"fil",
"xbe eksempel",
"xbe filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om XBE-filformat og API'er, der kan oprette og åbne XBE-filer.",
  "title": "XBE - iOS Application Package File",
  "linktitle": "XBE",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-xb-dae"
}
},
  "lastmod": "2021-08-31"
}

## Hvad er en XBE fil?
En fil med filtypenavnet .xbe er et eksekverbart program fra en Xbox-videospilsdisk. XBE-filerne er hovedfilerne, der udføres i Xbox-systemet, og det er ikke meningen, at de normalt skal åbnes på en computer, men de kan åbnes på en pc ved hjælp af et Xbox-emuleringsprogram. Disse filer er normalt oprettet af spiludviklere og derefter underskrevet af Microsoft. Filstrukturen ligner Windows PE-filerne, men nogle vigtige ændringer i henhold til XBox-indstillingerne anvendes for at gøre den kørebar på XBox.

## XBE filformat
XBE-filen er sammensat af en billedoverskrift, en samling af sektionsoverskrifter, et certifikat, lokale trådlagringsdata, en samling af biblioteksversioner, Microsoft bitmap og de sektioner, der indeholder koden og ressourcerne.

### Billedoverskrift
Billedhovedet omfatter informationen, der forklarer, hvor de andre komponenter af den eksekverbare er placeret i filen, og hvordan den runnable skal behandles og indlæses.

### TLS-tabel
TLS-tabellen består af al den information, som XBE'en behøver for korrekt opsætning af trådlokalt lager. Det er dybest set unikt for TLS-kataloget, der findes i PE32-filer, og kan kopieres direkte derfra. Denne tabel kan udelades, hvis XBE-filen ikke bruger nogen tråd-lokal lagring, og det respektive felt i billedhovedet er sat til nul.

| Offset | Størrelse | Navn | Beskrivelse |
--------|--------|--------|------------|
| 0x0000 | 0x0004 | Rådata Start | Absolut (dvs. ikke en RVA) adresse for start af TLS variable data i programbilledet. |
| 0x0004 | 0x0004 | Rådata slut | Absolut (dvs. ikke en RVA) adresse for slutningen af TLS variable data i programbilledet. |
| 0x0008 | 0x0004 | Indeksadresse | Absolut (dvs. ikke en RVA) adresse for TLS Index-variablen. |
| 0x000C | 0x0004 | Adresse på tilbagekald | Absolut (dvs. ikke en RVA) adresse for den nulterminerede TLS-tilbagekaldsfunktionstabel. |
| 0x0010 | 0x0004 | Størrelse af Zero Fyld | Antallet af bytes efter de rå data, der skal sættes til nul i hukommelsen. |
| 0x0014 | 0x0004 | Karakteristika | Beskriver justering. |

### Certifikat

 A a certificate is mandatory for each Xbox executable that contains information about the titles:
 
- Tid og dato, hvor certifikatet blev oprettet
- Titel-id
- Titelnavn
- Alternative titel-id'er
- Tilladte typer medier, som den eksekverbare kan køres fra (HD, DVD, CD osv.)
- Vildt område
- Spilbedømmelser
- Disknummer
- Version
- LAN nøgle rådata brugt til System Link
- Signaturnøglerådata (bruges til at signere savegames)
- Alternative signaturnøgler
- Certifikatets originale størrelse
- Onlinetjenestenavn (ikke til stede i tidlige eksekverbare filer)
- Køretidssikkerhedsflag (ikke til stede i tidlige eksekverbare filer)
 
### Tilladte medietyper
Medietyper, som tillades af den eksekverbare fil at blive kørt fra. Følgende værdier er kendt:
| Medietype | Værdi |
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

### Afsnit
Sektionerne er udtrykt ved sektionsoverskrifterne. Sektionsoverskrifterne starter lige efter certifikatet og indeholder oplysninger om, hvor i filen de faktiske sektioner findes. Mindst to sektioner er altid til stede i en Xbox-eksekverbar:
- .tekst
- .rdata


## Referencer 

* [Xbe - XBox Executable](https://xboxdevwiki.net/Xbe)



