{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ONETOC2 - Microsoft OneNote Fayl Format",
  "description": "ONETOC2 fayl formatı və ONETOC2 fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "ONETOC2",
  "menu": {
    "docs": {
      "parent": "note-taking",
      "identifier": "note-taking-onetoc-az2"
}
},
  "lastmod": "2019-09-10"
}

## ONEOC2 nədir? ##

Those who have worked with [Microsoft OneNote](https://products.office.com/en-us/onenote/digital-note-taking-app) application may have noticed the presence of .onetoc2 files in the notebook folder. Microsoft OneNote creates binary .onetoc2 file as Table of Contents for keeping an index about the ordering of different note-taking sections in a notebook. A notebook is a collection of section files that are stored in the same directory. The .onetoc2 file uses a collection of properties to specify settings such as order of sections within the notebook and the color of the notebook.

OneNote 2016-da notebook yaratdığınız zaman o, avtomatik olaraq yeni 2010-2016 fayl formatında saxlanılır. OneNote 2016-da riyaziyyat tənlikləri və əlaqəli qeydlər kimi bütün funksiyaların düzgün işləməsini istəyirsinizsə, bu formata ehtiyacınız olacaq.

## ONETOC2 Fayl Format ##

The .onetoc2 file format is represented as OneNote Revision Store File Format and is a collection of of structures that specify a revision store organized into cross-referenced object spaces, containing objects with property sets, and containing a transaction log to ensure file integrity across asynchronous writes. Complete specifications for the .onetoc2 file format are available [online](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx) and can be referred to for development of applications.

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

`guidFileFormat (16 bayt):` Faylın revizyon anbarı faylı olduğunu təyin edən GUID. {109ADD3F-911B-49F5-A5D0-1791EDC8AED8} OLMALIDIR.

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
:


|Fayl Format|Dəyər
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatMayReadThisFile (4 bayt):` İşarəsiz tam ədəd. Bu faylın fayl formatından asılı olaraq aşağıdakı cədvəldəki dəyərlərdən biri olmalıdır.


|Fayl Format|Dəyər
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

## İstinadlar ##

* [[MS-ONESTORE] - OneNote Fayl Formatı](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx)

* [Microsoft OneNote - Wikipedia](https://en.wikipedia.org/wiki/Microsoft_OneNote#References)


