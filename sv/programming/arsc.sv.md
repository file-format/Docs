{
  "date" : "2019-10-11",
  "keywords" :[ "arsc", ".arsc","vad är en arsc-fil","hur man öppnar en arsc-fil", "tillägg", "fil", "arsc-fil","arsc-filformat", "arsc-filtillägg", "arsc filexempel"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ARSC - Android Package Resource Table File",
  "description":"Läs mer om ARSC-filformat och API:er som kan skapa och öppna ARSC-filer.",
  "linktitle" : "ARSC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-22"
}

## Vad är en ARSC fil?

En ARSC-fil är en Android-resurstabellfil som innehåller programmets lista över resurser i ett tabellformat. Detta innehåller information som resursnamn, egenskaper och ID:n. ARSC-filer är en del av APK-paket som används för att installera dessa Android-appar. Alla resurser som bilder, layouter, stilar och strängar i en Android-applikation konverteras till binära filer när APK-filen genereras. ARSC-filen genereras också samtidigt, som innehåller en lista över alla programmets kompilerade resurser och deras ID:n.

## ARSC filformat

.arsc-tilläggsfilerna är binära filer som genereras efter att kompilatorn, såsom ANT (Eclipse) eller Gradle (AS), kompilerar Android-applikationskoden för att producera filen [APK](/sv/compression/apk/). Du kan extrahera APK-filen med vilket arkiveringsverktyg som helst som WinZip för att se dess innehåll, vilket är de kompilerade java-klassfilerna, dvs classes.dex. Utöver dessa innehåller den även denna ARSC-fil som innehåller metainformation om:

* XML-noderna
* Attributen
* Resurs-ID:n

Resurser i en APK-fil hänvisas av resurs-ID:n, medan attributen löses till ett värde vid körning. Android aapt-verktyget samlar in alla resurser som definieras i filer vid byggtid och tilldelar resurs-ID:n till dem. Efter att identifierare har tilldelats de kompilerade resurserna genereras en R.java-fil från källkoden såväl som resources.arsc.

## Referenser

* [Binär resurstabellstruktur](https://stackoverflow.com/questions/27548810/android-compiled-resources-resources-arsc)

