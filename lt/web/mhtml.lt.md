{
  "date": "2019-10-11",
  "keywords": [
"mhtml",
"mhtml failą",
"mhtml failo formatą",
"mhtml failo tipas",
"failą",
"tipo",
"kas yra mhtml failas"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MHTML – MIME HTML failas",
  "description": "Sužinokite apie MHTML failo formatą ir API, kurios gali kurti ir atidaryti MHTML failus.",
  "linktitle": "MHTML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-mhtm-ltl"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra MHTML failas?

Failai su MHTML plėtiniu yra tinklalapio archyvo formatas, kurį galima sukurti naudojant daugybę skirtingų programų. Šis formatas žinomas kaip archyvo formatas, nes jis išsaugo žiniatinklio **[HTML](/web/html/)** kodą ir susijusius išteklius viename faile. Šie ištekliai apima viską, kas susieta su tinklalapiu, pvz., vaizdus, programėles, animacijas, garso failus ir pan. MHTML failus galima atidaryti įvairiose programose, pvz., Internet Explorer ir Microsoft Word. Microsoft Windows naudoja MHTML failo formatą, kad įrašytų problemų, pastebėtų naudojant bet kurią Windows programą, kuri kelia problemų, scenarijus. MHTML failo formatas koduoja puslapio turinį, panašų į specifikacijas, nurodytas pranešime/rfc822, kuris yra su paprasto teksto el. paštu susijusios specifikacijos. Tikrosios formato specifikacijos pateiktos [RFC 2557](https://tools.ietf.org/html/rfc2557).

## MHTML failo formatas

MHTML taip pat žinomas kaip MIME Incapsulation of Aggregate HTML dokumentai dėl galimybės koduoti HTML tinklalapius kartu su ištekliais į vieną žiniatinklio archyvą. Remiantis RFC 2557 specifikacijomis, bendras dokumentas yra MIME užkoduotas pranešimas, kuriame yra šakninis šaltinis (objektas) ir kiti ištekliai, susieti su juo per URI. Tokie kiti ištekliai gali būti įterptųjų paveikslėlių, stiliaus lapų, programėlių ir tt vaizdavimas. Be to, tai gali būti kitų daugialypės terpės dokumentų šaknis. Išsamios MHTML failo formato dokumento specifikacijos pateiktos [RFC 2557](https://tools.ietf.org/html/rfc2557) ir turėtų būti nurodytos kuriant bet kokią šio failo formato skaitymo / rašymo programą. Standartas nurodo, kad kūno dalys, į kurias turi būti daroma nuoroda, gali būti identifikuojamos pagal turinio ID arba turinio vietą.

### MIME turinio antraštės

MIME turinio antraštė Content-Location yra apibrėžta siekiant išspręsti URI nuorodas į išteklius kitose kūno dalyse. Ši antraštė gali būti bet kurioje pranešimo ar turinio antraštėje.

### Turinio vietos antraštė

Turinio vieta yra URI, žyminčio kūno dalies, kurioje jis yra, turinys. Jo reikšmė gali būti absoliutus arba santykinis URI. Jis gali būti naudojamas žymėti išteklius, kurių kai kurie arba visi pranešimo gavėjai negali gauti. Viename pranešime leidžiama turėti tik vieną turinio vietos antraštę. Kelių dalių / susijusios struktūros, kurią sudaro kūno dalys su turinio vietos ir turinio ID etiketėmis, pavyzdys:

```
Content-Type: multipart/related; boundary#"boundary-example";
                    type#"text/html"

      --boundary-example

      Content-Type: text/html; charset#"US-ASCII"

      ... ... <IMG SRC#"fiction1/fiction2"> ... ...
      ... ... <IMG SRC#"cid:97116092811xyz@foo.bar.net"> ... ...

      --boundary-example
      Content-Type: image/gif
      Content-ID: <97116092511xyz@foo.bar.net>
      Content-Location: fiction1/fiction2

      --boundary-example
      Content-Type: image/gif
      Content-ID: <97116092811xyz@foo.bar.net>
      Content-Location: fiction1/fiction3

      --boundary-example--
```

### MHTML agregatų URI

MHTML agregato URI skiriasi nuo šakninio URI. Turinio vietos antraštės laukas turėtų būti taikomas visam agregatui, jei jis naudojamas kelių dalių / susijusios antraštės antraštėje. Panašiai gautų išteklių rinkinys gali skirtis nuo išteklių, gautų naudojant jo dalių turinio vietas, kai šiam agregatui nuskaityti naudojamas URI, nurodantis MHTML agregatą. Pavyzdžiui, nuskaitant MHTML agregatą gali būti grąžinta sena versija, o nuskaitant šakninį URI ir su juo susietus objektus gali būti grąžinta naujesnė versija.

## Nuorodos

* [Suvestinių dokumentų MIME inkapsuliavimas – RFC 2557](https://tools.ietf.org/html/rfc2557)

* [MHTML failo formatas – pagal Vikipediją](https://en.wikipedia.org/wiki/MHTML)


