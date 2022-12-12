{
  "date" : "2021-08-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFML – ColdFusion Markup Language File",
  "description" :"További információ arról, hogy mi az a CFML-fájl és az API-k, amelyek létrehozhatnak és megnyithatnak CFML-fájlokat.",
  "linktitle" : "CFML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-19"
}

## Mi az a CFML fájl?

A .cfml kiterjesztésű fájl egy ColdFusion Markup Language fájl, amelyet weboldal létrehozására használnak. Ez egy olyan szabálykészletre vonatkozik, amely meghatározza, hogy a ColdFusion alkalmazást a programozó hogyan fejleszti. A ColdFusion egy olyan programozási nyelv, amely szerveroldali webalkalmazások gyors és kevesebb felhasználásával hozható létre, mint más technológiák, például [ASP](/hu/web/asp/), [PHP](/hu/web/php/) stb. a CML-fájlokat megnyitni képes alkalmazások közé tartozik az Adobe ColdFusion 2018, az Adobe ColdFusion Builder és az Adobe Dreamweaver.

## CFML fájlformátum – További információ

A CFML fájlok jelölőfájlok, és webes elemeket tartalmaznak címkék formájában. Ezek olyan szöveges fájlok, amelyek bármely szövegszerkesztőben megnyithatók és szerkeszthetők. A CFML-fájlok több címkéből állnak, amelyek hasonlóak a [HTML]-hez (/hu/web/html/), és általában egy nyitó és egy záró címkéből állnak. Ezek a címkék egy vagy több attribútumot is tartalmazhatnak.

### Címkék szintaxisa

Az alábbiakban a CFML címkék általánosított szintaxisa látható.

```
<tagname>
  Code/text that is affected by the surrounding tags.
</tagname>
```

A legtöbb címke attribútumokat fogad el, és a következőképpen van meghatározva.

```
<tagname attribute="value">
  Code/text that is affected by the surrounding tags.
</tagname>
```

Ezen címkék némelyike több attribútumot is elfogad a következő szintaxissal.

```
<tagname attribute1="value" attribute2="value">
  Code/text that is affected by the surrounding tags.
</tagname>
```

## CFML kód példa

Íme egy példa, amely egy tényleges CFML címkét használ – a `cfoutput` címkét:

```
<cfoutput>
  #firstname#
</cfoutput>
```

## Hivatkozások

* [ColdFusion](https://www.quackit.com/coldfusion/tutorial/)

