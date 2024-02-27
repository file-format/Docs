{
  "date": "2022-08-05",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ATOM-fil - Atom-syndikeringsformat",
  "description": "Lær om, hvad en ATOM-fil og API'er er, der kan oprette og åbne ATOM-filer.",
  "linktitle": "ATOM",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-ato-dam"
}
},
  "lastmod": "2022-08-05"
}

## Hvad er en ATOM fil?

En ATOM-fil er et syndikeringsformat til strukturen af Atom-feed og indgangsdokumenter. I lighed med .RSS-filer er ATOM-filformatet et XML-baseret syndikeringsformat, der er en standard for udgivelse af indhold. En ATOM-fil bruges til web-feeds, der tillader softwareprogrammer at søge efter opdateringer, der er offentliggjort på webstedet. Den indeholder indlæg, der kan være af forskellige typer såsom overskrifter, fuldtekstartikler, uddrag eller links til indhold på en hjemmeside

Programmer, der kan **åbne ATOM-filer**, inkluderer **Apple Safari**.

## ATOM-filformat - flere oplysninger

ATOM-filer gemmes og udgives i det populære XML-filformat, der er et universelt format til udveksling af information. Det blev udviklet som et alternativ til RSS under hensyntagen til begrænsningerne og fejlene i RSS-filformatet.

### Typer af Atom-dokumenter

 1. `Atom Entry Documents` - Det er et XML-dokument, der består af et enkelt informationselement, kendt som entry, for Atom-feedet. Den har et atomindgangselement, der indeholder en række underordnede elementer. Indholdet af en Atom-post kan være almindelig tekst, HTML, XHTML eller en anden IANA (Internet Assigned Numbers Authority) medietype.
 1. `Atom Feed Documents` - Det er et XML-dokument, der giver metadata om et Atom-feed og en eller flere indgange til feedet. Når en klient fremsætter en anmodning om information fra feedet, genereres feeddokumentet af serveren, som inkluderer et antal Atom-indgange for at opfylde anmodningen.
 1. `Atom Collection` - Det er en speciel slags Atom-feeddokument, der indeholder URL'erne for Atom-indgange, der er tilgængelige til at blive redigeret.

## Referencer

* [Atom Syndication Format - RFC](https://www.rfc-editor.org/rfc/rfc4287.html)

* [Overview of Atom Feeds - IBM](https://www.ibm.com/docs/en/cics-ts/5.4?topic=support-overview-atom-feeds)
* [Atom - Web Standard](https://en.wikipedia.org/wiki/Atom_(web_standard))


