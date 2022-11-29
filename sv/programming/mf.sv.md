{
  "date" : "2019-10-11",
  "keywords": [ "mf file", "mf", "extension", "format", "mf file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MF - Java Manifest File Format",
  "description":"Läs mer om MF-filformat och API:er som kan skapa och öppna MF-filer.",
  "linktitle" : "MF",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Vad är MF fil?

En fil med filtillägget .mf är en Java Manifest-fil som innehåller information om de enskilda [JAR](/sv/programming/jar/)-filposterna. Själva MF-filen finns i JAR-filen och tillhandahåller all tilläggs- och paketrelaterade definition. JAR-filer kan produceras för att användas som en körbar fil. I sådana fall anger mainfest-filen huvudklassen för programmet som innehåller **`public static void main`**-satsen. Manifestfiler heter MANIFEST.MF och kan öppnas med valfri textredigerare på Windows, MacOS och Linux operativsystem.

## Manifest filformatspecifikationer

[Manifest filformatspecifikationer](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html) finns tillgängliga av Oracle i deras guide för JAR-filformat. En manifestfil består av huvudsektioner som följs av en lista med sektioner för individuella JAR-filposter. Varje avsnitt följer några regler och begränsningar.

### Huvudsektioner

Ett huvudavsnitt:

* innehåller information om säkerhet och konfiguration om JAR-filen
* innehåller information om applikationen eller tillägget som filen JAR är en del av
* definierar huvudattributen för varje enskild manifestartikel

**Obs**: Inget attribut i det här avsnittet kan heta "Namn".

### Individuella sektioner

En enskild sektion definierar olika attribut för paket eller filer i en JAR-fil. Varje avsnitt måste börja med ett attribut som heter "Namn" vars värde måste vara en relativ sökväg till filen, eller en absolut URL som refererar till data utanför arkivet.

### Manifestspecifikationer

|Attributer|Beskrivning|
---|---|
|manifest-fil|huvudsektion ny rad *individual-section|
|main-section|version-info newline *main-attribute|
|version-info|Manifest-Version : versionsnummer|
|versionsnummer|siffra+{.digit+}*|
|main-attribute|(alla legitima huvudattribut) newline|
|individual-section|Namn : värde newline *perentry-attribute|
|perentry-attribute|(alla legitima perentry-attribut) newline|
|nylinje|CR LF | LF | CR (följs inte av LF)|
|siffra|{0-9}|

## Referenser

* [Oracle - JAR-filformat](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html)
* [JAR-filformat](https://en.wikipedia.org/wiki/JAR_(file_format)#:~:text=A%20JAR%20(Java%20ARchive)%20is,into%20one%20file%20for% 20distribution.&text=De%20är%20byggda%20på%20,jar%20filen%20tillägget.)

