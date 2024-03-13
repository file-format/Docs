{
  "date": "2021-09-23",
  "keywords": [
"QOZ",
"fayl",
"uzadılması",
"fayl formatı",
"NUT rоgrаmming dili",
"Proqramlaşdırma bələdçisi",
"NUT nümunəsi",
"NUT fayl formatı",
"dələ dili",
".nut uzantısı faylı",
"NUT faylları"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "NUT - Squirrel Language File",
  "description": "NUT fayl formatı və NUT fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "NUT",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-nu-azt"
}
},
  "lastmod": "2021-09-23"
}

## NUT faylı nədir?

NUT fayl formatı Squirrel kimi tanınan proqramlaşdırma dilinə aiddir. Bu, daha çox quraşdırılmış sistemlərdə və video oyunlarda istifadə olunan obyekt yönümlü, yüksək səviyyəli və imperativ proqramlaşdırma dilidir.

Sincap dili, ölçü və bant genişliyinə görə asanlıqla tənzimlənə bilən yüngül skript dili hesab olunur. Bu, avtomatik istinadların sayılması və yaddaşdakı zibilin idarə edilməsinin üstünlüyünü nəzərdə tutur.

Squirrel dilinin sintaksisi tərtibatçıları cəlb edir, çünki o, C-yə bənzəyir və skript dilinin xüsusiyyətini ehtiva edir. Ancaq yenə də bu məqsəd üçün digər daha populyar proqramlaşdırma dilləri ilə müqayisədə daha az üstünlüklərə malikdir.



## Qısa tarix ##

It was designed by Alberto Demichelis in 2003. Bununla belə, bu dilin stabil versiyası 2016-cı ildə buraxılmışdır. O, zlib/libpng lisenziyası əsasında hazırlanmışdır. 2010-cu ildə lisenziya dəyişdirilərək MİT-ə verildi. Bu dil [LUA](/programming/lua/) (Proqramlaşdırma dili) dilinin ilhamlanmış versiyası hesab olunur. Alberto tərəfindən daha sərfəli etmək üçün hazırlanmış veb saytında keçmiş dil üçün təkliflərin siyahısı var.


## Texniki Spesifikasiya ##

Sincap dilinin xüsusiyyəti və spesifikasiyası çoxşaxəlidir. O, Dinamik yazma imkanını, nümayəndə heyətinin xüsusiyyətlərini, siniflərin və interfeyslərin bir neçə istifadəsini təmin edir. Bu dilin sintaksisi C dilinin sintaksisi ilə oxşarlığa malikdir. Enduro/X (klaster proqram serveri) kimi proqramlar bu dildən istifadə edir. Squirrel video oyunları üçün də istifadə edildiyi üçün onlardan bəziləri OpenTTD, GTA IV və s.

The stable release of the language is 3.0.7. MirthKit kimi tanınan alət dəsti iki ölçülü oyunlar üçün açıq mənbə və çarpaz platforma təmin etmək üçün Squirrel proqramlaşdırma dilindən istifadə edir. Bu dilin təbiəti dinamikdir və əksər funksiyalar [Python](/programming/py/), LUA və s. oxşardır. O, həmçinin registr əsaslı VM-nin həyata keçirilməsini nəzərdə tutur. Squirrel-in performansı LUA ilə müqayisədə daha yavaşdır.

Başqa bir .nut uzantılı fayl növü də var, ona görə də hansı NUT faylının olduğunu öyrənmək üçün faylın ölçüsünə baxmaq lazımdır. Squirrel script NUT faylları əsasən 1 MB-dan kiçikdir, video NUT faylları isə adətən 1 MB-dan böyükdür.


## NUT Fayl Format Nümunəsi ##

```
function factorial(x)
  {
    if (x == 0) {
      return 1;
}
    else {
      return x * factorial(x-1);
}
  }
```

```

class BaseVector {
    constructor(...)
    {
      if(vargv.len() >= 3) {
        x = vargv[0];
        y = vargv[1];
        z = vargv[2];
  }
}
    x = 0;
    y = 0;
    z = 0;
  }

  class Vector3 extends BaseVector {
    function _add(other)
    {
      if(other instanceof ::Vector3)
        return ::Vector3(x+other.x,y+other.y,z+other.z);
      else
        throw "wrong parameter";
}
    function Print()
    {
      ::print(x+","+y+","+z+"\n");
}
  }

  local v0 = Vector3(1,2,3)
  local v1 = Vector3(11,12,13)
  local v2 = v0 + v1;
  v2.Print();

```

## İstinad ##

* [NUT - by Wikipedia](https://en.wikipedia.org/wiki/Squirrel_(programming_language))
