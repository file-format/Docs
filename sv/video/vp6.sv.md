{
  "date" : "2021-02-15",
  "keywords" :[ "vp6-fil", "vp6-filformat", "vad är en vp6-fil", "fil", "vp6-exempel", "vp6-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VP6 - TrueMotion Video File",
  "description":"Läs mer om VP6-filformat och API:er som kan skapa och öppna VP6-filer.",
  "linktitle" : "VP6",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-02-16"
}

## Vad är VP6 fil?

VP6 är ett förlustformat komprimerat videoformat som introducerades av On2-teknologier i maj 2003. Det är en del av en serie videocodecs som utvecklats av TrueMotion, inklusive V3, V4 och V5. Formatet användes inom kort inom sändningsområdet som med BBC-rapporter och QuickLink-mjukvara. VP6 efterträddes av VP7 Codec i januari 2005 med bättre kompressionskompatibilitet.

## VP6 filformat

Fullständiga specifikationer för V6-filer är inte tillgängliga offentligt. On2 offentliggjorde till en början specifikationerna men snart gjordes dessa otillgängliga för allmänna användare. En inofficiell dokumentation av VP6-filformatet finns tillgänglig på [multimedia wiki](https://wiki.multimedia.cx/index.php?title=On2_VP6) som kan hänvisas till utvecklarens referens.

### Makroblock (MB)

I likhet med MPEG-2, MPEG-4 delar 2 och 10, är varje videobildruta i en VP6-fil sammansatt av en array med 16x16 makroblock (MB). Varje MB kan vara i ett av följande lägen:

* Intra MB
* Inter MB, noll MV, tidigare ramreferens
* Inter MB, differential MV, tidigare ramreferens
* Inter MB, fyra MV, föregående ramreferens
* Inter MB, MV 1, föregående ramreferens
* Inter MB, MV 2, föregående ramreferens
* Inter MB, noll MV, bokmärkt ramreferens
* Inter MB, differential MV, bokmärkt ramreferens
* Inter MB, MV 1, bokmärkt ramreferens
* Inter MB, MV 2, bokmärkt ramreferens

### Ramhuvud

Ramhuvudet för en VP6 är som visas nedan som följer big-endian bitpackningen.

|Syntax|Antal bitar|Typ|Symantecs|
---|---|---|---|
|frame_mode|1|Enum|0x0 anger en intraram|
|qp |6 |Osignerad |Giltigt intervall för kvantiseringsparameter 0..63|
|markör| 1| Konstant| 0=VP61/62, 1=VP60|
|om (ramläge == 0) { | 0 | |lika med INTRA_FRAME|
|version |5| Konstant| 6=VP60/61, 7=VP60(Electronic Arts), 8=VP62|
|version2 |2| Konstant |0=VP60, 3=VP61/62|
|interlace |1| Boolean |true (1) betyder att interlace kommer att användas|
|if (markör==1 eller version2==0) {||||
|offset |16 |Osignerad| sekundär buffertförskjutning (byte i förhållande till buffertstart)|
|}||||
|dim_y |8| Osignerad| Makroblockhöjd på video|
|dim_x |8| Osignerad| Makroblockbredd på video|
|render_y |8 |Osignerad |Visningshöjd på video|
|render_x |8 |Osignerad |Visningsbredd på video|
|}annat{||||
|if (markör==1 eller version2==0) {||||
|offset |16 |Osignerad |Sekundär buffertförskjutning (byte relaterad till start av buffert)|
|}||||
|}||||

## Referenser

* [VP6 Wikipedia](https://en.wikipedia.org/wiki/VP6#:~:text=On2%20TrueMotion%20VP6%20is%20a,Video%2C%20and%20JavaFX%20media%20files.)

