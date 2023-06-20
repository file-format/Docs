{
  "date" : "2022-08-05",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ATOM File - Atom Syndication Format",
  "description" :"Läs mer om vad en ATOM-fil och API:er är som kan skapa och öppna ATOM-filer.",
  "linktitle" : "ATOM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-08-05"
}

## Vad är ATOM fil?

En ATOM-fil är ett syndikeringsformat för strukturen för Atom-flöden och inträdesdokument. I likhet med .RSS-filer är ATOM-filformatet ett XML-baserat syndikeringsformat som är en standard för publicering av innehåll. En ATOM-fil används för webbflöden som gör att program kan söka efter uppdateringar som publiceras på webbplatsen. Den innehåller poster som kan vara av olika slag såsom rubriker, fulltextartiklar, utdrag eller länkar till innehåll på en webbplats

Applikationer som kan **öppna ATOM-filer** inkluderar **Apple Safari**.

## ATOM-filformat - Mer information

ATOM-filer lagras och publiceras i det populära XML-filformatet som är ett universellt format för utbyte av information. Det utvecklades som ett alternativ till RSS med tanke på begränsningarna och bristerna i RSS-filformatet.

### Typer av Atom-dokument

1. `Atom Entry Documents` - Det är ett XML-dokument som består av en enda informationspost, känd som entry, för Atom-flödet. Den har en atom-entry element som innehåller ett antal underordnade element. Innehållet i en Atom-post kan vara vanlig text, HTML, XHTML eller en annan IANA-mediatyp (Internet Assigned Numbers Authority).
1. `Atom Feed Documents` - Det är ett XML-dokument som tillhandahåller metadata om ett Atom-flöde och en eller flera poster för flödet. När en klient gör en begäran om information från flödet, genereras flödesdokumentet av servern som inkluderar ett antal Atom-poster för att uppfylla begäran.
1. `Atom Collection` - Det är en speciell typ av Atom-flödesdokument som innehåller URL:erna till Atom-poster som är tillgängliga för redigering.

## Referenser

* [Atom Syndication Format - RFC](https://www.rfc-editor.org/rfc/rfc4287.html)
* [Översikt över Atom-flöden - IBM](https://www.ibm.com/docs/en/cics-ts/5.4?topic=support-overview-atom-feeds)
* [Atom - Web Standard](https://en.wikipedia.org/wiki/Atom_(web_standard))

