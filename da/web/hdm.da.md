{
  "date": "2022-10-12",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "HDM File - Håndholdt enhed Markup Language File",
  "description": "Lær om HDM-filformat og API'er, der kan oprette og åbne HDM-filer.",
  "linktitle": "HDM",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-hd-dam"
}
},
  "lastmod": "2022-10-12"
}

## Hvad er en HDM fil?

En HDM-fil er en websidefil til markupsprog, der er oprettet i Handheld Device Markup Language (HDML). Den indeholder markup-tags, der ligner sproget [HTML](/web/html/), men er designet til håndholdte elektroniske enheder såsom smartphones og PDA'er. [HDML file format specifications](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html) blev sendt til W3C til standardisering, men kunne ikke blive en standard. HDM er baseret på filformatspecifikationerne for [HDML](/web/hdml/), der er tilgængelige på W3-webstedet.

## HDM-filformat - flere oplysninger

HDM-filen består af markup-tags, der gengives til visuelt designet websted på håndholdte enheder. HDM-filer kopieres til enheder ved hjælp af HDTP-protokollen (Handheld Device Transport Protocol) i stedet for HTTP-protokollen, som bruges til HTML-sider.

## HDML-filelementer

Det følgende er et lys af elementer, der giver et køretidsmiljø for HDML og omtales som brugeragenten.

|Element|Beskrivelse|
---|---|
|Kort|Dette er den grundlæggende byggesten i HDML, og viser og giver brugeren mulighed for at interagere med informationskort. |
|Decks|HDML-kort er grupperet sammen i dæk. Et HDML-dæk ligner en HTML-side, idet det identificeres ved URL [RFC1738] og er den enhed af indhold, der anmodes om fra en server og cachelagres af brugeragenten.|
|Handlinger|Handlinger kan være af PREV-, SOFT1-SOFT8- og HELP-typen. Disse er abstrakte og understøttes i brugergrænsefladen på en brugeragentspecifik måde.|
|Aktiviteter|En aktivitet er som en gruppe af relaterede kort, der udfører én logisk funktion. Disse kan strække sig over et eller flere dæk. HDML-navigations- og tilstandsmodellen er struktureret omkring aktiviteter.|
|Historik-baseret navigation|Brugeragenten vedligeholder en historik over de kort, der vises til brugeren. Hvert kort, der tilgås, føjes til korthistorikken. Brugeragenten giver brugeren mulighed for nemt at navigere tilbage til det forrige kort i historikken.|

## Referencer

* [HDML - Wikipedia](https://en.wikipedia.org/wiki/Handheld_Device_Markup_Language)

* [HDML-specifikationer - W3-skoler](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html)


