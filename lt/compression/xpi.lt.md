{
  "date" : "2022-06-07",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "XPI – kelių platformų diegimo programos paketo failas",
  "description":"Sužinokite apie XPI failo formatą ir API, kurios gali kurti ir atidaryti XPI failus.",
  "linktitle" : "XPI",
  "menu" : {
    "docs" : {
    "identifier": "compression-xpi-lt",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-07"
}

## Kas yra XPI failas?

XPI failas yra diegimo archyvas, kuris suglaudinamas siekiant sumažinti failo dydį. Jį naudoja Mozilla programos, norėdami įdiegti papildinius ir priedų failus. Jame yra diegimo scenarijus arba manifestas failo šaknyje kartu su daugybe duomenų failų. XPI faile gali būti temų, įrankių rinkinio arba Firefox papildinių, kuriuos vartotojas gali įdiegti, kad taptų Firefox naršyklės, Thunderbird ar SeaMonkey dalimi.

## XPI failo formatas – daugiau informacijos

XPI failai išsaugomi diske kaip [ZIP](/compression/zip/) archyvai, kurie sujungia kelis failus į vieną suspaustą failą. XPI faile gali būti diegimo scenarijaus failų, pvz., JS, ir žiniatinklio failų, tokių kaip [CSS](/web/css/), [HTML](/web/html/) ir [JSON](/web/json/). Kartais jame taip pat gali būti [PNG](/image/png/) vaizdo failų, kurie bus naudojami kaip priedo piktogramos.

### Kaip peržiūrėti XPI failo turinį?

XPI failas praktiškai yra ZIP archyvas, kurio turinį galima peržiūrėti atliekant šiuos veiksmus.

 * Pakeiskite failo plėtinį iš XPI į ZIP
 * Išskleiskite failo turinį naudodami bet kurią standartinę išskleidimo priemonę, pvz., WinZip (Windows, Mac), 7-Zip (Windows) arba Apple Archive Utility (Mac).

### Įdiekite XPI failą Firefox Android.

Dažniausiai žmonėms įdomu sužinoti, ar XPI failus galima įdiegti Firefox Android įrenginiuose. Android galite įdiegti priedą iš XPI failo, surasdami failą ir atidarydami jį naudodami Firefox.

## Nuorodos

* [XPInstall – Vikipedija](https://en.wikipedia.org/wiki/XPInstall)

* [Kaip atidaryti XPI failo plėtinį?](https://support.mozilla.org/en-US/questions/1009049)


