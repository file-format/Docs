{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "XAR - Genişlənən Arxiv Fayl Formatı",
  "description":"XAR faylları yarada və aça bilən XAR fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle" : "XAR",
  "menu" : {
    "docs" : {
    "identifier": "compression-xar-az",
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-13"
}

## XAR faylı nədir?

.xar (Genişləndirilə bilən Arxiv Format) genişləndirilməsi olan fayl sıxılmış və ya sıxılmamış formatda ola bilən UNIX arxividir. Paketlərin quraşdırılması üçün Mac OS-də də istifadə olunur. XAR açıq mənbəlidir və Safari brauzeri ilə istifadə üçün Mac OS X 10.5-in bir hissəsidir.

## XAR fayl formatı

[XAR](https://github.com/mackyle/xar/wiki/xarformat) faylının üç əsas bölgəsi var.

 * Başlıq
 * Mündəricat
 * Yığın

### XAR Başlığı

XAR başlığı aşağıdakı kimi qurulmuşdur.

|Sahə|Məlumat növü|Baytla ölçü|
---|---|---|
|Magic|Unsigned Int 32|4|
|Ölçü|İmzasız Int 16|2|
|Versiya|Unsigned Int 16|2|
|TOC Uzunluğu Sıxılmış|İmzasız Int 64|8|
|TOC Length UnCompressed|Unsigned Int 64|8|
|Checksum|Unsigned Int 32|4|
|Mesaj Digest Adı |Null Sonlandırıldı||

XAR başlığının C strukturu aşağıdakı kimi müəyyən edilə bilər.
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
Qeyd edək ki, başlığın bütün sahələri (magic, size, version, toc_length_compressed, toc_length_uncompressed, cksum_alg) həmişə XAR fayllarında şəbəkə baytı (aka böyük endian) qaydasında saxlanılır.

### XAR Mündəricat (TOC)

The table of contents is an XML document that is (and must) be encoded as UTF-8. O, faylın əvvəlində saxlanılır və fərdi faylı çıxarmaq üçün arxivdə skan etməyi asanlaşdırır. XAR arxivi [GZIP](/compression/gz/), [BZIP2](/compression/bz2/) və digər oxşar kimi müxtəlif sıxılma sxemlərindən istifadə edərək, arxivdəki fərdi faylları müstəqil şəkildə sıxışdırmağa/kodlaşdırmağa imkan verir.  

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

### Yığın

Yığın sıxılmış tokdan dərhal sonra başlayır. Bu, TOC tərəfindən istinad edilən strukturlaşdırılmamış məlumat yığınıdır. TOC-da sadalanan Ofset dəyərləri yığının əvvəlindən başlayır. Tocdakı uzunluq dəyərləri yığında saxlanılan baytların faktiki sayına (sıxılmış və ya olmayan), ölçü dəyəri isə elementin çıxarılan ölçüsünə aiddir (lazım olduqda sıxışdırıldıqdan sonra).

## İstinadlar

* [XAR](https://github.com/mackyle/xar/wiki/xarformat)
* [XAR - Wikipedia](https://en.wikipedia.org/wiki/Xar_(archiver))
