{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WMV-filformat",
  "description":"Läs mer om WMV-filformat och API:er som kan skapa och öppna WMV-filer.",
  "linktitle" : "WMV",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2019-09-16"
}

## Vad är en WMV fil?

Advanced Systems Format (ASF) är en digital multimediabehållare designad främst för att lagra och överföra mediaströmmar. Microsoft Windows Media Video (WMV) är det komprimerade videoformatet och Microsoft Windows Media Audio (WMA) är det komprimerade ljudformatet tillsammans med ytterligare metadata i ASF-behållaren utvecklad av Microsoft. När väl WMV- eller WMA-filerna är kodade med Windows Media Video och Windows Media Audio-codecs representeras de med .asf-tillägget. WMV komprimerar stora filer för en bättre överföringshastighet över ett nätverk samtidigt som kvaliteten på videon bibehålls. WMV är speciellt utformad för att köras på alla Windows-enheter. Efter standardiseringen av Society of Motion Picture and Television Engineers (SMPTE) anses WMV nu vara ett öppet standardformat.

## Historik ##

Med hjälp av Microsofts egenutvecklade codecs utvecklades ett nytt komprimerat videoformat 1999, känt som WMV7 som var baserat på MPEG-4 del 2. Förbättringar lades till i ytterligare två versioner, dvs. WMV8 och 9. Microsoft skickade in en 9^^th^^ version av WMV till SMPTE för standardisering 2003 som så småningom standardiserades 2006 som SMPTE 421M även känd som VC-1. Tanken bakom WMV var att utveckla ett mediaformat som kunde stödjas av all hårdvara och mjukvara som stöds av Microsoft. Ett annat stort syfte var dessutom att överföra videoströmmar över internet i ett optimalt scenario. Efter standardiseringen från SMPTE blev WMV även ett videoformat för Blu-ray-skivor.

## Filformatspecifikationer

### Behållare

I allmänhet packas WMV i en ASF-behållare, men dessutom kan Matroska- eller AVI-behållare även stödja den med tillägg av .mkv respektive .avi.

### Windows Media Video 9

Även om det finns olika ljud- och videocodec tillgängliga i Windows Media Video 9-serien för skapande och uppspelning av digitala media, är WMV-9 codec den senaste och bästa videocodec eftersom den kan uppnå optimal komprimering från mycket låga bithastigheter, dvs. 160 x 120 vid 10 Kbps till 1920 x 1080 vid 4-8 Mbps för en mängd olika HD-videor.

### Codecens struktur

WMV-9 har ett 8 bitars 4:2:0 internt färgformat. Liksom alla andra populära videokomprimeringsstandarder MPEG-1 och H.261 använder WMV-9 ett blockbaserat rörelsekompensations- och rumstransformationsschema. Generellt kan vi säga att dessa standarder utför block-för-block rörelsekompensation från den tidigare rekonstruerade ramen med hjälp av en 2D-storhet som kallas rörelsevektorn (MV) för att signalera rumslig förskjutning. Det aktuella blocket bildas med hjälp av att förutsäga värdena från samma storlek tidigare rekonstruerade ram som förskjuts från den aktuella positionen av rörelsevektorn. Så småningom beräknas restfelet som skillnaden mellan det rörelsekompenserade predikterade blocket och det faktiska blocket. Detta kvarvarande fel transformeras med hjälp av en linjär energikomprimerande transformation och kvantiseras sedan och entropikodas.

Kvantiserade transformationskoefficienter entropiavkodas, avkvantiseras och inverstransformeras för att producera en approximation av restfelet på avkodarsidan, som sedan läggs till den rörelsekompenserade förutsägelsen för att generera rekonstruktionen. Beskrivningen på hög nivå av codec visas i följande bild.

Resten av avsnittet kommer att diskutera de nya förbättringarna i WMV-9 som skiljer den från resten av videokodningslösningarna som MPEG-standarder. WMV-9 har intra (I), predikterade (P) och dubbelriktade predikterade (B) ramar. Intraramar är de som är kodade oberoende och inte har något beroende av andra ramar. Förutspådda bildrutor är bildrutor som är beroende av en bildruta i det förflutna. Avkodning av en förutsagd ram kan endast ske efter att alla referensramar före den aktuella ramen med början från den senaste (I)-ramen har avkodats. B-ramar är ramar som har två referenser - en i det tidsmässiga förflutna och en i den temporala framtiden. B-ramar sänds efter deras referenser, vilket innebär att B-ramar skickas i oordning för att säkerställa att deras referenser är tillgängliga vid tidpunkten för avkodningen. B-ramar i WMV-9 används inte som referens för efterföljande ramar. Detta placerar B-ramar utanför avkodningsslingan, vilket gör att genvägar kan tas under avkodningen av B-ramar utan drift eller långvariga visuella artefakter. Ovanstående definition av I-, P- och B-ramar gäller för både progressiva och sammanflätade sekvenser.

Prestandan hos videocodecs jämförs med deras hastighetsförvrängning (RD) plot. Det är en 2D-kurva som visar distorsionen som skapas av komprimeringen vid en viss bithastighet.

WMV-9 har åtgärdat detta problem med introduktionen av en mängd olika tekniker som anges nedan:

1. Adaptiv blockstorlekstransform

2. Transformationsuppsättning med begränsad precision

3. Rörelsekompensation

4. Kvantisering och avkvantisering

5. Avancerad entropikodning

6. Slingfiltrering

7. Avancerad B-ramkodning

8. Interlace-kodning

9. Överlappningsutjämning

10. Lågprisverktyg

11. Blekningskompensation

## Referenser ##

* [https://bytescout.com/blog/2014/10/windows-media-video-format.html](https://bytescout.com/blog/2014/10/windows-media-video-format.html )
* [https://en.wikipedia.org/wiki/Windows_Media_Video](https://en.wikipedia.org/wiki/Windows_Media_Video)
* [http://citeseerx.ist.psu.edu/viewdoc/download?doi#10.1.1.101.488&rep#rep1&type#pdf](http://citeseerx.ist.psu.edu/viewdoc/download?doi#10.1 .1.101.488&rep#rep1&type#pdf)

