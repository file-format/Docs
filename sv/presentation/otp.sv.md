{
  "date" : "2021-01-21",
  "keywords" :[ "otp-fil", "otp-filformat", "vad är en otp-fil", "fil", "otp-exempel", "otp-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OTP - OpenDocument Presentation Template",
  "description":"Läs mer om OTP-filformat och API:er som kan skapa och öppna OTP-filer.",
  "linktitle" : "OTP",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2021-01-21"
}

## Vad är en OTP-fil?

Filer med tillägget .otp representerar presentationsmallfiler skapade av applikationer i OASIS OpenDocument standardformat. Innehållet i en sådan fil inkluderar presentationsinformation i form av bilder med text, bilder, former, multimediainnehåll, övergångseffekter och andra bildelement. Dessa mallfiler används för att snabbt skapa nya presentationer baserat på stilinformationen som lagras i själva mallen. OTP-filer kan skapas och sparas med flera olika applikationer som Impress som följer med OpenOffice-sviten och Microsoft PowerPoint. OTP-filformatet liknar Microsoft PowerPoint-mallfilerna [.pot](/sv/presentation/pot/) och [.potx](/sv/presentation/potx/).

## OTP-filformat

OTP-filformatet är baserat på OpenDocument-standarden som stöder dokumentrepresentation som ett enda XML-dokument samt insamling av flera underdokument i ett enda zippat paket i formatet [ZIP](/sv/compression/zip/). Innehållet i filen distribueras i flera xml-filer paketerade tillsammans. Dessa flera [XML](/sv/web/xml/)-filer innehåller information om stil, innehåll, metainformation och inställningar för dokumentet enligt nedan.

* `content.xml` – Dokumentinnehåll och automatiska stilar som används i innehållet.
* `styles.xml` – Stilar som används i dokumentinnehållet och automatiska stilar som används i själva stilarna.
* `meta.xml` – Dokumentmetainformation, till exempel författaren eller tidpunkten för den senaste lagringsåtgärden.
* `settings.xml` – Programspecifika inställningar, såsom fönsterstorlek eller skrivarinformation.

## Referenser

* [OpenDocument - Av Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

