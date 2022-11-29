{
  "date" : "2019-10-11",
  "keywords" :[ "tar-fil", "tar-filformat", "vad är en tar-fil", "fil", "tar-exempel", "tar-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TAR - Unix Archive File Format",
  "description":"Läs mer om vad som är en Tar-fil och API:er som kan skapa och öppna TAR-filer.",
  "linktitle" : "TAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en TAR fil?

Filer med tillägget .tar är arkiv skapade med Unix-baserat verktyg för att samla in en eller flera filer. Flera filer lagras i ett okomprimerat format med stöd för att lägga till såväl filer som mappar till arkivet. TAR-verktyget på Unix är kommandobaserat, men filer som skapas stöds av de flesta filarkiveringssystem på nästan alla operativsystem. Den skapades först 1979 av AT&T Bell Laboratories och efterföljande versioner publicerades med tiden.

## TAR-filformat

TAR är ett öppet filformat med fullständiga specifikationer tillgängliga för utvecklarens referens. Dess filstruktur standardiserades i POSIX.1-1988 och senare i POSIX.1-2001. Datauppsättningarna som skapas av tar behåller information om filsystemparametrar som:

* Namn
* Tidsstämplar
* Ägande
* Behörigheter för filåtkomst
* Katalogorganisation

En Tar-fil har inget magiskt nummer. Den innehåller en serie block där varje block består av BLOCKSIZE byte.

Varje fil som arkiveras representeras av ett rubrikblock som beskriver filen, följt av noll eller fler block som ger innehållet i filen. I slutet av arkivfilen finns två 512-byte block fyllda med binära nollor som en filslutmarkör. Ett rimligt system bör skriva en sådan filslutmarkör i slutet av ett arkiv, men får inte anta att ett sådant block finns vid läsning av ett arkiv. I synnerhet utfärdar GNU tar alltid en varning om den inte stöter på den.

Blocken kan vara blockerade för fysiska I/O-operationer. Varje post med n block (där n ställs in av blockeringsfaktorn = 512-storleksalternativet för att tar) skrivs med en enda "write()"-operation. På magnetband är resultatet av en sådan skrivning en enda post. När du skriver ett arkiv ska den sista posten av block skrivas i full storlek, med block efter nollblocket som innehåller alla nollor. Vid läsning av ett arkiv bör ett rimligt system korrekt hantera ett arkiv vars sista post är kortare än resten, eller som innehåller skräpposter efter ett nollblock.

### Tar Header

Liksom alla andra filhuvuden innehåller tar-filrubrikposten metadata om en fil och visas i följande tabell.


|Fältförskjutning|Fältstorlek (Bytes)|Fält
---|---|---|
|0|100|Filnamn
|100|8|Filläge
|108|8|Ägarens numeriska användar-ID
|116|8|Gruppens numeriska användar-ID
|124|12|Filstorlek i byte (oktal bas)
|136|12|Senaste ändringstid i numeriskt Unix-tidsformat (oktal)
|148|8|Kontrollsumma för rubrikpost
|156|1|Länkindikator (filtyp)
|157|100|Namn på länkad fil

Oanvända fält fylls med NUL-byte. En rubrik består av 257 byte som är utfylld med NUL-byte för att göra den fylld till 512 byte-post.

## Referenser ##

* [TAR - av Wikipedia](https://en.wikipedia.org/wiki/Tar_(computing))
* [TAR Basic Format](https://www.gnu.org/software/tar/manual/html_node/Standard.html)

