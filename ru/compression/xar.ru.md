{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XAR — расширяемый формат файла архива",
  "description":"Узнайте о формате файлов XAR и API-интерфейсах, которые могут создавать и открывать файлы XAR.",
  "linktitle" : "XAR",
  "menu" : {
    "docs" : {
"идентификатор": "сжатие-xar",
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-13"
}

## .XAR вариант №

Файл с расширением .xar (Extensible Archive Format) представляет собой архив UNIX, который может быть в сжатом или несжатом формате. Он также используется в Mac OS для установки пакетов. XAR имеет открытый исходный код и является частью Mac OS X 10.5 для использования с браузером Safari.

## Формат XAR-файла

Файл [XAR](https://github.com/mackyle/xar/wiki/xarformat) имеет три основных области.

* Заголовок
* Оглавление
* Куча

### Заголовок XAR

Заголовок XAR имеет следующую структуру.

|Поле|Тип данных|Размер в байтах|
---|---|---|
|Магия|Целое без знака 32|4|
|Размер|Целое без знака 16|2|
|Версия|Целое без знака 16|2|
|TOC Length Compressed|Unsigned Int 64|8|
|TOC Длина без сжатия|Целое без знака 64|8|
|Контр.сумма|Целое без знака 32|4|
|Имя дайджеста сообщения |Окончание нулем||

Структура C заголовка XAR может быть определена следующим образом.
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
Обратите внимание, что все поля заголовка (magic, size, version, toc_length_compressed, toc_length_uncompressed, cksum_alg) всегда хранятся в файлах XAR в сетевом порядке байтов (также известном как big endian).

### XAR Содержание (TOC)

Оглавление — это XML-документ, который (и должен) быть закодирован как UTF-8. Он хранится в начале файла, что упрощает сканирование архива для извлечения отдельного файла. Архив XAR позволяет сжимать/кодировать отдельные файлы в архиве независимо, используя различные схемы сжатия, такие как [GZIP](/ru/compression/gz/), [BZIP2](/ru/compression/bz2) и другие подобные.

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

### Куча

Куча начинается сразу после сжатого toc. Это неструктурированная куча данных, на которую ссылается оглавление. Значения смещения, перечисленные в TOC, начинаются с начала кучи. Значения длины в оглавлении относятся к фактическому количеству байтов, хранящихся в куче (сжатых или нет), тогда как значение размера относится к извлеченному размеру элемента (после распаковки, если это необходимо).

## использованная литература

* [XAR] (https://github.com/mackyle/xar/wiki/xarformat)
* [XAR - Википедия](https://en.wikipedia.org/wiki/Xar_(архиватор))

