{
  "date": "2019-10-11",
  "keywords": [
"rtf-tiedosto",
"rtf tiedostomuoto",
"mikä on rtf-tiedosto",
"tiedosto",
"rtf esimerkki",
"rtf tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "RTF - Rich Text Format",
  "description": "Opi RTF-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata RTF-tiedostoja.",
  "linktitle": "RTF",
  "menu": {
    "docs": {
      "parent": "word-processing",
      "identifier": "word-processing-rt-fif"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on RTF-tiedosto?

Microsoftin esittelemä ja dokumentoima Rich Text Format (**RTF**) edustaa tapaa koodata muotoiltua tekstiä ja grafiikkaa sovelluksissa käytettäväksi. Muoto mahdollistaa eri alustojen välisen asiakirjojen vaihdon muiden Microsoft-tuotteiden kanssa, mikä palvelee yhteentoimivuuden tarkoitusta. Tämä ominaisuus tekee siitä standardin tiedonsiirrossa tekstinkäsittelyohjelmistojen välillä, ja siten sisältöä voidaan siirtää käyttöjärjestelmästä toiseen menettämättä asiakirjan muotoilua. Tiedostomuotomääritykset ovat Microsoftin saatavilla julkisesti download, ja niihin voidaan viitata kehittäjän näkökulmasta.

## RTF-tiedostomuodon ## lyhyt historia

RTF file format has underwent several revisions since its publication. Its official version for read/write was published as part of Microsoft Word 3.0 for Macintosh with version 1.0 specifications. The final version of specifications, 1.9.1 was published by Microsoft in Mar 2008. Tämän jälkeen vaatimuksiin ei tehdä enää parannuksia. Tällä hetkellä lähes kaikissa käyttöjärjestelmissä on enemmän ominaisuuksia täynnä sovelluksia, jotka ovat minimoineet/poistaneet RTF-tiedostomuodon käytön.

## RTF-tiedostomuodon tekniset tiedot ##

RTF serves as a standard of data transfer between word processing software and transfer of content from one operating system to another. This is achieved using control words that were introduced by Microsoft Office Word up through 2007. Vakio-RTF-tiedosto koostuu ASCII-tiedostosta, joka edustaa rich-tekstiä, ja muita kuin ASCII-merkkejä, jotka muunnetaan sopiviksi koodiarvoiksi. Wordin uudemmat versiot voivat lukea aiemmilla versioilla luotuja RTF-tiedostoja, kun taas vanhemmat versiot jättävät huomioimatta ohjaussanat ja ryhmät, joita he eivät ymmärrä.

### RTF:n perusteiden ymmärtäminen ###

RTF-tiedostot käyttävät 7-bittistä ASCII-tekstiä, joka koostuu:

* ohjaussanat

* ohjaussymbolit ja

* ryhmät.


Nämä toimivat rakennuspalikoina RTF-tietojen esittämiselle ymmärrettävänä tekstinä ja merkkikoodauksena.

#### Ohjaussana ####

Nämä edustavat erityisesti muotoiltuja komentoja, joita käytetään merkitsemään merkkejä näyttöä varten, ja ne eivät saa olla pidempiä kuin 32 kirjainta. Ohjaussana määritellään seuraavasti:

\<ASCII Letter Sequence> //<//Delimiter//> //

Jokainen ohjaussana erottelee isot ja pienet kirjaimet ja alkaa kenoviivalla. ASCII-kirjainsarja voi sisältää ASCII-aakkosia (a–z ja A–Z). The<Delimite> merkitsee ohjaussanan nimen lopun ja voi olla jokin seuraavista:

* Tila. Tätä käytetään vain ohjaussanan rajaamiseen, ja se jätetään huomiotta myöhemmässä käsittelyssä.

* Numeerinen numero tai ASCII-miinusmerkki, joka osoittaa, että numeerinen parametri liittyy ohjaussanaan. Seuraava digitaalinen sekvenssi rajataan sitten millä tahansa muulla merkillä kuin ASCII-numerolla (yleensä toinen ohjaussana, joka alkaa kenoviivalla). Parametri voi olla positiivinen tai negatiivinen desimaaliluku. Numeron arvojen alue on nimellisesti –32768 - 32767, eli etumerkillinen 16-bittinen kokonaisluku. Pieni määrä ohjaussanoja saa arvot välillä‌ -2 147 483 648 - 2 147 483 647 (32-bittinen etumerkillinen kokonaisluku). Näitä ohjaussanoja ovat **\binN**, **\revdttmN//**, **\rsidN** liittyvät ohjaussanat ja joitain kuvaominaisuuksia, kuten **\bliptagN**. Tässä **N** tarkoittaa numeerista parametria. RTF-jäsentimen on sallittava enintään 10 numeroa, joita edeltää valinnaisesti miinusmerkki. Jos erotin on välilyönti, se hylätään, eli sitä ei sisällytetä myöhempään käsittelyyn.

* Mikä tahansa muu merkki kuin kirjain tai numero. Tässä tapauksessa rajaava merkki päättää ohjaussanan eikä ole osa ohjaussanaa. Kuten kenoviiva "\", mikä tarkoittaa, että seuraava ohjaussana tai ohjaussymboli seuraa.


#### Ohjaussymboli ####

Ohjaussymboli edustaa erityistä tapahtumaa, jolla on erityinen merkitys sen sisällöstä riippuen. Se koostuu kenoviivasta, jota seuraa erikoismerkki (ei-aakkosmerkki), eikä siinä ole erottimia.

#### Ryhmä ####

Ryhmä voi koostua tekstistä, ohjaussanoista tai ohjaussymboleista aaltosulkeissa (**{ }**). Aloitusalkasulku (**{** ) osoittaa ryhmän alkua ja sulkeva aaltosulu (**}**) osoittaa ryhmän päättymisen. Jokainen ryhmä määrittelee tekstin, johon ryhmä vaikuttaa, ja kyseisen tekstin eri attribuutit.

### RTF-tiedostorakenne ###

RTF-tiedostolla on seuraava vakiosyntaksi:

Microsoftin esittelemä ja dokumentoima Rich Text Format (**RTF**) edustaa tapaa koodata muotoiltua tekstiä ja grafiikkaa sovelluksissa käytettäväksi. Muoto mahdollistaa eri alustojen välisen asiakirjojen vaihdon muiden Microsoft-tuotteiden kanssa, mikä palvelee yhteentoimivuuden tarkoitusta. Tämä ominaisuus tekee siitä standardin tiedonsiirrossa tekstinkäsittelyohjelmistojen välillä, ja siten sisältöä voidaan siirtää käyttöjärjestelmästä toiseen menettämättä asiakirjan muotoilua. Tiedostomuotomääritykset ovat Microsoftin saatavilla julkisesti download, ja niihin voidaan viitata kehittäjän näkökulmasta.

#### RTF-otsikko ####

RTF-otsikolla on seuraava esitys.

|Kenttä|Kuvaus
---|---|
|\<header> |**\rtf1\fbidis**? \<character set> \<from> ? \<deffont> \<deflang> \<fonttbl> ? \<filetbl> ? \<colortbl> ? \<stylesheet> ? \<stylerestrictions> ? \<listtables> ? \<revtbl> ? \<rsidtable> ? \<mathprops> ? \<generator> ?

Otsikkotaulukoiden on oltava tässä järjestyksessä, jos niitä on olemassa. RTF-tiedosto voi sisältää ryhmiä kirjasimille, tyyleille, näytön väreille, kuville, alaviitteille, kommenteille (huomautuksille), ylä- ja alatunnisteille, yhteenvetotiedoille, kenttiä, kirjanmerkkejä, asiakirjan, osion, kappaleen ja merkkien muotoiluominaisuuksia, matematiikkaa, kuvia ja esineitä. Jos kirjasin, tiedosto, tyyli, väri, versiomerkki ja yhteenvetotietoryhmät ja asiakirjan muotoilun ominaisuudet sisältyvät tiedostoon, niiden on oltava RTF-otsikossa, joka edeltää RTF-tekstiä. Jos jonkin ryhmän sisältöä ei käytetä, ryhmä voidaan jättää pois. Kaikkien ryhmien, jotka käyttävät toisessa ryhmässä määritettyjä ominaisuuksia, on oltava ominaisuudet määrittävän ryhmän jälkeen. Esimerkiksi väri- ja fonttiominaisuuksien on edeltävä tyyliryhmää.

#### RTF-versio ####

RTF-dokumentin tulee alkaa näillä kuudella merkillä:

```
{\rtf1
```
jossa 1 näyttää RTF-versionumeron.

#### Merkistö ####

{\rtf1:n jälkeen asiakirjan tulee ilmoittaa, mitä merkistöä se käyttää. Merkistö voidaan ilmoittaa jollakin seuraavista komennoista:

`\ansi` - Asiakirja on ANSI-merkistössä, joka tunnetaan myös nimellä Code Page 1252, tavallisessa MSWindows-merkistössä.

`\mac` - Asiakirja on MacAscii-merkistössä, joka on tavallinen merkistö Mac OS:n vanhoissa (10:tä edeltävissä) versioissa.

`\pc` - Asiakirja on DOS-koodisivulla 437, MS-DOS:n oletusmerkistössä. Kirjoittajat, joilla on hyvä lihasmuisti, huomaavat, että tämä on merkistö, jota käytetään edelleen Alt-numeeristen koodien tulkinnassa – eli kun pidät Alt-näppäintä painettuna ja kirjoitat numeronäppäimistöllä 130, se tuottaa é:n, koska merkki 130 CP437:ssä on é. Se on suunnilleen ainoa käyttö, jonka CP437 näkee nykyään.

`\pca` - Asiakirja on DOS-koodisivulla 850, joka tunnetaan myös nimellä MS-DOS Multilingual Code Page.

#### Fonttikomento ####

Merkkijoukon määritelmää seuraa komento \deffN. Tämä määrittää, että fonttinumero N on tämän asiakirjan oletusfontti. Fonttinumeroon N viitataan fonttitaulukosta. Komento `\deffN` on teknisesti valinnainen, mutta sen pitäisi olla turvassa yleisenä prologina, kuten seuraava valitsee fontin 0 oletusfonttiksi.

`{\rtf1\ansi\deff0`

#### Fonttitaulukko ####

Kaikki asiakirjassa käytettävät fontit on lueteltu fonttitaulukossa, jossa jokaista fonttia edustaa kirjasinnumero. Asiakirjassa on oltava fonttitaulukko, vaikka jotkut ohjelmat toimivat myös ilman sitä.

Fonttitaulukon syntaksi on {\fonttbl //...declarations//...}, jossa jokaisella ilmoituksella on tämä perussyntaksi:

`{\fnumber\familycommand Fontname;}`

Fonttitaulukko, jossa on neljä ilmoitusta, on seuraava:

```
{\fonttbl
{\f0\froman Times;}
{\f1\fswiss Arial;}
{\f2\fmodern Courier New;}
}
```

Asiakirjassa, jossa on tämä fonttitaulukko, `{\f2 stuff}` tulostaa jutut Courier Newissa. Fonttia ei voi käyttää asiakirjassa ennen kuin se on lueteltu kirjasintaulukossa.

### Asiakirjan loppu ###

Jokaisen RTF-dokumentin lopussa on oltava }, jolloin ryhmä sulkeutuu asiakirjan ensimmäisellä merkillä {. Mikään ei voi seurata lopullista }, paitsi mahdollisesti rivinvaihto.

## Viitteet ##

* [Rich Text Format](https://en.wikipedia.org/wiki/Rich_Text_Format)
