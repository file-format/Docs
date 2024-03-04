{
  "date": "2019-10-11",
  "keywords": [
"arsc",
".arsc",
"kas yra arsc failas",
"Kaip atidaryti arsc failą",
"pratęsimas",
"failą",
"arsc failą",
"arsc failo formatas",
"arsc failo plėtinys",
"arsc failo pavyzdys"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ARSC – „Android“ paketo išteklių lentelės failas ",
  "description": "Sužinokite apie ARSC failo formatą ir API, kurios gali sukurti ir atidaryti ARSC failą.",
  "linktitle": "ARSC",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-ars-ltc"
}
},
  "lastmod": "2021-06-22"
}

## Kas yra ARSC failas?

ARSC failas yra Android išteklių lentelės failas, kuriame yra programos išteklių sąrašas lentelės formatu. Čia yra tokia informacija kaip išteklių pavadinimai, ypatybės ir ID. ARSC failai yra APK paketų, naudojamų šioms Android programoms įdiegti, dalis. Visi ištekliai, pvz., vaizdai, išdėstymai, stiliai ir eilutės, Android programoje konvertuojami į dvejetainius failus, kai sugeneruojamas APK failas. Taip pat sugeneruojamas ARSC failas, kuriame yra visų programos sudarytų išteklių ir jų ID sąrašas.

## ARSC failo formatas

.arsc plėtinio failai yra dvejetainiai failai, sugeneruoti kompiliatoriui, pvz., ANT (Eclipse) arba Gradle (AS), sukompiliavus Android programos kodą, kad būtų sukurtas [APK](/compression/apk/) failas. Galite išskleisti APK failą naudodami bet kurią archyvavimo priemonę, pvz., WinZip, kad peržiūrėtumėte jo turinį, kuris yra sukompiliuoti Java klasės failai, ty classes.dex. Be šių, jame taip pat yra šis ARSC failas, kuriame yra metainformacijos apie:

 * XML mazgai
 * Atributai
 * Išteklių ID

APK failo ištekliai nurodomi pagal išteklių ID, o atributai išsprendžiami pagal vertę vykdymo metu. Android aapt įrankis surenka visus išteklius, apibrėžtus failuose kūrimo metu ir priskiria jiems išteklių ID. Kai kompiliuotiems ištekliams priskiriami identifikatoriai, iš šaltinio kodo ir išteklių.arsc sugeneruojamas R.java failas.

## Nuorodos

* [Dvejetainių išteklių lentelės struktūra](https://stackoverflow.com/questions/27548810/android-compiled-resources-resources-arsc)


