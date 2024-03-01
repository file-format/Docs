{
  "date" : "2024-01-25",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "FIG File - MATLAB Figure File - Mikä on .fig-tiedosto ja kuinka avata se?",
  "description" : "Tutustu MATLAB-kuvatiedostoon ja sen avaamiseen.",
  "linktitle" : "FIG",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-fig-fi",
      "parent" : "data"
}
},
  "lastmod" : "2024-01-25"
}

## Mikä on FIG-tiedosto?

FIG-tiedosto on erityinen tiedosto, joka sisältää MATLAB-ohjelmalla tehtyä kuvaa tai kuvaajaa, jota käytetään laskennan tekemiseen ja tietojen analysointiin. Tämä tiedosto sisältää tietoja kuvista tai kaavioista, jotka MATLAB piirtää auttaakseen ihmisiä näkemään ja ymmärtämään tietoja paremmin. Se on kuin kontti, joka säilyttää kaikki kaavioiden tiedot.

.FIG on oletusarvoinen MATLAB-kuvatiedostomuoto. Se tallentaa täydellisen kuvan, mukaan lukien kaikki akselit, tarrat ja asetukset. Voit tallentaa hahmon tässä muodossa käyttämällä `savefig`-toimintoa:

## Tietoja MATLAB Softwaresta - FIG-tiedoston avaaminen

MATLAB, lyhenne sanoista Matrix Laboratory, on tehokas ohjelmointi- ja numeerinen laskentaympäristö, jonka on kehittänyt The MathWorks. Sitä käytetään laajalti tehtäviin, kuten tietojen analysointiin, matemaattiseen mallinnukseen, algoritmien kehittämiseen ja tieteelliseen laskemiseen. MATLABin avulla käyttäjät voivat käsitellä matriiseja, piirtää kaavioita, toteuttaa algoritmeja ja luoda käyttöliittymiä, mikä tekee siitä monipuolisen työkalun insinööreille, tutkijoille ja tutkijoille eri tieteenaloilla. Sen intuitiivinen syntaksi ja laaja funktiokirjasto tekevät siitä suositun vaihtoehdon monimutkaisten matemaattisten ongelmien ratkaisemiseen ja simulaatioiden suorittamiseen.

## Kuinka luoda FIG-tiedosto MATLABilla?

Voit tehdä FIG-tiedoston MATLABilla seuraavasti:

1.  **Valitse tietosi:** Valitse muuttuja, jolle haluat luoda kuvaajan, MATLABin Työtila-ruudusta.
    
2.  **Valitse juonityyppi:** Siirry TONTIT-välilehteen ja napsauta haluamaasi juonityyppiä.
    
3.  **Tallenna kuvaaja FIG-tiedostona:**
    
- Siirry Tiedosto-valikkoon.
- Valitse joko Tallenna tai Tallenna nimellä.
- Anna tiedostollesi nimi ja päätä, minne haluat tallentaa sen.
- Luo FIG-tiedosto napsauttamalla Tallenna.

Voit myös tallentaa sen FIG-tiedostona käyttämällä savefig-toimintoa. Valitse tiedostonimi ja anna tunniste '.fig':

## Kuinka avata FIG-tiedosto?

Avaa FIG-tiedosto MATLABissa seuraavasti:

1.  **Avaa MATLAB:** Käynnistä MATLAB tietokoneellasi.
    
2.  **Siirry PLOTS-välilehdelle:** Napsauta tonttia PLOTS-välilehdellä ja valitse haluamasi juonityyppi.
    
3.  **Avaa FIG-tiedosto:**
    
- Siirry Tiedosto-valikkoon.
- Valitse Avaa.
- Siirry sijaintiin, johon FIG-tiedosto on tallennettu, valitse se ja napsauta Avaa.

Vaihtoehtoisesti voit käyttää `openfig`-toimintoa MATLABissa:

## Viitteet
* [MATLAB](https://en.wikipedia.org/wiki/MATLAB)


