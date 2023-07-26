{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XAR - Uitbreidbaar archiefbestandsformaat",
  "description":"Meer informatie over XAR-bestandsindelingen en API's die XAR-bestanden kunnen maken en openen.",
  "linktitle" : "XAR",
  "menu" : {
    "docs" : {
    "identifier": "compression-xar",
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-13"
}

## Wat is een XAR-bestand?

Een bestand met de extensie .xar (Extensible Archive Format) is een UNIX-archief dat in gecomprimeerde of niet-gecomprimeerde indeling kan zijn. Het wordt ook gebruikt op Mac OS voor de installatie van pakketten. XAR is open-source en maakte deel uit van Mac OS X 10.5 voor gebruik met de Safari-browser.

## XAR-bestandsindeling

Een [XAR](https://github.com/mackyle/xar/wiki/xarformat)-bestand heeft drie hoofdregio's.

* Koptekst
* Inhoudsopgave
* Hoop

### XAR-koptekst

De XAR-header is als volgt opgebouwd.

|Veld|Gegevenstype|Grootte in bytes|
---|---|---|
|Magic|Unsigned Int 32|4|
|Maat|Niet-ondertekend Int 16|2|
|Versie|Niet-ondertekend Int 16|2|
|TOC lengte gecomprimeerd|Unsigned Int 64|8|
|TOC-lengte niet gecomprimeerd|Unsigned Int 64|8|
|Checksum|Niet-ondertekend Int 32|4|
|Naam berichtoverzicht |Null beëindigd||

De C-structuur van de XAR-header kan als volgt worden gedefinieerd.
```
struct xar_header {
    uint32_t magic;
    uint16_t size;
    uint16_t version;
    uint64_t toc_length_compressed;
    uint64_t toc_length_uncompressed;
    uint32_t cksum_alg;
    /* A nul-terminated, zero-padded to multiple of 4, message digest name
     * appears here if cksum_alg is 3 which must not be empty ("") or "none".
     */
};
```
Merk op dat alle velden van de header (magic, size, version, toc_length_compressed, toc_length_uncompressed, cksum_alg) altijd worden opgeslagen in XAR-bestanden in netwerkbytevolgorde (ook bekend als big endian).

### XAR Inhoudsopgave (TOC)

De inhoudsopgave is een XML-document dat is (en moet) worden gecodeerd als UTF-8. Het wordt aan het begin van het bestand opgeslagen, waardoor het gemakkelijk is om door het archief te scannen om een afzonderlijk bestand uit te pakken. Met het XAR-archief kunt u de afzonderlijke bestanden in het archief onafhankelijk comprimeren/coderen met behulp van verschillende compressieschema's zoals [GZIP](/nl/compression/gz/), [BZIP2](/nl/compression/bz2/) en andere soortgelijke.

```
<?xml version="1.0"?>

<xar>
  <toc>
    <checksum style="sha1">
      <size>20</size>
      <offset>0</offset>
    </checksum>
    <file id="1">
      <name>xar</name>
      <type>file</type>
      <mode>0755</mode>
      <uid>0</uid>
      <gid>0</gid>
      <user>root</user>
      <group>wheel</group>
      <size>81180</size>
      <data>
        <offset>0</offset>
        <size>74108</size>
        <length>23083</length>
        <extracted-checksum style="md5">d852c77ac3c8e83f312c12b4c3198e6d</checksum>
        <archived-checksum style="md5">ceaf793ccb1990ecbadb20112d5f9e5d</checksum>
        <encoding style="application/x-gzip"/>
      </data>
      <ea>
        <name>com.apple.ResourceFork</name>
        <offset>0</offset>
        <size>7072</size>
        <length>3942</length>
        <extracted-checksum style="md5">0f7061dca2d7411352377db0e53792db</checksum>
        <archived-checksum style="md5">c72de8ac25abe462a930254d82958534</checksum>
        <encoding style="application/x-gzip"/>
      </ea>
    </file>
  </toc>
</xar>
```

### Hoop

De heap begint onmiddellijk na de gecomprimeerde toc. Het is een ongestructureerde hoop gegevens waarnaar wordt verwezen door de TOC. De Offset-waarden die in TOC worden vermeld, beginnen vanaf het begin van de heap. De lengtewaarden in de toc verwijzen naar het werkelijke aantal bytes dat in de heap is opgeslagen (gecomprimeerd of niet), terwijl de groottewaarde verwijst naar de geëxtraheerde grootte van het item (indien nodig na het decomprimeren).

## Referenties

* [XAR](https://github.com/mackyle/xar/wiki/xarformat)
* [XAR - Wikipedia](https://en.wikipedia.org/wiki/Xar_(archiver))

