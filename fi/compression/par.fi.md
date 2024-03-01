{
   "date":"2023-07-18",
   "keywords":[
"PAR",
"PAR-tiedosto",
"kuinka avata par-tiedosto",
"tiedosto",
"PAR tiedostopääte",
"laajennus",
"tiedosto"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"PAR-tiedostomuoto - arkiston hakemistotiedosto",
   "description":"Opi PAR-muodosta ja API-liittymistä, jotka voivat luoda ja avata PAR-tiedostoja.",
   "linktitle":"PAR",
   "menu":{
      "docs":{
         "identifier":"compression-par-fi",
         "parent":"compression"
}
},
   "lastmod":"2023-07-18"
}

## Mikä on PAR-tiedosto?

Parchive (PAR) -arkistojen sisällä .par-tiedosto viittaa hakemistotiedostoon, joka sisältää ryhmän pariteettitaltioita tai pariteettilohkoja. Tätä hakemistotiedostoa käytetään virheiden havaitsemiseen ja palauttamiseen, kun yksi tai useampi arkistossa oleva tiedosto katoaa tai vahingoittuu.

Arkistoarkisto koostuu tyypillisesti sekä alkuperäisistä tiedostoista että vastaavista pariteettitaltioista. Pariteettitilavuudet luodaan Reed-Solomonin virheenkorjausalgoritmeilla. Nämä pariteettitaltiot sisältävät redundantteja tietoja, joita voidaan käyttää alkuperäisten tiedostojen palauttamiseen.

.par-tiedosto, joka tunnetaan myös pariteettitaltiojoukona, sisältää tietoja pariteettitaltioiden rakenteesta ja sijainnista arkiston sisällä. Se toimii hakemistona tai karttana palautusprosessille. Käyttämällä .par-tiedostoa erikoistunut PAR-ohjelmisto voi määrittää, mitä pariteettitaltioita tarvitaan ja miten niitä tulee käyttää puuttuvien tai vaurioituneiden tiedostojen rekonstruoimiseen.

Kun yhteen tai useampaan arkiston tiedostoon ei pääse käsiksi tai se vioittuu, .par-tiedostoa voidaan käyttää yhdessä käytettävissä olevien pariteettitaltioiden kanssa kadonneiden tietojen palauttamiseen. PAR-ohjelmisto lukee .par-tiedoston, tunnistaa puuttuvat tai vahingoittuneet tiedostot ja rekonstruoi ne pariteettitaltioiden avulla.

## Kuinka avata PAR-tiedosto?

.par-tiedostojen avaamiseen ja käyttämiseen tarvitaan erikoistunut PAR-ohjelmisto. Tässä on muutamia suosittuja ohjelmistovaihtoehtoja, jotka voivat käsitellä .par-tiedostoja:

- **QuickPar:** QuickPar on laajalti käytetty PAR-ohjelmisto Windowsille. Sen avulla voit luoda, tarkistaa ja korjata PAR-tiedostoja. Voit avata .par-tiedoston QuickParissa varmistaaksesi sen eheyden tai käyttää sitä vaurioituneiden tai puuttuvien tiedostojen korjaamiseen Arkiston arkistossa.

- **MultiPar:** MultiPar on toinen suosittu PAR-ohjelmisto, joka on saatavana Windowsille. Se tukee sekä PAR- että PAR2-tiedostomuotoja ja tarjoaa edistyneitä ominaisuuksia arkistojen luomiseen, tarkistamiseen ja korjaamiseen. MultiPar voi avata .par-tiedostoja ja suorittaa virheiden havaitsemis- ja palautustoimia annettujen pariteettitaltioiden perusteella.

- **MacPAR deLuxe:** MacPAR deLuxe on PAR-ohjelmisto, joka on suunniteltu erityisesti macOS:lle. Se tukee PAR- ja PAR2-tiedostomuotoja ja tarjoaa samanlaisia toimintoja kuin QuickPar ja MultiPar. MacPAR deLuxe voi avata .par-tiedostoja ja auttaa arkistojen tarkistamisessa ja vaurioituneiden tai puuttuvien tiedostojen palauttamisessa.

## PAR-tiedostomuoto - lisätietoja

PAR-tiedostomuoto, jota kutsutaan yleisesti nimellä Parchive, on erityinen tiedostomuoto, jota käytetään pariteettitietojen luomiseen ja virheiden havaitsemiseen ja palauttamiseen tiedostoarkistoissa. PAR-tiedostomuoto koostuu yleensä kolmesta tyypistä: PAR, PAR2 ja PAR3.

- **PAR:** Alkuperäinen PAR-tiedostomuoto, joka tunnetaan myös nimellä PAR1, on Parchive-projektin kehittämä. Se sisältää alkuperäisistä tiedostoista luodut pariteettitiedot. PAR-tiedostot tarjoavat perustason virheiden havaitsemiseen ja palauttamiseen, mutta niissä on rajoituksia virheenkorjausominaisuuksien suhteen.

- **PAR2:** PAR2 on parannettu versio PAR-tiedostomuodosta. Se tarjoaa edistyneempiä virheenkorjausominaisuuksia ja parannettuja palautusominaisuuksia. PAR2-tiedostoja käytetään yleensä luomaan pariteettitietoja, jotka voivat palauttaa kadonneita tai vahingoittuneita tiedostoja arkistossa. PAR2-tiedostot tarjoavat paremman suojan tietojen vioittumiselta ja niitä käytetään laajalti tiedostojen arkistointitarkoituksiin.

- **PAR3:** PAR3 is the latest version of the PAR file format and provides further improvements in error correction and recovery. It offers even higher levels of redundancy and error correction capabilities compared to PAR2. PAR3-tiedostot on suunniteltu tarjoamaan tehokkaampia suoja- ja palautusvaihtoehtoja arkistoon tallennetuille tiedoille.

PAR-ohjelmisto tukee laajasti sekä PAR2- että PAR3-tiedostomuotoja, ja ne tarjoavat mahdollisuuden tarkistaa arkiston tiedostojen eheys ja palauttaa kadonneita tai vahingoittuneita tietoja. PAR- ja PAR2-tiedostoja käytetään edelleen yleisesti, kun taas PAR3-tiedostot ovat vähitellen yleistymässä niiden parannettujen virheenkorjausominaisuuksiensa ansiosta.

## Viitteet
* [Arkisto](https://en.wikipedia.org/wiki/Parchive)


