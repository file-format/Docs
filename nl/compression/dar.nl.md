{
  "date" : "2021-04-08",
  "keywords" :[ "dar file", "dar file format", "wat is een dar file", "file", "dar example", "dar file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DAR - Disk Archiver-bestandsindeling",
  "description":"Meer informatie over DAR-bestandsindelingen en API's die DAR-bestanden kunnen maken en openen.",
  "linktitle" : "DAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-09"
}

## Wat is een DAR-bestand?

Een bestand met de extensie .dar is een gecomprimeerd archief dat is gemaakt met behulp van het DAR Disk-archief. Het kan een back-up/archief maken voor de volledige schijf of een groep bestanden. Het is gemaakt om de bestandsindeling [TAR](/nl/compression/tar/) op UNIX OS te vervangen en kan worden gemaakt als gesplitste archiefbestanden voor een groot aantal bestanden. DAR-archief ondersteunt de optie om bestanden van het systeem te verwijderen die zijn gekoppeld aan de hoofdbestanden in het archief. De mogelijkheden om differentiële, incrementele en decrementele back-up te bieden, maken het superieur dan TAR-bestanden.

## DAR-bestandsindeling

DAR-bestanden zijn gecomprimeerde archieven die elke compressie per bestand kunnen gebruiken, zoals [gzip](/nl/compression/gz/), [bzip2](/nl/compression/bz2/), lzo, xz of lzma. De exacte bestandsindeling van een DAR-bestand hangt af van het type opmaak dat wordt gebruikt om de inhoud van het archief te comprimeren. Het staat ook optionele Blowfish, Twofish, AES, Serpent, Camellia encryptie en public key encryptie en handtekening (OpenPGP) toe.

### DAR-functies

Enkele kenmerken van het DAR-bestandsformaat zijn als volgt.

* Zorgt voor elk type inode (directory, gewone bestanden, symlinks, speciale apparaten, benoemde buizen, stopcontacten, deuren, ...)
* Zorgt voor hard-linked inodes (hard-linked platte bestanden, char devices, block devices, hard-linked symlinks)
* Zorgt voor schaarse bestanden
* Zorgt voor Linux-bestand Extended Attributes,
* Zorgt voor Linux-bestand ACL
* Zorgt voor Mac OS X-bestandsvorken
* Zorgt voor een aantal bestandssysteemspecifieke attributen zoals de geboortedatum van het HFS+ bestandssysteem en onveranderlijke, data-journaling, secure-deletion, no-tail-merging, undeletable, noatime attributen van het ext2/3/4 bestandssysteem.
* Per-bestandscompressie met gzip, bzip2, lzo, xz of lzma (in tegenstelling tot het comprimeren van het hele archief). Een persoon kan ervoor kiezen om reeds gecomprimeerde bestanden niet te comprimeren op basis van hun bestandsnaamachtervoegsel.
* Snel uitpakken van bestanden van overal in het archief
* Snelle lijst van archiefinhoud door de catalogus met bestanden in het archief op te slaan
* Live bestandssysteemback-up: detecteert wanneer een bestand is gewijzigd terwijl het werd gelezen voor back-up en kan opnieuw proberen het op te slaan tot een bepaald maximum aantal nieuwe pogingen
* Hashbestand (MD5, SHA1 of SHA-512) on-fly gegenereerd voor elke slice, het resulterende bestand is compatibel met md5sum of sha1sum, om snel de integriteit van elke slice te kunnen controleren
* Bestandssysteem onafhankelijk: het kan gebruikt worden om een systeem te herstellen naar een partitie van een andere grootte en/of naar een partitie met een ander bestandssysteem[5]

## Referenties

* [DAR](http://dar.linux.free.fr/)
* [DAR Disk Archiver](https://en.wikipedia.org/wiki/Dar_(disk_archiver))

