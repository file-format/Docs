{
  "date": "2019-10-11",
  "keywords": [
"djvu fil",
"djvu filformat",
"hvad er en djvu-fil",
"fil",
"djvu eksempel",
"djvu filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DJVU filformat",
  "description": "Lær om DJVU-filformater og API'er, der kan oprette og åbne DJVU-filer.",
  "linktitle": "DJVU",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-djv-dau"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en DJVU fil?

DjVu, udtales som déjà vu, er et grafikfilformat beregnet til scannede dokumenter og bøger, især dem, der indeholder en kombination af tekst, tegninger, billeder og fotografier. Det er udviklet af AT&T Labs. Det bruger flere teknikker som billedlagsadskillelse af tekst og baggrundsbilleder, progressiv indlæsning, aritmetisk kodning og tabskomprimering for bitonale billeder. Da DJVU-fil kan indeholde komprimerede, men alligevel højkvalitets farvebilleder, fotografier, tekst og tegninger og kan gemmes på mindre plads derfor, bruges den på nettet som e-bøger, manualer, aviser, gamle dokumenter osv.

DjVu kan bedømmes som et overlegent alternativ til [PDF](/pdf/). Filtypenavne knyttet til DjVu er .DJVU eller .DJV. DjVu kan opnå komprimeringsforhold omkring 5 – 10 bedre end eksisterende metoder såsom [JPEG](/image/jpeg/) og [GIF](/image/gif/) for farvedokumenter og 3 – 8 gange bedre end [TIFF](/image/tiff/) i sort/hvide dokumenter. Scannede dokumenter ved 300 DPI med fuldfarve op til 25 MB kan komprimeres ned til 30 til 100 KB. På samme måde kan sort-hvide dokumenter komprimeres op til 5 til 30 KB. Gennemsnitlig HTML-side kan være op til 50 KB, derfor kan disse dokumenter uploades på nettet uden problemer.

## Kort historie ##

The DjVu technology was developed in AT&T labs by [Yann LeCun](https://en.wikipedia.org/wiki/Yann_LeCun), [Léon Bottou](https://en.wikipedia.org/wiki/L%C3%A9on_Bottou), Patrick Haffner, and Paul G from 1996 to 2001. DjVu-filformatet har gennemgået forskellige revisioner, den seneste er fra 2005.


|Version|Udgivelsesdato|Bemærkninger
---|---|---|
|1–19|1996–1999|Dette er udviklingsversionerne.
|20|April 1999|Enkeltside blev ændret til flersideformat.
|23|Juli 2002|CID-del
|24|Februar 2003|LTAnno chunk
|21|September 1999|Indirekte lagerformat udskiftet. Tekstsøgningslag blev tilføjet.
|22|April 2001|Sideretning, farve JB2
|25|Maj 2003|NAVM-klump. Understøttelse af DjVu-bogmærker blev tilføjet.
|26|April 2005|Tekst/linjekommentarer

## DjVu filformat ##

DjVu documents are IFF85 files. The structure provides a hierarchy of containers which holds information in a DjVu file. These containers are also called “Chunks”. Chunk type and Chunk ID describes how the chunk is used. There is a 4byte header followed by IFF structure. The first four bytes of a DjVu file are 0x41 0x54 0x26 0x54. Dette afsnit diskuterer de forskellige slags DjVu-dokumenter og de tilsvarende bidder, som de består af.


|Chunk ID|Brug
---|---|
|FORM|Den sammensatte chunk har de første fire databytes af FORM chunken, som er sekundær identifikator.
|FORM:DJVM|Et flersidet DjVu-dokument. Sammensat chunk, der indeholder DIRM chunk.
|FORM:DJVU|Enkeltsidet DjVu-dokument. Sammensat chunk, der indeholder de bidder, der udgør en side i et djvu-dokument.
|FORM:DJVI|En delt DjVu-fil, som er inkluderet via INCL-klumpen. Delt annoteringer og formordbog.
|FORM:THUM|Sammensat chunk, der indeholder TH44 chunks, som er de indlejrede thumbnails.
|DIRM|Sidenavnoplysninger for flersidede dokumenter.
|NAVM|Bogmærkeoplysninger
|ANTa, ANTz|Annoteringer inklusive både indledende visningsindstillinger og overlejrede hyperlinks, tekstbokse osv.
|TXTA, TXTz|Unicode Tekst- og layoutoplysninger.
|Djbz|Delt formbord.
|Sjbz|BZZ komprimerede JB2-bitonale data, der bruges til at gemme maske.
|FG44|IW44-data bruges til at gemme forgrunden
|BG44|IW44-data bruges til at gemme baggrund
|TH44|IW44-data, der bruges til at gemme indlejrede miniaturebilleder
|WMRM|JB2-data kræves for at fjerne et vandmærke
|FGbz|Farve JB2-data. Giver en farve for hver (blit eller form?) i den tilsvarende Sjbz chunk.
|INFO|Information om a DjVu-siden
|INCL|ID'et for en inkluderet FORM:DJVI-del.
|BGjp|JPEG-kodet baggrund
|FGjp|JPEG-kodet forgrund
|Smmr|G4-kodet maske

### DJVU-komprimering

Et enkelt billede er opdelt i mange forskellige billeder, og derefter komprimeres hvert billede separat. Til oprettelse af en DjVu-fil opdeles billedet først i tre billeder, en baggrund, forgrund og et maskebillede. Typisk er baggrunds- og forgrundsbillederne farvebilleder med lavere opløsning; men maskebilledet er et billede i højere opløsning, og teksten er typisk gemt der. Efter adskillelsen komprimeres forgrunds- og baggrundsbillederne gennem en wavelet-baseret komprimeringsalgoritme IW44, mens maskebilledet komprimeres ved hjælp af en anden metode kaldet JB2.

JB2-kodningsmetoden eliminerer meget af redundansen i tekstbilledet ved at identificere identiske former på siden, såsom flere forekomster af et tegn i en bestemt skrifttype. JB2 koder først bitmappet for hver unik form ved at drage fordel af redundansen mellem lignende former. Den koder derefter de steder, hvor hver figur vises på siden. Både JB2 og IW44 er afhængige af en ny type adaptiv binær aritmetisk koder kaldet ZP-koderen, der presser enhver resterende redundans ud inden for et par procent af Shannon-grænsen. ZP-koderen er adaptiv og hurtigere end andre tilnærmede binære aritmetiske kodere.

## Referencer ##

* [DjVu - Wikipedia](https://en.wikipedia.org/wiki/DjVu)

* [DjVu File Format](https://www.cuminas.jp/docs/techinfo/DjVu3Spec.pdf)

