{
"datum": "2023-05-16",
  "keywords": [
"sami-bestand",
"wat is een sami-bestand",
"voorbeeld van sami-bestand",
"bestand",
"sami bestandsextensie",
"verlenging"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title":"SAMI-bestandsindeling - ondertitels en uitwisselingsbestand metagegevens",
  "description":"Leer meer over het SAMI-formaat en API's waarmee SAMI-bestanden kunnen worden gemaakt en geopend.",
"linktitle":"SAMI",
  "menu": {
    "docs": {
      "identifier": "video-sami",
"parent" : "video"
}
},
"laatste mod": "2023-05-16"
}

## Wat is een SAMI-bestand?

Een bestand met de extensie ".sami" verwijst doorgaans naar een SAMI-bestand (Subtitles And Metadata Interchange). SAMI is een ondertitelingsformaat dat wordt gebruikt voor het weergeven van ondertitels of ondertitels in video's. Het werd oorspronkelijk ontwikkeld door Microsoft voor hun Windows Media Player.

SAMI-bestanden bevatten timinginformatie en tekstinhoud voor ondertitels of ondertitels, waardoor ze kunnen worden gesynchroniseerd met het afspelen van video. Het formaat ondersteunt basisopmaakopties zoals lettertypestijl, kleur en positionering van de ondertitels op het scherm.

SAMI-bestanden zijn meestal platte tekstbestanden en kunnen worden geopend en bewerkt met een teksteditor. De inhoud van een SAMI-bestand bevat doorgaans een koptekstgedeelte dat informatie geeft over het bestand, gevolgd door individuele ondertiteling met hun respectieve timing en tekst.

Hier is een voorbeeld van hoe een SAMI-bestand eruit zou kunnen zien:

```
<SAMI>
<HEAD>
<TITLE>Example Subtitles</TITLE>
</HEAD>
<BODY>
<SYNC Start=100><P Class=ENCC>Subtitle 1</P></SYNC>
<SYNC Start=500><P Class=ENCC>Subtitle 2</P></SYNC>
<SYNC Start=1000><P Class=ENCC>Subtitle 3</P></SYNC>
</BODY>
</SAMI>
```

SAMI-bestanden worden vaak gebruikt in combinatie met videospelers of mediaspelers die de weergave van ondertitels ondersteunen, zoals Windows Media Player of VLC Media Player. De speler leest het SAMI-bestand en synchroniseert de ondertitels met de video-inhoud, waardoor kijkers de ondertitels kunnen lezen terwijl ze de video bekijken.

## Ondersteunde HTML-tags

SAMI-bestanden (Subtitles And Metadata Interchange) ondersteunen een beperkte set HTML-achtige tags voor het opmaken en stylen van de ondertitels. Hier zijn enkele van de veelgebruikte tags die door SAMI worden ondersteund:

- ``<SAMI> :`` Het hoofdelement dat het volledige SAMI-bestand omvat.
- ``<HEAD> :`` Bevat headerinformatie voor het SAMI-bestand.
<html>- ``<TITLE> :`` Specificeert de titel van het SAMI-bestand. </html>
- ``<BODY> :`` Bevat de ondertiteling en hun timinginformatie.
- ``<SYNC> :`` Vertegenwoordigt een synchronisatiepunt voor een ondertitelinvoer. Het specificeert het tijdstip waarop de ondertiteling moet worden weergegeven.
- ``<P> :`` Omsluit de daadwerkelijke tekstinhoud van een ondertitel. Het wordt meestal gebruikt binnen een<SYNC> blok.
<html>- `` <FONT>:`` Definieert lettertype-eigenschappen voor de ingesloten tekst. Attributen zoals Kleur, Gezicht, Grootte en Stijl kunnen worden gebruikt om de weergave van het lettertype te wijzigen.</font>
- ``<BR> :`` Voegt een regeleinde in binnen een ondertitel.
<html>- `` <B>:`` Geeft de ingesloten tekst vet weer.</b>
<html>- `` <I>:`` Geeft de ingesloten tekst cursief weer.</i>
<html>- `` <U>:`` Maakt de ingesloten tekst onderstreept.</u>
- ``<C> :`` Specificeert de positie of uitlijning van de ondertiteltekst op het scherm. Het ondersteunt attributen zoals Midden, Midden, Links, Rechts, Boven, Onder en hun combinaties.
- ``<LANG> :`` Specificeert de taalcode voor de ondertiteltekst. Het helpt bij het identificeren van de taal van de ondertitels.

Dit zijn enkele van de basistags die door SAMI-bestanden worden ondersteund. Het is belangrijk op te merken dat SAMI niet het volledige scala aan HTML-tags en -attributen ondersteunt. De ondersteunde tags zijn primair gericht op het stylen en positioneren van de ondertitels, in plaats van op het bieden van uitgebreide documentstructurering of interactiviteit.

## Referenties
* [SAMI](https://en.wikipedia.org/wiki/SAMI)

