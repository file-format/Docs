{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XAR - Formato de arquivo de arquivo extensível",
  "description":"Saiba mais sobre o formato de arquivo XAR e APIs que podem criar e abrir arquivos XAR.",
  "linktitle" : "XAR",
  "menu" : {
    "docs" : {
    "identifier": "compression-xar",
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-13"
}

## O que é um arquivo XAR?

Um arquivo com extensão .xar (Extensible Archive Format) é um arquivo UNIX que pode estar em formato compactado ou não compactado. Também é usado no Mac OS para instalação de pacotes. O XAR é de código aberto e faz parte do Mac OS X 10.5 para uso com o navegador Safari.

## Formato de arquivo XAR

Um arquivo [XAR](https://github.com/mackyle/xar/wiki/xarformat) tem três regiões principais.

* Cabeçalho
* Índice
* Pilha

### Cabeçalho XAR

O cabeçalho XAR é estruturado da seguinte forma.

|Campo|Tipo de Dados|Tamanho em Bytes|
---|---|---|
|Magic|Unsigned Int 32|4|
|Tamanho|Unsigned Int 16|2|
|Versão|Unsigned Int 16|2|
|Comprimento TOC compactado|Unsigned Int 64|8|
|Comprimento TOC não compactado|Unsigned Int 64|8|
|Checksum|Unsigned Int 32|4|
|Nome do resumo da mensagem |Nulo encerrado||

A estrutura C do cabeçalho XAR pode ser definida como segue.
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
Observe que todos os campos do cabeçalho (magic, size, version, toc_length_compressed, toc_length_uncompressed, cksum_alg) são sempre armazenados em arquivos XAR em ordem de byte de rede (também conhecido como big endian).

### Índice XAR (TOC)

O sumário é um documento XML que é (e deve) ser codificado como UTF-8. Ele é armazenado no início do arquivo, facilitando a varredura do arquivo para extrair um arquivo individual. O arquivo XAR permite compactar/codificar os arquivos individuais no arquivo de forma independente usando diferentes esquemas de compactação, como [GZIP](/pt/compression/gz/), [BZIP2](/pt/compression/bz2) e outros semelhantes.

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

### Pilha

O heap inicia imediatamente após o toc compactado. É uma pilha não estruturada de dados referenciados pelo TOC. Os valores de deslocamento listados em TOC começam no início do heap. Os valores de comprimento no toc referem-se ao número real de bytes armazenados no heap (compactados ou não), enquanto o valor de tamanho refere-se ao tamanho extraído do item (após descompactar, se necessário).

## Referências

* [XAR](https://github.com/mackyle/xar/wiki/xarformat)
* [XAR - Wikipedia](https://en.wikipedia.org/wiki/Xar_(archiver))

