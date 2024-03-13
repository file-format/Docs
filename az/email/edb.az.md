{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "EDB Fayl Format - Exchange Mail Database Faylı",
  "description": "EDB fayl formatı və EDB fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "EDB",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-ed-azb"
}
},
  "lastmod": "2020-09-16"
}

## EDB faylı nədir?

.edb fayl uzantısı olan fayl poçtla əlaqəli məlumatları saxlamaq üçün Microsoft Exchange Server tərəfindən yaradılmış poçt qutusu verilənlər bazasıdır. EDB, Exchange Database, prosesdə olan və SMTP olmayan mesajları saxlayır. EDB, həmçinin Genişləndirilə bilən Saxlama Mühərriki (ESE) Verilənlər Bazası faylları və b-ağac strukturundan istifadə edərək saxlama faylları kimi tanınır. Yaddaş faylları olan EDB faylları [PST](/email/pst/) və [OST](/email/ost/) kimi digər poçt yaddaşı fayl formatlarına çevrilə bilər.

## EDB fayl formatı

İstinad edilə bilən rəsmi/açıq EDB fayl formatı spesifikasiyası mövcud deyil. Fayl formatının tərs mühəndisliyi üçün müəyyən irəliləyişlər əldə edilib, nəticədə spesifikasiyaların qismən dekodlanması baş verib. Bunlara əsasən, EDB faylı aşağıdakılardan ibarətdir:
 * Fayl başlığı - verilənlər bazası faylının başlığı məlumatını ehtiva edir
 * Sabit Ölçü Səhifələri - Cədvəllərdən və indekslərdən ibarət verilənlər bazasını ehtiva edir

### Verilənlər Bazasının Fayl Başlığı
Verilənlər bazası faylının başlığı ilk verilənlər bazası səhifəsində yerləşir və ən azı 668 baytdır. Fayl başlığında digər sahələrə əlavə olaraq `Fayl Format Version` və `Fayl Tipi` var.

#### Fayl növləri
|Növü|Təsviri
---|---|
|0| Verilənlər bazası|
|1| Axın|

`Qeyd:` Bu növlər üçün identifikatorlar məlum deyil.

#### Fayl Format Versiyası
EİB-nin orijinal formatı 1997-ci ilin aprelində başlamış və sonra dəyişikliklər üçün inkişaf etməyə davam etmişdir.

|Revsion Date|Version|Revision|description
---|---|---|---|
|aprel 1997| 0x00000620|0x00000000| Orijinal əməliyyat sistemi Beta formatı.|
|May 1997 |0x00000620|0x00000001| Şərti indeksləşdirmə və OLD üçün kataloqa sütunlar əlavə edin.|
|İyun 1997|0x00000620|0x00000002|İİB-də fLocalizedText bayrağı əlavə edin.|
|Oktyabr 1997|0x00000620|0x00000003|Kosmos ağacı kök səhifələrinə SPLIT_BUFFER əlavə edin.|
|Yanvar 1998|0x00000620|0x00000002|ESE97-nin irəliyə uyğun olaraq qalması üçün düzəlişi geri qaytarın.|
||0x00000620|0x00000003|Kataloqa yeni etiketlənmiş sütunlar əlavə edin (Geri Zəng Məlumatları və Geri Çağırışdan Bağlılıqlar).|
|May 1998|0x00000620|0x00000004|Super Long Value (SLV) dəstəyi: signSLV, fSLVEdbheader-də mövcuddur.|
|May 1998|0x00000620|0x00000005|Yeni SLV kosmik ağacı.|
|Oktyabr 1998|0x00000620|0x00000006|SLV kosmik xəritəsi.|
|Dekabr 1998|0x00000620|0x00000007|4 bayt IDXSEG.|
|Yanvar 1999|0x00000620|0x00000008|Yeni şablon sütun formatı.|
|İyun 1999-cu il|0x00000620|0x00000009|Sortulanmış şablon sütunları. Windows XP SP3|-də istifadə olunur
||0x00000620|0x0000000b|Exchange-də istifadə olunan ECC yoxlama cəmi ilə səhifə başlığını ehtiva edir|
||0x00000620|0x0000000c|Windows Vista (SP0)-da istifadə olunur|
||0x00000620|0x00000011|2 KiB, 16 KiB və 32 KiB səhifələr üçün dəstək. Əlavə ECC yoxlama cəmi ilə genişləndirilmiş səhifə başlığı. Sütun sıxılması. Boşluq göstərişləri. Windows 7 (SP0)-da istifadə olunur|
|May 1999|0x00000623|0x00000000|Yeni Kosmos Meneceri.|

### Verilənlər Bazası Faylları

EDB verilənlər bazası faylı verilənlər bazasındakı bütün cədvəllər üçün sxemi ehtiva edir. Bundan əlavə, bütün verilənlər bazası cədvəlləri üçün qeydlər və cədvəllər üçün indekslər də daxildir. Onun yeri aşağıdakı identifikatorlarla müəyyən edilir.

* JetCreateDatabase

* JetCreateDatabase2

* JetAttachDatabase

* JetAttachDatabase2


Bunlara əsasən verilənlər bazasının vəziyyətini aşağıdakı kimi qiymətləndirmək olar.

|Dəyər|İdentifikator|Təsvir
---|---|---|
|1|JET_dbstateJustCreated|Verilənlər bazası yeni yaradılmışdır.|
|2|JET_dbstateDirtyShutdown|Verilənlər bazası istifadə edilə bilən və ya daşına bilən hala gəlmək üçün sərt və ya yumşaq bərpanın işə salınmasını tələb edir. Bu vəziyyətdə verilənlər bazalarını köçürməyə çalışmamaq lazımdır.|
|3|JET_dbstateCleanShutdown|Verilənlər bazası təmiz vəziyyətdədir. Verilənlər bazası heç bir log faylı olmadan əlavə edilə bilər.|
|4|JET_dbstateBeingConverted|Verilənlər bazası təkmilləşdirilir.|
|5|JET_dbstateForceDetachInternal|Bu dəyər WindowsXP-də təqdim olunub|
 
## İstinadlar
 * [Genişləndirilə bilən Yaddaş Mühərriki (ESE) Database File (EDB) Spesifikasiyaları](https://github.com/libyal/libesedb/tree/main/documentation)

