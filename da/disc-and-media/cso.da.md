{
  "date": "2021-08-09",
  "keywords": [
"cso fil",
"cso filformat",
"hvad er en cso-fil",
"fil",
"cso eksempel",
"cso filtypenavn",
"udvidelse",
"format",
"iso",
"DAX komprimering"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om CSO-filformat og API'er, der kan oprette og åbne CSO-filer.",
  "title": "CSO - komprimeret ISO-diskbillede",
  "linktitle": "CSO",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-cs-dao"
}
},
  "lastmod": "2021-08-09"
}

## Hvad er en CSO fil?

En fil med filtypen .cso er en komprimeret ISO-billedfil. CSO'en er et alternativ til DAX-komprimeringsmetoden; også kendt som CISO; var den første metode til at komprimere [ISO](/compression/iso/)-filerne og er normalt en foretrukken metode til at arkivere PlayStation Portable-ting. Dette format bruger Deflate-komprimering, som kan omfatte op til ni komprimeringslag. Software som Prometheus og YACC bruges til at skabe billederne.

## CSO filformat

CSO-filformatet var den første komprimeringsmetode til ISO for at spare mere hukommelsesplads. Forbedringerne blev foretaget fra tid til anden for bedre komprimering. CSO'en bruger Deflate-komprimering med ni niveauer af forudindstillinger, normalt kan hvert niveau håndtere 2 KiB-blokke individuelt. Mens de højeste niveauer af komprimering kan sænke og langvarige indlæsningstider i software, som i høj grad afhænger af diskstreaming, kan også de lavere niveauer udføre betydelig komprimering.

### CSO-filstruktur

CSO-filformatet indeholder en 24-byte header, datablokke og en indekstabel. Little-endian antages for felter større end en byte. PlayStation Portables arkitektur-endelighed er angivet nedenfor.

#### Header

| Offset (bytes) | Navn | Størrelse (bytes) | Formål |
----------|----------|--------------|---------|
| 0x0 | Magi | 4 | Altid CISO eller 0x4F534943, når det læses som et 32-bit heltal. Dette felt bruges til at identificere en CSO-fil. Bemærk, at dette felt kan være anderledes for de andre derivater af CSO, for eksempel brugte ZSO den magiske kode ZISO. |
| 0x4 | Overskriftstørrelse | 4 | For det originale CSO v1-filformat ignoreres dette felt og er derfor ikke nødvendigt at være nøjagtigt. v2 og ZSO-formatet kræver dog, at dette felt altid er 0x18 (24 bytes). |
| 0x8 | Ukomprimeret størrelse | 8 | Størrelsen af den originale ukomprimerede ISO i bytes. |
| 0x10 | Blokstørrelse | 4 | Størrelsen af hver datablok i bytes før komprimering. Normalt 2048 bytes, det samme som størrelsen af hver ISO 9660-sektor. |
| 0x14 | Version | 1 | The version of the file format in use. For the "v1" format, the value can be either 0 or 1. For v2-formatet skal dette være 2. Derudover kræver ZSO-formatet, at dette er 1. |
| 0x15 | Indeksjustering | 1 | Justeringen af hver indeksindgang, angivet i bit. |
| 0x16 | Reserveret | 2 | Dette felt er ubrugt. I v1-formatet ignoreres dette felt og kan indeholde vilkårlige værdier. I v2-formatet skal dette felt være nul. |

#### Indekstabel

Indekstabellen indeholder flere 4-byte poster, som angiver positionen af hver datablok, og en yderligere, sidste post, som peger mod slutningen af filen.
Indholdet af hver post er som følger:
| Bit | Længde | Maske | Navn | Formål |
-----|-----|----|-------|------------|
| 0 | 31 | 0x7FFFFFFF | Stilling | Dette felt, når det flyttes til venstre af indeksjusteringen angivet i overskriften, afgiver den position, hvor datablokken starter. |
| 31 | 1 | 0x80000000 | Kompressionstype | ZSO-formatet har lignende semantik, kun at 0 repræsenterer LZ4 i stedet for Deflate. I v2 format. Blokken anses implicit for at være ukomprimeret, hvis blokstørrelsen er lig med eller større end den blokstørrelse, der er angivet i filoverskriften. |

#### Datablokke

Datablokkene består af de ukomprimerede eller komprimerede data. Størrelsen af en blok beregnes ved at få dens position og derefter trække den fra positionen for den efterfølgende blok. Hvis indeksjusteringen er større end nul, er det sandsynligt, at blokstørrelsen er større end de data, den indeholder.


## Referencer 

* Ikke tilgængelig


