{
  "date" : "2021-04-11",
  "keywords" :[ "soubor xapk", "formát souboru xapk", "co je soubor xapk", "soubor", "příklad xapk", "přípona souboru xapk", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XAPK - Meta Package File Format",
  "description":"Další informace o formátu souboru XAPK a rozhraních API, která mohou vytvářet a otevírat soubory XAPK.",
  "linktitle" : "XAPK",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-11"
}

## Co je soubor XAPK?

Soubor s příponou .xapk je komprimovaný soubor balíčku, který se používá k instalaci aplikací pro Android do mobilních zařízení. Jedná se o kontejnerový formát souboru, který obsahuje APK a další související soubory potřebné pro instalaci. Druhý přidružený soubor je soubor OBB, který ukládá další soubory, jako jsou obrázky, mediální soubory a data aplikací, které jsou nutné k udržení aplikace v chodu. Soubory XAPK nejsou podporovány službou Google Play a používají se pouze k distribuci na webech třetích stran pro stahování aplikací pro Android. Ty lze nainstalovat do zařízení Android pomocí XAPK Installer.

## Formát souboru XAPK

Soubory XAPK jsou komprimovány pomocí standardního formátu souboru [ZIP](/cs/compression/zip/). Ty lze extrahovat pomocí standardního softwaru pro kompresi/dekompresi, jako je WinZIP. Jakmile je soubor XAPK rozbalen na disk, obsahuje ve složce následující soubory.

* APK – Standardní instalační soubor pro instalaci aplikace na zařízení Android
* OBB - Další soubor, který obsahuje příslušné zdrojové soubory

## Reference

* [Soubor balíčku Android](https://en.wikipedia.org/wiki/Android_application_package)

