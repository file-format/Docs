{
  "date" : "2022-05-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Torrent-filformat - BitTorrent-fil",
  "description":"Läs mer om TORRENT-filer och API:er som kan skapa och öppna TORRENT-filer.",
  "linktitle" : "TORRENT",
  "menu" : {
    "docs" : {
      "identifier":"misc-torrent",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## Vad är en TORRENT fil?

En TORRENT-fil är en textfil som används av BitTorrent och andra P2P-program (peer-to-peer) för nedladdning och utbyte av innehåll. Det nedladdningsbara innehållet kan innehålla dokument, videor, spel, filmer och andra medier som finns tillgängliga på internet. Den innehåller metadatainformation om innehållet och platsen för media som ska laddas ner. Programvara som BitTorrent använder information från denna fil såsom namn, filstorlek och mappstruktur för nedladdning av data. Torrentfiler kan konverteras till andra filformat som [PDF](/sv/pdf/) online.

## Vad är Torrenting? Filformatet TORRENT för datautbyte

Torrenting är konceptet med utbyte (nedladdning och uppladdning) av datafiler med hjälp av BitTorrent-nätverket. Till skillnad från konventionella servrar där data laddas upp för andra att komma åt och ladda ner, hämtas och skickas torrentfiler med hjälp av torrentnätverket. När en användare öppnar en .torrent-fil i applikationer som BitTorrent, börjar programvaran ladda ner innehållet i filen bitvis. Om flera användare har samma fil delar BitTorrent upp nedladdningar mellan alla användare för att påskynda nedladdningsprocessen. Samtidigt blir datorn för användaren som laddar ner filen också filkällan för att skicka den till andra användare som också laddar ner samma fil.

### Struktur för en TORRENT-fil

En torrentfil är en kombination av en lista med filer och metadatainformation om alla delar av filen som ska laddas ner. Den innehåller följande information i form av nycklar.

- "annonsera" - URL:en till spåraren som tillkännages för andra peers för att informera om filens tillgänglighet
- `info` — Detta mappar till en ordbok vars nycklar är beroende av om en eller flera filer delas:
  - files—a list of dictionaries each corresponding to a file (only when multiple files are being shared). Each dictionary has the following keys:
- 'längd' — storleken på filen i byte.
- `sökväg` — en lista med strängar som motsvarar underkatalognamn, varav den sista är det faktiska filnamnet
- `längd` — storleken på filen i byte (endast när en fil delas)
- `namn` — filnamn där filen ska sparas
- "piece length" — antal byte per bit. Detta är vanligtvis 28 KiB = 256 KiB = 262 144 B.
- `bitar` — en hashlista som är en sammanlänkning av varje bits SHA-1-hash.

## Är Torrenting säkert och lagligt?

Torrenting-protokoll för utbyte av data mellan P2P-användare är säkert eftersom det bara är ett sätt att dela vilken typ av fil som helst. Protokollet i sig är alltså inte osäkert eller olagligt. Innehållet som delas via nätverket kan dock innehålla filer eller media som kan bryta mot den juridiska statusen för de delade dokumenten. I sådana fall kan utbytet av sådan information orsaka rättsliga åtgärder mot de parter som är inblandade i att dela sådana filer offentligt.

## Referenser

* [TORRENT-fil - wikipedia](https://en.wikipedia.org/wiki/Torrent_file)

