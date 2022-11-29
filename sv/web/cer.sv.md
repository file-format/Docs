{
  "date" : "2021-07-13",
  "keywords" :[ "CER", "tillägg", "fil", "format", "webb", "certifikat", "språk" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CER - Certificate File Format",
  "description":"Läs mer om CER-filformat och API:er som kan skapa och öppna CER-filer.",
  "linktitle" : "CER",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-13"
}

## Vad är en CER fil? ##

En fil med filtillägget .cer är ansvarig för att lagra viss information om ägarcertifikatet och den specifika publika nyckeln. Detta filformat kan inte lagra de privata nycklarna och har kapacitet att lagra endast ett certifikat som är x509. De specifikt säkrade certifikatutfärdarna är de som tillhör HTTPS, ett pålitligt och säkert protokoll för surfning
CER är ett certifikat för din server. Det tas vanligtvis emot av certifikatutfärdaren för domänen. CER anses för det mesta vara detsamma som [CRT](/sv/web/crt/), även om båda har samma format för SSL-certifikat men är olika filnamnstillägg.
Dessa kan användas på operativsystem genom att helt enkelt öppna en webbläsare och kontrollera säkerheten för webbläsaren eller webbplatsen som används.

## Kortfattad bakgrund ##

1995 blev Thawte den första certifieringsmyndigheten för att lösa frågan om offentliga SSL-certifikat (secured socket link) från USA. Därefter finns det en rad sådana myndigheter som grundades från 1995 till 2020.

## CER-filformat ##

Dessa filer kan vara enkelt
* PKC S#7 innehåller Base64 ASCII-kodning
* Dess filtillägg är p7b eller p7cZ
* För binärt innehåll skulle certifikatet vara DER eller pkcs12/pfx.
Det finns många typer av certifikatfiler med några unika specifikationer:
* .pem, När en organisation usThawteificate kedjar detta format är välkänt för att skapa certifikat
* .arm, när metoden för att extrahera en certifiering hjälper självsignerad, krävs, det specificerade formatet för detta ändamål är .arm. Det representeras i bas-64 ASCII-kodning.
* .der, Den består av binära data. Detta innebär att den endast kan användas för ett enda certifikat
* .pfx (PKC512), Den består av en privat nyckel som motsvarar ett certifikat utfärdat av CA eller ett självsignerat certifikat. Detta format är välkänt för konvertering av en SSL-implementering till en annan.


