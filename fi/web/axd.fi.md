{
  "date": "2023-05-23",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "AXD-tiedosto - ASP.NET Web Handler -tiedostomuoto",
  "description": "Opi mikä on AXD-tiedosto ja API:t, jotka voivat luoda ja avata AXD-tiedostoja.",
  "linktitle": "AXD",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-ax-fid"
}
},
  "lastmod": "2023-05-23"
}

## Mikä on AXD-tiedosto?

AXD-tiedosto on verkkoasetustiedosto, jota käytetään sulautettujen resurssipyyntöjen käsittelemiseen ja hakemiseen ASP.NET:ssä. Se sisältää ohjeet upotettujen resurssien, kuten kuvien, JavaScript-tiedostojen ([.JS](/web/js/)) ja [.CSS](/web/css/)-tiedostojen, hakemiseen. AXD-tiedostoja käytetään resurssien lisäämiseen asiakaspuolen sivuille. Näin asiakassivut voivat käyttää näitä palvelimen resursseja normaalilla tavalla.

## AXD tiedostomuoto

AXD-tiedostot tallennetaan binääritiedostoina palvelinpuolelle. Se viittaa ASP.NET:n Web Handler -tiedostoon, jotka ovat komponentteja, jotka luovat vastauksia tiettyihin pyyntöihin verkkopalvelimelle. AXD-tiedostot suorittavat mukautetun käsittelyn ennen vastauksen luomista asiakaspuolen sivupyyntöjen perusteella. Nämä tallennetaan yleensä **WebResource.axd**-tiedostoina.

### Mikä on WebResource.axd-tiedosto?

Useimmat ASP.NET-projektit tallentavat AXD-tiedostot WebResource.axd-tiedostoina, joiden avulla asiakaspuolen sivut voivat ladata kokoonpanoon upotettuja resursseja. Sovelluksesi voi toimia hitaasti, jos suoritat sen virheenkorjaustilassa, koska WebResources.axd-käsittelijä ei ole välimuistissa.

## Viitteet

 * [WebResource.axd](https://social.msdn.microsoft.com/Forums/en-US/e6559555-5723-4590-9eb6-4b2af26a54cd/what-is-webresourceaxd?forum=aspgettingstarted)

