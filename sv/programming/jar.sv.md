{
  "date" : "2019-10-11",
  "keywords" :[ "JAR", ".jar","vad är en jar-fil","hur man öppnar en jar-fil", "tillägg", "fil", "jar-fil","jar-filformat", ".jar-tillägget" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JAR - Java Archive File Format",
  "description":"Läs mer om JAR-filformat och API:er som kan skapa och öppna JAR-filer.",
  "linktitle" : "JAR",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Vad är JAR fil?

En fil med filtillägget .jar är en Java Archive-fil som innehåller många olika programrelaterade filer som en enda fil. Detta filformat skapades för att minska hastigheten för att ladda en nedladdad Java-applet i webbläsaren via HTTP-transaktion, genom att undvika att skapa flera HTTP-anslutningar. En enda JAR-fil kan innehålla Java-klassfiler ([.class](/sv/programming/class/)), [images](/sv/image/) och [sounds](/sv/audio/). Enskilda objekt i en JAR-fil kan signeras digitalt av applikationsutvecklaren för att autentisera deras ursprung. JAR-filer används regelbundet för att skapa funktionella API:er som innehåller specifik funktionalitet relaterad till det API:et.

## JAR filformat

JAR-filer är baserade på det populära [ZIP-filformat](/sv/compression/zip/) som arkiverar sina individuella innehållsfiler i en enda fil. JAR-filformatet stöder komprimering, vilket resulterar i en mindre filstorlek för nedladdning och därmed ytterligare förbättrar nedladdningstiden. [JAR-filspecifikationer](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html) från Oracle ger fullständig information om de interna specifikationerna för JAR-filer.

### Manifestfilen

När en JAR-fil skapas skapas automatiskt en manifestfil inuti den som innehåller metadatainformation om innehållet i JAR-filen. Den här filen visar innehållet som är paketerat inuti JAR-filen. En typisk Manifest-fil ser ut som följer som visar mappar och klasser som ingår i JAR-filen.

```
META-INF/
META-INF/MANIFEST.MF
pack/
pack/class1.class
pack/class2.class
..
..
```

#### Manifestspecifikationer

Manifestspecifikationer definieras av Oracle enligt följande.

`manifest-fil`: huvudsektion newline \*individual-section

`main-section`: version-info newline \*main-attribute

`version-info`: Manifest-Version: version-nummer

`version-nummer` : siffra+{.digit+}*

`main-attribute`: (alla legitima huvudattribut) nyrad

`individual-section`: Namn : värde newline \*perentry-attribute

"perentry-attribute": (alla legitima perentry-attribut) nyrad

`nylinje` : CR LF | LF | CR (följs inte av LF)

`digit`: {0-9}

### Körbar JAR

JAR-filer kan också bestå av ett program som kan köras av Java Virtual Machine (JVM) liknande alla andra program på Microsoft Windows operativsystem. I det här fallet behöver JVM veta om applikationens ingångspunkt som är vilken klass som helst med en offentlig statisk void-huvudmetod. Manifestfilen identifierar en sådan klass med "Main-Class"-huvudet i följande format:

```
Main-Class: com.example.MyClassName
```



## Referenser

* [JAR-filöversikt](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jarGuide.html)
* [JAR-filformat](https://en.wikipedia.org/wiki/JAR_(file_format)#:~:text=A%20JAR%20(Java%20ARchive)%20is,into%20one%20file%20for% 20distribution.&text=De%20är%20byggda%20på%20,jar%20filen%20tillägget.)

