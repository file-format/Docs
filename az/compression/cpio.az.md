{
  "date" : "2023-05-10",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "CPIO Faylı - Unix CPIO Arxiv Fayl Formatı",
  "description":"CPIO faylının və CPIO fayllarını yarada və aça bilən API-lərin nə olduğunu öyrənin.",
  "linktitle" : "CPIO",
  "menu" : {
    "docs" : {
      "identifier" : "compression-cpio-az",
      "parent" : "compression"
}
},
  "lastmod" : "2023-05-10"
}

## CPIO faylı nədir?

CPIO faylı Unix-in Copy In Copy Out (CPIO) formatında yaradılmış arxiv faylıdır. Sıxılmamış olmasından başqa TAR fayl formatına bənzəyir. CPIO faylları cihaz fayllarını, simvolik bağlantıları və genişləndirilmiş fayl atributlarını saxlaya bilər.

## CPIO fayl formatı

CPIO arxivi insan tərəfindən oxunmayan ikili fayl kimi yaradılır. O, faylların və qovluqların kolleksiyasını saxlayır. CPIO arxivinin məzmunu fayl adları, icazələr, sahiblik və vaxt ştampları kimi metadata məlumatı ilə müəyyən edilir. Bu metadata məlumatı həmçinin sistem tərəfindən yanal giriş üçün arxiv faylında saxlanılır.

## CPIO arxivinin formatı

CPIO faylı bir və ya daha çox birləşdirilmiş üzv faylından ibarətdir. Arxivdəki hər bir fayl isteğe bağlı olaraq başlıqda qeyd edildiyi kimi fayl məzmunundan sonra başlıqdan ibarətdir. Arxivin sonunda TRAILER!! adlı boş fayl tərəfindən təsvir edilən başqa başlıq var.

### CPIO Arxivlərinin Növləri

İki növ CPIO arxivi var. Bunlar yalnız başlığın üslubunda fərqlənir.

* ASCII Arxivləri - Bu CPIO arxivlərinin çap edilə bilən başlığı var, əgər arxiv özü ASCII fayllarından ibarətdirsə, CPIO arxivinin bir hissəsinə çevrilir

* İkili Arxivlər - Bu CPIO arxivlərində ikili başlıqlar var.


## CPIO Arxivi ilə işləmək

### CPIO arxivlərini necə yaratmaq olar?

Siz **cpio** əmrindən istifadə edərək Unix-ə bənzər sistemlərdə CPIO yarada bilərsiniz. Aşağıdakı əmr cari qovluqdakı bütün faylları və qovluqları və onun alt kataloqlarını tapacaqdır. Bu çıxış daha sonra archive.cpio adlı yeni CPIO arxivini yaradacaq cpio əmrinə verilir.

```
find . -depth -print | cpio -ov > archive_cpio.cpio
```
### Faylları CPIO arxivindən necə çıxarmaq olar?

Aşağıdakı əmr faylları mövcud arxivdən çıxarır.

```
cpio -id < archive_cpio.cpio
```
O, standart girişdən archive.cpio faylını oxuyacaq və faylları cari qovluğa çıxaracaq.


## İstinadlar

* [CPIO - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/Cpio)

* [CPIO File Format](https://www.ibm.com/docs/en/zos/2.2.0?topic=formats-cpio-format-cpio-archives)

