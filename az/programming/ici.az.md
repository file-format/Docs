{
  "date": "2021-09-13",
  "keywords": [
"ici",
"fayl",
"uzadılması",
"fayl formatı",
"ICI tətbiqi",
"Proqramlaşdırma bələdçisi",
"ici misal",
"ICI proqramlaşdırma dili",
"ICI modulları",
"ICI məlumat modeli",
"ICI sənədləri",
"ICI dili"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "ICI - Proqramlaşdırma Dili Faylı",
  "description": "ICI faylları yarada və aça bilən ICI fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "ICI",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-ic-azi"
}
},
  "lastmod": "2021-09-13"
}

## ICI faylı nədir?

Təfsir edilən və çevik məlumat növləri ilə yanaşı dinamik yazma kimi bir neçə xüsusiyyəti ehtiva edən ümumi təyinatlı proqramlaşdırma dili ICI (qısaltma deyil) proqramlaşdırma dili kimi tanınır. O, [Perl](/programming/pl/) dilinə bənzəyir. Bu ICI dili axına nəzarət konstruksiyalarından ibarətdir və həmçinin C dilinin bəzi operatorlarını ehtiva edir. O, obyekt yönümlü bir dil deyil, lakin OOP-un bəzi xüsusiyyətlərinə üst quruluşlar kimi tanınan xüsusi miras metodu ilə nail olmaq olar. [C](/programming/c) kimi, bu ICI proqramlaşdırma dili eyni sistem interfeysinə və daxili funksiyalar üçün standart kitabxanaya malikdir.


## Qısa tarix ##

1980-ci illərin sonlarında Tim Long tərəfindən ümumi məqsədli şərh edilmiş proqramlaşdırma dili kimi işlənib hazırlanmışdır. Bu dilin əksər xüsusiyyətləri C dilinə bənzəyir və bəzi xüsusi üsulları tətbiq etməklə bəzi xüsusiyyətlərə də nail ola bilir. Bu dil ictimai domenə məxsusdur və yenidən satıla bilən dil kimi mövcuddur və heç kim mənbə kodunu haradan aldığını qeyd etməyə borclu deyil. ICI sənədləri Canon Information System Research Australia şirkətinin müəllif hüquqları altındadır.

## Texniki Spesifikasiya ##

Bu dildə iki fərqli məlumat növü istifadə olunur. Bu ikisi Primitiv və Ümumi məlumat növləridir. Bunların hər ikisi dildə əvvəlcədən müəyyən edilmiş tərkibinə görə müxtəlif ifadələri ehtiva edir. İç içə və alt proqramlar kimi müxtəlif modullar bu dil tərəfindən dəstəklənir. Onun bəzi xassələri Perl-ə bənzədiyi üçün müntəzəm ifadələrlə ciddi inteqrasiyaya malikdir.

Dəstlər heterojen və yuvalanmış olmaqla məhdudlaşır. Bu dəstlər Birlik və Kəsişmə və s. kimi çox istifadə edilən dəst əməliyyatları üçün dəstək verir. O, əsasən çoxmillətli təşkilatlara məxsus proqramlar üçün əsas tətbiq naminə dil kimi istifadə olunur.

Demək olar ki, bütün növ proqramlar bu dildə yazıla bilər və əsasən mürəkkəb məlumat strukturlarını əhatə edən xüsusi proqramlar ICI proqramlaşdırma dilində yazılır. Tətbiqlər ICI tətbiqini orada yazılacaq şəkildə əhatə edə bilər. Tətbiqin funksional hissələri ICI modulları tərəfindən həyata keçirilə bilər. ICI dili bir qədər C dilinə bənzəyir, lakin ICI-nin məlumat modeli kifayət qədər yüksək səviyyədədir və lüğətlər (struktur), dəstlər, dinamik massivlər, müntəzəm ifadələr və (real) sətirlər kimi növlərlə fərqlənir.


## ICI Fayl Format Nümunəsi ##

```

printf("Hello world.\n");

```

```
s = [set 200, 300, "a string"];
if (s[200])
	printf("200 is in the set\n");
if (s[400])
	printf("400 is in the set\n");
if (s["a string"])
	printf("\"a string\" is in the set\n");
s[200] = 0;
if (s[200])
	printf("200 is in the set\n");

```

```

forall (colour in [array "red", "green", "blue"])
	printf("%s\n", colour);

```

## İstinad ##

* [ICI Proqramlaşdırma Dili](http://atrn.org/ici/doc/ici.html)




