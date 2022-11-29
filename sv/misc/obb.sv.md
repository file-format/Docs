{
  "date" : "2022-02-16",
  "keywords" :[ "obb-fil", "obb-filformat", "vad är en obb-fil", "fil", "obb-exempel", "obb-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OBB-filformat - Android Opaque Binary Blob File",
  "description":"Läs mer om OBB-filformat och API:er som kan skapa och öppna OBB-filer.",
  "linktitle" : "OBB",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-02-16"
}

## Vad är OBB fil?

En OBB-fil är en expansionsfil som innehåller ytterligare data som är utöver Android-filen [APK](/sv/compression/apk/). Google Play Store tillåter inte att ha en Android APK-fil med en storlek på mer än 100 MB. Men vissa applikationer kan kräva högupplöst grafik, mediefiler eller andra stora tillgångar som värd förutom APK-filerna. Det är där OBB-filtyperna kommer in. Google Play tillåter att bifoga dessa expansionsfiler som ett komplement till APK-filen.

## OBB filformat

OBB-filer sparas som binära filer tillsammans med APK-filerna. När en APK följer med OBB-filerna, lagrar Google Play expansionsfilerna på sin server och ingen extra kostnad debiteras för utvecklaren. Dessa ytterligare filer lagras enhetens delade lagring på SD-kort eller USB-monterbar partition när appen laddas ner för installation.

OBB-filerna laddas ner och installeras vid nedladdning. Men i vissa fall laddas dessa ner för installation när applikationen körs för första gången.

### OBB maximal filstorlek

Google Play Butik låter dig ladda upp OBB-expansionsfiler i storlek upp till 2 GB. Stora filer rekommenderas att laddas upp som komprimerade [ZIP](/sv/compression/zip/)-filer för effektiv uppladdning via internet.

Dessa expansionsfiler kan lagras antingen som **huvud** primär expansionsfil för ytterligare resurser som krävs av appen eller en valfri patchexpansionsfil avsedd för små uppdateringar av huvudexpansionsfilen.

## Referenser

* [Android-utvecklare - expansionsfiler](https://developer.android.com/google/play/expansion-files)

