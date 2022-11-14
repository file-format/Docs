{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XAR - Formato de archivo de archivo extensible",
  "description":"Obtenga información sobre el formato de archivo XAR y las API que pueden crear y abrir archivos XAR",
  "linktitle" : "XAR",
  "menu" : {
    "docs" : {
    "identifier": "compression-xar",
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-13"
}

## ¿Qué es un archivo XAR?

Un archivo con extensión .xar (formato de archivo extensible) es un archivo UNIX que puede estar en formato comprimido o no comprimido. También se usa en Mac OS para la instalación de paquetes. XAR es de código abierto y forma parte de Mac OS X 10.5 para su uso con el navegador Safari.

## Formato de archivo XAR

Un archivo [XAR](https://github.com/mackyle/xar/wiki/xarformat) tiene tres regiones principales.

* Encabezado
* Tabla de contenido
* Montón

### Encabezado XAR

El encabezado XAR está estructurado de la siguiente manera.

|Campo|Tipo de datos|Tamaño en bytes|
---|---|---|
|Magia|Int sin firmar 32|4|
|Tamaño|Int sin signo 16|2|
|Versión|Int sin firmar 16|2|
|Longitud TOC comprimida|Int sin signo 64|8|
|Longitud de TOC sin comprimir|Int sin signo 64|8|
|Suma de comprobación|Int sin signo 32|4|
|Nombre del resumen del mensaje |Terminado nulo||

La estructura C del encabezado XAR se puede definir de la siguiente manera.
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
Tenga en cuenta que todos los campos del encabezado (magia, tamaño, versión, toc_length_compressed, toc_length_uncompressed, cksum_alg) siempre se almacenan en archivos XAR en orden de bytes de red (también conocido como big endian).

### Tabla de contenido XAR (TOC)

La tabla de contenido es un documento XML que está (y debe) estar codificado como UTF-8. Se almacena al principio del archivo, lo que facilita el escaneo a través del archivo para extraer archivos individuales. El archivo XAR le permite comprimir/codificar los archivos individuales en el archivo de forma independiente usando diferentes esquemas de compresión como [GZIP](/es/compression/gz/), [BZIP2](/es/compression/bz2) y otros similares.

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

### Montón

El montón comienza inmediatamente después del toc comprimido. Es un montón de datos no estructurados a los que hace referencia el TOC. Los valores de compensación enumerados en TOC comienzan desde el principio del montón. Los valores de longitud en el toc se refieren al número real de bytes almacenados en el montón (comprimidos o no), mientras que el valor de tamaño se refiere al tamaño extraído del elemento (después de descomprimir si es necesario).

## Referencias

* [XAR](https://github.com/mackyle/xar/wiki/xarformat)
* [XAR - Wikipedia](https://en.wikipedia.org/wiki/Xar_(archivador))

