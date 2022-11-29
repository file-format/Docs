{
  "date" : "2022-05-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FIT File Format- Garmin Activity File",
  "description":"Läs mer om FIT-filformat och API:er som kan skapa och öppna FIT-filer.",
  "linktitle" : "FIT",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2022-05-06"
}

## Vad är en FIT fil?

En FIT-fil är en GIS-fil skapad av Garmins bärbara sportenheter. Det används för att registrera personens aktiviteter när han/hon rör sig med dessa enheter på sig. Aktivitetsdata inkluderar plats och tid som registrerats av GPS-enheten. FIT-filer används också för att överföra registrerade aktivitetsdata med hjälp av webb-API:er. Det är anledningen till att FIT-filer är det mest använda filformatet för att dela träningsdata med andra träningsplattformar. Andra vanliga filformat inkluderar [GPX](/sv/gis/gpx/), TCX och [KML](/sv/gis/kml/).

## FIT-filformat - Mer information

FIT-filer sparas på skiva som binära filer med informationen som registreras av Garmin-enheterna för aktiviteten. Information som lagras i en FIT-fil inkluderar:

* Datum Tid
* Sporttyper
* Lap & split data
* GPS-spår
* Sensordata
* Händelser för aktiv session

Aktivitetsdata kan registreras i filen i realtid eller exporteras när aktivitetsregistreringen är klar.

### FIT-aktivitetsmeddelanden

En FIT-aktivitetsfil kan innehålla några obligatoriska meddelandetyper. Följande är de meddelanden som krävs för en aktivitetsfil.

|Meddelande|Syfte|
---|---|
|Fil-ID| Fil-ID-meddelandet krävs av alla FIT-filtyper och förväntas vara det första meddelandet i filen. För aktivitetsfiler ska egenskapen Type ställas in på 4.|
|Aktivitet| Ett enda aktivitetsmeddelande krävs i en FIT-aktivitetsfil. I aktivitetsmeddelandet ingår egenskaperna Lokal tidsstämpel och Sessionsräkning. Den lokala tidsstämpeln används för att bestämma tidszonförskjutningen som kan tillämpas på alla tidsstämplar i filen. De flesta enheter spelar in FIT-filer i realtid och antalet sessioner kommer att vara okänt fram till slutet av inspelningen. På grund av detta kommer aktivitetsmeddelandet ofta att vara det sista meddelandet i filen.|
|Session| Aktivitetsfiler kommer att innehålla ett eller flera sessionsmeddelanden. Ett sessionsmeddelande är en sammanfattningsmeddelandetyp. Starttid, Total förfluten tid, Total Timertid och Tidstämpel är obligatoriska fält för alla sammanfattningsmeddelanden.|
|Varv| Varvmeddelanden representerar varv eller intervall inom sessionen. Ett varvmeddelande är en sammanfattningsmeddelandetyp. Starttid, Total förfluten tid, Total Timertid och Tidstämpel är obligatoriska fält för alla sammanfattningsmeddelanden.|
|Skriva in| Spela in meddelanden inkluderar GPS-koordinater, hastighet, distans, puls, kraft, etc.|

## FIT-fil Användbara resurser

* [Avkoda FIT-aktivitetsfiler](https://developer.garmin.com/fit/cookbook/decoding-activity-files/)
* [Kodning av FIT-aktivitetsfiler](https://developer.garmin.com/fit/cookbook/encoding-activity-files/)
 

## Referenser ##

* [FIT Activity File](https://developer.garmin.com/fit/file-types/activity/)

