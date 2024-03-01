{
   "date":"2023-07-20",
   "keywords":[
"BIN",
"BIN-tiedosto",
"tiedosto",
"BIN tiedostopääte",
"laajennus",
"tiedosto"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"BIN-tiedostomuoto - MacBinary-koodattu tiedosto",
   "description":"Opi BIN-muodosta ja sovellusliittymistä, jotka voivat luoda ja avata BIN-tiedostoja.",
   "linktitle":"BIN",
   "menu":{
      "docs":{
         "identifier":"compression-bin-fi",
         "parent":"compression"
}
},
   "lastmod":"2023-07-20"
}

## Mikä on BIN-tiedosto?

BIN-tiedosto voi Macintosh-tietokoneissa viitata MacBinary-muodossa tallennettuun tiedostoon. MacBinary on tiedostomuoto, joka on erityisesti suunniteltu siirtämään Macintosh-tiedostoja Internetin, sähköpostin, FTP:n tai kannettavan median kautta. MacBinaryn tarkoitus on säilyttää Macintosh-tiedostojen täydellinen tiedostorakenne ja attribuutit, mukaan lukien sekä datahaarukka että resurssihaarukka, yhdessä tiedostossa.

MacBinary-muodossa tämä saavutetaan kapseloimalla Macintosh Hierarchical File System (HFS) -resurssihaarukka ja datahaarukka pakatuksi tiedostoksi. Se sisältää myös Finder-otsikon, joka sisältää tärkeitä metatietoja tiedostosta. Yhdistämällä kaikki nämä komponentit yhdeksi tiedostoksi MacBinary varmistaa, että tiedosto säilyttää eheytensä ja että se voidaan helposti siirtää ja jakaa eri alustojen välillä.

Applen tiedostojärjestelmien ja tiedostonsiirtoprotokollien kehittymisen myötä BIN-tiedostojen ja MacBinary-muodon käyttö on vähentynyt. Tiedostomuotojen, kuten ZIP, käyttöönotto ja siirtyminen nykyaikaisempiin tiedostojärjestelmiin, kuten HFS+ ja APFS, ovat vähentäneet MacBinary-koodattujen tiedostojen tarvetta. Nämä uudemmat tiedostojärjestelmät tarjoavat tehokkaampia tapoja käsitellä tiedostoattribuutteja, resurssihaarukoita ja datahaarukoita, mikä tekee MacBinary-muodosta vähemmän tarpeellista nykypäivän laskentaympäristössä.

## BIN-tiedostomuoto – lisätietoja 

Macintosh-tietokoneiden alkuaikoina tiedostot tallennettiin kahteen erilliseen haarukkaan tietorajoitusten vuoksi. Resurssihaarukka sisälsi strukturoitua dataa, kun taas datahaarukka sisälsi jäsentämätöntä dataa. Vaikka Classic Mac OS käsitteli näitä haarukoita yhtenä tiedostona, tiedostojen siirtäminen muihin kuin Mac-järjestelmiin johti tietojen menetykseen, koska ne eivät tunnistaneet haarukoita yhtenä kokonaisuutena. Tämän korjaamiseksi MacBinary-muodon loivat henkilöt, kuten Dennis Brothers, Harry Chesley ja Yves Lempereur. MacBinary pakkaa ja yhdisti haarukat yhdeksi tiedostoksi, joka tunnetaan nimellä BIN-tiedosto, siirtämistä varten muihin kuin Mac-järjestelmiin. Palattuaan Mac OS:ään haarukat erotettaisiin uudelleen. Kun haarukkapohjaisesta HFS:stä luovuttiin 2000-luvulla, MacBinary-muodon käyttö väheni merkittävästi. Nykyään MacBinary-koodatun BIN-tiedoston kohtaaminen on harvinaista, ellet törmää vanhaan tiedostoon muussa kuin Mac-järjestelmässä tai lataa sellaista Internetistä.

The MacBinary format has gone through several versions over time to accommodate changes in Macintosh systems and file handling. Here are some of the different versions of the MacBinary format:

- **MacBinary I:** MacBinaryn alkuperäinen versio, joka julkaistiin 1980-luvun lopulla. Se yhdisti resurssihaarukan ja datahaarukan yhdeksi binääritiedostoksi, mikä mahdollistaa Macintosh-tiedostojen siirron eri alustojen välillä.

- **MacBinary II:** Tämä 1990-luvun alussa julkaistu versio paransi alkuperäistä MacBinary-muotoa lisäämällä lisätietoja, kuten tiedostotyypin ja luojakoodit, binaaritiedoston otsikkoon. Nämä koodit auttoivat säilyttämään Macintosh-tiedostojen eheyden ja tunnistamisen siirron aikana.

- **MacBinary III:** The MacBinary III format, introduced in the mid-1990s, further enhanced the previous versions by including additional metadata, such as file name and file creation and modification dates, in the binary file's header. This allowed for more comprehensive preservation of Macintosh file attributes during transfer.

- **MacBinary IV:** MacBinary IV kehitettiin ratkaisemaan yhteensopivuusongelmia nousevan Mac OS X -käyttöjärjestelmän kanssa 2000-luvun alussa. Se sisälsi muutoksia mukautuakseen Mac OS X:n uuteen tiedostojärjestelmän rakenteeseen ja attribuutteihin.

## Kuinka avata BIN-tiedosto?

MacBinary Encoded BIN -tiedostoja voidaan avata käyttämällä erilaisia pakkausapuohjelmia. MacOS-käyttäjille **Apple Archive Utility** on sopiva vaihtoehto. Windows-käyttäjät voivat käyttää ohjelmistoja, kuten **Smith Micro StuffIt Deluxe**, purkaakseen MacBinary Encoded BIN -tiedoston sisällön. Toinen vaihtoehto macOS-käyttäjille on **The Unarchiver**, joka on monipuolinen työkalu, joka pystyy käsittelemään useita tiedostomuotoja, mukaan lukien MacBinary.

On tärkeää huomata, että .bin-tiedostotunnistetta käyttävät useat tiedostomuodot, ei vain MacBinary. Siksi, jos kohtaat BIN-tiedoston, jota ei voi avata edellä mainituilla apuohjelmilla, se voidaan tallentaa eri muotoon. Tällaisissa tapauksissa saatat joutua tunnistamaan tietyn tiedostomuodon ja käyttämään tiedoston sisältöä varten suunniteltua ohjelmistoa tai apuohjelmaa.

## Mikä on Macbinary Archive?

MacBinary-arkisto on varhaisille Macintosh-tietokoneille suunniteltu tiedostomuoto, joka käsittelee Macintosh-tiedostojen kaksoishaarukkarakennetta. Macintosh-tiedostojärjestelmät koostuvat datahaarukasta ja resurssihaarukasta, jotka sisältävät tiedot ja metatiedot erikseen. Järjestelmien välisen yhteensopivuuden ja verkkosiirtojen helpottamiseksi MacBinary koodaa molemmat haarukat yhdeksi binääritiedostoksi. Tämä muoto säilyttää tietojen ja niihin liittyvien resurssien eheyden siirrettäessä muihin kuin Macintosh-järjestelmiin.

## Voinko poistaa Macbinary-arkiston?

Kyllä, voit poistaa MacBinary-arkistotiedostoja, jos et enää tarvitse niitä tai jos olet purkanut sisällön ja tallentanut ne eri muotoon. MacBinary-arkistot ovat yksinkertaisesti tapa pakata Macintosh-tiedostoja tiettyihin tarkoituksiin, kuten järjestelmien väliseen siirtoon tai varastointiin. Arkiston poistaminen ei vaikuta sen sisältämiin tiedostoihin.

## Kuinka avata Macbinary-arkisto iPhonessa?

MacBinary-arkiston avaaminen iPhonessa saattaa edellyttää kolmannen osapuolen sovellusten käyttöä, koska iOS ei tue tätä muotoa.

## Macbinary Archive Extract - Kuinka purkaa Macintosh Bin -tiedostoja?

MacBinary (bin) -tiedostojen purkamiseen nykyaikaisella tietokoneella käytät yleensä tiedostojen purkuapuohjelmaa tai ohjelmistoa, joka tukee tätä muotoa.

Käytä Windowsissa tiedostojen arkistointityökalua, joka tukee MacBinary-tiedostoja. Suosittuja vaihtoehtoja ovat WinRAR, 7-Zip tai WinZip.

Mac OS:ssä on sisäänrakennettu arkistointiapuohjelma, joka pystyy käsittelemään erilaisia arkistomuotoja, mukaan lukien MacBinary. Etsi MacBinary-tiedosto Finderista. Kaksoisnapsauta MacBinary-tiedostoa. Arkistotyökalun pitäisi käynnistyä automaattisesti ja purkaa sisältö. Kun purkaminen on valmis, voit löytää puretut tiedostot samasta sijainnista kuin alkuperäinen MacBinary-tiedosto tai määritetystä kohteesta.

## Muut BIN-tiedostot

Tässä on muita tiedostotyyppejä, jotka käyttävät **.bin**-tiedostotunnistetta.

- {{HYPERLINKKI1}}
- {{HYPERLINKKI1}}
- {{HYPERLINKKI1}}
- {{HYPERLINKKI1}}
- {{HYPERLINKKI1}}

## Viitteet

* [MacBinary](https://en.wikipedia.org/wiki/MacBinary)


