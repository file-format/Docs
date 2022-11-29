{
  "date" : "2021-04-08",
  "keywords" :[ "dar-fil", "dar-filformat", "vad är en dar-fil", "fil", "dar-exempel", "dar-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DAR - Disk Archiver File Format",
  "description":"Läs mer om DAR-filformat och API:er som kan skapa och öppna DAR-filer.",
  "linktitle" : "DAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-09"
}

## Vad är en DAR fil?

En fil med filtillägget .dar är ett komprimerat arkiv skapat med hjälp av DAR Disk-arkivet. Det kan skapa backup/arkiv för hel disk eller en grupp filer. Det skapades för att ersätta filformatet [TAR](/sv/compression/tar/) på UNIX OS och kan skapas som delade arkivfiler för ett stort antal filer. DAR-arkivet stöder möjligheten att ta bort filer från systemet som är länkade till huvudfilerna i arkivet. Dess förmåga att tillhandahålla differentiell, inkrementell och dekrementell säkerhetskopiering gör den överlägsen än TAR-filer.

## DAR-filformat

DAR-filer är komprimerade arkiv som kan använda valfri komprimering per fil som [gzip](/sv/compression/gz/), [bzip2](/sv/compression/bz2/), lzo, xz eller lzma. Det exakta filformatet för en DAR-fil beror på vilken typ av formatering som används för att komprimera innehållet i arkivet. Den tillåter också valfri Blowfish, Twofish, AES, Serpent, Camellia-kryptering och offentlig nyckelkryptering och signatur (OpenPGP).

### DAR-funktioner

Några av funktionerna i DAR-filformatet är följande.

* Tar hand om alla typer av inoder (katalog, vanliga filer, symboliska länkar, speciella enheter, namngivna rör, uttag, dörrar, ...)
* Tar hand om hårt länkade inoder (hårt länkade vanliga filer, char-enheter, blockenheter, hårt länkade symboliska länkar)
* Tar hand om glesa filer
* Tar hand om Linux-filens utökade attribut,
* Tar hand om Linux-filen ACL
* Tar hand om Mac OS X-filgafflar
* Tar hand om vissa filsystemspecifika attribut som födelsedatum för HFS+ filsystem och oföränderliga, datajournalföring, säker radering, no-tail-sammanslagning, oborrbara, noatime-attribut för ext2/3/4 filsystem.
* Komprimering per fil med gzip, bzip2, lzo, xz eller lzma (i motsats till att komprimera hela arkivet). En individ kan välja att inte komprimera redan komprimerade filer baserat på deras filnamnssuffix.
* Snabbextrahering av filer från var som helst i arkivet
* Snabb lista över arkivinnehåll genom att spara katalogen med filer i arkivet
* Säkerhetskopiering av live filsystem: upptäcker när en fil har ändrats medan den lästes för säkerhetskopiering och kan försöka spara den upp till ett givet maximalt antal återförsök
* Hash-fil (MD5, SHA1 eller SHA-512) genererad direkt för varje skiva, den resulterande filen är kompatibel med md5sum eller sha1sum, för att snabbt kunna kontrollera varje skivas integritet
* Filsystemoberoende: det kan användas för att återställa ett system till en partition av en annan storlek och/eller till en partition med ett annat filsystem[5]

## Referenser

* [DAR](http://dar.linux.free.fr/)
* [DAR Disk Archiver](https://en.wikipedia.org/wiki/Dar_(disk_archiver))

