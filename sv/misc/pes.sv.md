{
  "date" : "2021-07-29",
  "keywords" :[ "pes fil", "pes filformat", "vad är en pes fil", "fil", "pes exempel", "pes filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PES-filformat - Brother PE-broderiformat",
  "description":"Läs mer om PES-filformat och API:er som kan skapa och öppna PES-filer.",
  "linktitle" : "PES",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2021-07-29"
}

## Vad är en PES-broderifil?

PES-broderifilen är en designfil som innehåller instruktioner för broderi-/symaskinerna. Det utvecklades av Brother Industries för deras broderimaskiner men formaliserades senare som ett allmänt filformat. PES-filer används av symaskiner för att läsa instruktioner för att sy ett mönster på tyg. Dessa filer tjänar två syften; först tillhandahåller designinformation för PE-Design-applikation utvecklad av Brother Industries och för det andra tillhandahåller designnamn, färger och broderimaskinkoder som "stopp", "hopp" och "trim".

## PES-filformat - Mer information

En PES-fil sparas på skiva i binärt filformat. Den innehåller flera sektioner som har sömnadsinformation lagrad med fördefinierad metod. PES-filformatet är som följer.

* Version Data - Ger versionsinformation och kan vara valfritt värde `#PES0001`, `#PES0020`, `#PES0030`, `#PES0040`, `#PES0050`, `#PES0055`, `#PES0060`
* PEC Seek Value - Ett 4 byte little-endian heltal som följer omedelbart efter versionsdata och representerar sökvärdet för PEC-sektionen som innehåller designdetaljer Information
* PSE-avsnittet - Innehåller designinformation som är relevant för Brother PE-design och kan vara andra sömnadstillämpningar
* PCE-sektion - Kan finnas var som helst i PSE-filen men refereras av PEC Seek Value.

## Typ av symaskiner som använder PES-fil

PES-filer skapas i första hand av PE-Design-programvaran som används med Brothers symaskiner. Några andra maskiner som kan stödja PES-filer inkluderar Babylock och Bernina hembroderimaskiner.

## Hur konverterar man PSE-filer?

PE-Design-programvaran kan [konvertera PSE-fil](https://support.brother.com/g/s/hf/htmldoc/ped/im/ped11/en/PED11_EN/index.html#!/11_1088392?hl =pes+fil) till andra format som .pes, .dst, .exp, .pcs, .hus, .vip, .shv, .jef, .sew, .csd eller .xxx. Det kan göras med PE-Design-applikationen genom att öppna filen och välja konverteringsformat.

## Referenser

* [PE Design - Instruktionsmanual](https://support.brother.com/g/s/hf/htmldoc/ped/im/ped11/en/PED11_EN/index.html#!/)

