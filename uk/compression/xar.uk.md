{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XAR - розширюваний формат файлу архіву",
  "description":"Дізнайтеся про формат файлу XAR та API, які можуть створювати та відкривати файли XAR.",
  "linktitle" : "XAR",
  "menu" : {
    "docs" : {
    "identifier": "compression-xar",
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-13"
}

## Що таке файл XAR?

Файл із розширенням .xar (Extensible Archive Format) — це архів UNIX, який може мати стиснений або нестиснутий формат. Він також використовується в Mac OS для встановлення пакетів. XAR має відкритий код і є частиною Mac OS X 10.5 для використання з браузером Safari.

## Формат файлу XAR

Файл [XAR](https://github.com/mackyle/xar/wiki/xarformat) має три основні області.

* Заголовок
* Зміст
* Купа

### Заголовок XAR

Заголовок XAR має наступну структуру.

|Поле|Тип даних|Розмір у байтах|
---|---|---|
|Magic|Unsigned Int 32|4|
|Розмір|Unsigned Int 16|2|
|Version|Unsigned Int 16|2|
|TOC Length Compressed|Unsigned Int 64|8|
|TOC Length UnCompressed|Unsigned Int 64|8|
|Контрольна сума|Unsigned Int 32|4|
|Назва дайджесту повідомлення |Null Terminated||

Структуру C заголовка XAR можна визначити наступним чином.
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
Зауважте, що всі поля заголовка (magic, size, version, toc_length_compressed, toc_length_uncompressed, cksum_alg) завжди зберігаються у файлах XAR у мережевому порядку байтів (він же big endian).

### XAR Зміст (TOC)

Зміст — це XML-документ, який (і повинен) бути закодований як UTF-8. Він зберігається на початку файлу, що дозволяє легко сканувати архів для вилучення окремого файлу. Архів XAR дозволяє стискати/кодувати окремі файли в архіві незалежно за допомогою різних схем стиснення, таких як [GZIP](/uk/compression/gz/), [BZIP2](/uk/compression/bz2/) тощо.

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

### Купа

Купа починається відразу після стисненого toc. Це неструктурована купа даних, на яку посилається TOC. Значення зсуву, наведені в TOC, починаються з початку купи. Значення довжини в toc стосуються фактичної кількості байтів, що зберігаються в купі (стиснутих чи ні), тоді як значення розміру стосується вилученого розміру елемента (після розпакування, якщо необхідно).

## Список літератури

* [XAR](https://github.com/mackyle/xar/wiki/xarformat)
* [XAR - Вікіпедія](https://en.wikipedia.org/wiki/Xar_(archiver))

