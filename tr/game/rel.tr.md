{
  "date" : "2021-09-08",
  "keywords" :[ "rel file", "rel file format", "rel file nedir", "file", "rel sample", "rel file extension","extension", "format"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"REL dosya formatı ve REL dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"REL - Yeri Değiştirilebilir Modül Dosyası",
  "linktitle" : "REL",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## .rel dosyası nedir?
.rel uzantılı bir dosya çok çeşitli amaçlar için kullanılabilir. Bu nedenle, oyun sınıflandırması açısından, Brawl, Super Smash Bros ve Mario Kart Wii gibi bazı Nintendo Wii oyunları tarafından kullanılan yeri değiştirilebilen bir modül dosyası olarak bilinir. Karakter modelleri ve aşamalar da dahil olmak üzere oynanış verilerini içerir. REL dosyaları, Microsoft Windows tarafından kullanılan .DLL dosyalarına benzer şekilde çalışır.

## REL dosya biçimi
Bir REL dosya biçiminde, dosya birkaç bölüme ayrılır, benzer erişime göre gruplanır, örneğin bir bölümdeki salt okunur veriler, tüm yürütülebilir kodlar başka bir bölüme yerleştirilir, vb. Dosya bir başlık bölümüyle başlar ve ardından:
- Bölüm bilgilerini içeren tablo.
- Bölüm verileri.
- Yer değiştirme bilgisi.

### Dosya başlığı
Dosya, en fazla 0x4C baytlık bir başlıkla başlar:
| Ofset | Boyut | Alan Adı | Açıklama |
--------------------|---------------|-------------------|---------------------------------|
| 0x00 | 4 | kimlik | Keyfi kimlik numarası. Bir oyun tarafından kullanılan tüm REL'ler arasında benzersiz olmalıdır. 0 olmamalıdır. |
| 0x04 | 4 | sonraki | Çalışma zamanında doldurulmuş bir sonraki modüle işaretçi. |
| 0x08 | 4 | önceki | Çalışma zamanında doldurulmuş, önceki modüle işaretçi. |
| 0x0c | 4 | numSections | Dosyadaki bölüm sayısı. |
| 0x10 | 4 | bölümBilgiOffset | Kesit tablosunun başlangıcına kaydır. |
| 0x14 | 4 | adOfset | Modül adını içeren ASCII dizisine kaydır. NULL olabilir. REL dosyasının başlangıcına göre. |
| 0x18 | 4 | isimBoyut | Bayt cinsinden modül adının boyutu. |
| 0x1c | 4 | sürüm | REL dosya biçiminin sürüm numarası. |
| 0x20 | 4 | bssBoyut | '.bss' bölümünün boyutu. |
| 0x24 | 4 | relOffset | Yer değiştirme tablosuna ofset. |
| 0x28 | 4 | impOffset | Gösterim tablosuna ofset. |
| 0x2c | 4 | impSize | Gösterim tablosunun bayt cinsinden boyutu. |
| 0x30 | 1 | prologBölümü | Prolog'un göreli olduğu bölüm tablosuna indeksleyin. Bu alan 0 ise atlayın. |
| 0x31 | 1 | sonsözBölümü | Epilogun göreli olduğu bölüm tablosuna dizin. Bu alan 0 ise atlayın. |
| 0x32 | 1 | çözülmemişBölüm | Çözülmemiş olan bölüm tablosuna endeksleyin. Bu alan 0 ise atlayın. |
| 0x33 | 1 | bssBölümü | bss'nin göreli olduğu bölüm tablosuna dizin. Çalışma zamanında dolu! |
| 0x34 | 4 | giriş | _prolog işlevinin belirtilen bölümüne kaydırma. |
| 0x38 | 4 | epilog | _epilog işlevinin belirtilen bölümüne kaydırma. |
| 0x3c | 4 | çözülmemiş | _unresolved işlevinin belirtilen bölümüne kaydırın. |
| 0x40 | 4 | hizala | Yalnızca sürüm ≥ 2. 2'nin kuvveti olarak ifade edilen tüm bölümlerde hizalama kısıtlaması. |
| 0x44 | 4 | bssAlign | Yalnızca sürüm ≥ 2. Tüm '.bss' bölümlerinde hizalama kısıtlaması, 2'nin kuvveti olarak ifade edilir. |
| 0x48 | 4 | düzeltmeBoyutu | Yalnızca sürüm ≥ 3. REL, OSLinkFixed ile bağlantılıysa (OSLink yerine), bu adresten sonraki boşluk başka amaçlar için (BSS gibi) kullanılabilir. |

### Bölüm Bilgi Tablosu
Bölüm bilgi tablosu, her biri 0x8 bayt uzunluğunda **numSections** girişlerini içerir:
| Ofset | Boyut | Açıklama |
-------|------------|-------------|
| 0x0 | 30 bit | REL'in başından bölüme ofset. Bu sıfırsa, bölüm başlatılmamış bir bölümdür (örn. .bss). |
| 0x3.6 | 1 bit | Bilinmeyen. |
| 0x3.7 | 1 bit | Yürütülebilir bayrak; bu 1 ise bölüm yürütülebilir. |
| 0x4 | 4 | Bölümün bayt cinsinden uzunluğu. Bu sıfırsa, bu giriş atlanır. |
| 0x8 | Sonraki giriş | Sonraki giriş |

### Yer Değiştirme Verileri
Yer değiştirme verileri, 0x8 bayt yapılarından oluşan bir veya daha fazla listedir. Her listenin sonu özel tip kodu 203 ile işaretlenmiştir:
| Ofset | İsim | Boyut | Açıklama |
-------|------------|------------|-----|
| 0x0 | ofset | 2 | Bir önceki yer değiştirmeden buna bayt cinsinden ofset. Bu, bölümdeki ilk yer değiştirme ise, bu bölüm başlangıcına göredir. |
| 0x2 | tür | 1 | Yer değiştirme türü. Aşağıda açıklanan. |
| 0x3 | bölüm | 1 | Sembolün yerinin değiştirileceği bölümü. Özel yer değiştirme tipi 202 için bu, bu dosyada aşağıdaki yer değiştirme girişlerinin geçerli olduğu bölümün numarasıdır. |
| 0x4 | ekle | 4 | Bölümün başlangıcına göre yeniden konumlandırılacak sembolün bayt cinsinden ofseti. Bu, main.dol'a karşı yer değiştirmeler yerine mutlak bir adrestir. |
| 0x8 | Sonraki giriş | Sonraki giriş | Sonraki giriş |


 




## Referanslar


* [Taşınabilir Nesne Modülü Biçimi](https://en.wikipedia.org/wiki/Relocatable_Object_Module_Format)


