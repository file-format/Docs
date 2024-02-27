{
  "date": "2021-07-28",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "QBL - QuickBooks-licensfil",
  "description": "Lær om QBL filformat og API'er, der kan oprette og åbne QBL filer.",
  "linktitle": "QBL",
  "menu": {
    "docs": {
      "parent": "word-processing",
      "identifier": "word-processing-qb-dal"
}
},
  "lastmod": "2021-07-28"
}

## Hvad er QBL fil?

En fil med filtypenavnet .qbl er en QuickBooks-licensfil, der indeholder licensoplysninger for brugerens købte kopi. Det er normalt gemt i det lokale system med navnet `license.qbl` efter QuickBooks er installeret, og brugeren indtaster licensoplysningerne i softwaren, når softwaren køres for første gang. QBL var det tidligere filformat, der blev brugt til at gemme QuickBooks licensoplysninger. Dette er nu blevet erstattet af QuickBooks `qbregisteration.dat`-filen og er udfyldt med information fra brugerens bekræftelses-e-mail, købte DVD eller gennem andre købsmetoder. QBL-filer kan åbnes i alle teksteditorer, såsom Windows Notesblok, Apple TextEdit, Notepad++, Github Atom-editor og mange flere.

## QBL-filformat - flere oplysninger

QBL-filer oprettes og gemmes som almindelige tekstfiler. Oplysningerne i disse filer kan læses af mennesker og kan redigeres/opdateres, når disse filer åbnes i teksteditorer. Licens- og brugerregistreringsoplysninger kan derefter kopieres i denne fil for at komme i gang med QuickBooks-softwaren. QBL-filer gemmes normalt i mappen Program Files\Intuit\QuickBooks\INET på Windows-operativsystemet.

En QBL-fil indeholder to typer information.

* `QuickBooks Version Information:` Henviser til den installerede version af QuickBooks og er i format som xx.x

* `Licensnøgle:` Tekst i 000-000 0000-0000-0000-000 000073adbf3f-format, hvor 000-000 0000-0000-0000-000 erstattes med brugerens qbregistration-nøgle


## Referencer

 * [QuickBooks by Intuit](https://quickbooks.intuit.com/)
 * [QuickBooks - Generering af filen qbregistration.dat](https://quickbooks.intuit.com/learn-support/en-us/help-article/license-information/create-create-qbregistration-dat-file/L7S5BwSst_US_en_US)

