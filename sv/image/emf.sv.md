{
  "date" : "2019-10-11",
  "keywords" :[ "emf-fil", "emf-filformat", "vad är en emf-fil", "fil", "emf-exempel", "emf-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EMF - Enhanced Metafile Format",
  "description":"Läs mer om EMF-filformat och API:er som kan skapa och öppna EMF-filer.",
  "linktitle" : "EMF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en EMF fil?

**Enhanced metafile format (EMF)** lagrar grafiska bilder enhetsoberoende. Metafiler av EMF består av poster med variabel längd i kronologisk ordning som kan återge den lagrade bilden efter analys på valfri utenhet. Dessa poster med variabel längd kan vara definitioner av inneslutna objekt, kommandon för ritning och grafikegenskaper som är viktiga för att återge bilden korrekt. När en enhet öppnar en EMF-metafil med sin egen grafikmiljö förblir proportionerna, dimensionerna, färgerna och andra grafiska egenskaper för originalbilden desamma oavsett vilken enhetsplattform som öppnas.

## Kortfattad bakgrund ##

1990 designade Microsoft ett bildfilformat Windows Metafile ([WMF](/sv/image/wmf/)) för Microsoft Windows. Windows-metafiler är 16-bitarsformat som kan innehålla vissa bitmappskomponenter. WMF kan bestå av vektorgrafik och är avsett att hållas portabel mellan olika applikationer. 1993 tillkännagav Win32/GDI Enhanced Metafile (EMF), en nyare version med förbättrad flexibilitet och skalbarhet. EMF används också som kommandon för grafikspråk för att köra skrivardrivrutinerna. Microsoft rekommenderar nu det förbättrade metafilformatet (EMF) framför Windows-formatet (WMF). När Windows XP introducerades släpptes versionen Enhanced Metafile Format Plus (EMF+). Den här nyare versionen hittar sin väg genom att serialisera GDI+ API-anrop, likaså registrerar WMF/EMF anrop till GDI. Det finns en gzip-komprimerad version av EMF som kallas EMZ.

## EMF-metafilformat ##

Följande är de väsentliga delarna av det förbättrade metafilformatet:

* En EMR_HEADER (version, storlek, upplösningen på bilden vid skapande)
* En tabell för GDI-objekt
* En reserverad palett (valfritt)
* Metafilposter ordnade i arraystruktur (egenskapsinställningar, definierade objekt, ritkommandon)
* EMR_EOF-post (senaste posten i EMF-metafilen)

## EMF-versioner ##
* **Original**: Originalversionen anger den post som krävs för att behålla originalbilden och behålla dess enhetsoberoende. Stöder dessutom posten som innehåller grafikobjekt och kommandon för ritning.
* **Version 1**: Den andra versionen av EMF förbättrade flexibiliteten och enhetsoberoendet genom att lägga till posten för pixelformat och tillhandahållande för att använda OpenGL-kommandot.
* **Version 2**: Den tredje versionen förbättrade noggrannheten genom att lägga till det metriska systemet för att mäta enhetens ytavstånd, vilket gör posten mer skalbar.

## Förbättrade metafilposter ##

Metafilposter är ordnade i form av array. Dessa poster har ENHMETARECORD-struktur och varierar i längd. ENHMETARECORD anger data som definierar GDI-funktioner för att skapa en bild med hjälp av förbättrat metafilformat. **ENHMETAHEADER**-strukturen är alltid den första posten i detta format. Detta EMF-huvud innehåller följande information.

Varje post av förbättrad metafil har två medlemmar av EMR (tillhandahåller basstrukturen) i början. Den första medlemmen känner igen GDI-funktionen (parametrar används i posten) som bestämmer typen av post och är känd som iType. Den andra medlemmen nSize definierar storleken på varje post. Återstående parametrar (om några) och ytterligare data ordnade omedelbart under nSize. Omedelbart efter rubriken kan en valfri textbeskrivning visas. Namnet på bilden och författaren finns antecknat i den textbeskrivningen. Paletten vars närvaro är ett alternativ anger färgerna som används för att skapa förbättrad metafil. De andra posterna används för att specificera GDI-funktionen som är väsentlig för att skapa bilder.

Minst en EMF-post bör finnas i varje metafil. Den korsande informationen från en post till en annan är beroende av EMF-poster, så dessa poster måste arrangeras intill varandra. Vid vilken som helst given post i metafilen förutom EOF_record, definierar längden på den specifika posten för att flytta till nästa post.

## Förbättrad metafilskapande ##

**CreateEnhMetaFile**-funktionen används för att skapa en förbättrad metafil. Denna funktionsargument används för dimensioner och lagring av bild på disk/minne. Dessutom kräver den här funktionen dimensionen på enheten där bilden visades först (referensenhet) och referensenhetens sammanhang (DC). Så argumenten för att hantera denna DC måste tillhandahålla när funktionen **CreateEnhMetaFile** anropas. Funktionens syntax är som följer:
```
HDC CreateEnhMetaFileExample(

  HDC        hdc,

  LPCSTR     lptoFilename,

  const OVAL *lprc,

  LPCSTR     lpDesc

);
```
**HDC:** handtag till en referensenhet.

**lptoFilename:** En pekare till filnamnet.

**lprc:** Pekare till oval struktur anger bildens mått i mm.

**lpDesc:** en pekare till en sträng för titeln på bilden och programmets namn som skapade bilden.

## Förbättrade metafiloperationer ##

Följande är jobb som kan utföras med hjälp av handtaget till en förbättrad metafil.

* Visa och redigera för den lagrade bilden.
* Producera förbättrade metafilkopior.
* Hämta kopian av en EMF-rubrik, valfri beskrivning och binär version av en förbättrad metafil
* Rekapitulera färgerna i paletten.

## Grafikobjekt ##

I ritnings- och målningsoperationer kan grafiska objekt skapas av objektskapande poster och kan sparas för vidare användning. En `EMR_SELECTOBJECT`-post kan hämta dessa grafikobjekt med hjälp av uppspelningsenhetskontexten. Pennor, paletter, penslar, färgrymder, typsnitt och lagerobjekt är några återanvändbara objekttyper.

## Bytebeställning ##

Little-endian-format används för att lagra data i metafilposter.

## Version ##

EMF-filformatet har reviderats två gånger. De ändrade versionerna är original, tillägg 1 och tillägg 2. Utökade versioner har möjlighet för OpenGL-poster och en valfri deskriptor för internt pixelformat. En mätanordning i milliliter läggs till för visade mått.

## Referenser ##

* [Enhanced-Format Metafiler | Microsoft Docs](https://learn.microsoft.com/en-us/windows/desktop/gdi/enhanced-format-metafiles)
* [Förbättrat metafilformat och specifikation](https://msdn.microsoft.com/en-us/library/cc230514.aspx)

