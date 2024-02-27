{
  "date": "2021-06-29",
  "keywords": [
"CAB",
"udvidelse",
"fil",
"format",
"system",
"Windows kabinet fil",
"Microsoft",
"installatør",
"Opsætning",
"AdvPak"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "CAB - Windows Cabinet File",
  "description": "Lær om CAB-filformat og API'er, der kan oprette og åbne CAB-filer.",
  "linktitle": "CAB",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-ca-dab"
}
},
  "lastmod": "2021-06-29"
}

## Hvad er CAB fil? ##

En fil med filtypenavnet .cab tilhører en Windows-kabinetfil, der tilhører kategorien systemfiler. Det er en fil, der er gemt i arkivfilformatet i de versioner af Microsoft Windows, der understøtter komprimerede dataalgoritmer, såsom [LZX](/compression/lzx/), Quantum og [ZIP](/compression/zip/). Filen kommer i vital brug, når en bruger eller udvikler ønsker at indeholde og dele softwareinstallationsdata og filer. Funktionerne ved tabsfri datakomprimering og den digitale certificering, der er inkluderet i disse filer, gør denne fil perfekt til lagring og deling af sådanne filer. Det understøtter forskellige Microsoft-installationsprogrammer såsom Device Installer, SetUp API og AdvPak.

## Kort historie ##

CAB-fil er en datakomprimeringsfiltype, der er udviklet af Microsoft. Det blev oprindeligt kaldt Diamond, men siden blev det populært kendt som CAB-fil, kort for ordet Cabinet

## Teknisk specifikation ##

En CAB-fil kan normalt indeholde op til maksimalt 65535 mapper, som til gengæld maksimalt kan indeholde 65536 filer hver. CAB-fillagringsmekanismen er tids- og pladseffektiv, da den gemmer hver mappe som en komprimeret blok i stedet for at komprimere og gemme hver fil separat. Tomme mapper kan ikke gemmes i CAB-arkivmapper. CAB-fil blev først udviklet af Microsoft og bruges i forskellige installationsprogrammer, såsom InstallShield med et lidt anderledes format. CAB-filer er almindeligvis forbundet med selvudpakkende programmer. Microsoft CAB-filer er let genkendelige på grund af deres unikke markør, der hjælper med at identificere formatet. Den unikke markør for alle Microsoft CAB-filer er et fire-ords præfiks, MSCF. Når du ser denne kode, kan en bruger nemt skelne en Microsoft CAB-fil fra andre filer og bruge den i overensstemmelse hermed i kompressorer eller versioner. Filerne kan komprimeres med flere softwareinstallationsdata, eller de nuværende data kan dekomprimeres ved hjælp af den rigtige software.


## CAB Eksempel ##

Følgende eksempel illustrerer forholdet mellem filer og mapper i en CAB-filstruktur:

{{< figure src="../cab.png" alt="CAB filformat" >}}

## Reference ##

* [CAB - WIKIPEDIA](https://en.wikipedia.org/wiki/Cabinet_(file_format))
