{
  "date": "2020-03-16",
  "keywords": [
"DWG",
"Tiedosto muoto",
"CAD",
"Avata",
"Luoda"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Opi DWG-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata DWG-tiedostoja.",
  "title": "DWG tiedostomuoto",
  "linktitle": "DWG",
  "menu": {
    "docs": {
      "parent": "cad",
      "identifier": "cad-dw-fig"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on DWG-tiedosto?

DWG-laajennuksella varustetut tiedostot edustavat patentoituja binääritiedostoja, joita käytetään 2D- ja 3D-suunnittelutietojen sisältämiseen. Kuten DXF, jotka ovat ASCII-tiedostoja, DWG edustaa CAD-piirustusten (Computer Aided Design) binaaritiedostomuotoa. Se sisältää vektorikuvan ja metatiedot CAD-tiedostojen sisällön esittämiseksi. DWG-tiedostojen katseluun Windows-käyttöjärjestelmässä on ilmaisia katseluohjelmia, kuten Autodeskin ilmainen DWG TrueView. On myös muita kolmannen osapuolen sovelluksia, jotka tukevat DWG-tiedostojen saavuttamista. DWG-tiedostot sisältävät käyttäjän luomia tietoja ja sisältävät:

* Suunnittelut

* Geometriset tiedot

* Kartat ja valokuvat


Arkkitehdit, insinöörit ja suunnittelijat käyttävät tätä muotoa laajasti erilaisiin suunnittelutarkoituksiin.

## Lyhyt historia ##

DWG file format has evolved with the time since its formal introduction in 1982. Lyhyt katsaus menneisiin tapahtumiin historian näkökulmasta on seuraava.

**1982:** Autodesk lisensoi DWG-tiedostomuodon, jonka Mike Riddle kehitti vuonna 1970, AutoCADin perustaksi.

**1998:** AutoCAD R14.01:n julkaisun myötä Autodesk lisäsi tiedostojen vahvistuksen DWGCHECK-nimisellä toiminnolla, joka upotti salatun tarkistussumman ja tuotekoodin, jota Autodesk kutsuu nimellä WaterMark, ohjelman luomiin DWG-tiedostoihin.

**2006:** Autodesk muokkasi AutoCAD 2007:ää sisällyttämällä TrustedDWG-teknologian tekstimerkkijonoon Autodesk DWG. Tämä tiedosto on Trusted DWG, jonka Autodesk-sovellus tai Autodeskin lisensoitu sovellus on viimeksi tallentanut DWG-tiedostoihin. Tämän tarkoituksena oli auttaa Autodesk-ohjelmiston käyttäjiä varmistamaan, että nämä tiedostot on luotu Autodesk- tai RealDWG-sovelluksella, mikä varmasti auttaa vähentämään yhteensopivuusriskiä.

## Tiedostorakenne ##

DWG on ollut yksi laajalti käytetyistä tiedostomuodoista useissa sovelluksissa, ja sillä on vankka tiedostorakenne. Koska DWG on binääritiedostomuoto, se ei ole ihmisen luettavissa kuten tavallinen ASCII [DXF](/cad/dxf/) -tiedostomuoto. DWG-tiedostot sisältävät yleensä tietoja kuvan koordinaateista ja kaikista niihin liittyvistä metatiedoista. OpenDesignin ladattavissa on täydellinen [specifications](https://www.opendesign.com/files/guestdownloads/OpenDesign_Specification_for_.dwg_files.pdf) DWG-tiedostomuodosta. DWG-tiedostomuodon tiedostorakenne on tiivistetty seuraavasti.

**Otsikko**: Tiedoston otsikko koostuu DWG-otsikkomuuttujista ja tiedoista CRC:stä (Cyclic Redundancy Check), jota käytetään virheiden havaitsemiseen. Jokainen alajakso on erikoistunut vektori, jossa eri pituisia bittejä käytetään edustamaan erilaisia etikettejä. Esimerkiksi DWG Header -muuttujan ensimmäiset 6 bittiä tarkoittavat versiomerkkijonoa.

**Luokkien määritelmät:** DWG-tiedosto voi sisältää useita luokkia tietystä .dwg-tiedoston tarkoituksesta riippuen. Tiedot, kuten luokan metatietojen koko luokan tietoalueen, luokan numero ja tarkistussumma muiden lisäksi.

**Malli**: Tämä on valinnainen, ja R15- ja R15-versioissa tämä osio on Object Free Space -osion alapuolella.

**Täyte**: Metatietoihin liitetään pääte ja jälkiliite tietyllä tavumäärällä, minkä ansiosta vanhemmat AutoCAD-ohjelmistoversiot ovat edelleen yhteensopivia uuden DWG-tiedostomuodon kanssa.

**Kuvatiedot**: Tämän osion metatiedot riippuvat tietystä .dwg-tyypistä. R14- ja R15-käyttäjille tämä osio on valinnainen.

**Objektidata**: Objektitieto koostuu täydellisestä luettelosta taulukkokokonaisuuksista, sanakirjamerkinnöistä jne., jotka vastaavat olemassa olevaa objektiluetteloa.

**Objektikartta**: Jokaisen kohteen sijainti tiedostossa määritetään tässä tiedoston osassa. Suurin osa tämän osion metatiedoista on tiedostokahvoja, joilla on rooli objektin tunnistamisessa ja uudelleenhahmontamisessa.

**Object Free Space**: Tämä osio on valinnainen kaikille käyttäjille

**Toinen otsikko**: kopio tiedoston otsikkoosion DWG-tiedoston lopussa

## Viitteet ##

* [DWG-tiedostomuodon tekniset tiedot](https://www.opendesign.com/files/guestdownloads/OpenDesign_Specification_for_.dwg_files.pdf)

* [DWG-tiedoston määritykset](https://www.scan2cad.com/blog/dwg/file-spec/)

* [DWG - Wikipedia](https://en.wikipedia.org/wiki/.dwg)


