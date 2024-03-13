{
  "date": "2019-10-11",
  "keywords": [
"ppsm faylı",
"ppsm fayl formatı",
"ppsm faylı nədir",
"fayl",
"ppsm nümunəsi",
"ppsm fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PPSM - Makro effektiv PowerPoint təqdimat faylı",
  "description": "PPSM fayl formatı və PPSM fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "PPSM",
  "menu": {
    "docs": {
      "parent": "presentation",
      "identifier": "presentation-pps-azm"
}
},
  "lastmod": "2019-09-10"
}

## PPSM faylı nədir?

PPSM uzantısı olan fayllar Microsoft PowerPoint 2007 və ya daha yüksək versiya ilə yaradılmış Makro-aktiv Slayd Şou fayl formatını təmsil edir. Digər oxşar fayl formatı [PPTM](/presentation/pptm/)-dir və Slayd Şousu kimi deyil, redaktə edilə bilən formatda Microsoft PowerPoint ilə açılması ilə fərqlənir. Slayd şousu kimi işə salındıqda, PPSM faylı slayd şousunda məzmunu pozulmamış təqdimat slaydlarını göstərir və defolt olaraq yalnız oxumaq üçün rejimdədir. PPSM faylları hələ də Microsoft PowerPoint-də onu PowerPoint-də açmaqla redaktə edilə bilər.

## Fayl Format ##

PPSM fayl formatı PowerPoint 2007 ilə təqdim edilib və məzmununu saxlamaq üçün XML və [ZIP](/compression/zip/) birləşməsindən istifadə edən OpenXML fayl formatına əsaslanır. Office Open XML fayl formatı ilə yaradılan fayllar, bütün tərkib faylları arasında əlaqə təmin edən digər fayllarla birlikdə XML faylları toplusudur. Bu kolleksiya əslində məzmununa baxmaq üçün çıxarıla bilən sıxılmış arxivdir. Bunu etmək üçün, sadəcə olaraq PPSM fayl uzantısının adını zip ilə dəyişdirin və məzmununu müşahidə etmək üçün onu çıxarın.

Aşağıdakı bölmələr bunların hər birinə bir qədər işıq salır.

### [Məzmun_Növləri].xml ###

Bu, zip çıxarıldıqda baza səviyyəsində tapılan yeganə fayldır. Paketdəki hissələrin məzmun növlərini sadalayır. Paketə daxil olan XML fayllarına bütün istinadlar bu XML faylında istinad edilir. Aşağıda slayd hissəsi üçün məzmun növü verilmişdir:
```
<Override PartName#"/ppt/slides/slide1.xml" ContentType#"application/vnd.openxmlformats-officedocument.presentationml.slide+xml"/>
```
Paketə yeni hissələrin əlavə edilməsi lazımdırsa, bu, yeni hissənin əlavə edilməsi və .rels faylları daxilində hər hansı əlaqənin yenilənməsi ilə edilə bilər. Nəzərə almaq lazımdır ki, belə bir dəyişiklik üçün Content_Types.xml də yenilənməlidir.

### \_rels (Qovluq) ###

Digər hissələr və paketdən kənar resurslar arasındakı əlaqələr əlaqələr hissəsi tərəfindən qorunur. Əlaqələr qovluğunda paket səviyyəli əlaqələri saxlayan tək XML faylı var. Təqdimat fayllarının əsas hissələrinə keçidlər bu faylda URI-lər kimi yer alır. Bu URI-lər hər bir əsas hissənin paketlə əlaqə növünü müəyyən edir. Bura ppt/presentation.xml kimi yerləşən əsas ofis sənədi ilə əlaqə və əsas və genişləndirilmiş xüsusiyyətlər kimi docProps daxilindəki digər hissələr daxildir.
```
<Relationship Id#"rId1" Type#"http:~/~/schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"ppt/presentation.xml"/>.
```
Bir və ya bir neçə əlaqənin mənbəyi olan sənədin hər bir hissəsinin öz əlaqələr hissəsi olacaq, burada hər bir belə əlaqə hissəsi hissənin \_rels alt qovluğunda yerləşir və adın adına '.rels' əlavə edilməklə adlandırılır. hissəsi. Əsas məzmun hissəsinin (presentation.xml) öz əlaqələr hissəsi (presentation.xml.rels) var. O, slideMaster1.xml, notesMaster1.xml, handoutMaster1.xml, slide1.xml, presProps.xml, tableStyles.xml, theme1.xml kimi məzmunun digər hissələri ilə əlaqələri, həmçinin xarici keçidlər üçün URI-ləri ehtiva edir.

#### Açıq Münasibət ####

Açıq əlaqə üçün a-nın Id atributundan istifadə edərək mənbəyə istinad edilir<Relationship> element. Yəni mənbədəki İd hədəfə açıq istinadla birbaşa əlaqə elementinin İd-si ilə xəritələnir.

Məsələn, slaydda bu kimi hiperlink ola bilər:
```
<a:hlinkClick r:id#"rId2">
```
r:id#rId2 slayd üçün əlaqələr hissəsində aşağıdakı əlaqəyə istinad edir (slide1.xml.rels).
```
<Relationship Id#"rId2" Type#"http:~/~/. . ./hyperlink" Target#"http:~/~/www.google.com/" TargetMode#"External"/>
```
#### Gizli Münasibət ####

Gizli əlaqə üçün `-ə belə birbaşa istinad yoxdur<Relationship> ID`. Bunun əvəzinə istinad başa düşülür.

### ppt Qovluğu ###

Bu, Təqdimatın məzmunu ilə bağlı bütün təfərrüatları ehtiva edən əsas qovluqdur. Varsayılan olaraq, aşağıdakı qovluqlara malikdir:

* \_rels

* mövzu

* slaydlar

* slideLayouts

* slideMasters


və aşağıdakı xml faylları:

* təqdimat.xml

* presProps.xml

* tableStyles.xml

* viewProps.xml


## İstinadlar ##

* [OpenXML Təqdimat Fayl Formatı](https://msdn.microsoft.com/en-us/library/dd926741(v#office.12).aspx)

* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-pptx.php)


