{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XAR - Format de fichier d'archive extensible",
  "description":"En savoir plus sur le format de fichier XAR et les API qui peuvent créer et ouvrir des fichiers XAR.",
  "linktitle" : "XAR",
  "menu" : {
    "docs" : {
    "identifier": "compression-xar",
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-13"
}

## Qu'est-ce qu'un fichier XAR ?

Un fichier avec l'extension .xar (Extensible Archive Format) est une archive UNIX qui peut être au format compressé ou non compressé. Il est également utilisé sur Mac OS pour l'installation de packages. XAR est open-source et fait partie de Mac OS X 10.5 pour une utilisation avec le navigateur Safari.

## Format de fichier XAR

Un fichier [XAR](https://github.com/mackyle/xar/wiki/xarformat) comporte trois régions principales.

* Entête
* Table des matières
* Tas

### En-tête XAR

L'en-tête XAR est structuré comme suit.

|Champ|Type de données|Taille en octets|
---|---|---|
|Magique|Entier non signé 32|4|
|Taille|Entier non signé 16|2|
|Version|Entier non signé 16|2|
|Longueur de la table des matières compressée|Entier non signé 64|8|
|Longueur de la table des matières non compressée|Entier non signé 64|8|
|Somme de contrôle|Entier non signé 32|4|
|Nom du résumé du message |Null terminé||

La structure C de l'en-tête XAR peut être définie comme suit.
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
Notez que tous les champs de l'en-tête (magic, size, version, toc_length_compressed, toc_length_uncompressed, cksum_alg) sont toujours stockés dans les fichiers XAR dans l'ordre des octets du réseau (aka big endian).

### Table des matières XAR (TOC)

La table des matières est un document XML qui est (et doit) être encodé en UTF-8. Il est stocké au début du fichier, ce qui facilite la lecture de l'archive pour extraire un fichier individuel. L'archive XAR vous permet de compresser/encoder les fichiers individuels de l'archive indépendamment en utilisant différents schémas de compression tels que [GZIP](/fr/compression/gz/), [BZIP2](/fr/compression/bz2/) et d'autres similaires.

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

### Tas

Le tas commence immédiatement après la table des matières compressée. Il s'agit d'un tas de données non structurées référencées par la table des matières. Les valeurs de décalage répertoriées dans la table des matières commencent au début du tas. Les valeurs de longueur dans la table des matières font référence au nombre réel d'octets stockés dans le tas (compressé ou non) tandis que la valeur de taille fait référence à la taille extraite de l'élément (après décompression si nécessaire).

## Références

* [XAR](https://github.com/mackyle/xar/wiki/xarformat)
* [XAR - Wikipédia](https://en.wikipedia.org/wiki/Xar_(archiver))

