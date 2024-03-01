{
  "date": "2019-10-11",
  "keywords": [
"xoml",
"Tiedosto",
"Laajennus",
"Tiedosto muoto",
"Tiedostopääte",
"Extensible Object Markup Language"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "XOML - Windowsin työnkulun tiedostomuoto",
  "description": "Opi XOML-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata XOML-tiedostoja.",
  "linktitle": "XOML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-xom-fil"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on XOML-tiedosto?

XOML on lyhenne sanoista Extensible Object Markup Language ja se on Windows Workflow Foundationin työnkulkuobjektien serialisointimuoto. Perustuu **[XAML](/web/xaml/)**, sitä käytetään enimmäkseen käyttöliittymien luomiseen pelkällä **[XML](/web/xml/)**. Näitä käytetään ilmoittamaan käyttöliittymän työnkulku, ja ne käännetään yhdessä toteutuslogiikan sisältävän erillisen tiedoston kanssa. Se sisältää puupohjaisen rakenteen, joka määrittää juurityönkulun solmun, sisäkkäisiä alielementtejä ja upotettuja koodisegmenttejä. Kun Visual Studio for .NET -sovelluksella luodaan uusi työnkulku, voit valita, onko se Code-muodossa vai Code Separated -muodossa. Jos valitset myöhemmän, IDE luo kaksi tiedostoa puolestasi; yksi XOML-muodossa (joka koostuu työnkulun asettelusta ja asetuksista), ja toinen on [.CS](/programming/cs/)/[.VB](/programming/vb/)-muodossa, jossa ohjelmointikoodi sijaitsee.

