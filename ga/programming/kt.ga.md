---
date: 2019-10-11
keywords: kt, .kt, kotlin file format, how to open kotlin files, how to run kotlin files, .kt file format, kt file , kotlin file extension, .kt extention, kotlin vs java
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: KT Foirm Chomhaidat
linktitle: KT
description: Ltuilleamh faoi fhormáid comhaid KT agus APIs ar féidir leo comhad KT a chruthú agus a oscailts.
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-20
---

## Cad is comhad KT ann? ##

Sábháiltear cód foinse scríofa in Kotlin le síneadh .kt ar a dtugtar go coitianta **Eisínteacht comhaid Kotlin**. Is teanga ríomhchláraithe tras-ardán ilchuspóireach é an Kotlin arna fhorbairt ag JetBrains le bheith lán-idir-inoibritheach le [Java](/programming/java/). Tá trádmharc Kotlin cosanta ag Fondúireacht Kotlin.

Kotlin was announced as the preferred programming language for Android App development by Google on 7th May 2019. Thosaigh Android Studio 3.0 ag tacú le Kotlin mar mhalairt ar fhorbairt App Android i mí Dheireadh Fómhair 2017.

## Stair Achomair ar Formáid Chomhaid Kotlin KT##

Nocht JetBrains Kotlin i mí Iúil 2011 mar theanga ríomhchlárúcháin nua do JVM. Dúirt ceannaire JetBrains Dmitry Jemerov go raibh an chuid is mó de na teangacha in easnamh ar na gnéithe a bhí á lorg acu seachas Scala ach míbhuntáiste a bhí i dtiomsú mall Scala. Ceann de na príomhspriocanna a bhí ag Kotlin ná tiomsú chomh tapa le Java. Foinsíodh tionscadal Kotlin faoi Cheadúnas Apache 2 i mí Feabhra 2012.

Version 1.0 of Kotlin was released on 15 February 2015. D'fhógair Android tacaíocht den chéad scoth do Kotlin ar Android ag Google I/O 2017. Eisíodh Kotlin 1.2 an 28 Samhain 2017 agus bhí sé in ann cód a roinnt idir ardáin JVM agus JavaScript. Eisíodh Kotlin 1.3 ar 29 Deireadh Fómhair 2018 le tacaíocht do ríomhchlárú asincrónach. D’fhógair Google gurb í Kotlin an rogha teanga ríomhchláraithe le haghaidh forbairt App Android ar 7 Bealtaine 2019. Eisíodh Kotlin 1.4 i mí Lúnasa 2020 le roinnt athruithe beaga chun tacú le hidir-inoibritheacht le Swift/Objective-C.

## Comhréir Kotlin ##

Ceapadh Kotlin le bheith níos fearr ná Java ach fós a bheith idir-inoibritheach le cód Java chun aistriú de réir a chéile ó Java go Kotlin a cheadú.

 * Tá leathcholúin roghnach i Kotlin. Is leor líne nua chun deireadh an ráitis a chur in iúl.
 * Tacaíonn Kotlin le dhá chineál athróg, inléite amháin, sainmhínithe ag an eochairfhocal *val*, agus mutable, arna sainmhíniú ag an eochairfhocal *var*.
 * Tá na ranganna príobháideach agus deiridh de réir réamhshocraithe. Chun teacht ó rang, ní mór an bunrang a dhearbhú leis an eochairfhocal *oscailte*.
 * Tacaíonn Kotlin le cláir nós imeachta freisin.
 * Is é an pointe iontrála chuig clár Kotlin an príomhfheidhm cosúil le Java, C #, etc.

### Sampla Comhréire ###

Seo a leanas sampla de chomhréir Kotlin.

```kotlin
// The example code prints Hello World from Kotlin to the console.
    fun main() {
      val audience = "World"
      println("Hello, $audience!")
}
```

Sa chód thuas, sainmhíníonn an eochairfhocal **spraoi** an phríomhfheidhm ainmnithe. Laistigh den fheidhm, dearbhaítear ‘lucht féachana’ athróg inléite amháin leis an eochairfhocal **val**. Trí úsáid a bhaint as an modh **println**, clóitear Hello World from Kotlin ar an consól. Cuirtear luach an lucht féachana inathraithe isteach sa teaghrán leis an gcomhartha **$**.

## Kotlin vs Java
Is teanga oifigiúil é an Kotlin chun aipeanna Android a scríobh le go leor ardghnéithe a thairiscint, ach ní léiríonn go leor forbróirí Java saineolach a spéis chun aistriú go Kotlin. Ceapann siad gur féidir leo go léir a dhéanamh le Java amháin. Mar sin seo a leanas an chomparáid idir dhá theicneolaíocht a d'fhéadfadh a chur ina luí ar fhorbróirí java aistriú:

| Paraiméadar | Java | Kotlin |
|---------------------------------------------- -|
| Réada Singletons | √ | √ |
| Cineálacha saoróg | √ | Χ |
| Tiomsú | Bytecodes | Meaisín Fíorúil |
| Slonn Lambda | Χ | √ |
| Eagrán Invariant | Χ | √ |
| Réimsí Neamhphríobháideacha | √ | Χ |
| Casts Cliste | Χ | √ |
| Sábháilteacht Neamhspleách | Χ | √ |
| Baill Statach | √ | Χ |

## Tagairtí ##

- [Kotlin (programming language) - Wikipedia](https://en.wikipedia.org/wiki/Kotlin_(programming_language))

