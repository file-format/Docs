{
  "date": "2020-01-10",
  "keywords": [
"otg tiedosto",
"otg-tiedostomuoto",
"mikä on otg-tiedosto",
"tiedosto",
"otg esimerkki",
"otg tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "OTG - OpenDocument-piirustusmallin tiedostomuoto",
  "description": "Opi OTG-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata OTG-tiedostoja.",
  "linktitle": "OTG",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-ot-fig"
}
},
  "lastmod": "2020-01-10"
}

## Mikä on OTG-tiedosto?

OTG-tiedosto on piirustusmalli, joka on luotu OpenDocument-standardilla, joka seuraa OASIS Office Applications -sovellusta {{HYPERLINKKI}}. Se edustaa vektorikuvan piirustuselementtien oletusorganisaatiota, jota voidaan käyttää edelleen parantamaan tiedoston sisältöä. OTF-tiedostot ovat kuten kaikki muut OpenDocument-muotoon perustuvat tiedostot, jotka perustuvat XML-muotoon edustamaan asiakirjan sisältöä. OTF-tiedostoja voi tarkastella avaamalla ne missä tahansa teksti- tai tavallisessa XML-editorissa.

## OTG-tiedostomuodon tekniset tiedot ##

OTG-tiedostomuoto perustuu OpenDocument XML -muotoon, jolla on vakiintunut skeema. OpenDocument-muodon kunkin osan rakennetta edustaa elementti, jolla on siihen liittyviä attribuutteja ja joka on yhteinen kaikille asiakirjatyypeille, kuten tekstiasiakirjalle, laskentataulukolle tai piirustustiedostolle. OTG, joka on piirustusmalli, hyödyntää laajasti Graphics Content -määrityksiä, jotka sisältävät:

  * Parannetut sivuominaisuudet graafisille sovelluksille
  * Muotojen piirtäminen
  * Kehykset
  * 3D-muodot
  * Mukautettu muoto
  * Esitysmuodot
  * Esityksen animaatiot
  * SMIL-esitysanimaatiot
  * Esittelytapahtumat
  * Esitä tekstikentät
  * Esitysasiakirjan sisältö

### Parannetut sivuominaisuudet graafisille sovelluksille ###
#### Moniste Master ####

Moniste Master -elementti on malli, jolla luodaan automaattisesti monisteen sivut sovelluksille, jotka tukevat tällaisten sivujen tulostamista.
Attribuutit, jotka voidaan liittää `<style:handout-master> ` elementit ovat:

|Layout|Attribuutti|Kuvaus
---|---|---|
|Esityssivun asettelu|esitys:esityksen-sivun-asettelun-nimi|Linkit kohteeseen `<style:presentation-page-layout> `-attribuutti
|Sivun asettelu|`tyyli:sivun asettelun-nimi` | Määrittää sivuasettelun, joka sisältää monisteen perussivun koot, reunat ja suunnan.
|Sivun tyyli|`draw:style-name`|Määrittää lisämuotoiluattribuutit monisteen perussivulle määrittämällä piirustussivun tyylin.|
|Otsikkoilmoitus| `presentation:use-header-name`| Määrittää otsikkokentän määrityksen nimen, jota käytetään kaikille monisteen pääsivulla näytettäville otsikkokentille.
|Alatunnisteilmoitus| presentation:use-footer-name|Määrittää alatunnistekentän määrityksen nimen, jota käytetään kaikille monisteen pääsivulla näytettäville alatunnistekentille.
|Päivämäärä- ja aikailmoitus|use-date-time-name|Määrittää päivämäärä-aika-kentän määrityksen nimen, jota käytetään kaikissa monisteen perussivulla näytettävissä päivämäärä-aika-kentissä.

### Muotojen piirtäminen ###
OpenDocument-muoto tukee useita piirustusmuotoja, joita voidaan käyttää kaikentyyppisissä dokumenteissa.

