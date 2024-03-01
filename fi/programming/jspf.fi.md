{
  "date": "2021-04-20",
  "keywords": [
"JSPF-tiedosto",
"jspf",
"JSPF esimerkki",
"laajennus",
"muoto",
"jspf opetusohjelma",
"jsp fragmentti",
"JSPF-tiedostomuoto"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "JSPF - JSP-fragmenttitiedostomuoto",
  "description": "Opi JSPF-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata JSPF-tiedostoja.",
  "linktitle": "JSPF",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-jsp-fif"
}
},
  "lastmod": "2021-04-21"
}

## Mikä on JSPF-tiedosto?
Tiedostoa, jonka tunniste on .jspf, kutsutaan JSP-fragmentiksi. staattinen tiedosto, joka sisältyy toiseen JSP-tiedostoon. JSPF-tiedostoja ei käännetä yksinään, vaan ne käännetään sen sivun viereen, johon ne sisältyivät. Sen syntaksi on samanlainen kuin Java Server Pages (JSP) -koodi. Se sisältää vain osan JSP:stä; ei sisällä koko JSP-asiakirjaa.

## JSPF-tiedostomuoto
Termiä JSP-segmentti käytetään sen sijaan, koska termi JSP-fragmentti on ylikuormitettu JSP 2.0 -spesifikaatiossa. JSP-fragmentit voivat käyttää joko .jsp- tai .jspf-päätteitä, ja ne tulee sijoittaa joko tiedostoon **/WEB-INF/jspf** tai muiden staattisten tiedostojen kanssa. JSP-osien, jotka eivät ole täydellisiä sivuja, on käytettävä .jspf-tunnistetta ja ne on sijoitettava kansioon **/WEB-INF/jspf**

### JSP tai JSP Fragment File Organization
JSP-tiedosto sisältää seuraavat osat siinä järjestyksessä kuin ne on lueteltu:

1. Kommenttien avaaminen
2. JSP-sivudirektiivi(t)
3. Valinnaiset tunnistekirjaston käskyt
4. Valinnaiset JSP-ilmoitukset
5. HTML- ja JSP-koodi

Sekä JSP- että JSPF-tiedostot alkavat palvelinpuolen tyylikommentilla, jota kutsutaan nimellä **Avauskommentti**:

```
<%-- 
  - Author(s):
  - Date:
  - Copyright Notice:
  - @(#)
  - Description: 
  --%>
```
Tämä kommentti voi näkyä vain palvelinpuolella, koska se poistetaan JSP-sivun renderöinnin aikana.

## Milloin käyttää JSP-fragmenttitiedostoa?
Kun JSP-sivu vaatii tietyn mutta monimutkaisen rakenteen, jota voidaan käyttää uudelleen myös muilla JSP-sivuilla, yksi tapa käsitellä tämä on pilkkoa se osiin käyttämällä Composite View -mallia (Java Blueprintsin Patterns-osio). Esimerkiksi JSP-sivulla on joskus seuraava looginen asettelu esitysrakenteessa:

{{< figure src="../jspf.png" alt="JSPF-tiedostomuoto" >}}

Tässä tilanteessa tämä komposiitti JSP-sivu voidaan muuntaa useiksi moduuleiksi, joista jokaista kutsutaan erilliseksi JSP-fragmentiksi. JSP-fragmentit voidaan sitten sijoittaa sopiviin paikkoihin JSP-yhdistelmäsivulla. Siksi JSPF-tiedostoa käytetään, kun staattisia sisällytyksiä käytetään sisällyttämään sivu, jota ei kutsuta itsestään, tiedostot, joiden pääte on .jspf, tulee sijoittaa verkkosovellusarkiston /WEB-INF/jspf/-hakemistoon ( sota).

## JSPF esimerkki
```
<%@ include file="/WEB-INF/jspf/header.jspf" %>
...
<%@ include file="/WEB-INF/jspf/menuBar.jspf" %>
...
<jsp:include page="<%= currentBody %>" />
...
<%@ include file="/WEB-INF/jspf/footnote.jspf" %>
...
<%@ include file="/WEB-INF/jspf/footer.jspf" %>
...
```

## Viitteet

 * [JavaServer-sivujen koodikäytännöt](https://www.oracle.com/technical-resources/articles/javase/code-convention.html)

