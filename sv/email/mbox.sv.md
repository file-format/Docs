{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MBOX - Fil för e-postbrevlåda",
  "description":"Läs mer om MBOX-filformat och API:er som kan skapa och öppna MBOX-filer.",
  "linktitle" : "MBOX",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en MBOX fil?

MBox-filformat är en generisk term som representerar en behållare för insamling av elektroniska postmeddelanden. Meddelanden lagras inuti behållaren tillsammans med deras bilagor. Meddelanden från en hel mapp sparas i en enda databasfil och nya meddelanden läggs till i slutet av filen. Många applikationer och API ger stöd för MBox-filformat som Apple Mail och Mozilla Thunderbird.

## MBOX-filformat ##

MBox-filformatet förblev icke-standardiserat under ganska lång tid fram till 2005 då applikationen/mbox standardiserades som [RFC 4155.](https://tools.ietf.org/rfc/rfc4155.txt) Meddelanden, i RFC 2822-format , är sammanlänkade i MBox-filformatet efter varandra. Varje meddelande börjar med en avgränsningsrad som identifierar meddelandeavsändaren och identifierar även datum och tid då meddelandet togs emot av den slutliga mottagaren (antingen sista hopp-systemet i överföringsvägen eller systemet som fungerar som mottagarens postbutik). Varje meddelande avslutas vanligtvis med en tom rad. Slutet på databasen känns vanligtvis igen av antingen frånvaron av ytterligare data eller av närvaron av en explicit filslutmarkör.

## Läser ett meddelande från MBox fil ##

En läsare skannar igenom en mbox-fil och letar efter From_-linjer. Vilken From_-rad som helst markerar början på ett meddelande. Läsaren ska inte försöka dra fördel av att varje From_-rad (förbi början av filen) är tom. När läsaren väl hittar ett meddelande extraherar den en (möjligen skadad) kuvertsändare och leveransdatum från From_-raden. Den läser sedan tills nästa From_-rad eller slutet av filen, beroende på vad som kommer först. Den tar bort den sista tomma raden och tar bort citatet av >From_ lines och >>From_ lines och så vidare. Resultatet är ett RFC 822-meddelande.

## Kodningsöverväganden ##

Innehållet i en MBox-fil kan bli oåterkalleligt blandad när ett mottaget e-postmeddelande innehåller en Mbox-fil som bilaga och sparas i en annan Mbox-fil. För att undvika detta måste meddelandesystem koda en mbox-databas med icke-transparent överföringskodning (som BASE64 eller Quoted-Printable) närhelst ett sådant objekt överförs via meddelandeprotokoll. Implementerare bör också vara beredda att koda mbox-data lokalt om icke-kompatibla data tas emot.

## Referenser ##

* [MBox - RFC4155](https://tools.ietf.org/rfc/rfc4155.txt)
* [Mbox - Wikipedia](https://en.wikipedia.org/wiki/Mbox)

