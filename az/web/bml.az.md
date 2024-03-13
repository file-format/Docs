{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "BML Fayl Format - Bean Markup Language File",
  "description": "BML fayl formatı və BML faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "BML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-bm-azl"
}
},
  "lastmod": "2021-08-12"
}

## BML faylı nədir?

.bml uzantılı fayl Java proqramlarını dəstəkləmək üçün Java siniflərini saxlayan Bean Markup Language faylıdır. Bu, Java obyektlərinə və metodlarına daxil olmağa imkan verir və Java siniflərindən istifadə edərək yeni funksionallıq yaratmağa ehtiyac yoxdur. Faydalı vəzifələri yerinə yetirmək üçün komponentlərin bir-biri ilə necə əlaqəli olduğunu müəyyənləşdirir. BML strukturları və komponentlər əlaqələrini təsvir etmək üçün IBM alphaWorks tərəfindən hazırlanmışdır. BML faylları Veb Brauzerlər, Microsoft Notepad və Notepad++ kimi istənilən mətn redaktoru vasitəsilə açıla və baxıla bilər.

## BML fayl formatı

IBM alphaworks veb-saytı BML-in iki tətbiqini təmin etmişdir. Birinci tətbiq, istədiyiniz lobya iyerarxiyasını yaratmaq üçün BML skriptini oynayan tərcüməçidir. İkinci tətbiq hər hansı BML skriptini əks olunmayan Java koduna tərtib edən kompilyatordur. Bu o mənada sərfəlidir ki, o, proqramın komponentlərarası strukturunu bu xüsusi məqsəd üçün nəzərdə tutulmuş dildən istifadə etməklə tutmağa imkan verir, əlavə olaraq onu 'normal' Java kodunda tərtib etmək imkanı verir.

## BML etiketləri

Aşağıda BML dilində istifadə olunan bəzi teqlərin izahı verilmişdir:

### The<bean> etiket:

The<bean> element yeni lobya yaratmaq və ya lobya adı ilə axtarmaq üçün istifadə olunur. The<bean> etiket aşağıdakı formatdadır:
```
<bean class = "classname or serialized file" [id = "name"]>
</bean>
```
Teqdəki id JavaBean üçün obyekt reyestri ilə əlaqələndirilir.

### The<string> etiket

Simli etiketdən istifadə etməyin iki yolu var:

 1. Boş olmayan sətir yaratmaq üçün:

```
<string [value = "value of string"]> [value of string]
</string>
```
 2. Boş sətir yaratmaq üçün:

```
<string/>
```
## İstinadlar

* [Object-Oriented Messaging with XML](https://docs.oracle.com/cd/A87860_01/doc/appdev.817/a86030/adx16nt5.htm)
* [Fiziki İşarələmə Dili](http://web.mit.edu/mecheng/pml/standards.htm)



