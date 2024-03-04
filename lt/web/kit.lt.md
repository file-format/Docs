{
  "date" : "2022-07-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Sužinokite apie KIT failo formatą ir API, kurios gali kurti ir atidaryti KIT failus.",
  "title" : "KIT failo formatas – CodeKit failas",
  "linktitle" : "KIT",
  "menu" : {
    "docs" : {
      "identifier":"web-kit-lt",
      "parent" : "web"
}
},
  "lastmod" : "2022-07-04"
}

## Kas yra KIT failas?

Failas su plėtiniu .kit yra HTML failas, sukurtas naudojant [CodeKit](https://codekitapp.com/) programavimo kalbos programą. Be esamų [HTML](/web/html/) failų, jame yra importai ir kintamieji, todėl jis idealiai tinka statinėms svetainėms. CodeKit sukompiliuoja KIT failus į HTML, kuriuos galima lengvai naudoti kaip statinius svetainės failus.

## KIT failo formatas

KIT failai yra HTML failai, kuriuose papildomai yra importuojami elementai ir kintamieji. Jie saugomi kaip paprasto teksto failai ir gali būti atidaryti naudojant bet kurį teksto rengyklę arba žiniatinklio failų rengyklę.

### KIT failų importavimas

Beveik bet kokio tipo failus galima importuoti į rinkinio failą. Toliau pateikiama importavimo sintaksė, naudojama failams importuoti į .kit failą.

```
<!-- @import "someFile.kit" -->
<!-- @import "file.html" -->
```

Kai importas įtraukiamas į KIT failą ir išsaugomas, jis pakeičiamas importuojamo failo tekstu. Taip pat galite naudoti @include vietoj @import.

### Keli importai KIT faile

Taip pat galite importuoti daugiau nei vieną failą vienu metu naudodami kableliais atskirtą sąrašą:

```
<!-- @import someFile, otherFile.html, ../thirdFile.kit -->
```

## Nuorodos

* [Kas yra rinkinys?](https://codekitapp.com/help/kit/)


