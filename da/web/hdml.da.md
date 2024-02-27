{
  "date": "2021-08-21",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Håndholdt enhed Markup Language File",
  "description": "Lær om HDML-filformat og API'er, der kan oprette og åbne HDML-filer.",
  "linktitle": "HDML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-hdm-dal"
}
},
  "lastmod": "2021-08-21"
}

## Hvad er en HDML fil?

En fil med .hdml-udvidelsen (Handheld Device Markup Language) er et opmærkningssprog til oprettelse af websider til bærbare elektroniske enheder såsom håndholdte computere, smartphones og informationsdisplayapparater. HDML siges at være en udvidelse af sproget [SGML](https://en.wikipedia.org/wiki/Standard_Generalized_Markup_Language). HDML ligner HTML, men til trådløse og håndholdte enheder, der har små skærme såsom PDA, mobiltelefoner og så videre. Det blev erstattet med WML, som det fungerede som en vigtig indflydelse.

## HDML-filformat - flere oplysninger

HDML er et opmærkningssprog til håndholdte enheder, der er baseret på opmærkningstags, der ligner HTML. HDML blev sendt til W3C til standardisering, men det blev aldrig en standard. Dets filformatspecifikationer er dog tilgængelige på [W3 website](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html) til reference. [syntax for HDML language](https://www.w3.org/TR/hdml20-5.html#HEADING5-0) er tilgængelig for udviklerens reference og kan bruges til eksempeludvikling af applikationer.

## HDML elementer

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


