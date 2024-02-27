{
  "date": "2021-06-30",
  "keywords": [
"mst fil",
"mst filformat",
"hvad er en mst-fil",
"fil",
"mst eksempel",
"mst filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om MST-filformat og API'er, der kan oprette og åbne MST-filer.",
  "title": "MST - Windows Installer Package File",
  "linktitle": "MST",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-ms-dat"
}
},
  "lastmod": "2021-06-30"
}

## Hvad er en MST fil?
Filerne med filtypenavnet .mst bruges til at transformere indholdet af en MSI-pakke. De bruges almindeligvis af systemadministratorer til at anvende de brugerdefinerede indstillinger på en eksisterende MSI-fil. MST-filerne bruges sammen med den originale MSI-pakke i deres softwaredistributionssystemer såsom gruppepolitikker. MST-filer bruges generelt i softwareudvikling og -test til at konfigurere deres under udviklingsversioner af softwaren.

## MST filformat
En MST- eller Transform-fil bruges til at samle installationsmulighederne for programmer, der bruger Microsoft Windows Installer, i en fil. Disse filer bruges almindeligvis på kommandolinjen Installer (MSIEXEC.EXE) eller bruges i en gruppepolitik for softwareinstallation; i et Microsoft Active Directory-domæne. MST-filerne kan også bruges med indpakkede eksekverbare installationsprogrammer. Et generelt tilfælde er, at nogen ønsker at videregive kommandolinjeparametre til det indpakkede installationsprogram. For at gøre det skal du bruge en MST-fil, der tilføjer egenskaben WRAPPED_ARGUMENTS til egenskabstabellen. Disse filer kan ikke oprettes eller redigeres ved hjælp af generelle editorer. Specifikke værktøjer er tilgængelige til dette formål.

### Hvordan bruger man MST-filer?
MST-filerne kan genereres ved at bruge forskellige værktøjer, og Ocra bruges generelt til at generere MST-filer. Derefter kan indstillinger tilpasses efter behov og gemme dem på et bestemt sted. Derefter kan MST-filerne bruges sammen med MSI-filer. Hvis du vil teste disse filer; brug følgende syntaks på kommandolinjen

```
msiexec /i setup_1.0.msi TRANSFORMS=mylog.mst
```
### TRANSFORMER egenskab

Du kan også bruge **TRANSFORMS**-egenskaben til Windows-installationsprogrammet, som faktisk er en liste over de transformationer, som installationsprogrammet anvender, når pakken installeres. Installationsprogrammet udfører transformationerne i samme rækkefølge, som de er angivet i TRANSFORM-egenskaben. Transformers kan angives ved filnavn med filtypenavnet .mst eller fuld sti. For at angive mere end én transformation skal du adskille hvert filnavn eller et semikolon som følgende eksempel.

```
TRANSFORMS=transform1.mst;transform2.mst;transform3.mst
```

## Referencer 

* [MST Transformation Files](https://www.exemsi.com/documentation/mst-transformation-files/)

* [TRANSFORMER egenskab](https://learn.microsoft.com/en-us/windows/win32/msi/transforms)



