{
  "date": "2023-05-23",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "AXD failas – ASP.NET žiniatinklio tvarkyklės failo formatas",
  "description": "Sužinokite, kas yra AXD failas ir API, kurios gali kurti ir atidaryti AXD failus.",
  "linktitle": "AXD",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-ax-ltd"
}
},
  "lastmod": "2023-05-23"
}

## Kas yra AXD failas?

AXD failas yra žiniatinklio nustatymų failas, naudojamas ASP.NET įterptųjų išteklių užklausoms tvarkyti ir nuskaityti. Jį sudaro instrukcijos, kaip atkurti įterptuosius išteklius, pvz., vaizdus, JavaScript ([.JS](/web/js/)) ir [.CSS](/web/css/) failus. AXD failai naudojami ištekliams į kliento puslapius įterpti. Tai leidžia klientų puslapiams standartiniu būdu pasiekti šiuos išteklius serveryje.

## AXD failo formatas

AXD failai saugomi kaip dvejetainiai failai serverio pusėje. Tai reiškia žiniatinklio tvarkyklės failą ASP.NET, kurie yra komponentai, generuojantys atsakymus į konkrečias žiniatinklio serverio užklausas. AXD failai atlieka pasirinktinį apdorojimą prieš generuodami atsakymą pagal kliento puslapio užklausas. Paprastai jie išsaugomi kaip **WebResource.axd** failai.

### Kas yra WebResource.axd failas?

Dauguma ASP.NET projektų išsaugo AXD failus kaip WebResource.axd failus, kurie leidžia kliento puslapiams atsisiųsti išteklius, įterptus į mazgą. Jūsų programa gali veikti lėtai, jei paleisite ją derinimo režimu, nes WebResources.axd tvarkytojas nėra talpykloje.

## Nuorodos

 * [WebResource.axd](https://social.msdn.microsoft.com/Forums/en-US/e6559555-5723-4590-9eb6-4b2af26a54cd/what-is-webresourceaxd?forum=aspgettingstarted)

