{
  "date": "2021-04-08",
  "keywords": [
"rpm failą",
"rpm failo formatas",
"kas yra rpm failas",
"failą",
"rpm pavyzdys",
"rpm failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "RPM – „Red Hat Package Manager“ failas",
  "description": "Sužinokite apie RPM failo formatą ir API, kurios gali kurti ir atidaryti RPM failus.",
  "linktitle": "RPM",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-rp-ltm"
}
},
  "lastmod": "2021-04-09"
}

## Kas yra RPM failas?

Failas su plėtiniu .rpm yra Red Hat Linux operacinės sistemos paketas, skirtas programoms įdiegti Linux sistemose. Red Hat Package Manager naudoja RPM failo formatą ir yra nemokama atvirojo kodo paketų valdymo sistema. Nors RPM failus galima naudoti programoms diegti, juos galima konvertuoti į kitus paketų formatus, tokius kaip [DEB](/compression/deb/), naudojant Debian programą, vadinamą Alien.

## RPM failo formatas

RPM failas yra dvejetainis failas, kuriame gali būti failų rinkinys. Dažniausiai RPM failai yra dvejetainiai RPM, kurie yra sudaryti programinės įrangos vykdomieji failai. RPM faile gali būti šaltinio RPM (SRPM), kuriuos galima naudoti kuriant paketą iš šaltinio kodo. RPM failo formatas susideda iš keturių skyrių.

 * Švinas – identifikuoja failą kaip RPM failą
 * Parašas – jis gali būti naudojamas siekiant užtikrinti vientisumą ir (arba) autentiškumą
 * Antraštė – yra metaduomenys, įskaitant paketo pavadinimą, versiją, architektūrą, failų sąrašą ir kt.
 * Failų archyvas – taip pat žinomas kaip naudingoji apkrova, kuri paprastai yra cpio formatu, suglaudinta naudojant [GZIP](/compression/gz/)

## Nuorodos

* [RPM – Vikipedija](https://rpm.org)

* [RPM dokumentacija](https://rpm.org/documentation.html)


