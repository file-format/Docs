{
  "date": "2019-10-11",
  "keywords": [
"chm",
"chm tiedosto",
"chm tiedostomuoto",
"chm tiedostotyyppi",
"tiedosto",
"tyyppi",
"mikä on chm-tiedosto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CHM - Käännetty HTML-ohjetiedostomuoto",
  "description": "Tutustu CHM-tiedostoon ja sovellusliittymiin, jotka voivat luoda ja avata niitä.",
  "linktitle": "CHM",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-ch-fim"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on CHM-tiedosto?

CHM-tiedostomuoto edustaa Microsoftin **[HTML](/web/html/)** ohjetiedostoa, joka koostuu kokoelmasta HTML-sivuja. Se tarjoaa hakemiston, jonka avulla pääset nopeasti käsiksi aiheisiin ja navigoi ohjeasiakirjan eri osiin. CHM-tiedoston sisältöä voidaan etsiä tarjotun hakuvaihtoehdon avulla. CHM on Microsoftin patentoitu online-ohjetiedostomuoto, jota käytetään usein ohjelmistojen dokumentaatioon. Lisäksi sitä käytetään useissa muissa sovelluksissa, kuten koulutusoppaissa, interaktiivisissa kirjoissa ja sähköisissä uutiskirjeissä. Useimmat nykyaikaiset Microsoftin kehitysympäristöt tukevat CHM-dokumentaation luomista sovelluksessa olevista tiedoista.

CHM-tiedostomuodon ainutlaatuinen kyky toteuttaa yhdistetty sisällysluettelo ja hakemisto tekee siitä eron muista tavallisista HTML-sivuista. Luotu CHM-tiedosto on kooltaan suhteellisen pieni, ja siksi sitä voidaan helposti jakaa ohjelmistopakettien kanssa. Ohjeen kirjoitustyökalu, HTML Help Workshop, tarjoaa helppokäyttöisen järjestelmän ohjeprojektien ja niihin liittyvien tiedostojen luomiseen ja hallintaan. CHM-tiedostot voivat sisältää tekstiä, kuvia ja hyperlinkkejä; katseltavissa Web-selaimessa; Windows ja muut ohjelmat käyttävät sitä online-apuratkaisuna.

## CHM-tiedostomuoto

Luodun CHM-tiedoston lopullinen muoto riippuu siitä, kuinka ohjejärjestelmä on suunniteltu ja onko se tarkoitettu sovellukselle vai verkkosivustolle. CHM-tiedosto tukee tietojen pakkaamista LZX-pakkauksella pakattujen HTML-tiedostojen luomiseksi. Siinä on sisäänrakennettu hakukone nopeaa sisällönhakua varten sekä mahdollisuus yhdistää useita .CHM-tiedostoja. CHM-tiedosto koostuu joukosta HTML-tiedostoja, linkitetystä sisällysluettelosta ja hakemistotiedostosta.

### HTML-tiedostot

Luotpa ohjeaiheita jakelua varten ohjelman avulla tai Webissä, kirjoittamasi asiakirjat luodaan käyttämällä erityistä muotoilukieltä, joka tunnetaan nimellä Hypertext Markup Language (HTML). HTML-aihetiedostoilla on .htm- tai .html-tiedostotunniste.

Vaikka jokainen kirjoittamasi ohjeaihe tai Web-sivu näyttää olevan asiakirja, jossa on tekstiä, grafiikkaa tai animoituja kuvia, .htm-tiedostot ovat itse asiassa tekstidokumentteja, joissa on erityiset HTML-muotoilukoodit. Nämä koodit, joita kutsutaan tunnisteiksi, kertovat selaimelle, kuinka kukin sivu näytetään. Vain aiheessa tai Web-sivulla näkyvä teksti on todellisuudessa .htm-tiedostossa. Kaikki grafiikat, äänet, animoidut kuvat tai muut näkyvät elementit ovat erillisiä tiedostoja, joihin HTML-tiedostosi osoittaa. Selain kopioi tai lataa grafiikkaa, ääniä tai muita elementtejä, kun se näkee tunnisteet, jotka kehottavat sitä tekemään niin.

### Sisällysluettelo (TOC)
Ohjeen sisällysluettelo (.hhc) on HTML-tiedosto, joka sisältää sisällysluettelosi aiheiden otsikot. Kun käyttäjä avaa käännetyn ohjetiedoston (tai Web-sivun) sisällysluettelon ja napsauttaa aiheen otsikkoa, siihen liittyvä HTML-tiedosto avautuu.

### Hakemistotiedosto
Hakemistotiedosto (.hhk) on HTML-tiedosto, joka sisältää hakemistosi hakemistomerkinnät (avainsanat). Kun käyttäjä avaa hakemiston käännetyssä ohjetiedostossa tai Web-sivulla ja napsauttaa avainsanaa, avainsanaan liittyvä HTML-tiedosto avautuu.

## HTML-ohjekomponentit

HTML Help koostuu useista osista. Näitä ovat seuraavat:

* `HTML Help Workshop`: a help authoring tool with an easy-to-use graphical interface for creating project files, HTML topic files, contents files, index files, and everything else you need to put together an online help system or Web site.
* `HTML Help ActiveX -ohjaus`: pieni, modulaarinen ohjelma, jota käytetään lisäämään ohjeen navigointi ja toissijainen ikkunatoiminto HTML-tiedostoon.

* "HTML Help Viewer": täysin toimiva ja muokattavissa oleva kolmiruutuinen ikkuna, jossa online-ohjeaiheita voi näkyä.

* "Microsoft HTML Help Image Editor": online-grafiikkatyökalu kuvakaappausten luomiseen; ja kuvatiedostojen muuntamiseen, muokkaamiseen ja katseluun.

* `HTML Help Java Applet`: pieni, Java-pohjainen ohjelma, jota voidaan käyttää ActiveX-komponentin sijasta ohjenavigoinnin lisäämiseen HTML-tiedostoon.

* "HTML-ohjeen suoritettava ohjelma": ohjelma, joka näyttää ja suorittaa ohjeen, kun napsautat käännettyä ohjetiedostoa.

* `HTML Help compiler`: ohjelma, joka kokoaa projektin, sisällön, hakemiston, aiheen ja muut tiedostot käännetyksi ohjetiedostoksi.

* `The HTML Help Authoring Guide`: an online guide designed to assist help authors in using HTML Help to design a help system. The guide also contains a complete HTML Help reference for developers and an HTML tag reference for authors.

## Viitteet

* [Microsoft HTML Help](https://learn.microsoft.com/en-us/previous-versions/windows/desktop/htmlhelp/microsoft-html-help-1-4-sdk)

* [Microsoft Compiled HTML Help](https://en.wikipedia.org/wiki/Microsoft_Compiled_HTML_Help)


