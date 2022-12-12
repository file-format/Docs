{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XAR - Разширяем архивен файлов формат",
  "description":"Научете за файловия формат XAR и API, които могат да създават и отварят XAR файлове.",
  "linktitle" : "XAR",
  "menu" : {
    "docs" : {
    "identifier": "compression-xar",
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-13"
}

## Какво е XAR файл?

Файл с разширение .xar (Extensible Archive Format) е UNIX архив, който може да бъде в компресиран или некомпресиран формат. Използва се и в Mac OS за инсталиране на пакети. XAR е с отворен код и е част от Mac OS X 10.5 за използване с браузър Safari.

## XAR файлов формат

Файлът [XAR](https://github.com/mackyle/xar/wiki/xarformat) има три основни региона.

* Заглавка
* Съдържание
* Купчина

### XAR заглавка

XAR заглавката е структурирана както следва.

|Поле|Тип данни|Размер в байтове|
---|---|---|
|Magic|Unsigned Int 32|4|
|Размер|Unsigned Int 16|2|
|Версия|Unsigned Int 16|2|
|TOC Length Compressed|Unsigned Int 64|8|
|TOC Length Uncompressed|Unsigned Int 64|8|
| Контролна сума| Unsigned Int 32|4|
|Име на обобщеното съобщение |Null Terminated||

C структурата на XAR заглавката може да се дефинира както следва.
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
Обърнете внимание, че всички полета на заглавката (magic, size, version, toc_length_compressed, toc_length_uncompressed, cksum_alg) винаги се съхраняват в XAR файлове в мрежов ред на байтове (известен още като big endian).

### XAR Съдържание (TOC)

Съдържанието е XML документ, който е (и трябва) да бъде кодиран като UTF-8. Той се съхранява в началото на файла, което улеснява сканирането през архива за извличане на отделен файл. Архивът XAR ви позволява да компресирате/кодирате отделните файлове в архива независимо, като използвате различни схеми за компресиране като [GZIP](/bg/compression/gz/), [BZIP2](/bg/compression/bz2) и други подобни.

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

### Купчина

Купчината започва веднага след компресирания toc. Това е неструктуриран набор от данни, посочени от TOC. Стойностите на отместване, изброени в TOC, започват от началото на купчината. Стойностите на дължината в toc се отнасят до действителния брой байтове, съхранени в купчината (компресирани или не), докато стойността на размера се отнася до извлечения размер на елемента (след декомпресиране, ако е необходимо).

## Препратки

* [XAR](https://github.com/mackyle/xar/wiki/xarformat)
* [XAR - Wikipedia](https://en.wikipedia.org/wiki/Xar_(архиватор))

