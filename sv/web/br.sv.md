{
  "date" : "2022-08-20",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BR-fil - Brotli-komprimerat filformat",
  "description":"Läs mer om BR-filformat och API:er som kan skapa och öppna BR-filer.",
  "linktitle" : "BR",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-08-20"
}

## Vad är BR fil?

En BR-fil är en komprimerad webbfil som genereras genom att använda datakomprimeringsalgoritmen med öppen källkod, **Brotli**. Den används för att lagra webbsidor som stilmallar ([CSS](/sv/web/css/)), bilder ([SVG](/sv/image/svg/)), [XML](/sv/web/xml/) och skript filer ([JS](/sv/web/js/)). Moderna webbplatser, som Chrome och Firefox, använder BR-filer för att minska sidladdningstiden, vilket resulterar i en bättre användarupplevelse.

## BR filformat

BR-filer är komprimerade webbfiler som genereras med Brotli-komprimeringsalgoritmen. Brotli-komprimering är en förlustfri datakomprimeringsalgoritm och utvecklades av Google till Zopfli-komprimeringsalgoritmen. Den är baserad på en kombination av LZ77 förlustfri komprimeringsalgoritm och Huffman-kodning.

På grund av dess ringa storlek används BR-filer av webbservrar och innehållsleveransnätverk (CDN). De förfrågningar som görs till dessa servrar resulterar i komprimering av HTTP-innehåll, vilket gör att webbplatser laddas snabbare. Brotli har blivit mer populärt och ger bättre komprimering än gzip.

## Referenser

* [Brotli - Wikipedia](https://en.wikipedia.org/wiki/Brotli)

