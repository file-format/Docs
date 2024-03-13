{
  "date": "2020-03-16",
  "keywords": [
"IGES faylı",
"Fayl Format",
"CAD"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "IGES fayl formatı və IGES fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "title": "IGES fayl formatı",
  "linktitle": "IGES",
  "menu": {
    "docs": {
      "parent": "cad",
      "identifier": "cad-ige-azs"
}
},
  "lastmod": "2020-07-28"
}

## IGES faylı nədir?

.iges uzantılı fayl kompüter dəstəkli dizayn (CAD) proqramları arasında dizayn məlumatlarının mübadiləsi üçün istifadə olunur. IGES, İlk Qrafik Mübadilə Xüsusiyyətləri deməkdir. IGES istifadə edərək mübadilə edilən məlumatlara dövrə diaqramı, tel çərçivəsi, sərbəst forma səthi və ya bərk modelləşdirmə təsvirləri daxildir. IGES öz tətbiqlərini ənənəvi mühəndislik rəsmlərində, modellərin təhlilində və istehsal funksiyalarında tapır. Format CAD proqramları arasında həm 2D, həm də 3D dizayn məlumatlarını mübadilə edə bilər. IGES faylları Autodesk və CADSoftTools ABViewer kimi bir neçə CAD proqramları ilə açıla bilər. IGES fayllarını proqramlı şəkildə açmaq və çevirmək üçün bir neçə API mövcuddur.

## IGES fayl formatı

IGES faylları ASCII mətn formatındadır və faylın məzmununa baxmaq üçün istənilən mətn redaktorunda açıla bilər. IGES faylındakı mətn məlumatı Hollerith formatında təqdim olunur. Ümumi IGES faylı bu formata uyğun olaraq mübadilə edilə bilən 2D və ya 3D məlumatı təmsil edən minlərlə sətirdən ibarət ola bilər. IGES faylı 73-cü sütunda xüsusi böyük hərflə işarələnən beş hissəyə bölünür. Bu bölmələr Başlat” (S), Qlobal” (G), Məlumat Girişi” (D), Parametr Məlumatı” (P) və Sonlandır” (T) bölmələridir. Data Entry və Parameter Data bölmələri adətən müvafiq olaraq DE və PD kimi qısaldılır.

### IGES Fayl Başlığı

Başlanğıc və Qlobal bölmələr aşağıdakılar haqqında əsas məlumatları ehtiva edir:
 * Faylın adı və mənbəyi
 * Parametr məlumatları bölməsi üçün ayırıcılar
 * Faylın müəllifi və digər ümumi məlumatlar.

Vikipediyadakı nümunə sənəddən Başlanğıc və Qlobal bölmələr aşağıdakı kimidir.
```
S      1
1H,,1H;,4HSLOT,37H$1$DUA2:[IGESLIB.BDRAFT.B2I]SLOT.IGS;,                G      1
17HBravo3 BravoDRAFT,31HBravo3->IGES V3.002 (02-Oct-87),32,38,6,38,15,  G      2
4HSLOT,1.,1,4HINCH,8,0.08,13H871006.192927,1.E-06,6.,                   G      3
31HD. A. Harrod, Tel. 313/995-6333,24HAPPLICON - Ann Arbor, MI,4,0;     G      4
```
As can be seen, the start field contains human readable descriptions of the file, and my have any characters in columns 1-72, with the line ending with the section header and section line number. There must be at least 1 line of the Start section. The global section contains preprocessor data. It also must be present in the file and end with the G000000# format.

### Məlumat Girişi (DE) və Parametr Məlumatları (PD) Bölməsi

#### Məlumat Girişi Bölməsi
IGES faylı IGES fayl formatının əsas məlumatları haqqında məlumatları ehtiva edən bir neçə obyektdən ibarətdir. Müəssisə IGES məlumat formatının müxtəlif elementləri haqqında məlumatları ehtiva edir və rəsm üçün istifadə olunur. Daha çox istifadə edilən qurumlara aşağıdakılar daxildir:
 * Dairəvi qövs
 * Kompozit əyri
 * Konus qövsü
 * Təyyarə
 * Xətt

Bunlar yalnız bir neçəsidir və IGES-də təxminən 150 müxtəlif qurum var. Hər bir obyekt Növ nömrəsi ilə müəyyən edilir, məsələn:
 * Dairəvi Qövs(Növ 100)
 * XƏT (Növ 110)

##### Müəssisə Xüsusiyyətləri

Hər elan edilmiş qurum aşağıdakı xüsusiyyətlərə malikdir.

|Sahənin Adı|Təsvir|
---|---|
|Müəssisə Tipi |Bu təsvir edilən obyekt növüdür. Məsələn, 116 Nöqtə obyektini təsvir edir.|
|PD göstərici |Bu, Parametr Məlumatları bölməsində bu obyektlərin məlumatlarının yerini verir. Bu yer sadəcə olaraq PD bölməsinin daxilində bu obyekt məlumatının ilk sətirinə malik olan sətir nömrəsidir.|
|Struktur |Sıfır və ya tərif obyektinə göstərici. Əksər müəssisələr üçün tətbiq edilmir|
|Line Font Pattern| Number or pointer to line font pattern entity. Number signifies: * 0 Naxış göstərilməyib (defolt) * 1 Bərk * 2 Çizilmiş * 3 Phantom * 4 Mərkəz xətti * 5 Nöqtəli|
|Səviyyə| Bu qurumla əlaqələndiriləcək səviyyələri müəyyən edir. Müəssisə birdən çox səviyyədə görünməyə imkan verir|
|Görünüş| Baxış seçimlərini müəyyən edir. Bunlar: 0 Bütün görünüşlərdə bərabər görünmə və xüsusiyyətləri göstərir. Görünüş obyektinə (Növ 410) Defolt Göstərici, Görünüşün Görünən Assosiativliyinə istinaddan (Növ 402, Forma 3) baxıla bilər.
|Transformasiya matrisinin göstəricisi| Transformasiya matrisi obyektinə istinad edir (Tip 124) və ya defolt olaraq sıfırdır (transformasiya yoxdur)|
|Etiket göstərilməsi assosiativliyi| Müəssisə etiketinin necə göründüyünü müəyyən edən Etiket Ekranı Assosiativliyinə (Tip 402, Forma 5) istinad edir.|
|Status nömrəsi| İki ədəddən ibarət dörd hissədən ibarətdir. 1-2: Boş status. Normal üçün ya 00, ya da boşluq üçün 01. 3-4: Tabeliyində olan obyekt keçidi: müstəqil üçün 00, fiziki asılılıq üçün 01, məntiqi asılılıq üçün 02 və hər ikisi üçün 03-dür. 5-6: Müəssisə İstifadəsi bayrağı: Həndəsə üçün 00, annotasiya üçün 01, tərif üçün 02, Digər üçün 03, Məntiqi üçün 04, 2D parametrik üçün 05 və İnşaat həndəsəsi üçün 06-dır. Nəhayət, 7-8 iyerarxiyadır, burada 00 qlobal yuxarıdan aşağıya işarə edir (bu obyektin xüsusiyyətlərindən istifadə edin), 01 qlobal təxirə salma (bu qurumun xüsusiyyətlərindən istifadə etməyin) və 02 iyerarxiya xassəsindən istifadə edir (İerarxiya obyektindən istifadə edin (Tip 406, Forma). 10)ierarxik qruplaşmanın xüsusiyyətlərini müəyyən etmək).|
|Sıra nömrəsi| D# ilə göstərilmişdir, burada # bu bölmə üçün sətir nömrəsidir (faylın yuxarı hissəsindən deyil). Bu, həmçinin bu Məlumat Girişi obyektinə işarə etmək üçün istifadə olunur.|
|Müəssisə Növü| hər bir müəssisə siyahısı üçün iki dəfə müəyyən edilir|
|Sətrin çəkisi nömrəsi| Obyekti göstərərkən qalınlığı təyin edir. Ən kiçik 1, 0 standartdır|
|Rəng nömrəsi| Müəssisənin rəngini müəyyən edir. İcazə verilən tam dəyərlər bunlardır: 0 Rəng yoxdur (defolt) 1 Qara 2 Qırmızı 3 Yaşıl 4 Göy 5 Sarı 6 Magenta 7 Mavi 8 Ağ|
|Parametr Xətti Sayının Nömrəsi| Bu obyektin Parametr Məlumat Bölməsində tutduğu sətirlərin sayını müəyyən edir|
|Forma nömrəsi| Bu qurumun formasını və ya təmsilçiliyini göstərir. Parametr məlumatlarının necə şərh edildiyini dəyişir. Defolt 0|-dır
|Ehtiyat Sahə| İstifadə olunmayıb|
|Ehtiyat Sahə| İstifadə olunmayıb|
|Müəssisə Etiketi| Tətbiq müəyyən edilmiş identifikator- doğru əsaslandırılmış|
|Altyazı Nömrəsi| Müəssisə etiketi üçün rəqəmli kvalifikator. Hər ikisi birlikdə obyekt| üçün unikal identifikator təşkil edir
|Ardıcıllıq Nömrəsi Yuxarıda baxın. |Bu, D#+1 olacaq, çünki hər bir obyekt iki sətirdə göstərilmişdir.|

#### Parametr Məlumat Bölməsi
Data Entries bölməsindən sonra Parameter Data bölməsi gəlir. O, hər bir müvafiq giriş üçün məlumatları sadalayır və Qlobal bölmədə göstərilən ayırıcılara (adətən parametrləri ayırmaq üçün vergüllər və siyahıya son qoymaq üçün nöqtəli vergül) əsaslanan qurum üçün parametrləri sadalayır.


## İstinadlar
 * [WikiPedia tərəfindən IGES](https://en.wikipedia.org/wiki/IGES)

