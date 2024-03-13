{
  "date": "2021-04-08",
  "keywords": [
"lz4 faylı",
"lz4 fayl formatı",
"lz4 faylı nədir",
"fayl",
"lz4 nümunəsi",
"lz4 fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "LZ4 - LZ4 Sıxılmış Fayl Formatı",
  "description": "LBR fayl formatı və LZ4 fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "LZ4",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-lz-az4"
}
},
  "lastmod": "2021-04-19"
}

## LZ4 faylı nədir?

.lz4 uzantılı fayl [LZ4](https://en.wikipedia.org/wiki/LZ4_(compression_algorithm)) sıxılmasını dəstəkləyən proqramlar/utilitlər ilə yaradılmış sıxılmış arxiv faylıdır. LZ4 alqoritmi sürət və sıxılma nisbəti arasında mübadilə üzərində fokuslanır. Sıxılmış LZ4 arxivləri LZ4 əmr satırı yardım proqramı ilə yaradıla bilər və eyni istifadə edərək sıxıla bilər.

## LZ4 Fayl Format

LZ4 sıxılma alqoritminə əsaslanan LZ4 fayl formatı CPU növündən, əməliyyat sistemindən, fayl sistemindən və simvol dəstindən müstəqildir. LZ4 alqoritmindən istifadə edərək fayl sıxılması və axın sıxılması üçün uyğundur. LZ4 formatının ilkin tətbiqi 2011-ci ildə Yann Collet tərəfindən [C](/programming/c/) dilində həyata keçirilib və [Github](https://github.com/lz4/lz4) üzərində tərtibatçının istinadı üçün əlçatandır.

### LZ4 Çərçivə Format

LZ4 fayl formatının ümumi strukturu aşağıda göstərildiyi kimidir.

|MagicNb|F. Deskriptor| Blok|(...)|EndMark |C. Yoxlama məbləği|
---|---|---|---|---|---|
|4 bayt| 3-15 bayt||| 4 bayt| 0-4 bayt|

#### Sehrli Nömrə

4 bayt, kiçik endian formatı. Dəyər: 0x184D2204

#### Çərçivə Deskriptoru

Çərçivə deskriptoru 3 t0 15 baytdan ibarətdir və spesifikasiyaların ən vacib hissəsidir. Magic_Number və Frame_Descriptor sahələri birlikdə LZ4 Frame Header adlanır və onun ölçüsü 7 ilə 19 bayt arasında dəyişir. Aşağıda göstərildiyi kimidir.

|FLG| BD| (Məzmun ölçüsü)| (Lüğət ID)| HC|
---|---|---|---|---|
|1 bayt| 1 bayt| 0 - 8 bayt| 0 - 4 bayt| 1 bayt|

#### Məlumat blokları

Hər bir məlumat bloku aşağıdakı ardıcıllığa əməl edir.

|Blok Ölçüsü| data| (Blok yoxlama məbləği)|
---|---|---|
|4 bayt| |0 - 4 bayt|

#### EndMark

Blokların axını sonuncu məlumat blokunun ardınca 32 bitlik 0x00000000 dəyəri gələndə başa çatır.

#### Məzmun Yoxlama Cəmi

Content_Checksum düzgün deşifrə olunan məzmunun etibarlılığını yoxlayır və xxHash-32 alqoritminin nəticəsi ilə həyata keçirilir. O, bütün blokların düzgün ardıcıllıqla və heç bir səhvsiz uğurla ötürülməsinin nəticələrini təsdiqləyir.

## İstinadlar

* [LZ4 Frame Format](https://github.com/lz4/lz4/blob/dev/doc/lz4_Frame_format.md)
* [LZ4 Compression Algorithm - Wikipedia](https://en.wikipedia.org/wiki/LZ4_(compression_algorithm))
