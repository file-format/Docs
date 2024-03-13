{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "BİR - Microsoft OneNote Fayl Formatı",
  "description": "BİR faylı yarada və aça bilən BİR fayl formatı və API haqqında məlumat əldə edin.",
  "linktitle": "ONE",
  "menu": {
    "docs": {
      "parent": "note-taking",
      "identifier": "note-taking-on-aze"
}
},
  "lastmod": "2019-09-10"
}

## .ONE fayl nədir? ##

.ONE genişləndirilməsi ilə təmsil olunan fayl Microsoft OneNote proqramı tərəfindən yaradılmışdır. OneNote sizə qeydlər aparmaq üçün qaralama blokundan istifadə edirmiş kimi proqramdan istifadə edərək məlumat toplamağa imkan verir. OneNote fayllarında sənəd səhifələrində sabit olmayan yerlərdə yerləşdirilə bilən müxtəlif elementlər ola bilər. Bu elementlər mətn, rəqəmsal əlyazma və şəkillər, çertyojlar və multimedia (audio/video) kliplər də daxil olmaqla digər proqramlardan kopyalanmış obyektlərdən ibarət ola bilər. Microsoft indi Office365-in bir hissəsi kimi OneNote-un onlayn versiyasını təklif edir, burada qeydlər internet üzərindən digər OneNote istifadəçiləri ilə paylaşıla bilər.

## .ONE Fayl Formatının Xüsusiyyətləri ##

OneNote fayl formatı rəqəmsal qeydləri bölmələrin və səhifələrin iyerarxik dəstləri kimi təqdim etmək üçün effektiv üsul təqdim edir. Hər bir səhifə Document Object Model (DOM) fayl formatı ilə təmsil olunmaq üçün xüsusi strukturda istifadəçi tərəfindən müəyyən edilmiş məzmunu ehtiva edir. Bu format üçün məlumat modeli aşağıda göstərildiyi kimidir.

### Struktura Baxış ###

OneNote fayl formatı üçün məlumat modelində göstərildiyi kimi, OneNote sənədi müxtəlif elementlərdən ibarətdir.

#### Bölmə ####

Bölmə OneNote faylındakı ən yüksək konteynerdir və içərisində əlavə olaraq müxtəlif elementləri ehtiva edir:

* Səhifələr

* Metadata

* Xüsusiyyətlər


Metadata və xassələrə bölmə adı, bölmədə olan səhifələrin identifikasiyası və həmin səhifələrin görünmə ardıcıllığı daxildir. Bölmə termini bölmədə olan bütün səhifələrə və .one fayl adı uzantısına malik olan OneNote® revizyon mağazası faylında həmin məlumatların təqdim edilməsinə aiddir.

#### Səhifə ####

OneNote sənədində istifadəçi tərəfindən müəyyən edilmiş məzmun səhifənin içərisindədir. Səhifə məlumatına mətn, siyahılar, cədvəllər, səhifə başlıqları, şəkillər və qeyd teqləri daxildir. Səhifə, daxil olan obyektlərin əksəriyyətinin əlavə olunduğu kontur obyektlərindən ibarətdir. Hər bir səhifəyə mənalı təqdimat üçün ad verilə bilər və obyektlər birbaşa səhifələrə əlavə edilə bilər. Səhifədə daha sonra iyerarxik sistemdə alt səhifələr ola bilər.

#### Xüsusiyyətlər və Əmlak Dəstləri ####

OneNote məzmunu xassələrdən, əmlak dəstlərindən və fayl məlumat obyektlərindən ibarətdir. Mülkiyyət dəsti bəzi məzmun növünü təmsil edən xüsusiyyətlər toplusudur. Fayl verilənləri obyekti şəkillər, daxil edilmiş fayllar və ya audio/video məzmunu olan ikili verilənlər blokudur.

#### OneNote Notebook ####

Notebook eyni kataloqda saxlanılan bölmə faylları toplusudur. Xüsusiyyətlər toplusu notebook daxilindəki bölmələrin sırası və notebookun rəngi kimi parametrləri müəyyən etmək üçün istifadə olunur.

### Fayl strukturu ###

Reviziya mağazası faylı **Başlıq** strukturu ilə başlamalıdır. Faylın qalan hissəsi bayt bloklarına bölünür, burada hər blokun ölçüsü və strukturu ona istinad edən sahə ilə müəyyən edilir. Bloka **Başlıq** strukturu tərəfindən istinad edilirsə və ya başqa əlçatan blokdakı sahəyə istinad edilirsə, əlçatandır. **Başlıq** strukturundan kənar verilənlər və hər hansı əlçatan bloklar nəzərə alınmamalıdır.

