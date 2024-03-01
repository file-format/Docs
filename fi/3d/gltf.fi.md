{
  "date": "2019-12-12",
  "keywords": [
"GLTF",
"tiedosto",
"laajennus",
"muoto",
"3D",
"Khronos Group 3D"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Opi GLTF-tiedostoista ja sovellusliittymistä, jotka voivat luoda ja avata GLTF-tiedostoja.",
  "title": "GLTF - GL-lähetystiedostomuoto",
  "linktitle": "GLTF",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-glt-fif"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on GLTF-tiedosto?

glTF (GL Transmission Format) on 3D-tiedostomuoto, joka tallentaa 3D-mallitiedot JSON-muodossa. JSONin käyttö minimoi sekä 3D-resurssien koon että ajonaikaisen käsittelyn, joka tarvitaan näiden resurssien purkamiseen ja käyttämiseen. Se otettiin käyttöön 3D-kohtausten ja -mallien tehokkaaseen lähettämiseen ja lataamiseen sovellusten mukaan. glTF:n on kehittänyt Khronos Group 3D Formats Working Group, ja sen luojat kuvailevat sitä myös 3D:ksi [JPEG](/image/jpeg/).

GLTF-tiedostomuoto määrittelee laajennettavan, yleisen julkaisumuodon 3D-sisältötyökaluille ja -palveluille, mikä virtaviivaistaa luontityönkulkua ja mahdollistaa sisällön yhteentoimivan käytön koko alalla. glTF-tiedostomuodon luomisen taustalla oli tarkoitus määritellä laajennettava, yhteinen julkaisumuoto 3D-sisältötyökaluille ja -palveluille, joiden pitäisi virtaviivaistaa luontityönkulkua ja mahdollistaa sisällön yhteentoimiva käyttö koko alalla. Se minimoi WebGL:ää ja muita sovellusliittymiä käyttävien sovellusten ajonaikaisen käsittelyn.

## GLTF-tiedoston lyhyt historia

The first specifications for glTF file format 1.0 were announced in October 2015. Tämä oli tullut sarjana ponnisteluja, jotka Khronos aloitti maaliskuussa 2012. Näiden ponnistelujen tavoitteena oli arvioida WebGL-vedon mahdollisuuksia. Tämän seurauksena ensimmäinen JSON-muotoon perustuva glTF-muodon demo esiteltiin WebGl-tapaamisessa vuonna 2012. Useat yritykset omaksuivat muotoa ajoittain, mukaan lukien Cesium, 3D Tiles, Oculus, Microsoft, Archilogic ja muut.

glTF 2.0 julkaistiin 5. kesäkuuta 2017 Web3D 2017 -konferenssissa. On olemassa pitkä luettelo yrityksistä, jotka ottivat käyttöön glTF-tiedostomuodon sen jälkeen.

## GLTF-tiedostomuoto

glTF 2.0:n tiedostomuotospesifikaatiot ovat saatavilla {{HYPERLINKKI}} viitteeksi, ja niitä tulee tarkastella kaikissa glTF-tiedostomuodon tukemiseen liittyvissä toteutuksissa, jotka liittyvät lukemiseen/kirjoittamiseen.

glTF määrittelee resurssit JSON-tiedostoiksi, jotka tukevat ulkoista dataa. Se edustaa 3D-malleja seuraavien avulla:

* Full scene description contained in a JSON-formatted .glTF file that includes information about node hierarchy, materials, cameras, as well as descriptor information for meshes, animations and other constructs
* Binaaritiedostot (.bin), jotka sisältävät geometria- ja animaatiotietoja ja muita puskuripohjaisia tietoja

* Kuvatiedostot ([.jpg](/image/jpeg/), [.png](/image/png/)) pintakuvioita varten


Kaikki ulkoiset resurssit, kuten kuvat, tallennetaan ulkoisiin tiedostoihin, joihin viitataan URI:n kautta. Nämä URI:t tallennetaan GLB-säilön viereen tai upotetaan suoraan JSON:iin data-URI:ien avulla. Jokaisen kelvollisen glTF:n on määritettävä versionsa.

glTF on suunniteltu saavuttamaan pieni tiedostokoko, nopea lataus, täydellinen 3D-näkymän esitys ja laajennettavuus. Nämä ainutlaatuiset suunnittelutavoitteet ovat tärkeimmät syyt glTF-tiedostomuodon suosioon 3D-verkkotunnuksessa. Seuraavat ovat glTF-tiedostomuodon tukemat mime-tyypit eri tiedostotyypeille:

* .gltf-tiedostot käyttävät mallia/gltf+json

* .bin-tiedostot käyttävät sovellusta/octet-streamia

* Tekstuuritiedostot käyttävät virallista image/*-tyyppiä tietyn kuvamuodon perusteella. Yhteensopivuuden vuoksi nykyaikaisten verkkoselaimien kanssa tuetaan seuraavia kuvamuotoja: image/jpeg, image/png.


### JSON-koodaus

glTF asettaa seuraavat lisärajoitukset JSON-tiedostomuodolle

Asiakaspuolen toteutuksen yksinkertaistamiseksi glTF:llä on lisärajoituksia JSON-muodolle ja koodaukselle.

1. JSONin on käytettävä UTF-8-koodausta ilman tuoteluetteloa.
1. Kaikki tässä määritellyt merkkijonot (ominaisuuksien nimet, luettelot) käyttävät vain ASCII-merkkijoukkoa, ja ne on kirjoitettava pelkkänä tekstinä, esim. puskuri `\u0062\u0075\u0066\u0066\u0065\u0072` sijasta.
1. JSON-objektien nimien (avainten) on oltava yksilöllisiä, eli päällekkäiset avaimet eivät ole sallittuja.

### URI:t

Puskureihin ja kuvaresursseihin viitataan URI:iden kautta. Asiakkaiden on tuettava seuraavia kahta URI-tyyppiä.

**Datan URI:t:** Data-URI:t ovat RFC 2397:n määrittämiä, ja glTF käyttää niitä upottaakseen resursseja JSONiin.

**Relative URI Paths:** or path-noscheme as defined by RFC 3986, [Section 4.2](https://datatracker.ietf.org/doc/html/rfc3986#section-4.2) — without scheme, authority, or parameters. Reserved characters must be percent-encoded, per RFC 3986, [Section 2.2](https://datatracker.ietf.org/doc/html/rfc3986#section-2.2).

## Viitteet ##

* [glTF 2.0 -tiedot – Khronos](https://github.com/KhronosGroup/glTF)

* [glTF-tiedostomuoto - Wikipedia](https://en.wikipedia.org/wiki/GlTF)


