{
  "date" : "2019-10-11",
  "keywords" :[ "soubor gpx", "co je soubor gpx", "soubor", "příklad gpx", "přípona souboru gpx", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GPX - GPX Exchange File Format",
  "description":"Další informace o formátu souboru GPX a rozhraních API, která mohou vytvářet a otevírat soubory GPX.",
  "linktitle" : "GPX",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor GPX?

Soubory s příponou GPX představují formát GPS Exchange pro výměnu GPS dat mezi aplikacemi a webovými službami na internetu. Jedná se o odlehčený formát souboru XML, který obsahuje data GPS, tj. trasové body, trasy a prošlé trasy, které mají být importovány a červené více programy. Formát souboru GPX je otevřený a je podporován různými aplikacemi a zařízeními GPS. GPS data z takových souborů lze načíst pro zobrazení v mapových aplikacích pro geoprostorové účely.

## Formát souboru GPX ##

Soubor GPX se skládá z dat o zeměpisné šířce a délce, hodnot nadmořské výšky a dalších případně dalších popisných informací. Údaje o poloze jsou vyjádřeny jako desetinné stupně a nadmořská výška je vyjádřena v metrech. Čas v souboru GPX je v koordinovaném světovém čase (UTC) ve formátu ISO 8601. Výhody použití souboru GPX jsou následující:

* GPX umožňuje výměnu dat s rostoucím seznamem programů pro Windows, MacOS, Linux, Palm a PocketPC.
* GPX lze transformovat do jiných formátů souborů pomocí jednoduché webové stránky nebo programu pro převod.
* GPX je založeno na standardu XML, takže mnoho nových programů, které používáte (například Microsoft Excel), umí číst soubory GPX.
* GPX usnadňuje každému na webu vývoj nových funkcí, které budou okamžitě fungovat s vašimi oblíbenými programy.

[Schéma GPX](https://www.topografix.com/GPX/1/1/gpx.xsd) ukazuje reprezentaci formátu souboru GPX pro referenci.

### Základní údaje ###

Následují základní údaje, které jsou součástí souboru GPX pro reprezentaci dat GPS.

* **Waypoints**: Trasový bod je WGS84 (GPS) souřadnice bodu a představuje vrstvu prvků typu OGR wkbPoint
* **Routes**: Představují vrstvu funkcí typu OGR wkbLineString. Obsahuje seznam trasových bodů, což jsou trasové body ukazující body odbočení nebo etapy, které vedou k cíli
* **Stopy**: Stopy představují vrstvu funkcí typu OGR wkbMultiLineString. Je tvořen alespoň jedním segmentem obsahujícím trasové body v uspořádaném seznamu bodů popisujících cestu. Skládá se ze seznamu bodů trasy, které představují souvislou trasu GPS.

### Příklad souboru GPX ###

Následující soubor GPX ukazuje organizaci dat GPS v souboru GPX a může poskytnout dobrou představu o obsahu souboru GPX.

```
<gpx xmlns#"http://www.topografix.com/GPX/1/1" xmlns:gpxx#"http://www.garmin.com/xmlschemas/GpxExtensions/v3" xmlns:gpxtpx#"http://www.garmin.com/xmlschemas/TrackPointExtension/v1" creator#"Oregon 400t" version#"1.1" xmlns:xsi#"http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation#"http://www.topografix.com/GPX/1/1 http://www.topografix.com/GPX/1/1/gpx.xsd http://www.garmin.com/xmlschemas/GpxExtensions/v3 http://www.garmin.com/xmlschemas/GpxExtensionsv3.xsd http://www.garmin.com/xmlschemas/TrackPointExtension/v1 http://www.garmin.com/xmlschemas/TrackPointExtensionv1.xsd">
  <metadata>
    <link href#"http://www.garmin.com">
      <text>Garmin International</text>
    </link>
    <time>2009-10-17T22:58:43Z</time>
  </metadata>
  <trk>
    <name>Example GPX Document</name>
    <trkseg>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>4.46</ele>
        <time>2009-10-17T18:37:26Z</time>
      </trkpt>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>4.94</ele>
        <time>2009-10-17T18:37:31Z</time>
      </trkpt>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>6.87</ele>
        <time>2009-10-17T18:37:34Z</time>
      </trkpt>
    </trkseg>
  </trk>
</gpx>
```

## Reference ##

* [Formát souboru GPX] (http://www.topografix.com/gpx.asp)
* [GPX – z Wikipedie](https://en.wikipedia.org/wiki/GPS_Exchange_Format)

