{
  "date" : "2019-12-12",
  "keywords" :[ "EPUB", "fil", "tillägg", "format", "E-bok", "Digital bok" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Läs mer om EPUB-filformat och API:er som kan skapa och öppna EPUB-filer.",
  "title" :"Vad är en EPUB-fil?",
  "linktitle" : "EPUB",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2019-12-12"
}

## Vad är en EPUB fil?

Filer med filtillägget .epub är ett e-boksfilformat som tillhandahåller ett standardformat för digitala publikationer för förlag och konsumenter. Formatet har varit så vanligt vid det här laget att det stöds av många e-läsare och mjukvaruapplikationer. Till exempel, på Mac OS, ger den förinstallerade programvaran **Books** stöd för att öppna sådana filer. Dessutom finns det en hel del kompatibel mjukvara för smartphones, surfplattor och datorer. EPUB-filstandarder underhålls av [International Digital Publishing Forum ](https://idpf.org/epub/30/spec/epub30-publications.html)(IDPF). Versionen EPUB 3 är också godkänd av Book Industry Study Group (BISG), en ledande bokhandelsorganisation för standardiserade bästa praxis, forskning, information och evenemang, för paketering av innehåll.

## Kort historik över EPUB-filformat

* **oktober 2007** - EPUB 2.0 godkändes
* **September 2010** - Underhållsuppdatering släpptes
* **oktober 2011** - EPUB 3.0-specifikationerna trädde i kraft
* **Juni 2014** - Mindre underhållsuppdatering släpptes för att ersätta 3.0-versionen
* **Januari 2017** – EPUB 3.1 trädde i kraft

## EPUB filformat

EPUB-filformatet är ett arkiv som kan döpas om till [ZIP](/sv/compression/zip/) förlängning och dess innehåll kan ses genom att extrahera arkivet med valfri arkivextraktor. Det är ett öppet XML-baserat format och består av HTML-filer, bilder, CSS-formatmallar och andra element. Den kan också konverteras till PDF, Mobi och flera andra filformat genom ett antal mjukvaruapplikationer och API:er.

{{< figure src="../epub.png" alt="EPUB filformat" >}}

**EPUB E-bok öppnad med Mac OS Books Application**

EPUB-filformatet är baserat på följande tre öppna standarder.

### Open Public Structure (OPS) ###

En EPUB 2.0-fil använder XHTML 1.1 för att konstruera innehållet i en publikation. I huvudsak betyder detta att en EPUB-fil består av en eller flera webbsidor. Även om du skulle kunna inkludera hela innehållet i en bok eller tidning på en enda sida, är det bättre att en sådan fil inte överstiger 300K, både av prestanda- och kompatibilitetsskäl. Precis som med vanliga webbsidor definieras stilen och layouten med hjälp av cascading style sheets (CSS). I EPUB-filer måste en delmängd (begränsad serie av kommandon) av CSS2 användas. Många av de nya funktionerna i CSS3, som rundade rutor eller skuggor, är inte tillgängliga ännu. För bakåtkompatibilitet kan en skapare också använda DTBook istället för XHTML för att koda innehållet.

### Open Packaging Format (OPF) ###

Den här delen av specifikationerna handlar om strukturell information som metadata (vem är författaren och utgivaren, vad är titeln,...), manifestet (en lista över alla filer i en epub-fil) och innehållsförteckningen. Alla dessa data är inbäddade med XML.

### Open Container Format (OCF) ###

Som ovanstående beskrivningar borde ha gjort det klart består ett EPUB-dokument av en serie filer. OCF-specifikationerna definierar hur alla dessa filer slutar paketeras i en enda containerfil. ZIP-komprimering används för detta.

## Bildfilformat som stöds ##

Filformatet EPUB stöder följande bildfilformat.

* [GIF](/sv/image/gif/)
* [JPG](/sv/image/jpeg/)
* [PNG](/sv/image/png/)
* [SVG](/sv/page-description-language/svg/),

## Referenser ##

* [EPUB - av Wikipedia](https://en.wikipedia.org/wiki/EPUB)

