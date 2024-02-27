{
  "date": "2019-10-11",
  "keywords": [
"mht",
"mht fil",
"mht filformat",
"mht filtype",
"fil",
"type",
"hvad er en mht-fil"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MHT - MIME HTML-filformat",
  "description": "Lær om MHT-filformat og API'er til at oprette og åbne MHT-filer.",
  "linktitle": "MHT",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-mh-dat"
}
},
  "lastmod": "2021-02-29"
}

## Hvad er en MHT fil?

En fil med filtypenavnet .mht er et MIME-aktiveret arkiveringsfilformat, der indeholder forskellige typer data i en enkelt fil. Den kan gemme data såsom tekst, billeder, sidestil i form af [CSS](/web/css/) filer, JavaScript og andre ressourcer som indlejrede ressourcer i den. MHT-filer, der har MIME-typen message/rfc822, indkapsler alt indholdet af en HTML-fil som en enkelt arkivfil til lagring ved arkivering på lagerenheder. Softwareapplikationer såsom Microsoft Word lader dig konvertere dine WORD-dokumenter til MHT ved at eksportere som MHT-fil. MHT-filer kan åbnes ved hjælp af populære browsere som Microsoft Internet Explore og Google Chrome.

## MHT filformat

Ligesom [MHTML](/web/mhtml/) er MHT også en MIME-indkapsling af aggregerede HTML-dokumenter. Dokumentindhold inde i et MHT-dokument såsom inline-billeder, typografiark, applets osv. er MIME-ecncoded, hvor disse er knyttet til en rodressource via URI'er. E-mail-klienter såsom Microsoft Outlook gemmer e-mails (normalt [EML](/email/eml/)) i MHT-filformat. Komplette specifikationer for MHT-filformat er tilgængelige i [RFC 822](https://tools.ietf.org/html/rfc822) og kan henvises til for udvikling af softwareapplikationer, der kan behandle MHT-filer.

## Forskellen mellem MHT og MHTML

Mens du gemmer en onlineside, bliver brugeren bedt om at bestemme sig for, hvilken type filformat onlinesiden skal gemmes i det oprindelige system. Mest typisk bliver brugeren forvirret mellem markupsprog og MHTML-filformater. De bemærker, at det er besværligt at se, at filformatet er sundere mellem disse.

Når en bruger beslutter sig for at undgå at spilde en onlineside som opmærkningssprog, dannes der en mappe, der indeholder flere filer for forskellige indhold på siden, dvs. totalt forskellige filer, arealenheder, der er oprettet til tekst, grafik, applets osv. På den modsatte side, gemmer onlinesiden som MHTML opretter én fil til hele onlinesiden. Alle sidens elementer sammen med grafik, links og alternative filer områdeenhed indlejret i én fil.

Det er naturligvis ligetil at håndtere MHT- eller MHTML-filer, fordi filen, der kan beskyttes og deles blot via e-mail. Imidlertid kan markeringssprogfilernes områdeenhed under risikoen for tab af information, da tab eller sletning af selv én fil gøre hele markupsprogmappen ubrugelig for brugeren.

## Referencer

* [MHTML - Wikipedia](https://en.wikipedia.org/wiki/MHTML)

* [MHT RFC](https://tools.ietf.org/html/rfc822)


