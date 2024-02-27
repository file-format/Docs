{
  "date": "2021-07-16",
  "keywords": [
"ins fil",
"ins filformat",
"hvad er en ins-fil",
"fil",
"ins eksempel",
"ins filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om INS-filformater og API'er, der kan oprette og åbne INS-filer.",
  "title": "INS - Internetindstillingsfil",
  "linktitle": "INS",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-in-das"
}
},
  "lastmod": "2021-07-16"
}

## Hvad er en INS fil?

Filen med filtypenavnet .ins bruges generelt af Microsoft Windows til opsætning af opkalds- og bredbåndsinternetforbindelser. Faktisk indeholder den forbindelsesopsætningsoplysninger, der gør det muligt for Windows at konfigurere internetadgang til en internetudbyder. En INS-fil bruges almindeligvis til at konfigurere Internet Explorer (IE) LAN-forbindelsesindstillinger. IE-forbindelsesindstillingsfilerne leveres nogle gange af internetudbyderne og systemadministratorerne til brugerne med en URL til INS-filen.

## INS filformat
Du kan bruge internetindstillingsfilerne (INS) sammen med Internet Explorer Administration Kit 11 (IEAK 11) til at konfigurere din brugerdefinerede browser og dens komponenter. Du kan skrive forskellige versioner af din brugerdefinerede pakke ved at tilpasse kopier af INS-filen.

### Mulige INS-indstillinger
De mulige INS-indstillinger er angivet i følgende tabel:

| Indstilling | Beskrivelse |
-----|---------|
| URL | Om der skal bruges en automatisk konfigureret proxyserver. |
| Branding | Tilpas branding og opsætningsoplysninger i din browserpakke. |
| Medier | Medietyper, hvor din brugerdefinerede installationspakke er tilgængelig. |
| Browserværktøjslinjer | Tilpas udseendet af IE-værktøjslinjen. |
| CabSigning | Digital signaturoplysninger for dine programmer. |
| HideCustom | Om den globalt unikke identifikator (GUID) skal skjules for hver tilpasset komponent. |
| Forbindelsesindstillinger | Info om netværksforbindelsesindstillingerne, der bruges til at installere din brugerdefinerede pakke. |
| CustomBranding | URL-placering til din branding-kabinet-fil (.cab). |
| ExtRegInf | Navne på dine installationsinformationsfiler (.inf) og installationstilstanden for komponenter. |
| FavoritterEx | Tilføj en sti til din ikonfil for Favoritter, beslut om Favoritter er tilgængelige offline, og tilføj URL'er til hvert Foretrukne websted. |
| ISP_Sikkerhed | Rodcertifikatet, du føjer til din tilpassede pakke. |
| Fuldmagt | Om der skal bruges en proxyserver. |
| Sikkerhedsimport | Om du skal importere sikkerhedsoplysninger til din tilpassede pakke. |




## Referencer 

* [Brug af internetindstillingsfiler (.INS) med IEAK 11](https://learn.microsoft.com/en-us/internet-explorer/ie11-ieak/using-internet-settings-ins-files)



