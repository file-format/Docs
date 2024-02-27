{
  "date": "2021-06-22",
  "keywords": [
"Z",
"Komprimeret",
"Fil",
"Udvidelse",
"Filformat",
"UNIX",
"Kartz"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "Z Komprimeret filformat",
  "description": "Lær om Z-filformat og API'er, der kan oprette og åbne Z-filer.",
  "linktitle": "Z",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression--daz"
}
},
  "lastmod": "2021-06-22"
}

## Hvad er en Z fil? ##

AZ-fil er en kategori af filer, der tilhører UNIX-komprimerede datafiler. Komprimerede Unix-filer er den mest populære og udbredte udvidelsestype af Z-filen. Z-fil gør formatering, kørsel og åbning af filer nemmere, da de bruges til at skabe små computerfiler, der nemt kan køres på Linux/Unix-operativsystemer. Det er fordelagtigt for brugere, der ønsker at spare diskplads, da brugere ved at komprimere store filer til én Z-fil kan spare meget lagerplads og gøre deres filer mere organiserede. Disse komprimerede Z-filer kan nemt dekomprimeres i Unix-systemet ved at bruge en simpel kommando uncompress abc.z for en fil med navnet abc.


## Kort historie ##

Z-filen blev oprettet som et resultat af en urokkelig efterspørgsel efter en hurtig arkiver i slutningen af 80'erne og begyndelsen af 90'erne. Da internettet ikke var særlig populært og tilgængeligt på det tidspunkt, måtte brugerne kæmpe for at dele grundlæggende filer og få adgang til internettet. En sådan måde, som brugere plejede at overføre filer på, var ved at bruge en arkiver. Z-filen blev introduceret af Phil Katz, som en hurtigere og mere understøttende form for Archiver, hvorigennem store filer kunne komprimeres i én og overføres. Den endelige version af Kartz blev introduceret i 1989, efter en juridisk kamp, og den var dedikeret til det offentlige domæne, som annonceret af Kartz.


## Teknisk specifikation ##

Z-filen er en fil, der understøtter arkivfilformatet. Det er en af de første filtyper, der giver hurtig og tabsfri datakomprimering og dekomprimering ved hjælp af Unix- og Linux-operativsystemerne. I nogle operativsystemer repræsenterer en filtypenavn med små bogstaver Z (.z) en GNU-komprimeret fil, mens en fil med store bogstaver Z (.Z) repræsenterer en komprimeret fil. Z-filen har flere versioner, som den understøtter, såsom 2.0, 2.1, 4.5, 4.6, blandt andre. Der er forskellige algoritmer i forskellige Z-filversioner, og den mest populære er DEFLATE.




