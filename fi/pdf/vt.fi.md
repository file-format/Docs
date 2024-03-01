{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PDF/VT-tiedostomuoto",
  "description": "Opi PDF/VT-tiedostomuodoista ja sovellusliittymistä, jotka voivat luoda ja avata PDF/VT-tiedostoja.",
  "linktitle": "PDF/VT",
  "menu": {
    "docs": {
      "parent": "pdf",
      "identifier": "pdf-v-fit"
}
},
  "lastmod": "2019-09-10"
}

# Mikä on PDF/VT? #

PDF/VT, joka julkaistiin standardina elokuussa 2010 nimellä [ISO 16612-2](https://www.iso.org/standard/46428.html), on suunniteltu mahdollistamaan muuttuvien asiakirjojen tulostaminen (VDP) useissa eri ympäristöissä. Standardi tekee muuttuvan tiedon ja transaktioiden tulostuksen standardin perustaksi. Muuttuvan datan tulostusta käytetään silloin, kun osa tiedoista on erilainen jokaiselle sisällön vastaanottajalle. Transaktiotulostus sisältää laskut, tiliotteet ja muut asiakirjat, joissa laskutustiedot yhdistetään markkinointitietoihin. Tämä johtaa yhdistelmään parannettua kuvien, tekstin ja muiden sisältötyyppien käsittelyä. PDF/VT mahdollistaa luotettavan ja dynaamisen sivujen hallinnan HVTO (High Volume Transactional Output) -tulostusdatalle käyttämällä asiakirjan osan metadata (DPM) -konseptia. PDF/VT-tiedostot voidaan avata Adobe Acrobat viewerissa ilman, että tarvitsee lisätä muita komponentteja.

## Asiakirjan osahierarkia ##

Asiakirjan osan (DPart) hierarkia on kuin asiakirjan osan solmujen puurakenne, joka perustuu asiakirjan kaikkiin sivuihin. Tämän puun elementtejä kutsutaan DPart-solmuiksi. Jokainen sisäinen solmu sisältää muita DPart-solmuja ja jokainen lehtisolmu määrittää yhden tai useamman sivun vastaanottajalle. Pohjimmiltaan DPart-hierarkia määrittää PDF/VT-tiedostossa olevien asiakirjojen tai asiakirjojen osien järjestyksen ja suhteen. DPart-solmujen puurakenne edustaa PDF/VT-dokumentin sisäistä sisältöä helposti, koska se voi sisältää aliasiakirjoja useille vastaanottajille ja jokainen asiakirjan osa vastaa yhden vastaanottajan sivuja. DPart-hierarkia vaaditaan PDF/VT-tiedostoissa.

## Asiakirjan osan metatiedot (DPM) ##

Document Part Metadata (DPM) liittyy kuhunkin solmuun asiakirjan osahierarkiassa, ja sitä voidaan käyttää tiedon välittämiseen tietyn vastaanottajan aliasiakirjasta ja sen osista. Erityisesti DPM voi sisältää tietoa ominaisuuksista tai tietoja vastaanottajista koodatussa muodossa.

## Vaatimustenmukaisuustasot ##

PDF/VT on myönnetty seuraaville kolmelle vaatimustenmukaisuustasolle. Nämä kaikki perustuvat versioon [PDF](/pdf/) 1.6.

* `PDF/VT-1` - Se perustuu PDF/X-4:ään ja sisältää kaikki PDF-dokumentin hahmontamiseen tarvittavat resurssit.

* `PDF/VT-2` - Suunniteltu usean tiedoston vaihtoon, PDF/VT-2-asiakirjat voivat viitata ulkoisiin tulostustarkoituksiin, ulkoiseen sisältöön tai molempiin. PDF/VT-dokumenttia ja kaikkia siihen viitattuja PDF-tiedostoja ja ulkoisia tulostustavoitteita kutsutaan yhteisesti PDF/VT-2-tiedostojoukoksi. Acrobat 9 ja tukevat tätä ominaisuutta.

* `PDF/VT-2s` - Tukee PDF/VT-2 suoratoistoa. Tämä mahdollistaa segmentoitujen dataosien käsittelyn.


## Viitteet ##

* [PDF/VT – Wikipedia](https://en.wikipedia.org/wiki/PDF/VT)

* [ISO 16612-2 Graphic Technology](https://www.iso.org/standard/46428.html)


