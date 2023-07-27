{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XAR - Formato file di archivio estensibile",
  "description":"Scopri il formato di file XAR e le API che possono creare e aprire file XAR.",
  "linktitle" : "XAR",
  "menu" : {
    "docs" : {
    "identifier": "compression-xar",
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-13"
}

## Che cos'è un file XAR?

Un file con estensione .xar (Extensible Archive Format) è un archivio UNIX che può essere in formato compresso o non compresso. Viene utilizzato anche su Mac OS per l'installazione di pacchetti. XAR è open-source e faceva parte di Mac OS X 10.5 per l'utilizzo con il browser Safari.

## Formato file XAR

Un file [XAR](https://github.com/mackyle/xar/wiki/xarformat) ha tre regioni principali.

* Intestazione
* Sommario
* Cumulo

### Intestazione XAR

L'intestazione XAR è strutturata come segue.

|Campo|Tipo di dati|Dimensioni in byte|
---|---|---|
|Magic|Senza segno Int 32|4|
|Taglia|Senza segno Int 16|2|
|Versione|Senza segno Int 16|2|
|Lunghezza TOC compressa|Unsigned Int 64|8|
|TOC Length UnCompressed|Unsigned Int 64|8|
|Checksum|Senza segno Int 32|4|
|Nome digest del messaggio |Null terminato||

La struttura C dell'intestazione XAR può essere definita come segue.
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
Nota che tutti i campi dell'intestazione (magic, size, version, toc_length_compressed, toc_length_uncompressed, cksum_alg) sono sempre archiviati nei file XAR in ordine di byte di rete (aka big endian).

### XAR Sommario (TOC)

Il sommario è un documento XML che è (e deve) essere codificato come UTF-8. Viene memorizzato all'inizio del file, semplificando la scansione dell'archivio per estrarre il singolo file. L'archivio XAR consente di comprimere/codificare i singoli file nell'archivio in modo indipendente utilizzando diversi schemi di compressione come [GZIP](/it/compression/gz/), [BZIP2](/it/compression/bz2/) e altri simili.

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

### Mucchio

L'heap inizia subito dopo il toc compresso. È un mucchio di dati non strutturato a cui fa riferimento il TOC. I valori di offset elencati in TOC iniziano dall'inizio dell'heap. I valori di lunghezza nel toc si riferiscono al numero effettivo di byte memorizzati nell'heap (compresso o meno) mentre il valore di dimensione si riferisce alla dimensione estratta dell'elemento (dopo la decompressione se necessario).

## Riferimenti

* [XAR](https://github.com/mackyle/xar/wiki/xarformat)
* [XAR - Wikipedia](https://en.wikipedia.org/wiki/Xar_(archiver))

