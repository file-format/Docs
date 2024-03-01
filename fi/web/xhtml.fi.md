{
  "date": "2019-10-11",
  "keywords": [
"xhtml",
"Tiedosto",
"Laajennus",
"Tiedosto muoto",
"Tiedostopääte",
"laajennettava html"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "XHTML - Extensible Hypertext Markup Language File Format",
  "description": "Tutustu XHTML-tiedostomuotoon ja sovellusliittymiin, jotka voivat luoda ja avata XHTML-tiedostoja.",
  "linktitle": "XHTML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-xhtm-fil"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on XHTML-tiedosto?

The XHTML is a text based file format with markup in the XML, using a reformulation of HTML 4.0. Nämä tiedostot sopivat hyvin avattavaksi tai katseltavaksi verkkoselaimessa. XHTML suunniteltiin jäsennellymmäksi, vähemmän komentosarjaksi, yleiseksi; käyttämällä kaikkia olemassa olevia XML-ominaisuuksia ja enemmän laiteriippumattomia. XHTML tarjoaa yleisesti hyödyllisen joukon elementtejä ja attribuutteja, laajennusvaihtoehtoja yhdessä tyylisivujen kanssa. Attribuutteja käytetään metatietomääritekokoelmasta. XHTML tarjoaa joustavuutta ja helppokäyttöisyyttä alistamalla kaikki **[HTML](/web/html/)** esityselementit tyylisivuille. Tyylisivut ovat monipuolisempia kuin nämä esittelyelementit. World Wide Web Consortium (W3C) kehittää dynaamisesti HTML 4.01:n, HTML5:n ja XHTML:n määrityksiä.

## XHTML-tiedostomuodon lyhyt historia

The history of XHTML starts with a draft document released in December 1998 by the World Wide Web Consortium. This document refers the "Reformulating HTML in XML", a specification called XHTML 1.0.This new specification reformulated HTML in XML using the existing elements or attributes. In May 1999, W3 Consortium declared that HTML 4.0 had been re-formed as an XML application. i.e. XHTML. In January 26, 2000, the first specification that defines XHTML 1.0 was released by W3C. Further in May 31, 2001, the W3C announced XHTML as an independent language and started working on development of HTML 5.0. Vuonna 2005 kuitenkin perustettiin työryhmä (WHATWG), jonka tavoitteena oli parantaa tavallista HTML:ää XHTML:stä riippumatta. WHATWG alkoi lopulta työstää HTML5:tä rinnakkain XHTML 2:n kanssa.

## XHTML-tiedostomuoto

XHTML is a format, which is a collection of different document types and modules that mimic, categorize, and extend HTML 4. XHTML-tiedostot ovat XML-pohjaisia, ja ne on tarkoitettu toimimaan XML-pohjaisten käyttäjäagenttien kanssa. XHTML-tiedostot ovat XML-yhteensopivia. Tavallisia XML-työkaluja käytetään XHTML-tiedostojen katseluun, muokkaamiseen ja validointiin. HTML Document Object Model tai XML Document Object Model [DOM] riippuvat sovellukset voivat toimia XHTML-dokumenttien kautta. Valitsemalla XHTML:n tänään sisällönkehittäjät voivat nauttia kaikista XML:n eduista huolehtimatta sisältönsä yhteensopivuudesta eteenpäin tai taaksepäin.

Joukko toisiinsa liittyviä elementtejä rakentaa moduulin XHTML-kielellä. Lomake- tai taulukkomoduuli voi sisältää erilaisia lomake- tai taulukkoelementtejä, jotka voidaan näyttää verkkosivulla. Modularisoinnin tarkoituksena oli eristää HTML-elementtejä lukuisten linkitettävien elementtien ryhmiksi. Jotta sisällön kehittäjät voivat hyödyntää moduulien valintaa erityyppisille laitteille. Lisäksi moduulien avulla käyttäjäagentit voivat valita elementtejä menettämättä yhdenmukaisuutta XHTML-standardin kanssa. XHTML:n jäsennysvaatimukset ovat samat kuin XML:n, kun taas HTML harjoittelee omiaan.

### Asiakirjan vaatimustenmukaisuus

XHTML2 offer specifications conforming XHTML 1.0 documents, which uses the namespaces elements and attributes from the XML and XHTML 1.0. Asiakirjan vaatimustenmukaisuutta on kahta tyyppiä.

Strictly Conforming Document on XML-pohjainen, joka tarvitsee vain tässä määrittelyssä määritellyt pakolliset palvelut. XHTML-tiedostojen on täytettävä seuraavat kriteerit:

* Tiedoston on oltava DTD:ssä ja liitteessä B määriteltyjen rajoitusten mukainen.

* Tiedoston peruselementin tulee olla html.

* Tiedoston peruselementin tulee sisältää XHTML-nimiavaruuden määrittely, ja se tulee määritellä seuraavasti:


```
http://www.w3.org/1999/xhtml.
```

* Peruselementti voidaan kirjoittaa seuraavasti:


```
<html xmlns#"http://www.w3.org/1999/xhtml" xml:lang#"en" lang#"en">
```

Peruselementtiä aikaisemmin on ilmoitettava DOCTYPE, jonka julkisen tunnisteen tulee viitata johonkin kolmesta asiakirjatyypin määrittelystä (DTD). Järjestelmän tunnistetta voidaan muokata nykyisten järjestelmäkäytäntöjen mukaiseksi.

```
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"  "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
 "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Frameset//EN"
 "http://www.w3.org/TR/xhtml1/DTD/xhtml1-frameset.dtd">
```

XML-dokumenteissa ei ole tarpeen määrittää XML-määrityksiä kaikissa dokumenteissa. sisällön kehittäjät kuitenkin houkuttelevat käyttämään XML-määrityksiä kaikissa XHTML-dokumenteissaan. Nämä ilmoitukset ovat pakollisia joko silloin, kun asiakirjan merkkikoodaus poikkeaa UTF-8 /16:sta tai kun hallitseva protokolla ei ole määrittänyt koodausta. Seuraava esimerkki XHTML-dokumentista määrittelee XML-ilmoitukset

```
<!DOCTYPE html
     PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
    "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns#"http://www.w3.org/1999/xhtml" xml:lang#"en" lang#"en">
  <head>
    <title>Public Property</title>
  </head>
  <body>
    <p>changed to <a href#"http://sample.com/">sample.com</a>.</p>
  </body>
</html>
```

Vaatimustenmukaisen käyttäjäagentin on täytettävä seuraavat säännöt:

* XHTML-asiakirjan jäsennyksen ja arvioinnin suorittaa käyttäjäagentti, joka varmistaa sen yhdenmukaisuuden XML 1.0 -suosituksen kanssa.

* Jos käyttäjäagentti vahvistetaan, sen on tarkistettava dokumenttien kelpoisuus viitatuille DTD:ille XML:n mukaan. Kun käyttäjäagentti käsittelee XHTML-tiedoston yleisenä XML-muodossa, ID-tyypin ominaisuudet kuitataan fragmenttitunnisteiksi.


Jos käyttäjäagentti törmää tuntemattomaan elementtiin, seuraavat ovat pakolliset kriteerit, jotka sen on täytettävä

* käsittelee tuntemattoman elementin sisältöä

* ohita attribuutti ja sen arvo

* Käytä oletusarvona annettua määritteen arvoa.


Kun käyttäjäagentti törmää entiteettiviittausilmoitukseen, jota ei ole käsitelty aikaisemmin, se tulee käsitellä merkkinä (alkaen &-merkillä ja päättyen puolipisteeseen). Sisällönkäsittelyn aikana merkit tai merkkikokonaisuuksien viittaukset, jotka käyttäjäagentti voi ennakoida, mutta jotka eivät ole hahmonnettavissa, voivat käyttää mitä tahansa vaihtoehtoista hahmonnusta, joka antaa samanlaisen merkityksen. Tällöin dokumentti on esitettävä tavalla, joka tekee käyttäjälle selväksi, että renderöintiprosessi ei ole ollut normaali. Välilyöntien käsittelyä varten käyttäjäagentin on etsittävä määritelmää CSS-merkeistä [CSS2].

## XHTML taaksepäin yhteensopivuus

The back ward compatibility of XHTML 1.  dokumentit tuntee hyvin HTML 4 -käyttäjäagentit, jos asianmukaisia sääntöjä noudatetaan. XHTML 1.1 on täysin yhteensopiva rubiinimerkintöjä lukuun ottamatta, vaikka HTML 4 -selaimet yleensä ohittavat ne. XHTML 2.0 on verrattain vähemmän yhteensopiva, mutta ongelmaa on kuitenkin jossain määrin ratkaistu komentosarjojen avulla.

## Viitteet

* [XHTML:n historia: 1990-luvulta nykypäivään](https://www.brighthub.com/internet/web-development/articles/109224.aspx)


