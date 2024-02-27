{
  "date": "2021-08-11",
  "keywords": [
"wim fil",
"wim filformat",
"hvad er en wim-fil",
"fil",
"wim eksempel",
"wim filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om WIM-filformater og API'er, der kan oprette og åbne WIM-filer.",
  "title": "WIM - Windows Imaging Format File",
  "linktitle": "WIM",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-wi-dam"
}
},
  "lastmod": "2021-08-11"
}

## Hvad er en WIM fil?
Filerne med .wim-udvidelser blev første gang set i Windows Vista. WIM tilhører et filbaseret billedformat, som typisk blev introduceret i Microsoft Windows Vista. Det gør det muligt at implementere et enkelt diskbillede til forskellige computerplatforme. WIM-filer bruges til at administrere filer såsom opdateringer, drivere og komponenter uden at genstarte operativsystembilledet. AQ WIM-filen indeholder et sæt filer og tilhørende metadata, som minder meget om andre diskfilformater.

## WIM filformater
WIM-filformatet er ikke som sektorbaserede formater som VHD eller IS, faktisk er det filbaseret, hvilket betyder, at den grundlæggende informationsenhed i en WIM er en fil. Den grundlæggende fordel ved at være filbaseret er, at en enkelt-instans lagring af en fil refereret til flere gange i filsystemtræet og hardwareuafhængighed. Det reducerer omkostningerne ved at åbne og lukke forskellige filer individuelt, fordi filerne er gemt i en enkelt WIM fil. WIM-filer kan gemme flere diskbilleder, som enten refereres til ved deres unikke navn eller ved deres numeriske indeks.
### Understøttelse af kompressionsalgoritmer
WIM understøtter følgende familier af kompressionsalgoritmer i faldende hastighed og stigende forhold:
- XPRESS
- LZX
- LZMS
- Solid kompression.
De første tre familier er LZ77-baserede, mens Solid-compression blev introduceret sammen med LZMS i WIMGAPI Windows 8 og DISM Windows 8.1.
### Værktøjer til WIM-filformat
Følgende værktøjer understøtter normalt WIM-filformatet:

- **ImageX**: Et kommandolinjeværktøj, der bruges til at redigere, oprette og implementere Windows-diskbilleder i Windows Imaging Format. Sammen med den relevante WIMGAPI distribueres den som en del af det gratis Windows Automated Installation Kit. Startende med Windows Vista bruger Windows Setup WAIK API til at installere Windows.
- **DISM**: Et værktøj introduceret i Windows 7 og Windows Server 2008 R2, der kan udføre servicerelaterede opgaver på et Windows-installationsbillede, det være sig et onlinebillede eller et offlinebillede i en mappe eller WIM-fil. dette værktøj var i stand til at montere og afmontere billeder, tilføje en enhedsdriver til et offlinebillede og forespørge om installerede enhedsdrivere i et offlinebillede.
 



## Referencer 

* [Windows Imaging Format - af Wikipedia](https://en.wikipedia.org/wiki/Windows_Imaging_Format)



