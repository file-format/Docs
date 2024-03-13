{
  "date": "2023-06-08",
  "keywords": [
"crx faylı",
"crx faylı nədir",
"crx faylını google chrome-da necə quraşdırmaq olar",
"crx faylını necə açmaq olar",
"crx faylında nə var",
"crx faylının formatı nədir",
"fayl",
"crx fayl uzantısı",
"uzadılması"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "CRX Fayl Format - Google Chrome Genişləndirilməsi",
  "description": "CRX faylları yarada və aça bilən CRX formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "CRX",
  "menu": {
    "docs": {
      "identifier": "misc-crx-az",
      "parent": "misc"
}
},
  "lastmod": "2023-06-08"
}

## CRX faylı nədir?

CRX fayl formatı Google Chrome brauzer uzantıları ilə əlaqələndirilir. CRX faylı mahiyyətcə Google Chrome-da quraşdırılıb işə salınacaq genişləndirmə üçün lazımi faylları və metadatadan ibarət sıxılmış paketdir. O, əlavə xüsusiyyət və ya mövzu təqdim etməklə veb brauzerin funksionallığını və ya görünüşünü artırır.

CRX faylı Google Chrome-da yükləndikdə və quraşdırıldıqda, brauzer açıq açar və imzadan istifadə edərək genişləndirmənin bütövlüyünü yoxlayır. Doğrulama uğurlu olarsa, Chrome CRX faylının məzmununu çıxarır və genişləndirməni quraşdıraraq onu istifadə üçün əlçatan edir. İstifadəçilər quraşdırılmış genişləndirmələri işə salmağa, söndürməyə və ya silməyə imkan verən Chrome Genişləndirmələri səhifəsi vasitəsilə öz genişləndirmələrini idarə edə bilərlər.

## CRX faylını Google Chrome-da necə quraşdırmaq olar?

Google Chrome-da CRX faylını quraşdırmaq üçün bu addımları yerinə yetirə bilərsiniz:

1. Chrome brauzerini açın.
2. Ünvan çubuğuna `chrome://extensions` yazın və Enter düyməsini basın.
3. Genişləndirmələr səhifəsinin yuxarı sağ küncündə yerləşən Tərtibatçı rejimi keçidini aktivləşdirin.
4. Paketdən çıxarılan yüklə düyməsini basın.
5. CRX faylının çıxarılmış məzmununu ehtiva edən qovluğu tapın və seçin (və ya sadəcə CRX faylının özünü seçin).
6. Genişlənməni quraşdırmaq üçün Açıq düyməsini basın.

## CRX faylında nə var?

CRX faylı Google Chrome genişləndirilməsi üçün tələb olunan zəruri faylları və metadatadan ibarətdir. Budur CRX faylında tapılan tipik məzmunun bölgüsü:

- **Manifest file (manifest.json):** This file is a JSON-formatted file that includes information about extension such as its name, version, description, permissions and background scripts. It defines the structure and behavior of extension.
- **JavaScript faylları:** Bu fayllar genişlənmənin funksionallığını müəyyən edən kodu ehtiva edir. Onlara hadisələrin idarə edilməsi, veb səhifələrin dəyişdirilməsi və ya Chrome API-ləri ilə qarşılıqlı əlaqə üçün skriptlər daxil ola bilər.
- **HTML, CSS və şəkil faylları:** Genişləndirmələrə tez-tez pop-up pəncərələri və ya seçim səhifələri kimi istifadəçi interfeysi elementləri daxildir. HTML faylları bu interfeyslərin strukturunu müəyyən edir, CSS faylları isə onların görünüşünü idarə edir. Şəkil faylları nişanlar və ya digər qrafik aktivlər üçün istifadə olunur.
- **İstəyə bağlı resurs faylları:** Genişləndirmələrə bir çox dilləri dəstəkləmək üçün lokalizasiya faylları kimi əlavə resurslar daxil ola bilər. Bu fayllar genişlənmənin istifadəçi interfeysində istifadə olunan mətnin tərcümələrini ehtiva edir.
- **Arxa fon skriptləri:** Əgər genişlənmənin fon prosesləri və ya aktiv veb səhifəsindən asılı olmayaraq işləyən skriptləri varsa, bu skriptlər CRX faylına daxil ediləcək.
- **Məzmun skriptləri:** Məzmun skriptləri davranışlarını dəyişdirmək və ya məzmunu ilə qarşılıqlı əlaqə yaratmaq üçün veb səhifələrə yeridilə bilən skriptlərdir. Genişlənmə məzmun skriptlərindən istifadə edirsə, həmin skriptlər üçün lazımi fayllar CRX faylında mövcud olacaq.
- **Digər aktivlər:** Uzatmanın xüsusi tələblərindən asılı olaraq audio və ya video faylları, şriftlər və ya məlumat faylları kimi əlavə fayllar daxil edilə bilər.

CRX fayl formatı mahiyyətcə bütün bu faylları və qovluqları strukturlaşdırılmış şəkildə ehtiva edən sıxılmış paketdir. CRX faylı Google Chrome-da quraşdırıldıqda, brauzer məzmunu çıxarır və onları müvafiq yerlərdə yerləşdirir, bu da genişləndirmənin yüklənməsinə və brauzer daxilində işləməsinə imkan verir.

## CRX faylının formatı nədir?

CRX fayl formatı Google Chrome genişləndirmələrinin qablaşdırılması və yayılması üçün xüsusi formatdır. Bu, mahiyyətcə fərqli fayl uzantısı olan sıxılmış ZIP arxividir. CRX faylının əsas strukturu aşağıdakı kimidir:

- **Fayl imzası:** Faylın ilk 4 baytında faylı CRX faylı kimi müəyyən etmək üçün imza kimi xidmət edən sehrli Cr24 (onaltılıq: 43 72 32 34) nömrəsi var.
- **Versiya nömrəsi:** Növbəti 4 bayt CRX formatının versiya nömrəsini təmsil edir.
- **İctimai açarın uzunluğu:** Aşağıdakı 4 bayt genişləndirmə imzasının yoxlanılması üçün istifadə edilən kodlanmış açıq açarın uzunluğunu göstərir.
- **İmza uzunluğu:** Sonrakı 4 bayt genişlənmənin imza uzunluğunu müəyyən edir.
- **İctimai açar:** Bu bölmə genişləndirmənin bütövlüyünü yoxlamaq üçün istifadə edilən kodlanmış açıq açarı ehtiva edir.
- **İmza:** Bu bölmə yuxarıda qeyd olunan açıq açara uyğun şəxsi açardan istifadə edərək genişləndirmənin məzmununu imzalamaqla yaradılan genişləndirmə imzasını ehtiva edir.
- **Poçt arxivi:** CRX faylının qalan baytları sıxılmış ZIP arxivindən ibarətdir. Bu arxiv bütün lazımi faylları və genişləndirmə qovluqlarını, o cümlədən manifest faylı, JavaScript faylları, HTML faylları, CSS faylları, şəkillər və hər hansı digər resursları ehtiva edir.

## İstinadlar
* [CRX format spesifikasiyası](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/K3YIsNL_Et4)


