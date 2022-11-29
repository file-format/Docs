{
  "date" : "2021-07-29",
  "keywords" :[ "md5-fil", "md5-filformat", "vad är en md5-fil", "fil", "md5-exempel", "md5-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MD5 - MD5 Checksum File",
  "description":"Läs mer om MD5-filer och API:er som kan skapa och öppna MD5-filer.",
  "linktitle" : "MD5",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2021-07-29"
}

## Vad är en MD5 fil?

En MD5-fil är en kontrollsummafil som används för att verifiera en fils integritet. Det liknar ett fingeravtryck för den associerade filen och genereras unikt med hjälp av en algoritm som använder antalet bitar i filen. Den används för att verifiera filen med programvara som [md5sum](http://www.gnu.org/software/coreutils/manual/html_node/md5sum-invocation.html). En fördel med att använda MD5-filer är att verifiera att de nedladdade filerna inte är korrupta.

## MD5-filformat - Mer information

Vanligtvis sparas en MD5-fil med samma namn som det ursprungliga filnamnet men med tillägget .md5. Till exempel, om det associerade filnamnet är `abc_987_123456.grb`, kommer motsvarande MD5-filnamn att vara `abc_987_123456.grb.md5`. MD5-filer hjälper till att identifiera att en mottagen eller nedladdad fil inte är skadad eller påverkad av skadligt innehåll. Kort sagt, MD5-filer garanterar en fils fullständighet.


## Hur kontrollerar man MD5 Checksum?

En enskild fil kan kontrolleras/verifieras för MD5 med hjälp av verktyget [md5sum](https://en.wikipedia.org/wiki/Md5sum) enligt följande.

```
md5sum -c abc_987_123456.grb.md5
```

## Referenser

* [md5sum - Wikipedia](https://en.wikipedia.org/wiki/Md5sum)

