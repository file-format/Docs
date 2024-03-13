{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Make File - Xcode Makefile Skript Faylı",
  "description": "MakeFile fayllarını yarada və aça bilən XCode MakeFile Format və API-lər haqqında məlumat əldə edin.",
  "linktitle": "MAKE",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-mak-aze"
}
},
  "lastmod": "2020-09-10"
}


## MAKE faylı nədir?

MAKE faylı kodun tərtibini təşkil edən XCode skript faylıdır. Çox mənbə kodu fayllarından proqramları tərtib etmək və əlaqələndirmək üçün istifadə olunur. Bu, tətbiqin yenilənməsi lazım olduqda, böyük proqramın hansı hissələrinin yenidən tərtib edilməli olduğuna qərar verməyə kömək edir. Hansı faylların dəyişdiyindən asılı olaraq faylları işə salmaq üçün bir sıra təlimatlardan istifadə edin.

## Fayl Formatının Nümunəsini YARATIN

Aşağıdakı məzmun Make utilitindən istifadə etməklə yerinə yetirilir və çıxışlar aşağıdakı kimidir.

```
hello:
	echo "hello world"
```
**Çıxış etmək**

```
$ make
echo "hello world"
hello world
```

## İstinadlar
 * [XCode və Make - Apple Forumları](https://developer.apple.com/forums/thread/657458)
 * [Obyekt-C Bələdçisi](https://blog.teamtreehouse.com/beginners-guide-objective-c-classes-objects)

