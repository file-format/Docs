{
  "date": "2021-12-09",
  "keywords": [
"asa",
".asa",
"tiedosto muoto",
"tiedostotyyppi",
"mikä on .asa-tiedosto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ASA - ASP-määritystiedosto",
  "description": "Opi mikä on ASA-tiedosto ja API:t, jotka voivat luoda ja avata ASA-tiedostoja.",
  "linktitle": "ASA",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-as-fia"
}
},
  "lastmod": "2021-12-09"
}

## Mikä on ASA-tiedosto?

ASA-tiedosto on määritystiedosto, joka on luotu [ASP](/web/asp/)/ASP.NET-projekteille. Se sisältää muuttujien, sisältöjen ja funktioiden määritykset, jotka on tarkoitettu käytettäväksi sovelluksessa globaalilla tasolla. Kaikilla projektin sivuilla on pääsy näihin muuttujiin ja funktioihin, jolloin vältytään niiden kirjoittamiselta uudelleen. Yksi tällainen esimerkki on Global.asa-sivu, joka on tallennettu juurihakemistoon, jotta muut ASP-sivuston sivut voivat käyttää sitä. Global.asa-tiedostot ovat valinnaisia, mutta jos niitä käytetään, kussakin sovelluksessa voi olla vain yksi Global.asa-tiedosto.

## ASA-tiedostomuoto – lisätietoja

ASA-tiedostot ovat pelkkiä tekstitiedostoja, joissa on seuraavat tiedot.

 * Sovellustapahtumat
 * Session tapahtumat
 * \<object> ilmoituksia
 * TypeLibrary-ilmoitukset
 * #include-direktiivi

## Esimerkki ASA-tiedostosta

Global.asa-tiedosto voisi näyttää suunnilleen tältä.

```
<script language="vbscript" runat="server">

sub Application_OnStart
'some code
end sub

sub Application_OnEnd
'some code
end sub

sub Session_OnStart
'some code
end sub

sub Session_OnEnd
'some code
end sub

</script>
```

## Viitteet

* [ASP Global.asa -tiedosto - w3schools](https://www.w3schools.com/asp/asp_globalasa.asp)


