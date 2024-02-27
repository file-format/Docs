{
  "date": "2022-05-06",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "FIT filformat - Garmin aktivitetsfil",
  "description": "Lær om FIT-filformat og API'er, der kan oprette og åbne FIT-filer.",
  "linktitle": "FIT",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-fi-dat"
}
},
  "lastmod": "2022-05-06"
}

## Hvad er en FIT fil?

En FIT-fil er en GIS-fil, der er oprettet af Garmin sportsbærbare enheder. Det bruges til at registrere personens aktiviteter, når han/hun bevæger sig iført disse enheder. Aktivitetsdataene inkluderer placering og tid som registreret af GPS-enheden. FIT-filer bruges også til at overføre de registrerede aktivitetsdata ved hjælp af web-API'er. Det er grunden til, at FIT-filer er det mest brugte filformat til at dele fitnessdata med andre fitnessplatforme. Andre almindelige filformater omfatter [GPX](/gis/gpx/), TCX og [KML](/gis/kml/).

## FIT-filformat - flere oplysninger

FIT-filer gemmes på disken som binære filer med de oplysninger, der registreres af Garmin-enhederne for aktiviteten. Oplysninger gemt i en FIT-fil inkluderer:

 * Dato tid
 * Sport typer
 * Lap & split data
 * GPS spor
 * Sensordata
 * Begivenheder for aktiv session

Aktivitetsdata kan registreres i filen i realtid eller eksporteres, når aktivitetsregistreringen er afsluttet.

### FIT-aktivitetsmeddelelser

En FIT-aktivitetsfil kan indeholde nogle påkrævede meddelelsestyper. Følgende er de nødvendige meddelelser til en aktivitetsfil.

|Besked|Formål|
---|---|
|Fil-id| Fil-id-meddelelsen er påkrævet af alle FIT-filtyper og forventes at være den første meddelelse i filen. For aktivitetsfiler skal egenskaben Type indstilles til 4.|
|Aktivitet| En enkelt aktivitetsmeddelelse er påkrævet i en FIT-aktivitetsfil. Inkluderet i aktivitetsmeddelelsen er egenskaberne Lokalt tidsstempel og Sessionstal. Det lokale tidsstempel bruges til at bestemme tidszoneforskydningen, der kan anvendes på alle tidsstempler i filen. De fleste enheder optager FIT-filer i realtid, og sessionsantallet vil være ukendt indtil slutningen af optagelsen. På grund af dette vil aktivitetsmeddelelsen ofte være den sidste besked i filen.|
|Session| Aktivitetsfiler vil indeholde en eller flere sessionsmeddelelser. En sessionsmeddelelse er en opsummeringsmeddelelsestype. Starttid, Samlet forløbet tid, Samlet timertid og Tidsstempel er obligatoriske felter for alle oversigtsmeddelelser.|
|Skød| Meddelelser om omgange repræsenterer omgange eller intervaller i sessionen. En Lap-meddelelse er en Resumé-meddelelsestype. Starttid, Samlet forløbet tid, Samlet timertid og Tidsstempel er obligatoriske felter for alle oversigtsmeddelelser.|
|Optag| Optag beskeder inkluderer GPS-koordinater, hastighed, distance, puls, effekt osv.|

## FIT-fil Nyttige ressourcer

 * [Afkodning af FIT-aktivitetsfiler](https://developer.garmin.com/fit/cookbook/decoding-activity-files/)
 * [Encoding FIT Activity Files](https://developer.garmin.com/fit/cookbook/encoding-activity-files/)
 
## Referencer ##

* [FIT Activity File](https://developer.garmin.com/fit/file-types/activity/)