|Muoto|liittyvät attribuutit| elementtejä
---|---|---|
Suorakulmio - `<draw:rect> `|Sijainti, koko, tyyli, taso, Z-indeksi, tunnus, kuvatekstitunnus, tekstiankkuri, taulukon tausta, piirrosten päätekohta, pyöristetyt kulmat|otsikko, pitkä kuvaus, tapahtumaseuraajat, liimapisteet, teksti
Rivi `<draw:line> `|Tyyli, taso, Z-indeksi, tunnus, kuvatekstitunnus ja muunnos, tekstiankkuri, taulukon tausta, piirtämisen loppukohta, aloituspiste, loppupiste|otsikko, pitkä kuvaus, tapahtumaseuraajat, liimapisteet, teksti
Polyline `<draw:polyline> `| Sijainti, koko, näkymäruutu, tyyli, taso, Z-indeksi, tunnus, kuvatekstitunnus ja muunnos, tekstiankkuri, taulukon tausta, piirrä päätepiste, pisteet| Otsikko, pitkä kuvaus, tapahtumaseuraajat, liimakohdat, teksti
Monikulmio `<draw:polygon> `|Sijainti, koko, näkymäruutu, tyyli, taso, Z-indeksi, tunnus, kuvatekstitunnus ja muunnos, tekstiankkuri, taulukon tausta, piirtämisen loppukohta, pisteet| otsikko, pitkä kuvaus, tapahtumaseuraajat, liimapisteet, teksti
|Säännöllinen monikulmio `<draw:regular-polygon> `|Sijainti, koko, tyyli, taso, Z-indeksi, tunnus, kuvatekstitunnus ja muunnos, tekstiankkuri, taulukon tausta, piirrosten päätekohta, kovera, kulmat, terävyys|otsikko, pitkä kuvaus, tapahtumaseuraajat, liimapisteet, teksti
|Paht `<draw:path> `|Sijainti, koko, näkymäruutu, tyyli, taso, Z-indeksi, tunnus, kuvatekstitunnus ja muunnos, tekstiankkuri, taulukon tausta, piirroksen loppupaikka, polkutiedot| Otsikko, pitkä kuvaus, tapahtumaseuraajat, liimakohdat, teksti

### Kehykset ###
Piirustusdokumentin kehys on suorakaiteen muotoinen säiliö, joka sisältää tekstilaatikoita, kuvia tai objekteja. Kehykset tukevat lisäominaisuuksia, kuten ääriviivoja, kuvakarttoja ja hyperlinkkejä. Kehys voi sisältää kohteen sekä kuvan, jolloin objektista voidaan esittää useita toistoja. Sovellukset renderöivät kunkin elementin parhaan tuen perusteella.

Kehykset voivat sisältää:
  * Tekstilaatikot
  * Objektit, jotka esitetään joko OpenDocument-muodossa tai objektikohtaisessa binäärimuodossa
  * Kuvat
  * Sovelmat
  * Laajennukset
  * Kelluvat kehykset

Kehys sisältyy asiakirjaan alla olevan kuvan mukaisesti.

```
<define name=draw-frame>
<element name=draw:frame>
<ref name=common-draw-shape-with-text-and-styles-attlist/>
<ref name=common-draw-position-attlist/>
<ref name=common-draw-rel-size-attlist/>
<ref name=common-draw-caption-id-attlist/>
<ref name=presentation-shape-attlist/>
<ref name=draw-frame-attlist/>
<zeroOrMore>
<choice>
<ref name=draw-text-box/>
<ref name=draw-image/>
<ref name=draw-object/>
<ref name=draw-object-ole/>
<ref name=draw-applet/>
<ref name=draw-floating-frame/><ref name=draw-plugin/>
</choice>
</zeroOrMore>
<optional>
<ref name=office-event-listeners/>
</optional>
<zeroOrMore>
<ref name=draw-glue-point/>
</zeroOrMore>
<optional>
<ref name=draw-image-map/>
</optional>
<optional>
<ref name=svg-title/>
</optional>
<optional>
<ref name=svg-desc/>
</optional>
<optional>
<choice>
<ref name=draw-contour-polygon/><ref name=draw-contour-path/>
</choice>
</optional>
</element>
</define>
```

## Viitteet ##
* [OASIS Open Document Format for Office Applications](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)

* [OpenDocument-muoto - Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)


