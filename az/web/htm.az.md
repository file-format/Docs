{
  "date": "2019-10-11",
  "keywords": [
"htm",
"htm faylı",
"htm fayl formatı",
"htm fayl növü",
"fayl",
"növü",
"htm faylı nədir"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "HTM fayl formatı",
  "description": "HTM faylının və onları yarada və aça bilən API-lərin nə olduğunu öyrənmək üçün fayl formatı bələdçisi.",
  "linktitle": "HTM",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-ht-azm"
}
},
  "lastmod": "2019-09-10"
}

## HTM faylı nədir?

**.htm** uzantısı olan fayllar Google Chrome, Internet Explorer, Firefox və bir sıra başqaları kimi veb-brauzerlərdə göstərmək üçün veb səhifələr yaratmaq üçün Hipermətn İşarələmə Dilini təmsil edir. O, başqalarının girişi üçün Ümumdünya Şəbəkəsində (WWW) dərc olunacaq statik səhifələrin yaradılması üçün işarələmələri müəyyən edir. Bu işarələmələr brauzerlərə veb səhifənin məzmununu necə göstərəcəklərini bildirir. Belə səhifələrdə düz mətn, şəkillər, digər səhifələrə hiperlinklər, videolar və digər media məlumatları ola bilər. Veb səhifə dərc edildikdə, onun səhifə mənbəyinə baxmaqla onun arxasındakı işarələmə koduna nəzər sala bilərsiniz. Müasir brauzerlər HTM mənbəyində hər bir alt bölmənin və ya işarələmə elementinin işləndiyi veb səhifənin hər bir hissəsini yoxlamağa imkan verir.

## HTM-in qısa tarixi

Since its inception and first role out, the HTML specifications have been maintained by World Wide Web Consortium (W3C) since 1996. 2000-ci ildə o, həm də beynəlxalq standarta çevrildi (ISO/IEC 15445:2000). 1999-cu ildə HTML 4.01 nəşr olundu. 2004-cü ildə Veb Hipermətn Tətbiqi Texnologiyası İşçi Qrupu (WHATWG) 2008-ci ildə W3C ilə birgə təqdim edilən HTML5 versiyası üzərində işləməyə başladı. O, 28 oktyabr 2014-cü ildə tamamlandı və standartlaşdırıldı.

## HTML fayl formatı

HTML 4 sənədi üç hissədən ibarətdir:

1. HTML versiyası məlumatını ehtiva edən sətir
1. deklarativ başlıq bölməsi
1. sənədin faktiki məzmununu ehtiva edən orqan. Bədəni çərçivələrdə saxlamaq üçün BODY elementi və ya FRAMESET elementi tərəfindən həyata keçirilə bilər

Hər bir bölmənin ardınca ağ boşluqlar, yeni sətirlər, nişanlar və şərhlər ola bilər. Sadə bir HTML sənədinin nümunəsi aşağıda göstərildiyi kimidir:

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
   <HEAD>
      <TITLE>Understanding HTML File Format</TITLE>
   </HEAD>
   <BODY>
      <P>Hello World!
   </BODY>
