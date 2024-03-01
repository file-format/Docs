{
  "date" : "2023-06-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "BROWSER File - ASP.NET Browser Definition File Format",
  "description":"Lisätietoja BROWSER-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata BROWSER-tiedostoja.",
  "linktitle" : "BROWSER",
  "menu" : {
    "docs" : {
      "parent" : "web",
      "identifier": "web-browse-fir"
}
},
  "lastmod" : "22023-06-06"
}

## Mikä on BROWSER-tiedosto?

ASP.NET-verkkosovellukset käyttävät .browser-tunnisteella varustettua tiedostoa verkkoselaimien kyvyn ja kokoonpanon määrittämiseen. Se sisältää tietoja selaimen ominaisuuksista, rajoituksista ja ominaisuuksista. Nämä ominaisuudet auttavat ASP.NET-kehystä tunnistamaan pyytävän selaimen ja esittämään verkkosivun käyttäjille sen mukaisesti.

## BROWSER Tiedostomuoto

ASP.NET-sovellus käyttää BROWSER-määritystiedostoja selaimen ominaisuuksien määrittämiseen. Palvelin käyttää tämän tiedoston sisältämiä tietoja merkintöjen ja muiden resurssien luomiseen, jotka ovat yhteensopivia pyytävän selaimen kanssa.

BROWSER-tiedostot tallennetaan pelkkää tekstiä sisältävässä tiedostomuodossa. Voit avata BROWSER-tiedoston tekstieditorilla, kuten Notepad, Notepad++, Apple TextEdit ja Visual Studio IDE.

### BROWSER-tiedostomuodon tiedostorakenne

BROWSER-määritystiedostot käyttävät hierarkkista rakennetta. Jokainen .browser-tiedosto sisältää XML-merkinnän, joka sisältää tietyn selaimen tai selainryhmän ominaisuudet ja ominaisuudet. Näitä tietoja ovat ominaisuudet, kuten agenttimerkkijono, versionumerot ja tuki teknologioille, kuten JavaScript, CSS tai muut HTML-elementit. Käyttämällä näitä selaimen määritystiedostoja ASP.NET-kehittäjät mukauttavat käyttökokemuksia eri selainten ominaisuuksien perusteella.

## Viitteet

 * [Tiedostojen käsittely ASP.NET-verkkosivuilla](https://learn.microsoft.com/en-us/aspnet/web-pages/overview/data/working-with-files)



