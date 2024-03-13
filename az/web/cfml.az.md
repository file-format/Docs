{
  "date": "2021-08-19",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CFML - ColdFusion İşarələmə Dil Faylı",
  "description": "CFML faylının nə olduğunu və CFML fayllarını yarada və aça bilən API-lər haqqında öyrənin.",
  "linktitle": "CFML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-cfm-azl"
}
},
  "lastmod": "2021-08-19"
}

## CFML faylı nədir?

.cfml uzantılı fayl veb səhifə yaratmaq üçün istifadə edilən ColdFusion İşarələmə Dili faylıdır. Bu ColdFusion tətbiqinin proqramçı tərəfindən necə hazırlanacağını müəyyən etmək üçün istifadə olunan qaydalar toplusuna istinad edir. ColdFusion, [ASP](/web/asp/), [PHP](/programming/php/) və s. kimi digər texnologiyalara nisbətən tez və daha az istifadə etməklə, server tərəfli veb proqramları yaratmaq üçün istifadə edilən proqramlaşdırma dilidir. CML fayllarını aça bilən proqramlardan bəzilərinə Adobe daxildir. ColdFusion 2018, Adobe ColdFusion Builder və Adobe Dreamweaver.

## CFML Fayl Format - Ətraflı Məlumat

CFML faylları işarələmə fayllarıdır və teqlər şəklində veb elementləri ehtiva edir. Bunlar istənilən mətn redaktorunda açıla və redaktə edilə bilən mətn fayllarıdır. CFML faylları [HTML](/web/html/) ilə oxşar olan bir neçə teqdən ibarətdir və adətən açılış və bağlanış teqindən ibarətdir. Bu teqlər də bir və ya bir neçə atributdan ibarət ola bilər.

### Teqlərin Sintaksisi

Aşağıda CFML teqlərinin ümumiləşdirilmiş sintaksisi verilmişdir.

```
<tagname>
  Code/text that is affected by the surrounding tags.
</tagname>
```

Əksər teqlər atributları qəbul edir və aşağıdakı kimi müəyyən edilir.

```
<tagname attribute="value">
  Code/text that is affected by the surrounding tags.
</tagname>
```

Bu teqlərdən bəziləri həmçinin aşağıdakı sintaksislə çoxlu atributları qəbul edir.

```
<tagname attribute1="value" attribute2="value">
  Code/text that is affected by the surrounding tags.
</tagname>
```

## CFML kodu nümunəsi

Budur, faktiki CFML teqindən - `cfoutput` teqindən istifadə edən bir nümunə:

```
<cfoutput>
  #firstname#
</cfoutput>
```

## İstinadlar

* [ColdFusion](https://www.quackit.com/coldfusion/tutorial/)


