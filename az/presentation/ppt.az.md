{
  "date": "2019-12-13",
  "keywords": [
"ppt faylı",
"ppt fayl formatı",
"ppt faylı nədir",
"fayl",
"ppt nümunəsi",
"ppt fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "PPT faylları yarada və aça bilən PPT fayl formatı və API-lər haqqında məlumat əldə edin.",
  "title": "PPT - PowerPoint fayl formatı",
  "linktitle": "PPT",
  "menu": {
    "docs": {
      "parent": "presentation",
      "identifier": "presentation-pp-azt"
}
},
  "lastmod": "2019-09-10"
}

## PPT faylı nədir?

A file with PPT extension represents PowerPoint file that consists of a collection of slides for displaying as SlideShow. It specifies the Binary File Format used by Microsoft PowerPoint 97-2003. PPT faylı mətn, markerli nöqtələr, şəkillər, multimedia və digər daxil edilmiş OLE obyektləri kimi bir neçə müxtəlif növ məlumatı ehtiva edə bilər. Microsoft, 2007-ci ildən etibarən PowerPoint üçün [PPTX](/presentation/pptx/) kimi tanınan daha yeni fayl formatını təklif etdi, bu format Office OpenXML-ə əsaslanır və bu ikili fayl formatından fərqlidir. OpenOffice Impress və Apple Keynote kimi bir sıra digər proqram proqramları da PPT faylları yarada bilər.

## Qısa tarix ##

Microsoft introduced the PPT file format with the release of PowerPoint in 1987. Stabil ikili format Windows üçün PowerPoint 97-2003-də defolt olaraq paylaşıldı. İkili fayl formatı PowerPoint-in ən son versiyaları, o cümlədən PowerPoint 2016 tərəfindən oxumaq və yazmaq üçün dəstəklənir.

## Fayl Formatının Xüsusiyyətləri ##

Tətbiq edildiyi gündən PPT fayl formatı yeni funksiyaların və təkmilləşdirmələrin əlavə edilməsi üçün bir neçə düzəlişdən keçmişdir. Mövcud olan ən son versiya spesifikasiyalar 2018-ci ilin avqustunda dərc edilmiş 6.0 revizyonunun spesifikasiyasıdır ki, bu da PPT fayl formatının real məhsul nömrəsi ilə qarışdırılmamalıdır, çünki Microsoft artıq bu format üçün dəyişiklik etmir.

### Fayl Formatına Baxış ###

PPT fayl formatının əsas komponentlərindən bəziləri aşağıdakılardır:

#### Slaydlar ####

Şəkillər, mətn, animasiyalar və media kimi istifadəçi məlumatları Slayd daxilində təqdimata əlavə edilir. Təqdimatda təqdimat işə salındıqda slayd şousu kimi göstərilən bir və ya bir neçə slayd ola bilər. Təqdimatda təqdimat slaydlarının ümumi vizual xüsusiyyətləri üçün şablon rolunu oynayan əsas slaydlar və başlıq əsas slaydlar var. Oxşar məqsədə xidmət edən və bütün qeyd slaydları və bütün çap olunmuş paylama materialları üçün ümumi vizual xassələri təmin edən qeydlər üzrə master slayd və paylayıcı material slaydı da mövcuddur.

#### Formalar ####

Formalar, istifadəçilərə slaydda yer tutan formalar, şəkillər və qrafiklər şəklində müxtəlif məzmun əlavə etməyə imkan verən obyektlərdir. Əsas slayddakı formalar forma qrupları üçün ümumi məlumatları müəyyənləşdirir.

#### Yertutanların Formaları ####

Bunlar müxtəlif obyektlər üçün konteyner kimi xidmət edən xüsusi yer tutuculardır. Cədvəllər və ya diaqramlar kimi xüsusi forma növlərini daxil etmək üçün ipucu vermək üçün müxtəlif yertutan formalardan istifadə edilə bilər. Slaydın içərisində yer tutucu forması əsas master slaydın, başlıq əsas slaydının və ya qeydlərin əsas slaydının vizual xüsusiyyətlərini qəbul edir.

#### Xarici Obyektlər ####

Daxili və əlaqəli audio, əlaqəli video, daxil edilmiş və əlaqəli OLE obyektləri və hiperlinklər kimi xarici obyektlər slaydda yerləşdirilə bilər. Bu obyektlər slayd şousu zamanı xarici resurslara daxil olmaq üçün əlaqəli obyektləri aktivləşdirmək üçün istifadə edilə bilər.

### Fayl Format Strukturları ###

PowerPoint ikili fayl formatları ümumi sənəd strukturunu və məlumatları təmsil etmək üçün aşağıdakı axınlardan ibarətdir.

* Cari İstifadəçi axını

* PowerPoint sənəd axını

* Şəkillər axını

* Xülasə Məlumat və Sənəd Xülasə Məlumatı (İstəyə görə)


DOC fayl formatı üçün tam spesifikasiyalar [Microsoft](https://msdn.microsoft.com/en-us/library/office/cc313106(v#office.12).aspx tərəfindən təqdim olunduğu kimi tapıla bilər və aşağıdakı təfərrüatlarda qeyd olunan bölmələrə istinadla məsləhətləşməlidir.

#### Cari İstifadəçi Axını ####

Sənədi açan sonuncu istifadəçinin qeydini aparır və onun adı Cari İstifadəçi” olmalıdır.

#### PowerPoint sənəd axını ####

PowerPoint təqdimatı haqqında bütün məlumatların qeydini aparır və onun tərtibatını və məzmununu izah edir. Bu, adı PowerPoint Sənədi OLMALIDIR. Bu axının məzmunu yüksək səviyyəli qeydlər ardıcıllığı ilə müəyyən edilir. Qeyd ardıcıllığı üzrə qismən sifariş məhdudiyyətləri PersistDirectoryAtom və UserEditAtom qeydlərində müəyyən edilmişdir.

Konteyner qeydləri kimi DocumentContainer, MainMasterContainer (bölmə 2.5.3), HandoutContainer (bölmə 2.5.8), SlideContainer (bölmə 2.5.1) və NotesContainer (bölmə 2.5.6) qeydlərinin hər biri konteyner qeydləri ağacının köküdür. və atom qeydləri. İstənilən konteyner qeydinin içərisində açıq şəkildə uşaq qeydləri kimi qeyd olunmayan digər qeydlər mövcud ola bilər. Naməlum qeydlər RecordHeader strukturunun recType sahəsində (bölmə 2.3.1) RecordType sadalanması (bölmə 2.13.24) tərəfindən təyin olunmayan dəyəri ehtiva etdikdə müəyyən edilir. Bu naməlum qeydlər, rastlaşdıqda, nəzərə alınmamalı və MAY<1> saxlanıla bilər. RecordHeader strukturunun sonundan irəli recLen baytlarını axtarmaqla naməlum qeydlərə məhəl qoyula bilməz.

Bu axın hər dəfə yazıldıqda, yeni yüksək səviyyəli qeydlər, istifadəçi redaktəsi mövcud axına əlavə edilə bilər və ya bütün axın məzmunu yüksək səviyyəli qeydlərin yenilənmiş ardıcıllığı ilə əvəz edilə bilər. Bütün axın dəyişdirilmədikdə, hər hansı əvvəlki istifadəçi redaktəsini təşkil edən hər hansı əvvəllər mövcud olan yuxarı səviyyəli qeydlər, cari istifadəçi redaktəsini təşkil edən sonradan əlavə edilmiş yüksək səviyyəli qeydlər tərəfindən köhnələ bilər.

#### Şəkil Yayımı ####

Bu, PowerPoint təqdimatında olan şəkillər haqqında məlumatları ehtiva edən əlavə axındır. Onun adı Şəkillər olmalıdır. Bu axının məzmunu [MS-ODRAW] 2.2.21 bölməsində göstərildiyi kimi OfficeArtBStoreDelay qeydi ilə müəyyən edilir.

#### Xülasə məlumat axını ####

Microsoft Office standartına uyğun olaraq sənəd haqqında statistika aparır. Xülasə Məlumat Yayımının adı \005SummaryInformation olmalıdır, burada \005 \005 sətri deyil, 0x0005 dəyəri olan simvoldur. Bu axın şifrələnmiş sənədlər üçün buraxılmamalıdır. Bu axının məzmunu [MS-OSHARED] bölmə 2.3.3.2.1-də göstərilmişdir.

#### Sənədin Xülasə Məlumat axını ####

Adı \005DocumentSummaryInformation OLMALIDIR, burada \005 \005 sətri deyil, 0x0005 dəyəri olan simvoldur. Bu axın şifrlənmiş sənədlər üçün buraxıla bilər<2>. Bu axının məzmunu [MS-OSHARED] bölmə 2.3.3.2.2-də göstərilmişdir.

#### Şifrələnmiş xülasə məlumat axını ####

Adı Şifrələnmiş Xülasə OLMALIDIR isteğe bağlı yayım. Bu axın yalnız şifrələnmiş sənəddə mövcuddur. Bu axının məzmunu [MS-OFFCRYPTO] bölmə 2.3.5.4-də göstərilmişdir.

#### Rəqəmsal İmza Yaddaşı ####

Adı _xmlsignatures OLMALIDIR isteğe bağlı yaddaş. O, buraxıla bilər və nəzərə alına bilər. Bu yaddaşın məzmunu [MS-OFFCRYPTO] bölmə 2.5.2-də göstərilmişdir.

#### Xüsusi XML Məlumat Yaddaşı ####

Adı MsoDataStore OLMALIDIR isteğe bağlı yaddaş. Saxlamanın məzmunu [MS-OSHARED] bölmə 2.3.6-da göstərilmişdir.

#### İmza Yayımı ####

Adı _signatures OLMALIDIR isteğe bağlı yayım. O, buraxılmalı və nəzərə alına bilməz. Bu axının məzmunu [MS-OFFCRYPTO] bölmə 2.5.1-də göstərilmişdir.

## İstinadlar ##

* [PPT Fayl Formatının spesifikasiyası](https://msdn.microsoft.com/en-us/library/office/cc313106(v#office.12).aspx)

* [[MS-OSHARED]: Office Ümumi Məlumat Növləri və Obyekt Strukturları](https://msdn.microsoft.com/en-us/library/office/cc313156(v#office.12).aspx)

* [[MS-OFFCRYPTO] - Ofis Sənədinin Kriptoqrafiya Strukturu](https://msdn.microsoft.com/en-us/library/office/cc313071(v#office.12).aspx)

* [PowerPoint Fayl Formatları](https://en.wikipedia.org/wiki/Microsoft_PowerPoint#File_formats)


