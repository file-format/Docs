{
  "date": "2020-03-02",
  "keywords": [
"SVG",
"fayl",
"fayl formatı",
"Səhifənin təsviri Dil",
"Skalyar"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "SVG fayl formatı və SVG faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "title": "SVG faylı nədir?",
  "linktitle": "SVG",
  "menu": {
    "docs": {
      "parent": "page-description-language",
      "identifier": "page-description-language-sv-azg"
}
},
  "lastmod": "2020-03-02"
}

## SVG faylı nədir? ##

An SVG file is a Scalar Vector Graphics file that uses XML based text format for describing the appearance of an image. The word Scalable refers to the fact that the SVG can be scaled to different sizes without losing any quality. Text-based description of such files makes them independent of resolution. It is one of the most used formats for building a website and print graphics in order to achieve scalability. The format can only be used for two-dimensional graphics though. SVG files can be viewed/opened in almost all modern browsers including Chrome, Internet Explorer, Firefox, and Safari.

## Qısa tarix ##

SVG specifications are available as open standard by World Wide Web Consortium (W3C) since 1999. Bundan əvvəl, altı müxtəlif formatda oxşar fayl formatı spesifikasiyası 1998-ci ilə qədər W3C-yə təqdim edilmişdir. 2011-ci ildə spesifikasiyalara yeniləmə tətbiq edilmiş və o, 1.1 versiyasına çevrilmişdir. 2016-cı ildə SVG 2 SVG 1.1-dəki xüsusiyyətlərə əlavə olaraq daha yeni versiya kimi nəşr olundu.

## Fayl Formatının Xüsusiyyətləri ##

SVG Sənəd Obyekt Modeli (DOM) spesifikasiyaların xüsusi bölmələrinə uyğun gələn bütün spesifikasiyaların və interfeyslərin əsasını qoyur. SVG izləyiciləri SVG DOM interfeyslərini W3C spesifikasiyalarında müəyyən edildiyi kimi həyata keçirməlidirlər. Onun DOM müxtəlif məlumat növləri və elementləri üçün bir neçə interfeysi ifşa edir.

### SVG formaları ###

SVG tərtibatçılar tərəfindən istifadə edilə bilən bəzi əvvəlcədən təyin edilmiş forma elementlərinə malikdir:

* Düzbucaqlı<rect>

* Dairə<circle>

* Ellips<ellipse>

* Xətt<line>

* Polyline<polyline>

* Polygon <polygon>

* Yol<path>


Bu formalara və spesifikasiyalara əsasən, SVG-nin funksional sahələri aşağıdakılardır.

**Yollar** - Yollar sadə, eləcə də mürəkkəb forma konturlarını təmsil etmək üçün istifadə olunur. Kodlaşdırmalar əməliyyatın xarakterini müəyyən etmək üçün istifadə olunur. Məsələn, M Move To, L Line To, Z yolu bağlamaq üçün istifadə olunur və s.

**Əsas Fiqurlar** - Bir-birinə bağlı düz xətt seqmentləri (polixəttlər), həmçinin qapalı çoxbucaqlılar, dairələr və ellipslərdən ibarət düz xəttli yollar və yollar çəkilə bilər. Düzbucaqlılar və yuvarlaq künclü düzbucaqlılar da standart elementlərdir.

**Mətn** - Mətn təsviri mətnə çoxlu vizual effektlərin tətbiq oluna biləcəyi XML xarakter məlumatları kimi ifadə edilir. Spesifikasiyalar əyri yol boyunca iki istiqamətli mətni, şaquli mətni və simvolları idarə etməyə imkan verir.

**Rəsm** - Formalar rəng, qradiyent və ya naxışla doldurula və ya konturlaşdırıla bilər ki, bu da onu qeyri-şəffaf etməyə və ya istənilən şəffaflıq dərəcəsinə malik olmağa imkan verir. Çoxbucaqlının təpəsində görünən ox başlıqları və ya simvollar kimi sətir sonu xüsusiyyətləri Markerlərlə təmsil olunur.

**Rəng** - SVG spesifikasiyası bütün görünən SVG elementlərinə rəngləri birbaşa və ya doldurma, ştrix və digər xüsusiyyətlər vasitəsilə tətbiq etməyə imkan verir. Qara və ya mavi, hex təmsil, onluq və ya RGB formasının faizləri kimi müəyyən etmək üçün müxtəlif rəng kodlaşdırmalarından istifadə edilə bilər.

**Qradientlər və Nümunələr** - SVG faylındakı formalar bərk rənglər, gradientlər və ya təkrarlanan naxışlarla doldurula və ya təsvir edilə bilər.

**Filtr Effektləri** - Bu, əslində dəyişdirilmiş nəticə əldə etmək üçün verilmiş mənbə vektor qrafikinə tətbiq olunan bir sıra qrafik əməliyyatlardır.

**İnteraktivlik** - İstifadəçilər fokus, siçan klikləri, sürüşdürmə və ya şəkli böyütməklə SVG faylları ilə qarşılıqlı əlaqə qura bilərlər. İnteraktivlik SVG şəkillərinə yuxarıda qeyd olunduğu kimi müxtəlif yollarla istifadəçilərlə qarşılıqlı əlaqə yaratmağa imkan verir.

**Linking** - SVG şəkillərinin digər sənədlərə hiperlinkləri olması mümkündür. Bu, XML Linking Language və ya XLink vasitəsilə əldə edilir. Bu, müəyyən bir sahəni böyütmək/kiçiltmək və ya görünüşü müəyyən elementlə məhdudlaşdırmaq üçün istifadə olunan xüsusi görünüş vəziyyətləri yaratmağa imkan verir.

**Scripting** - HTML kimi, SVG sənədinin bütün aspektləri skriptlərdən istifadə etməklə manipulyasiya üçün əlçatandır. SVG DOM obyektləri SVG elementi və atributundan istifadə edərək buna nail olmaq üçün təlimat verir. Skriptlər `skript` teq elementlərinə əlavə olunur və tələb olunduqda göstərici, klaviatura və ya sənəd hadisələrinə cavab olaraq işləyə bilər.

**Animasiya** - DOM elementləri<animate> ,<animateMotion> və<animateColor> SVG məzmunu üçün animasiya daxil etməyə imkan verir. Əlbəttə ki, skriptlərdən və daxili taymerlərdən istifadə etmədən buna nail olmaq mümkün deyil. Bu animasiyalar fasiləsiz ola bilər və istifadəçi hadisələrinə cavab verərkən eyni zamanda təkrarlar kimi dövrəyə də qoyula bilər.

**Şriftlər** - SVG-dəki mətn sistem şriftləri kimi xarici şrift fayllarına istinad edə bilər. Belə şriftlər olmadıqda, SVG-dəki mətn çıxışa göstərilməyəcək. Bu, tələb olunan qlifləri belə bir fayla şrift kimi daxil etməklə aradan qaldırıla bilər.<text> element.

## Nümunələr ##
Aşağıdakı sətirlər SVG skripti ilə Dairənin necə təmsil olunduğunu göstərir.

```
<html>
<body>

<h1>My first SVG</h1>

<svg width#"100" height#"100">
  <circle cx#"50" cy#"50" r#"40" stroke#"green" stroke-width#"4" fill#"yellow" />
</svg>

</body>
</html>
```

Aşağıdakı kod sətirləri necə istifadə olunacağını göstərir<text> mətni SVG-yə göstərmək üçün blok.

```
<svg height#"30" width#"200">
  <text x#"0" y#"15" fill#"red">I love SVG!</text>
</svg>
```

## İstinadlar ##

* [W3C SVG Spesifikasiyaları](https://www.w3.org/TR/SVG2/Overview.html)

* [SVG - Wikipedia](https://en.wikipedia.org/wiki/Scalable_Vector_Graphics)