</HTML>
```

### Versiya Məlumatı

Kodun birinci sətri,<!DOCTYPE html> , sənəd növü bəyannaməsi adlanır və brauzerə səhifənin hansı HTML versiyasında yazıldığını bildirir. HTML versiyasından asılı olaraq, sənəd üçün istifadə olunan sənəd növü tərifini (DTD) adlandıran bir sıra müxtəlif sənəd tipli bəyannamələr mövcuddur. Hər bir DTD digərlərindən dəstəklədiyi elementlərə görə fərqlənir və aşağıdakı kimi fərqlənir:

* HTML 4.01 Strict - [deprecated](https://www.w3.org/TR/html401/conform.html#deprecated) və ya çərçivə sənədlərində görünməyən bütün elementləri və atributları ehtiva edir

* HTML 4.01 Transitional - ciddi DTD-dəki hər şeyi və köhnəlmiş elementləri və atributları (əksəriyyəti vizual təqdimata aiddir) ehtiva edir

* HTML 4.01 Çərçivə dəsti - keçid DTD üstəgəl çərçivələrdəki hər şeyi ehtiva edir


**HTML5** üçün versiya məlumatı sadəcə aşağıda qeyd edildiyi kimidir.

```
<!DOCTYPE html>
```

### Başlıq Məlumatı

HTML sənədinin başlığına brauzer tərəfindən göstərilməyən bir sıra HTML elementləri daxil ola bilər. Bu cür elementlər ya səhifə haqqında məlumatı təsvir edən metadatadır, ya da CSS üslub cədvəlləri və ya JavaScript faylları kimi xarici resurslardan məlumat əldə etmək üçün istifadə olunan bölmələri ehtiva edir. Səhifənin başlığı \ ilə təmsil olunur<head> tag və \ ilə bitir</head> etiket.

Səhifənin başlığını təyin etmək üçün \<title> element \<head> teqləri daxilində tələb olunan yeganə elementdir. Eyni şey axtarış motorları tərəfindən səhifənin başlığını müəyyən etmək üçün istifadə olunur.

### Bədən Məlumatı

Bu, brauzerlər tərəfindən göstərilən faylın bütün məzmununu ehtiva edən faylın əsas bölməsidir. Html gövdəsində etiketlər şəklində müxtəlif tikinti bloklarına istinad edə bilən işarələr ola bilər. O, mətn, şəkillər, rənglər, qrafika və s. kimi bir neçə müxtəlif növ məlumatı ehtiva edə bilər. Bundan əlavə, audio və video elementləri brauzerlər tərəfindən göstərilmək üçün html gövdəsinə də daxil edilə bilər. Vizual təqdimat üçün müasir üslub vərəqləri tətbiqi mövcud olduqda, BODY-nin fon rəngi, keçid rəngi, mətn rəngi və s. kimi təqdimat atributları köhnəlmişdir. Beləliklə, eyni effektləri aşağıda göstərildiyi kimi üslub cədvəllərindən istifadə etməklə əldə etmək olar:

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
<HEAD>
 <TITLE>Inline Style Sheets referencing</TITLE>
 <STYLE type#"text/css">
  BODY { background: white; color: black}
  A:link { color: red }
  A:visited { color: maroon }
  A:active { color: fuchsia }
 </STYLE>
</HEAD>
<BODY>
  ... document body...
</BODY>
</HTML>
```

Daxili üslub vərəqlərini yerləşdirmək asandır və vizual effektlərə sürətli tətbiqlər üçün xarici üslub vərəqləri onu bir dəfə yerləşdirməyi və bir çox yerə daxil olmağı daha rahat edir.

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
<HEAD>
 <TITLE>Linking to External style sheets</TITLE>
 <LINK rel#"stylesheet" type#"text/css" href#"smartstyle.css">
</HEAD>
<BODY>
  ... document body...
</BODY>
</HTML>

```

### HTML elementləri

Daha əvvəl qeyd edildiyi kimi, HTML Body daxilindəki məzmunlar Html Elementləri kimi tanınan teqlərlə təmsil olunur. Hər bir etiket kimi yazılan atributlar şəklində əlavə məlumat ola bilər
```
<tag attribute1#"value1" attribute2#"value2">
```
baxmayaraq ki, hər teqdə atributların olması vacib deyil. Atributlar qeyd edilmirsə, hər bir halda standart dəyərlər istifadə olunur. Aşağıda bəzi element nümunələri verilmişdir:

#### Başlıq

```
<head>
  <title>The Title</title>
</head>
```

#### Başlıqlar

```
<h1>Heading level 1</h1>
<h2>Heading level 2</h2>
<h3>Heading level 3</h3>
<h4>Heading level 4</h4>
<h5>Heading level 5</h5>
<h6>Heading level 6</h6>
```

#### Paraqraflar

```
<p>Paragraph 1</p> <p>Paragraph 2</p>
```

## İstinadlar

* [HTML sənədinin Qlobal Strukturu](https://www.w3.org/TR/html401/struct/global.html#h-7.5.4)


