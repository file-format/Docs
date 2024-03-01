{
  "date": "2022-05-09",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Opi PYC-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata PYC-tiedostoja.",
  "title": "PYC-tiedostomuoto - Python-käännetty tiedosto",
  "linktitle": "PYC",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-py-fic"
}
},
  "lastmod": "2022-05-09"
}

## Mikä on PYC-tiedosto?

PYC-tiedosto on Python-ohjelmointikielellä kirjoitetusta lähdekoodista luotu käännöstiedosto. Kun PY-tiedostoa ajetaan Python-tulkin avulla, se muunnetaan tavukoodiksi suorittamista varten. Samanaikaisesti käännetty tavukoodi tallennetaan myös .pyc-tiedostona, jotta sitä voidaan tarvittaessa käyttää uudelleen välimuistista myöhemmin.

## PYC-tiedostomuodon rakenne

PYC-tiedostot ovat tavukoodia, eivätkä niiden tiedostomuotomääritykset ole saatavilla julkisesti. Joidenkin lähteiden tutkimukset kuitenkin osoittavat, että {{HYPERLINKKI}} koostuu:

 * Nelitavuinen maaginen numero - Yksinkertaisesti kaksi tavua, jotka muuttuvat jokaisella järjestyskoodin muutoksella, ja sitten kaksi tavua 0d0a.
 * Nelitavuinen muokkausaikaleima - .pyc-tiedoston luoneen lähdetiedoston Unix-muokkauksen aikaleima, jotta se voidaan kääntää uudelleen, jos lähde muuttuu.
 * Järjestetty koodiobjekti - koodiobjektin marshal.dump tulos, joka on tulos lähdetiedoston kääntämisestä.

## UKK

1. **Miten PYC-tiedosto luodaan?** PYC-tiedosto luodaan, kun Python-lähdekoodi käännetään Python-tulkin avulla. Käännetty koodi tallennetaan sitten PYC-tiedostoon.

1. **Onko PYC nopeampi kuin py?** PYC-tiedostot tallennetaan sen jälkeen, kun python-lähdekoodi on käännetty. Koska ne on jo tulkittu, nämä tiedostot ovat nopeampia kuin .py-tiedostot.

1. **Mitä eroa on py- ja pyc-tiedostoilla?** PY-tiedostot sisältävät ohjelman Python-lähdekooditiedoston, kun taas .pyc-tiedostot sisältävät sovelluksen tulkitun tavukoodin.

1. **Onko PYC binääritiedosto?** Kyllä, PYC-tiedosto on binääritiedosto, joka sisältää 4-tavuisen maagisen numeron, 4-tavuisen muokkausaikaleiman ja järjestetyn koodiobjektin.

1. **Voimmeko muuntaa .pyc:n .py:ksi?** Kyllä, pyc-tiedostot voidaan muuntaa py:ksi. Decompileri, kuten Decompyle++, voidaan käyttää kääntämään käännetty Python-tavukoodi takaisin kelvolliseksi ja ihmisen luettavaksi Python-lähdekoodiksi.

## Viitteet

* [.pyc-tiedostojen rakenne](https://nedbatchelder.com/blog/200804/the_structure_of_pyc_files.html)