Bütün strukturlar 1 baytlıq sərhədlərə uyğunlaşdırılıb. Əgər başqa cür göstərilməyibsə, bütün tam ədədlər imzalanır. Başqa cür göstərilmədiyi halda bütün sahələr [little-endian](https://msdn.microsoft.com/en-us/library/dd773246(v#office.12).aspx#gt_079478cb-f4c5-4ce5-b72b-2144da5d2ce7).

#### Başlıq ####

.ONE faylının başlığı müxtəlif unikal identifikatorları və fayl məlumatlarını aşağıdakı kimi təqdim etmək üçün sahələri ehtiva edən hissələrdən ibarətdir:

`guidFileType (16 bayt):` Reviziya anbarı faylının növünü təyin edən GUID. Aşağıdakı cədvəldəki dəyərlərdən biri olmalıdır.


|Fayl Format|Dəyər
--- | --- |
|.one|{7B5C52E4-D88C-4DA7-AEB1-5378D02996D3}
|.onetoc2|{43FF2FA1-EFD9-4C76-9EE2-10EA5722765F}

`guidFile (16 bayt):` Bu reviziya anbarı faylının kimliyini təyin edən GUID. Qlobal miqyasda unikal olmalıdır.

`guidLegacyFileVersion (16 bayt):` {00000000-0000-0000-0000-000000000000} OLMALIDIR və nəzərə alınmamalıdır.

`guidFileFormat (16 bayt):` Faylın revizyon anbarı faylı olduğunu müəyyən edən GUID. {109ADD3F-911B-49F5-A5D0-1791EDC8AED8} OLMALIDIR.

`ffvLastCodeThatWroteToThisFile (4 bayt):` İşarəsiz tam ədəd. Fayl növündən asılı olaraq aşağıdakı cədvəldəki dəyərlərdən biri olmalıdır.

|Fayl Format|Dəyər
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatHasWrittenToThisFile (4 bayt):` İşarəsiz tam ədəd. Bu faylın fayl formatından asılı olaraq aşağıdakı cədvəldəki dəyərlərdən biri olmalıdır.


|Fayl Format|Dəyər
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvNewestCodeThatHasWrittenToThisFile (4 bayt):` İşarəsiz tam ədəd. Bu faylın fayl formatından asılı olaraq aşağıdakı cədvəldəki dəyərlərdən biri olmalıdır.

|Fayl Format|Dəyər
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatMayReadThisFile (4 bayt):` İşarəsiz tam ədəd. Bu faylın fayl formatından asılı olaraq aşağıdakı cədvəldəki dəyərlərdən biri olmalıdır.

|Fayl Format|Dəyər
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`fcrLegacyFreeChunkList (8 bayt):` **FileChunkReference32** strukturu, fcrZero dəyərinə malik olmalıdır.

`fcrLegacyTransactionLog (8 bayt):` fcrNil OLMALIDIR **FileChunkReference32** strukturu.

`cTransactionsInLog (4 bayt):` Əməliyyat jurnalında əməliyyatların sayını təyin edən imzasız tam ədəd. Sıfır OLMALIDIR.

`cbLegacyExpectedFileLength (4 bayt):` İşarəsiz tam ədəd, Sıfır olmalıdır və nəzərə alınmamalıdır.

`rgbPlaceholder (8 bayt):` İşarəsiz tam ədəd, Sıfır olmalıdır və nəzərə alınmamalıdır.

`fcrLegacyFileNodeListRoot (8 bayt):` fcrNil OLMALIDIR **FileChunkReference32** strukturu.

`cbLegacyFreeSpaceInFreeChunkList (4 bayt):` Sıfır olmalı və nəzərə alınmamalı olan işarəsiz tam ədəd.

`fNeedsDefrag (1 bayt):` nəzərə alınmamalıdır.

`fRepairedFile (1 bayt):` nəzərə alınmamalıdır.

`fNeedsGarbageCollect (1 bayt):` nəzərə alınmamalıdır.

`fHasNoEmbeddedFileObjects (1 bayt):` Sıfır olmalı və nəzərə alınmamalı olan işarəsiz tam ədəd.

`guidAncestor (16 bayt):` Mündəricat faylının **Header.guidFile** sahəsini təyin edən GUID, aşağıdakı cədvəldə verilmişdir:


|Mündərici fayl formatı|Mündəricat faylının yeri
--- | --- |
|Bölmə Faylı - .Bir|Mündəricat faylı bu fayl ilə eyni kataloqda yerləşir.
|Mündəricat Faylı - .onetoc2|Mündəricat faylı bu faylın əsas kataloqunda yerləşir.

GUID {00000000-0000-0000-0000-000000000000} olarsa, bu sahə məzmun cədvəlinə istinad etmir.

`crcName (4 bayt):` Bu düzəliş saxlama faylının adının CRC dəyərini təyin edən işarəsiz tam ədəd. Ad, genişləndirilməsi və sonunda əlavə null simvolu ilə fayl adının Unicode təmsilidir. Bu CRC həmişə .bir fayl üçün CRC alqoritmindən istifadə etməklə hesablanır, bu reviziya mağazası fayl formatından asılı olmayaraq.

`fcrHashedChunkList (12 bayt):` Hashed yığın siyahısında ilk **FileNodeListFragment**-ə istinadı təyin edən **FileChunkReference64x32** strukturu. **FileChunkReference64x32** strukturunun dəyəri fcrZero və ya fcrNildirsə, hashed yığın siyahısı mövcud deyil.

`fcrTransactionLog (12 bayt):` Tranzaksiya jurnalında ilk **TransactionLogFragment** strukturuna istinadı təyin edən **FileChunkReference64x32** strukturu. **fcrTransactionLog** sahəsinin dəyəri fcrZero OLMALIDIR və fcrNil OLMALIDIR.

`fcrFileNodeListRoot (12 bayt):` Kök fayl qovşağı siyahısına istinad təyin edən **FileChunkReference64x32** strukturu. **fcrFileNodeListRoot** sahəsinin dəyəri fcrZero OLMALIDIR və fcrNil OLMALIDIR.

`fcrFreeChunkList (12 bayt):` İlk **FreeChunkListFragment** strukturuna istinadı təyin edən **FileChunkReference64x32** strukturu. Əgər **FileChunkReference64x32** strukturunun dəyəri fcrZero və ya fcrNildirsə, pulsuz yığın siyahısı mövcud deyil.

`cbExpectedFileLength (8 bayt):` Bu düzəliş saxlama faylının baytla ölçüsünü təyin edən işarəsiz tam ədəd.

`cbFreeSpaceInFreeChunkList (8 bayt):` Sərbəst yığın siyahısı ilə müəyyən edilmiş boş yerin baytlarla ölçüsünü təyin etməli olan işarəsiz tam ədəd.

`guidFileVersion (16 bayt):` GUID. **cTransactionsInLog** sahəsinin və ya **guidDenyReadFileVersion** sahəsinin dəyəri dəyişdirildikdə, **guidFileVersion** yeni GUID-ə dəyişdirilməlidir.

`nFileVersionGeneration (8 bayt):` Faylın neçə dəfə dəyişdiyini göstərən işarəsiz tam ədəd. **guidFileVersion** sahəsi dəyişdikdə artırılmalıdır.

`guidDenyReadFileVersion (16 bayt):` GUID. Faylın **Başlıq** strukturu və istifadə olunmamış yaddaş blokları istisna olmaqla, faylın mövcud məzmunu dəyişdirilərkən, **guidDenyReadFileVersion** yeni GUID-ə dəyişdirilməlidir.

`grfDebugLogFlags (4 bayt):` Sıfır olmalıdır. nəzərə alınmamalıdır.

`fcrDebugLog (12 bayt):` **FileChunkReference64x32** strukturu, fcrZero dəyərinə sahib olmalıdır. nəzərə alınmamalıdır.

`fcrAllocVerificationFreeChunkList (12 bayt):` fcrZero OLMALIDIR **FileChunkReference64x32** strukturu. nəzərə alınmamalıdır.

`bnCreated (4 bayt):` Bu reviziya anbarı faylını yaradan proqramın quruluş nömrəsini təyin edən imzasız tam ədəd. nəzərə alınmamalıdır.

`bnLastWroteToThisFile (4 bayt):` Bu reviziya anbarı faylına sonuncu dəfə yazılmış proqramın quruluş nömrəsini təyin edən imzasız tam ədəd. nəzərə alınmamalıdır.

`bnOldestWritten (4 bayt):` Bu reviziya anbarı faylına yazılan ən köhnə proqramın quruluş nömrəsini təyin edən işarəsiz tam ədəd. nəzərə alınmamalıdır.

`bnNewestWritten (4 bayt):` Bu reviziya anbarı faylına yazılan ən yeni proqramın quruluş nömrəsini təyin edən imzasız tam ədəd. nəzərə alınmamalıdır.

`rgbReserved (728 bayt):` Sıfır olmalıdır. nəzərə alınmamalıdır.

## İstinadlar ##

* [[MS-ONESTORE] - OneNote Fayl Formatı](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx)

* [Microsoft OneNote - Wikipedia](https://en.wikipedia.org/wiki/Microsoft_OneNote#References)


