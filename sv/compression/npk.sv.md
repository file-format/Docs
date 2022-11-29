{
  "date" : "2022-06-21",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"NPK-filformat",
  "description":"Läs mer om NPK-filformat och API:er som kan skapa och öppna NPK-filer.",
  "linktitle" : "NPK",
  "menu" : {
    "docs" : {
      "identifier":"compression-npk",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-21"
}

## Vad är en NPK fil?

En NPK-fil är en mjukvaruuppgraderingspaketfil som används av **MikroTik**-routrar för uppgradering av routerns operativsystem. Det kommer som ett komprimerat binärt arkiv som laddas i routern för att installera programuppdateringar. Information som finns i en NPK-fil inkluderar nätverksinformation som IP-adress och IP-tjänst, kontaktinformation (ethernet-gränssnitt och serieport), e-postinställningar, bryggkonfiguration och lokal användarhantering.

## NPK filformat

NPK-filer lagras som komprimerat binärt arkiv. Det är ett slutet filformat som endast används av MikroTik själva. Det är inte avsett att skapa RouterOS-tillägg via tredje part. NPK-filer underhålls av MikroTik själv och uppgraderade versioner av desamma kan laddas ner från nedladdningssektionerna på webbplatsen [MikroTik](https://mikrotik.com/download).

När en NPK-fil laddas upp till en router träder inte routerns OS i kraft om det inte startas om. Därför krävs en omstart för att routerns OS ska kunna uppgraderas.

## Referenser

* [MikroTik - Uppgradering av router OS](https://mikrotik.com/download)
* [Hur man skapar NPK-filer](https://forum.mikrotik.com/viewtopic.php?t=87126)

