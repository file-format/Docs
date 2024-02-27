{
  "date": "2021-08-13",
  "keywords": [
"sdi fil",
"sdi filformat",
"hvad er en sdi-fil",
"fil",
"sdi eksempel",
"sdi filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om SDI-filformat og API'er, der kan oprette og åbne SDI-filer.",
  "title": "SDI - Windows System Deployment Image File",
  "linktitle": "SDI",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-sd-dai"
}
},
  "lastmod": "2021-08-13"
}

## Hvad er en SDI fil?
Filen med .sdi-udvidelsen indeholder en load-blob, boot-blob og en del blob; almindeligvis brugt af Windows Embedded Studio til at oprette RAM-diske eller boot-diske til indlæsning og installation af Windows. SDI er forkortet til System Deployment Image. Windows Embedded Studio er et program, der bruges til at oprette diskbilleder til Windows. Faktisk indeholder dette program SDI File Manager-program og et kommandolinjeværktøj kaldet **sdimgr.exe**, begge kan bruges til at kopiere, oprette og redigere SDI-billeder.

## SDI filformat
SDI-filformatet er meget brugt til at muliggøre brugen af en virtuel disk til opstart af et system. Nogle versioner af Microsoft Windows aktiverer **RAM-opstart**, hvilket er vigtigt for at indlæse en SDI-fil i hukommelsen og derefter starte fra den. SDI-filformatet gør det også muligt for netværksstart ved at bruge PXE (Preboot Execution Environment). Det bliver også brugt til harddisk-billeddannelse.
### SDI-filsektioner
Selve SDI-filen kan underopdeles i følgende sektioner:
- **Boot BLOB**: Dette indeholder det faktiske opstartsprogram, STARTROM.COM. Dette er en analog til opstartssektoren på en harddisk.
- **Load BLOB**: Dette indeholder typisk NTLDR og startes af boot BLOB.
- **Del BLOB**: Dette indeholder den faktiske starttid; inkluderer også filerne boot.ini og ntdetect.com, som skal være placeret i rodmappen til runtime.
- **Disk BLOB**: Dette er et fladt HDD-billede, der starter med en MBR. Det bruges til harddisk-billeddannelse i stedet for at starte. Også kun Disk BLOB'er kan monteres med Microsofts hjælpeprogrammer.


## Referencer 

* [System Deployment Image - af Wikipedia](https://en.wikipedia.org/wiki/System_Deployment_Image)



