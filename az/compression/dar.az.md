{
  "date": "2021-04-08",
  "keywords": [
"dar faylı",
"dar fayl formatı",
"dar faylı nədir",
"fayl",
"dar misal",
"dar fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DAR - Disk arxivləşdirici fayl formatı",
  "description": "DAR faylları yarada və aça bilən DAR fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "DAR",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-da-azr"
}
},
  "lastmod": "2021-04-09"
}

## DAR faylı nədir?

.dar uzantılı fayl DAR Disk arxivindən istifadə edərək yaradılmış sıxılmış arxivdir. Tam disk və ya bir qrup fayl üçün ehtiyat nüsxə/arxiv yarada bilər. O, UNIX ƏS-də [TAR](/compression/tar/) fayl formatını əvəz etmək üçün yaradılmışdır və çoxlu sayda fayllar üçün bölünmüş arxiv faylları kimi yaradıla bilər. DAR arxivi arxivdəki əsas fayllarla əlaqəli olan faylları sistemdən silmək variantını dəstəkləyir. Diferensial, Artan və Dekremental ehtiyat nüsxəsini təmin etmək imkanları onu TAR fayllarından üstün edir.

## DAR fayl formatı

DAR faylları [gzip](/compression/gz/), [bzip2](/compression/bz2/), lzo, xz və ya lzma kimi istənilən fayl başına sıxılmadan istifadə edə bilən sıxılmış arxivlərdir. DAR faylının dəqiq fayl formatı arxivin məzmununu sıxışdırmaq üçün hansı formatlaşdırma növündən istifadə olunduğundan asılıdır. O, həmçinin isteğe bağlı Blowfish, Twofish, AES, Serpent, Camellia şifrələməsi və açıq açar şifrələməsi və imzasına (OpenPGP) imkan verir.

### DAR Xüsusiyyətləri

DAR fayl formatının bəzi xüsusiyyətləri aşağıdakılardır.

 * İstənilən növ inode (kataloq, sadə fayllar, simvolik bağlantılar, xüsusi qurğular, adlandırılmış borular, rozetkalar, qapılar, ...) qayğısına qalır.
 * Takes care of hard-linked inodes (hard-linked plain files, char devices, block devices, hard-linked symlinks)
 * Seyrək faylların qayğısına qalır
 * Linux faylının Genişləndirilmiş Atributlarına diqqət yetirir,
 * Linux faylı ACL ilə maraqlanır
 * Mac OS X fayl çəngəllərinin qayğısına qalır
 * HFS+ fayl sisteminin Doğum tarixi və ext2/3/4 fayl sisteminin dəyişməz, məlumat jurnalı, təhlükəsiz silinmə, quyruq birləşməsiz, silinməyən, noatime atributları kimi bəzi fayl sisteminə xüsusi atributların qayğısına qalır.
 * gzip, bzip2, lzo, xz və ya lzma ilə fayl başına sıxılma (bütün arxivi sıxmaqdan fərqli olaraq). Fərdi fayl adı şəkilçisinə əsasən artıq sıxılmış faylları sıxmamağı seçə bilər.
 * Arxivin istənilən yerindən faylların sürətli çıxarılması
 * Arxivdə faylların kataloqunu saxlamaqla arxiv məzmununun sürətli siyahısı
 * Canlı fayl sisteminin ehtiyat nüsxəsi: faylın ehtiyat nüsxə üçün oxunarkən dəyişdirildiyini aşkar edir və onu verilmiş maksimum təkrar cəhd sayına qədər saxlamağa yenidən cəhd edə bilər.
 * Hash faylı (MD5, SHA1 və ya SHA-512) hər bir dilim üçün dərhal yaradılır, nəticədə alınan fayl hər bir dilimin bütövlüyünü tez yoxlamaq üçün md5sum və ya sha1sum ilə uyğun gəlir.
 * Fayl sistemi müstəqil: sistemi fərqli ölçülü bölməyə və/yaxud fərqli fayl sistemi olan bölməyə bərpa etmək üçün istifadə edilə bilər[5]

## İstinadlar

* [DAR](http://dar.linux.free.fr/)

* [DAR Disk Arxivatoru](https://en.wikipedia.org/wiki/Dar_(disk_archiver))


