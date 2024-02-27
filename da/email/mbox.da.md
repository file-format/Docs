{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MBOX - E-mail-postkassefil",
  "description": "Lær om MBOX filformat og API'er, der kan oprette og åbne MBOX filer.",
  "linktitle": "MBOX",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-mbo-dax"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en MBOX fil?

MBox-filformat er et generisk udtryk, der repræsenterer en beholder til indsamling af elektroniske postmeddelelser. Beskederne gemmes inde i beholderen sammen med deres vedhæftede filer. Beskeder fra en hel mappe gemmes i en enkelt databasefil, og nye meddelelser føjes til slutningen af filen. Talrige applikationer og API understøtter MBox-filformater såsom Apple Mail og Mozilla Thunderbird.

## MBOX-filformat ##

The MBox file format remained non-standardized for quite long time until 2005 when the application/mbox  was standardized as [RFC 4155.](https://tools.ietf.org/rfc/rfc4155.txt) Messages, in RFC 2822 format, are concatenated inside MBox file format one after another. Each message begins with a separator line that identifies the message sender, and also identifies the date and time at which the message was received by the final recipient (either the last-hop system in the transfer path, or the system which serves as the recipient's mailstore). Each message is typically terminated by an empty line. The end of the database is usually recognized by either the absence of any additional data, or by the presence of an explicit end-of-file marker.

## Læser en besked fra MBox fil ##

En læser scanner gennem en mbox-fil og leder efter From_-linjer. Enhver Fra_-linje markerer begyndelsen af en besked. Læseren bør ikke forsøge at udnytte det faktum, at hver From_-linje (efter begyndelsen af filen) er tom. Når læseren finder en besked, trækker den en (muligvis beskadiget) konvolutafsender og leveringsdato ud af From_-linjen. Den læser derefter indtil den næste From_-linje eller slutningen af filen, alt efter hvad der kommer først. Den fjerner den sidste tomme linje og sletter citeringen af >Fra_ linjer og >>Fra_ linjer og så videre. Resultatet er en RFC 822-meddelelse.

## Kodningsovervejelser ##

Indholdet af en MBox-fil kan blive irreversibelt blandet, når en modtaget e-mail indeholder en Mbox-fil som vedhæftet fil og gemmes i en anden Mbox-fil. For at undgå dette skal meddelelsessystemer kode en mbox-database med ikke-transparent overførselskodning (såsom BASE64 eller Quoted-Printable), når et sådant objekt overføres via meddelelsesprotokoller. Implementere bør også være forberedt på at indkode mbox-data lokalt, hvis der modtages ikke-kompatible data.

## Referencer ##

* [MBox - RFC4155](https://tools.ietf.org/rfc/rfc4155.txt)

* [Mbox - Wikipedia](https://en.wikipedia.org/wiki/Mbox)


