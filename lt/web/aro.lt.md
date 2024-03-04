{
  "date": "2021-12-09",
  "keywords": [
"aro",
".aro failą",
"aro failo formatas",
"failo tipas",
"failą",
"tipo",
"kas yra .aro failas"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ARO failo formatas – „SteelArrow“ žiniatinklio programos failas",
  "description": "Sužinokite, kas yra ARO failas ir API, kurios gali kurti ir atidaryti ARO failus.",
  "linktitle": "ARO",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-ar-lto"
}
},
  "lastmod": "2021-12-09"
}

## Kas yra ARO failas?

ARO failas yra serverio pusės tinklalapio failas, sugeneruotas naudojant SteelArrow Web Application. Jame yra [HTML](/web/html/) ir SteelArrow žymos ir scenarijai. Jie vykdomi serveryje, kad būtų sukurtas pilnas atsakymo puslapis, prieš siunčiant juos į vartotojo naršyklę. ARO failuose yra beveik 95% HTML turinio, o likusį sudaro SteelArrow kodas. Kad ARO failai veiktų jums, SteelArrow Web Applications serveris turi būti įdiegtas ir paleistas žiniatinklio serverio įrenginyje.

## ARO failo formatas

ARO files are written in HTML markup language file with embedded JavaScript code and Java applets. [SteelArrow tags](http://www.steelarrow.com/docs/basics1.aro) are the basic building blocks for development of web pages. Though these don't change the display of the page, they are used to fill the page with data. In addition, they may also be used to control the output with conditional statements.

### ARO žymos pavyzdys

The<SAOUTPUT> ARO žyma leidžia kūrėjams išvesti duomenų reikšmes bet kurioje scenarijaus vietoje. Pavyzdžiui, jis gali būti naudojamas norint gauti PARAM lentelės išvestį su<SAOUTPUT VALUE=PARAM[]> kurie gali būti rodomi HTML<BODY> žyma.

## Nuorodos

* [SteelArrow tags](http://www.steelarrow.com/docs/basics.aro)

