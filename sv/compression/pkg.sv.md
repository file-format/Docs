{
  "date" : "2021-04-08",
  "keywords" :[ "pkg fil", "pkg filformat", "vad är en pkg fil", "fil", "pkg exempel", "pkg filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PKG - Extensible Archive File Format",
  "description":"Läs mer om PKG-filformat och API:er som kan skapa och öppna PKG-filer.",
  "linktitle" : "PKG",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-13"
}

## Vad är PKG fil?

En fil med filtillägget .pkg är en installationspaketfil som används för att installera programvara på macOS. Förutom Macintosh-datorer används den även på iPhone. Det inbyggda Apple-installationsprogrammet kan användas för att installera innehållet i en PKG-fil. En PKG-fil liknar en MSI-fil som används på Windows operativsystem för installation av programvara. Under installationen kan dessa paketfiler logga meddelanden som ger dig en uppfattning om vilka extra saker som installeras av detta paket.

## PKG filformat

PKR är binära filer som komprimeras för att minska den totala filstorleken. Sedan OSX 10.5 har platta paket med enstaka installationsfiler introducerats av Apple. Dessa skiljer sig från de tidigare förpackningsformaten som kom som en bunt snarare än enstaka filer. Dessa paketerade paket innehöll en strukturerad kataloghierarki som lagrade filer på ett sätt som underlättar deras hämtning via någon indexfil. Det platta PKG-filformatet är faktiskt ett [XAR](/sv/compression/xar/)-arkiv som har ett:

* Header - Definierar storlek, kontrollsumma och versionsinformation
* Innehållsförteckning - Ett XML-dokument som är (och måste) kodas som UTF-8 och lagras i början av filen, vilket gör det enkelt att skanna igenom arkivet för att extrahera enskild fil
* Heap - ostrukturerad hög med data som refereras av TOC

## Referenser

* [Flat paketfilformat](http://s.sudre.free.fr/Stuff/Ivanhoe/FLAT.html)
* [PKG - Wikipedia](https://en.wikipedia.org/wiki/.pkg)

