{
  "date": "2021-03-30",
  "keywords": [
"PMLZ",
"Lynlåst Palm Markup Language File",
"udvidelse",
"Fil",
"format",
"e-bog",
"Palm Markup Language"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om PMLZ-filformat, Palm Markup Language og API'er, der kan oprette og åbne PMLZ-filer.",
  "title": "PMLZ - Zipped Palm Markup Language File",
  "linktitle": "PMLZ",
  "menu": {
    "docs": {
      "parent": "ebook",
      "identifier": "ebook-pml-daz"
}
},
  "lastmod": "2021-03-30"
}

## Hvad er en PMLZ fil?

Palm Inc introducerede en e-bog filtype; kendt som PMLZ-filformatet, som er en komprimeret version af [PML](/ebook/pml/)-filformatet, og derfor er filerne med .pmlz-udvidelser kendt som **Zipped Palm Markup Language File**. PMLZ-filen er blot en zip-beholder af en fil, der kompilerer [PDB](/programming/pdb/)-filer for at oprette dokumenter til **eReader** (kendt som en e-bogslæseenhed, såsom en tablet-computer). PML-filen giver layoutet til en PDB-fil (indeholder forskellige datafiler) til visning på en Palm-enhed. Hvorimod en PDB-fil er en databasefil, som bruges af forskellige applikationer, herunder Quicken, Pegasus, Microsoft Visual Studio og Palm Pilot. Kort sagt er en PMLZ en komprimeret beholder af PML- og PDB-filer.


## Viden om Palm Markup Language
Følgende tabel specificerer PML-kommandoer:

|Kommando|Beskrivelse|
---|---|
| \p | Ny side |
| \x | Nyt kapitel; forårsager også et nyt sideskift. Omslut kapiteltitel (og eventuelle stilkoder) med \x og \x |
| \Xn | Nyt kapitel, indrykket n niveauer (n mellem 0 og 4 inklusive) i kapiteldialogen; forårsager ikke sideskift. Omslut kapiteltitel (og eventuelle stilkoder) med \Xn og \Xn |
| \Cn=Kapiteltitel | Indsæt Kapiteltitel i kapiteloversigten med niveau n (som \Xn). Teksten vises ikke på siden og fremtvinger ikke et sideskift. Det kan nogle gange være nyttigt at indsætte et kapitelmærke i begyndelsen af en introduktion til kapitlet, f.eks. |
| \c | Centrer denne tekstblok; luk med \c i begyndelsen af linjen |
|             \r              |                                                                                                    Right justify text block; close with \r on beginning of line                                                                                                     |
| \i | Kursiv blok; lukke med \i |
| \u | Understreget blok; luk med \u |
| \o | Overslagsblok; lukke med \o |
| \v | Usynlig tekst; luk med \v (kan bruges til kommentarer) |
| \t | Indrykningsblok. Start ved begyndelsen af en linje, luk med \t i slutningen af en linje |
| \T=50% | Indrykker den angivne procentdel af skærmbredden, 50 % i dette tilfælde. Hvis den aktuelle tegningsposition allerede er forbi den angivne skærmplacering, ignoreres dette tag. |
| \w=50% | Integrer en vandret regel for en given procentvis bredde af skærmen, i dette tilfælde 50 %. Dette tag forårsager et linjeskift før og efter det. Reglen er centreret. Procenttegnet er obligatorisk. |
| \n | Skift til den normale skrifttype, som er angivet af brugeren |
| \s | Skift til stdFont; luk med \s for at vende tilbage til normal skrifttype |
| \b | Skift til fed skrifttype; luk med \b for at vende tilbage til normal skrifttype (forældet; brug \B i stedet) |
| \l | Skift til largeFont; luk med \l for at vende tilbage til normal skrifttype |
| \B | Marker tekst som fed. I modsætning til \b-tagget ændrer \B ikke skrifttypen, så du kan have stor fed tekst. Du kan ikke blande \b og \B i den samme PML-fil. |
| \Sp | Marker tekst som hævet. Bør ikke blandes med andre stilarter såsom fed, kursiv osv. Vedlæg overskrevet tekst med \Sp. |
| \Sb | Marker tekst som underskrift. Bør ikke blandes med andre stilarter såsom fed, kursiv, osv. Vedlæg indskrevet tekst med \Sb. |
| \k | Lav lukket tekst til små bogstaver; lukke med \k. Eventuelle tegn indesluttet i \k tags (inklusive dem med accenter) er lavet med store bogstaver og gengives med en mindre punktstørrelse end et almindeligt stort tegn. |
| \\ | Repræsenterer en enkelt omvendt skråstreg |
| \aXXX | Indsæt ikke-ASCII-tegn, hvis Windows-1252-kode er decimal XXX. Se PML-tegntabellen for detaljer. |
| \UXXXX | Indsæt ikke-ASCII-tegn, hvis Unicode-kode er hexadecimal XXXX. Se den udvidede PML-tegntabel for detaljer. |
| \m=imagename.png | Indsæt det navngivne billede. Se afsnittet om billeder nedenfor. |
| \q=#linkanchorNoget tekst\q | Henvis til et linkanker, som er et andet sted i dokumentet. Strengen efter ankerspecifikationen og før den afsluttende \q er understreget eller på anden måde vist som et link, når dokumentet vises. |
| \Q=linkanchor | Angiv et linkanker i dokumentet. |
| \- | Indsæt en blød bindestreg. En blød bindestreg vises kun, hvis det er nødvendigt at bryde et ord over en linje. |
| \Fn=fodnote11\Fn | Link 1 til en fodnote, hvis navn er fodnote1, tagget i slutningen af PML-dokumentet. Se afsnittet om fodnoter og sidebjælker nedenfor. |
| \Sd=sidebjælke1Sidebjælke\Sd | Link Sidebar-teksten til en sidebar, hvis navn er sidebar1, tagget i slutningen af PML-dokumentet. Se afsnittet om fodnoter og sidebjælker nedenfor. |
| \I | Markér som et referenceindekselement. Indsæt indekselement (og eventuelle stilkoder) med \I og \I.|


## Referencer

* [Palm Markup Language - Af MobileRead](https://wiki.mobileread.com/wiki/EReader)

* [E-Reader - By MobileRead](https://en.wikipedia.org/wiki/E-reader)


