{
  "date": "2021-06-24",
  "keywords": [
"EN DEL",
"delvis",
"udvidelse",
"fil",
"format",
"web",
"downloadet"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "DEL - Delvist downloadet fil",
  "description": "Lær om PART filformat og API'er, der kan oprette og åbne PART filer.",
  "linktitle": "PART",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-par-dat"
}
},
  "lastmod": "2021-06-24"
}

## Hvad er en PART fil? ##

En delfil eller .part-udvidelse er en delvist downloadet fil. Det bruges, når downloads er i gang eller er blevet afbrudt på grund af ethvert problem, hvilket giver downloadmanageren mulighed for at genoptage download, når det er muligt.
Det betyder, at browseren, såsom Firefox eller filoverførselsprogrammer som eMule, eMule plus, FlashGet osv. gemmer en del af filen, kaldet Part-fil, mens overførslen finder sted på din enhed. Denne delfil vil vise dig, om overførslen er i gang eller er blevet afbrudt før fuldførelse. Ikke kun dette, men PART-filen gemmer alle data, indtil overførslen er afsluttet, hvorfor nogle af dem senere kan genoptages, hvis du vil starte downloadingen igen.

## PART Filformat ##

There are few browsers that break large download files into smaller downloads and assign each portion a .part extension. These files can be seen in the “Download” folder. Once the download is finished, the browser will combine all the PART files to give a final downloaded file. For example, while downloading a file from Firefox, the download manager will store the data being downloaded in a PART file and replaces the name with certain characters, and add a .part extension at the end, such as **doodle.or** becomes **JKzMn.or.part**. After completion, Firefox will remove the .part extension and the file will be ready to launch.
