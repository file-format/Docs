{
  "date": "2019-10-11",
  "keywords": [
"rtf faylı",
"rtf fayl formatı",
"rtf faylı nədir",
"fayl",
"rtf nümunəsi",
"rtf fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "RTF - Zəngin mətn formatı",
  "description": "RTF faylları yarada və aça bilən RTF fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "RTF",
  "menu": {
    "docs": {
      "parent": "word-processing",
      "identifier": "word-processing-rt-azf"
}
},
  "lastmod": "2019-09-10"
}

## RTF faylı nədir?

Microsoft tərəfindən təqdim edilmiş və sənədləşdirilmiş Zəngin Mətn Format (**RTF**) proqramlarda istifadə üçün formatlaşdırılmış mətn və qrafiklərin kodlaşdırılması metodunu təmsil edir. Format digər Microsoft Məhsulları ilə çarpaz platforma sənəd mübadiləsini asanlaşdırır və beləliklə, qarşılıqlı fəaliyyət məqsədinə xidmət edir. Bu imkan onu mətn emal proqramı arasında məlumat ötürülməsi standartına çevirir və beləliklə, məzmun sənəd formatını itirmədən bir əməliyyat sistemindən digərinə ötürülə bilər. Fayl formatının spesifikasiyası Microsoft tərəfindən ictimai yükləmək üçün mövcuddur və tərtibatçının nöqteyi-nəzərindən istinad edilə bilər.

## RTF Fayl Formatının Qısa Tarixi ##

RTF file format has underwent several revisions since its publication. Its official version for read/write was published as part of Microsoft Word 3.0 for Macintosh with version 1.0 specifications. The final version of specifications, 1.9.1 was published by Microsoft in Mar 2008. Bundan sonra spesifikasiyalara əlavə təkmilləşdirmələr edilmir. Hal-hazırda, demək olar ki, bütün əməliyyat sistemlərində RTF fayl formatının istifadəsini minimuma endirən/ortadan qaldıran daha çox xüsusiyyətlə zəngin proqramlar var.

## RTF Fayl Formatının Xüsusiyyətləri ##

RTF serves as a standard of data transfer between word processing software and transfer of content from one operating system to another. This is achieved using control words that were introduced by Microsoft Office Word up through 2007. Standart RTF faylı zəngin mətni təmsil etmək üçün ASCII-dən və müvafiq kod dəyərlərinə çevrilən ASCII olmayan simvollardan ibarətdir. Word-ün daha yeni versiyaları əvvəlki versiyalarla yaradılan RTF fayllarını oxuya bilər, köhnə versiyalar isə anlamadıqları nəzarət söz və qruplarına məhəl qoymur.

### RTF-in əsaslarını anlamaq ###

RTF faylları aşağıdakılardan ibarət 7 bitlik ASCII düz mətnindən istifadə edir:

* nəzarət sözləri

* nəzarət simvolları və

* qruplar.


Bunlar RTF məlumatlarının başa düşülən mətn və simvol kodlaşdırması kimi təqdim edilməsi üçün tikinti blokları kimi çıxış edir.

#### Nəzarət sözü ####

Bunlar ekran üçün simvolları qeyd etmək üçün istifadə olunan xüsusi formatlaşdırılmış əmrləri təmsil edir və 32 hərfdən çox ola bilməz. Nəzarət sözü aşağıdakılarla müəyyən edilir:

\<ASCII Letter Sequence> //<//Delimiter//> //

Hər bir nəzarət sözü hərflərə həssasdır və əks kəsik işarəsi ilə başlayır. ASCII Hərf Ardıcıllığı ASCII əlifbalarını (a-dan z və A-dan Z-yə qədər) ehtiva edə bilər. The<Delimite> nəzarət sözünün adının sonunu qeyd edir və aşağıdakılardan biri ola bilər:

* Bir boşluq. Bu, yalnız nəzarət sözünü ayırmağa xidmət edir və sonrakı emalda nəzərə alınmır.

* Rəqəmsal rəqəm və ya ASCII mənfi işarəsi, rəqəmsal parametrin nəzarət sözü ilə əlaqəli olduğunu göstərir. Sonrakı rəqəmsal ardıcıllıq daha sonra ASCII rəqəmindən başqa hər hansı bir simvolla ayrılır (adətən əks xətt ilə başlayan başqa bir nəzarət sözü). Parametr müsbət və ya mənfi onluq ədəd ola bilər. Nömrə üçün dəyərlər diapazonu nominal olaraq –32768-dən 32767-yə qədərdir, yəni işarələnmiş 16 bitlik tam ədəddir. Az sayda nəzarət sözləri‌ −2,147,483,648 ilə 2,147,483,647 (32 bit işarəli tam ədəd) diapazonunda qiymətlər alır. Bu nəzarət sözlərinə **\binN**, **\revdttmN//**, **\rsidN** əlaqəli nəzarət sözləri və **\bliptagN** kimi bəzi şəkil xassələri daxildir. Burada **N** ədədi parametri ifadə edir. RTF analizatoru isteğe bağlı olaraq mənfi işarəsi olan 10-a qədər rəqəmə icazə verməlidir. Əgər ayırıcı boşluqdursa, o, atılır, yəni sonrakı emala daxil edilmir.

* Hərf və ya rəqəmdən başqa hər hansı simvol. Bu halda, ayırıcı simvol nəzarət sözünü dayandırır və nəzarət sözünün bir hissəsi deyil. Ardınca yeni nəzarət sözü və ya nəzarət simvolu mənasını verən əks slash "\" kimi.


#### Nəzarət Simvol ####

Nəzarət simvolu məzmunundan asılı olaraq xüsusi məna daşıyan xüsusi hadisəni təmsil edir. O, xüsusi simvoldan (qeyri-əlifba sırası ilə) gələn tərs xəttdən ibarətdir və heç bir ayırıcı yoxdur.

#### Qrup ####

Qrup mətn, nəzarət sözlərindən və ya mötərizə (**{ }**) içərisində olan nəzarət simvollarından ibarət ola bilər. Açılış mötərizəsi (**{** ) qrupun başlanğıcını, bağlanış mötərizəsi ( **}**) qrupun sonunu bildirir. Hər bir qrup qrupun təsir etdiyi mətni və həmin mətnin müxtəlif atributlarını müəyyən edir.

### RTF Fayl Strukturu ###

RTF faylı aşağıdakı Standart sintaksisə malikdir:

Microsoft tərəfindən təqdim edilmiş və sənədləşdirilmiş Zəngin Mətn Format (**RTF**) proqramlarda istifadə üçün formatlaşdırılmış mətn və qrafiklərin kodlaşdırılması metodunu təmsil edir. Format digər Microsoft Məhsulları ilə çarpaz platforma sənəd mübadiləsini asanlaşdırır və beləliklə, qarşılıqlı fəaliyyət məqsədinə xidmət edir. Bu imkan onu mətn emal proqramı arasında məlumat ötürülməsi standartına çevirir və beləliklə, məzmun sənəd formatını itirmədən bir əməliyyat sistemindən digərinə ötürülə bilər. Fayl formatının spesifikasiyası Microsoft tərəfindən ictimai yükləmək üçün mövcuddur və tərtibatçının nöqteyi-nəzərindən istinad edilə bilər.

#### RTF Başlığı ####

RTF Başlığı aşağıdakı təsvirə malikdir.

|Sahə|Təsvir
---|---|
|\<header> |**\rtf1\fbidis**? \<character set> \<from> ? \<deffont> \<deflang> \<fonttbl> ? \<filetbl> ? \<colortbl> ? \<stylesheet> ? \<stylerestrictions> ? \<listtables> ? \<revtbl> ? \<rsidtable> ? \<mathprops> ? \<generator> ?

Başlıq cədvəlləri varsa, bu ardıcıllıqla görünməlidir. RTF faylına şriftlər, üslublar, ekran rəngi, şəkillər, alt qeydlər, şərhlər (annotasiyalar), başlıqlar və altbilgilər, xülasə məlumatı, sahələr, əlfəcinlər, sənəd, bölmə, paraqraf və simvol formatlaşdırma xassələri, riyaziyyat, şəkillər və obyektlər. Şrift, fayl, üslub, rəng, təftiş işarəsi və xülasə məlumat qrupları və sənəd formatı xassələri fayla daxil edilirsə, onlar RTF gövdəsindən əvvəl olan RTF başlığında görünməlidir. Hər hansı bir qrupun məzmunu istifadə edilmirsə, qrup buraxıla bilər. Başqa qrupda müəyyən edilmiş xassələrdən istifadə edən hər hansı qrup həmin xassələri təyin edən qrupdan sonra görünməlidir. Məsələn, rəng və şrift xassələri stil qrupundan əvvəl olmalıdır.

#### RTF Versiyası ####

RTF sənədi bu altı simvolla başlamalıdır:

```
{\rtf1
```
burada 1 RTF versiya nömrəsini göstərir.

#### Xarakter Dəsti ####

{\rtf1-dən sonra sənəd hansı simvol dəstindən istifadə etdiyini bildirməlidir. Simvol dəstini elan etməyin yolu bu əmrlərdən biri ilə həyata keçirilir:

`\ansi` - Sənəd Kod Səhifə 1252 kimi tanınan ANSI simvol dəstindədir, adi MSWindows simvol dəsti.

`\mac` - Sənəd MacAscii simvol dəstindədir, Mac OS-nin köhnə (10-dan əvvəlki) versiyalarında adi simvol dəstidir.

`\pc` - Sənəd DOS Kodu Səhifə 437-də, MS-DOS üçün standart simvol dəstidir. Əzələ yaddaşı yaxşı olan makinaçılar qeyd edəcəklər ki, bu, hələ də Alt rəqəmli” kodların təfsirində istifadə olunan simvol dəstidir, yəni Alt düyməsini basıb rəqəmsal klaviaturada 130” yazdığınız zaman o, é verir, çünki simvol CP437-də 130 é-dir. Bu, CP437-nin bu günlərdə gördüyü yeganə istifadə haqqındadır.

`\pca` - Sənəd MS-DOS Çoxdilli Kod Səhifəsi kimi tanınan DOS Kodu Səhifə 850-dədir.

#### Şrift Komandası ####

Simvol dəsti tərifindən sonra `\deffN` əmri gəlir. Bu, N şrift nömrəsinin bu sənəd üçün standart şrift olduğunu müəyyən edir. Şrift nömrəsi N şrift cədvəlindən istinad edilir. `\deffN` əmri texniki cəhətdən isteğe bağlıdır, lakin o, standart şrift kimi 0 şriftini seçdiyi kimi ümumi proloq kimi təhlükəsiz tərəfdə olmalıdır.

`{\rtf1\ansi\deff0`

#### Şrift Cədvəli ####

Sənəddə istifadə oluna bilən bütün şriftlər hər bir şriftin şrift nömrəsi ilə təmsil olunduğu şrift cədvəlində verilmişdir. Sənəddə şrift cədvəli olmalıdır, baxmayaraq ki, bəzi proqramlar onsuz da işləyəcək.

Şrift cədvəlinin sintaksisi {\fonttbl //...declarations//...}-dir, burada hər bəyannamədə bu əsas sintaksis var:

`{\fnumber\familycommand Fontname;}`

Dörd bəyannamə ilə şrift cədvəli aşağıdakı kimidir:

```
{\fonttbl
{\f0\froman Times;}
{\f1\fswiss Arial;}
{\f2\fmodern Courier New;}
}
```

Həmin şrift cədvəli olan sənəddə `{\f2 stuff}` Courier New-də materialları” çap edəcək. Şrift şrift cədvəlində qeyd olunana qədər sənəddə istifadə edilə bilməz.

### Sənədin Sonu ###

Hər bir RTF sənədi sənədin ilk simvolu olan { ilə açılan qrupu bağlamaq üçün } ilə bitməlidir. Yeni sətir istisna olmaqla, heç nə son }-ni izləyə bilməz.

## İstinadlar ##
* [Zəngin Mətn Format](https://en.wikipedia.org/wiki/Rich_Text_Format)


