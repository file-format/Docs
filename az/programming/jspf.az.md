{
  "date": "2021-04-20",
  "keywords": [
"JSPF faylı",
"jspf",
"JSPF nümunəsi",
"uzadılması",
"format",
"jspf dərsliyi",
"jsp fraqmenti",
"JSPF fayl formatı"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "JSPF - JSP fraqment fayl formatı",
  "description": "JSPF fayl formatı və JSPF fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "JSPF",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-jsp-azf"
}
},
  "lastmod": "2021-04-21"
}

## JSPF faylı nədir?
.jspf uzantılı fayl JSP fraqmenti adlanır; başqa JSP faylına daxil edilmiş statik fayl. JSPF faylları öz-özünə tərtib edilmir, lakin onlar daxil olduqları səhifənin yanında tərtib edilir. Onun sintaksisi Java Server Pages (JSP) koduna bənzəyir. O, JSP-nin sadəcə bir hissəsini ehtiva edir; bütün JSP sənədini daxil etmir.

## JSPF fayl formatı
JSP 2.0 Spesifikasiyasında JSP fraqmenti termini həddindən artıq yükləndiyi üçün JSP seqmenti termini əvəzinə istifadə olunur. JSP fraqmentləri ya .jsp, ya da .jspf genişləndirmələrindən istifadə edə bilər və ya **/WEB-INF/jspf** və ya digər statik fayllarla birlikdə yerləşdirilməlidir. Tam səhifə olmayan JSP fraqmentləri .jspf genişləndirməsindən istifadə etməli və **/WEB-INF/jspf**-də yerləşdirilməlidir.

### JSP və ya JSP Fraqment Fayl Təşkilatı
JSP faylı sadalanan ardıcıllıqla aşağıdakı bölmələri ehtiva edir:

1. Şərhlərin açılması
2. JSP səhifə direktiv(ləri)
3. Könüllü etiket kitabxanası direktiv(lər)i
4. Könüllü JSP bəyannaməsi(lər)i
5. HTML və JSP kodu

JSP və ya JSPF faylı hər ikisi **Açılış Şərhi** adlanan server tərəfi stil şərhi ilə başlayır:

```
<%-- 
  - Author(s):
  - Date:
  - Copyright Notice:
  - @(#)
  - Description: 
  --%>
```
Bu şərh yalnız server tərəfində görünə bilər, çünki JSP səhifəsinin göstərilməsi zamanı silinir.

## JSP Fragment faylını nə vaxt istifadə etməli?
JSP səhifəsi digər JSP səhifələrində də təkrar istifadə edilə bilən müəyyən, lakin mürəkkəb struktur tələb etdikdə, bunu həll etməyin bir yolu Kompozit Görünüş nümunəsindən (Java Planlarının Nümunələr bölməsi) istifadə edərək, onu parçalara bölməkdir. Məsələn, JSP səhifəsi bəzən təqdimat strukturunda aşağıdakı məntiqi tərtibata malikdir:

{{< figure src="../jspf.png" alt="JSPF fayl formatı" >}}

Bu vəziyyətdə, bu kompozit JSP səhifəsi müxtəlif modullara çevrilə bilər, hər biri ayrıca JSP fraqmenti adlanacaqdır. JSP fraqmentləri daha sonra kompozit JSP səhifəsində müvafiq yerlərdə yerləşdirilə bilər. Beləliklə, JSPF faylı öz-özünə çağırılmayacaq səhifəni daxil etmək üçün statik daxiletmə direktivlərindən istifadə edildikdə istifadə olunur, .jspf uzantılı fayllar Veb proqram arxivinin /WEB-INF/jspf/ kataloquna yerləşdirilməlidir ( müharibə).

## JSPF nümunəsi
```
<%@ include file="/WEB-INF/jspf/header.jspf" %>
...
<%@ include file="/WEB-INF/jspf/menuBar.jspf" %>
...
<jsp:include page="<%= currentBody %>" />
...
<%@ include file="/WEB-INF/jspf/footnote.jspf" %>
...
<%@ include file="/WEB-INF/jspf/footer.jspf" %>
...
```

## İstinadlar

 * [JavaServer Səhifələri üçün Kod Konvensiyaları](https://www.oracle.com/technical-resources/articles/javase/code-convention.html)

