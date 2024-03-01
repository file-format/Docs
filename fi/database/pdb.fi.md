{
  "date": "2023-06-26",
  "keywords": [
"pdb",
"pdb-tiedostoja",
"pdb-tietokanta",
"pdb-tiedostomuoto",
"pdb-tiedostotyyppejä",
"RCSB ATE",
"kuinka avata pdb-tiedostoja",
"pdb tiedostopääte"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "Mitä ovat PDB-tiedostot? ATE Files: A Crucial Tool for Structural Biology",
  "description": "Lisätietoja siitä, mitä ovat PDB-tiedostot? ATE Files: A Crucial Tool for Structural Biology",
  "linktitle": "PDB",
  "menu": {
    "docs": {
      "identifier": "database-pdb",
      "parent": "database"
}
},
  "lastmod": "2023-06-26"
}

## ATE-tiedostojen ymmärtäminen: tärkeä työkalu rakennebiologialle

Rakennebiologian alalla **Protein Data Bank (PDB)** on arvokas resurssi tiedemiehille ja tutkijoille. PDB-tiedostot, standardoitu muoto proteiinien ja muiden makromolekyylien kolmiulotteisten (3D) rakenteiden tallentamiseen, ovat keskeisessä asemassa niiden atomikoordinaattien selvittämisessä ja niiden toiminnassa. Tässä artikkelissa perehdymme **PDB-tiedostojen** maailmaan ja tutkimme niiden merkitystä, rakennetta ja niiden tiedeyhteisölle tarjoamaa tiedon runsautta.

## Mitä ovat PDB-tiedostot?

**PDB-tiedostot** ovat pelkkiä tekstitiedostoja, jotka sisältävät yksityiskohtaista tietoa atomikoordinaateista, sidosten pituuksista, kulmista ja muista olennaisista tiedoista, jotka määrittelevät makromolekyylin 3D-rakenteen. Niitä käytetään laajasti rakennetietojen tallentamiseen ja jakamiseen, mikä varmistaa uusittavuuden ja helpottaa tutkijoiden yhteistyötä maailmanlaajuisesti.

## PDB-tiedoston rakenne - PDB-tiedostomuoto

Tyypillinen PDB-tiedosto koostuu useista osista, joista jokainen palvelee tiettyä tarkoitusta **PDB-tiedostomuodossa**. Tärkeimmät osat sisältävät:

- **Header:** Contains general information about the structure, such as the title, author, and publication details.
- **Koordinaattiosio:** Näyttää atomikoordinaatit ja niihin liittyvät tiedot, mukaan lukien elementin tyypin, käyttöasteen ja lämpötilatekijän.
- **Yhteysosio:** Määrittää atomien välisen liitettävyyden, sidokset ja makromolekyylin yleisen topologian.
- **Annotaatioosio:** Sisältää lisätietoja, kuten proteiinien sekundaarirakenteen elementit, ligandit ja rakenteessa olevat liuotinmolekyylit.
- **Kysallografinen osa:** Sisältää tiedot rakenteen määrittämiseen käytetyistä kristallografisista parametreista (jos sovellettavissa).
- **Huomautusosio:** Sallii valinnaiset kommentit tai huomautukset rakenteesta.

## ATE-tiedostojen merkitys:

**PDB-tiedostot** toimivat rakennebiologian kulmakivenä ja tarjoavat lukuisia etuja:

- **Rakenneanalyysi:** PDB-tiedostot antavat tutkijoille mahdollisuuden tutkia proteiinien ja makromolekyylien 3D-rakennetta, mikä antaa tärkeitä tietoja niiden laskostumisesta, toiminnasta ja vuorovaikutuksista muiden molekyylien kanssa.
- **Drug Discovery:** PDB-tiedostot auttavat mahdollisten lääkekohteiden tunnistamisessa antamalla tutkijoille mahdollisuuden visualisoida proteiinien sitoutumiskohdat ja suunnitella molekyylejä, jotka voivat muuttaa niiden toimintaa.
- **Vertailevat tutkimukset:** ATE-tiedostot helpottavat toisiinsa liittyvien rakenteiden vertailevaa analysointia, auttaen tutkijoita ymmärtämään evoluutiosuhteita ja tunnistamaan säilyneitä rakenteellisia motiiveja.
- **Validointi ja laadunvalvonta:** ATE-tiedostojen saatavuus mahdollistaa julkaistujen rakenteiden riippumattoman validoinnin ja todentamisen, mikä edistää avoimuutta ja tieteellistä kurinalaisuutta.
- **Koulutus ja tiedotus:** PDB-tiedostot ovat korvaamattomia opetustyökaluja, joiden avulla opiskelijat ja suuri yleisö voivat tutkia ja visualisoida molekyylirakenteiden monimutkaista maailmaa.

## Eri tyyppisiä PDB-tiedostoja:

**PDB (Protein Data Bank) -tiedostoja** käytetään yleisesti kolmiulotteisen rakennetietojen tallentamiseen biomolekyyleistä, pääasiassa proteiineista ja nukleiinihapoista. ATE-tiedostoja on useita eri tyyppejä, joista jokainen palvelee tiettyä tarkoitusta. Tässä on joitain yleisimmistä tyypeistä:

- **Rakenteen määritys PDB (mmCIF-muoto):** Tämä on standardi PDB-tiedostomuoto, jota käytetään edustamaan kokeellisesti määritettyjä biomolekyylien kolmiulotteisia rakenteita. Se sisältää tietoa molekyylin atomien atomikoordinaateista sekä rakenteen määritysprosessiin liittyviä metatietoja.
- **Malli PDB:** Joissakin tapauksissa saatavilla on useita biomolekyylirakenteen malleja tai konformaatioita. Mallin PDB-tiedostot edustavat yhdistelmää rakenteita, joista jokaisella on omat atomikoordinaatit. Näitä tiedostoja käytetään edustamaan molekyylin dynamiikkaa tai vaihtoehtoisia konformaatioita.
- **NMR PDB:** Ydinmagneettiresonanssin (NMR) PDB-tiedostot edustavat erityisesti NMR-spektroskopialla määritettyjä rakenteita. NMR-kokeet tarjoavat tietoa atomien välisistä etäisyyksistä molekyylissä, ja NMR PDB -tiedostot sisältävät tietoa näistä etäisyyksistä sekä johdetuista atomikoordinaateista.
- **Small Molecule PDB:** Vaikka PDB-tiedostoja käytetään ensisijaisesti proteiineille ja nukleiinihapoille, ne voivat myös tallentaa rakennetietoja pienistä molekyyleistä, kuten lääkeyhdisteistä tai ligandeista. Pienimolekyyliset PDB-tiedostot sisältävät pienen molekyylin atomikoordinaatit ja siihen liittyvät metatiedot.
- **Kokeelliset tiedot PDB:** PDB-tiedostot voivat myös tallentaa biomolekyylirakenteeseen liittyviä kokeellisia tietoja, kuten diffraktiotietoja röntgenkristallografiakokeista. Nämä tiedostot sisältävät tietoa kokeellisesta asetelmasta ja havaituista diffraktiokuvioita.
- **Annotated PDB:** Annotoidut PDB-tiedostot sisältävät lisätietoja atomikoordinaattien lisäksi. Ne voivat sisältää huomautuksia proteiinidomeeneista, sekundaarisista rakenneelementeistä, ligandia sitovista kohdista ja muista molekyylin toiminnallisista tai rakenteellisista piirteistä.
- **Homologia/vertailumallinnus PDB-tiedostot:** Homologia- tai vertaileva mallinnus PDB-tiedostot luodaan, kun proteiinin tai makromolekyylin rakenne ennustetaan perustuen sen sekvenssin samankaltaisuuteen tunnetun kokeellisesti määritetyn rakenteen kanssa. Nämä tiedostot tarjoavat arvokkaita näkemyksiä proteiinien rakenteellisista ominaisuuksista ja mahdollisista toiminnoista, joista puuttuu kokeellisia rakenteita.
- **Teoreettiset/laskennalliset PDB-tiedostot:** Teoreettiset tai laskennalliset PDB-tiedostot luodaan käyttämällä laskennallisia menetelmiä, kuten molekyylidynamiikan simulaatioita tai proteiinirakenteen ennustusalgoritmeja. Nämä tiedostot edustavat ennustettuja rakenteita ja voivat tarjota arvokasta tietoa proteiinien dynamiikasta, laskostumisreiteistä ja vuorovaikutuksista ligandien tai muiden molekyylien kanssa.
- **Hybridi PDB-tiedostot:** Hybridi PDB-tiedostot yhdistävät kokeellisen ja laskennallisen tiedon tarjotakseen kattavamman esityksen makromolekyylin rakenteesta. Ne sisältävät kokeellisia tietoja, kuten matalaresoluutioisia elektronimikroskopiakuvia tai pienen kulman röntgensirontatietoja (SAXS), ja laskennallisia malleja luodakseen hybridirakenteita, jotka tallentavat sekä kokeellisia että ennustettuja piirteitä.
- **Ligand-Bound PDB -tiedostot:** Ligandiin sidotut PDB-tiedostot sisältävät proteiinien tai makromolekyylien 3D-rakenteita, jotka ovat kompleksoituneita pienten molekyylien, kuten lääkkeiden, kofaktorien tai substraattien, kanssa. Nämä tiedostot tarjoavat tärkeitä näkemyksiä proteiini-ligandivuorovaikutuksista, mikä auttaa ymmärtämään lääkkeiden sitoutumista ja järkevää lääkesuunnittelua.
- **Ensemble PDB -tiedostot:** Ensemble PDB -tiedostot edustavat kokoelmaa rakenteellisesti samanlaisia malleja, jotka kuvaavat makromolekyylin luontaista joustavuutta tai dynamiikkaa. Niitä käytetään usein tutkimaan konformaatiomuutoksia, proteiinidynamiikkaa tai edustamaan molekyylin erilaisia toiminnallisia tiloja.

## RCSB ATE

**RCSB PDB (Research Colaboratory for Structural Bioinformatics Protein Data Bank)** on laajalti tunnustettu ja arvovaltainen resurssi biologisten makromolekyylien 3D-rakenneinformaation saamiseksi ja tutkimiseksi. Se on ATE-tietojen ensisijainen arkisto ja rakennebiologian tutkimuksen keskus.

Tässä on joitain keskeisiä ominaisuuksia ja tietoja **RCSB PDB:stä**:

- **Tietovarasto:**
RCSB PDB -tietokanta toimii kokeellisesti määritettyjen proteiinien, nukleiinihappojen ja kompleksisten kokoonpanojen 3D-rakenteiden arkistona. Se tallentaa laajan kokoelman PDB-tiedostoja, jotka sisältävät atomikoordinaatteja, kokeellisia tietoja, huomautuksia ja muuta asiaankuuluvaa tietoa.

- **Maailmanlaajuinen yhteistyö:**
RCSB PDB on yhteistyöhanke, johon osallistuu useita oppilaitoksia, mukaan lukien Rutgersin yliopisto, Kalifornian yliopisto San Diegossa, Kalifornian yliopisto San Franciscossa ja National Institute of Standards and Technology (NIST). Yhteistyö varmistaa PDB-tietokannan jatkuvan ylläpidon, kuroinnin ja saavutettavuuden.

- **Esteettömyys ja käyttöliittymä:**
RCSB PDB tarjoaa käyttäjäystävällisen verkkoliittymän (www.rcsb.org), jonka avulla tutkijat, tutkijat ja suuri yleisö voivat etsiä, selata ja hakea rakennetietoja. Sivusto tarjoaa erilaisia hakuvaihtoehtoja, edistyneitä kyselyominaisuuksia sekä työkaluja visualisointiin ja analysointiin.

- **Tietojen integrointi ja ristiviittaukset:**
RCSB PDB integroi tiedot eri lähteistä ja tietokannoista, jolloin käyttäjät voivat saada käyttöönsä tiettyihin rakenteisiin liittyviä lisätietoja. Siinä ristiviittaukset muihin biologisiin tietokantoihin, kuten UniProt, Pfam, Gene Ontology ja PubMed, tarjoavat kattavan kuvan makromolekyylien rakenteellisista ja toiminnallisista näkökohdista.

- **Työkalut ja resurssit:**
RCSB PDB -verkkosivusto tarjoaa valikoiman työkaluja ja resursseja rakenneanalyysin ja visualisoinnin tukemiseen. Näitä ovat muun muassa molekyylikatselulaitteet, kohdistustyökalut, sekvenssihakutyökalut ja validointipalvelut. Nämä resurssit helpottavat rakennetietojen tutkimista ja tulkintaa.

-**Koulutus ja tiedotus:**
RCSB:n ATE on sitoutunut edistämään koulutus- ja tiedotusaloitteita. Sivusto tarjoaa opetusresursseja, opetusohjelmia ja luokkahuonemateriaaleja, jotka auttavat opiskelijoita, opettajia ja suurta yleisöä ymmärtämään molekyylirakenteita ja niiden merkitystä.

- **Continuous Updates and Improvements:**
RCSB:n ATE:ta päivitetään jatkuvasti uusilla rakenteilla, kun niitä tulee saataville. Se käy läpi säännöllisiä huolto- ja laadunvalvontaprosesseja, jotta varmistetaan tallennettujen tietojen tarkkuus ja eheys. Tieteellisen tutkimuksen tueksi pyritään myös tehostamaan tiedon tallettamista, kuratointia ja integrointia.

**RCSB PDB** on kattava resurssi, joka tarjoaa avoimen pääsyn biologisten makromolekyylien 3D-rakennetietoihin. Sen tehtävänä on helpottaa tutkimusta, mahdollistaa tiedon löytäminen ja edistää tieteellistä yhteistyötä rakennebiologian alalla.

## ATE-tietokannan merkitys

**PDB-tietokanta** toimii keskitettynä 3D-rakennetietojen arkistona, joka tarjoaa tutkijoille runsaasti tietoa ja oivalluksia makromolekyylien monimutkaiseen maailmaan. Sen merkitys voidaan tiivistää seuraavasti:

- **Rakenteen ja toiminnan välinen suhde:** PDB-tietokannan avulla tutkijat voivat paljastaa proteiinien ja muiden makromolekyylien rakenteen ja toiminnan välisen suhteen. Tutkimalla 3D-atomikoordinaatteja tutkijat voivat saada arvokasta tietoa biologisten prosessien ja solujen toimintojen taustalla olevista mekanismeista.
- **Drug Discovery and Design:** PDB-tietokanta auttaa lääkkeiden löytämisessä ja suunnittelussa tarjoamalla yksityiskohtaista tietoa proteiinien sitoutumiskohdista ja niiden vuorovaikutuksista pienten molekyylien kanssa. Tämän tiedon avulla tutkijat voivat kehittää uusia terapeuttisia aineita, jotka kohdistuvat tiettyihin sairauksiin liittyviin proteiineihin.
- **Vertaileva analyysi ja evoluutiotutkimukset:** ATE-tietokanta mahdollistaa toisiinsa liittyvien rakenteiden vertailevan analyysin, mikä helpottaa säilyneiden rakenteellisten motiivien ja evoluutiosuhteiden tunnistamista. Tämä tieto auttaa tutkijoita ymmärtämään eri proteiiniperheiden välisiä suhteita ja niiden toiminnallisia vaikutuksia.
- **Validointi ja laadunvalvonta:** ATE-tietokannan saatavuus edistää avoimuutta ja tieteellistä kurinalaisuutta mahdollistamalla julkaistujen rakenteiden riippumattoman validoinnin ja todentamisen. Tutkijat voivat vertailla omia kokeellisia tai laskennallisia mallejaan olemassa oleviin rakenteisiin, mikä varmistaa tarkkuuden ja luotettavuuden.

## ATE-tietokannan organisaatio ja sisältö:

**PDB-tietokanta** on järjestetty hierarkkisen rakenteen perusteella, ja jokainen merkintä edustaa ainutlaatuista 3D-rakennetta. ATE-tietokannan avainkomponentteja ovat:

- **PDB ID and Entry Information:** Each entry in the PDB database is assigned a unique identifier known as the PDB ID. This ID is used to access and reference specific structures within the database. Entry information includes details about the deposition date, authors, experimental techniques employed, and associated publication-fis.
- **Atomic Coordinates and Metadata:** Jokaisen PDB-tietokannan merkinnän ydin on atomikoordinaattiosio, joka antaa makromolekyylin jokaisen atomin avaruudellisen sijainnin. Tähän osioon liittyy metatietoja, kuten B-tekijät (lämpötilatekijät), käyttöastearvot ja kokeelliset lisätiedot.
- **Funktionaaliset huomautukset ja biologinen konteksti:** PDB-tietokanta sisältää tietoja kunkin rakenteen biologisesta kontekstista, mukaan lukien toiminnalliset merkinnät, ligandit, kofaktorit ja vuorovaikutuksessa olevat kumppanit. Tällaiset yksityiskohdat lisäävät ymmärrystämme rakenteen roolista biologisissa prosesseissa.
- **Tietojen integrointi ja ristiinviittaukset:** PDB-tietokanta integroituu muihin biologisiin tietokantoihin, jolloin tutkijat voivat käyttää asiaankuuluvaa lisätietoa. Ristiviittaukset tietokantoihin, kuten UniProt, Gene Ontology ja Enzyme Commission, tarjoavat käyttäjille kattavaa tietoa proteiinisekvensseistä, toiminnallisista huomautuksista ja asiaan liittyvästä kirjallisuudesta.

## ATE-tietokannan käyttö ja käyttö:

Tutkijat voivat käyttää **PDB-tietokantaa** useilla eri tavoilla, mukaan lukien virallisella verkkosivustolla (www.rcsb.org), joka tarjoaa käyttäjäystävällisen käyttöliittymän rakenteiden etsimiseen, selaamiseen ja hakemiseen. Lisäksi useat ohjelmistotyökalut ja -resurssit, sekä verkkopohjaiset että erilliset, mahdollistavat ATE-tietojen syvällisen analyysin, visualisoinnin ja manipuloinnin.

Nämä työkalut antavat tutkijoille mahdollisuuden:

- **Search for Structures:** Users can search for specific structures based on PDB IDs, keywords, author names, or sequence similarity to known structures.
- **Visualisoi rakenteita:** Molekyylivisualisointiohjelmiston avulla tutkijat voivat visualisoida ja tutkia 3D-rakenteita, mikä mahdollistaa paremman ymmärryksen atomien, toissijaisten rakenne-elementtien ja proteiini-ligandivuorovaikutuksista.
- **Analysoi ja vertaile rakenteita:** Erilaiset analyysityökalut auttavat vertailemaan ja analysoimaan rakenteita, tunnistamaan säilyneitä motiiveja, havaitsemaan rakenteellisia yhtäläisyyksiä ja arvioimaan makromolekyylin eri tilojen välisiä rakenteellisia muutoksia.
- **Hae tukitiedot:** Tutkijat pääsevät käsiksi niihin liittyviin kokeellisiin tietoihin, julkaisuihin ja tiettyihin rakenteisiin liittyviin lisätietoihin ATE-tietokannassa.

**PDB-tietokanta** kehittyy ja laajenee edelleen kokeellisten tekniikoiden ja laskentamenetelmien kehityksen tahdissa. Uudet tekniikat, kuten kryoelektronimikroskooppi (cryo-EM) ja integratiiviset rakennebiologian lähestymistavat, myötävaikuttavat siihen, että ATE-tietokantaan tallennetaan yhä useampia korkearesoluutioisia rakenteita. Lisäksi pyritään tehostamaan tietojen integrointia, parantamaan tietojen laatua ja helpottamaan toiminnallisten ja kontekstuaalisten tietojen integrointia tietokantaan.

**Protein Data Bank (PDB) -tietokanta** on rakennebiologian kulmakivi ja tarjoaa tutkijoille laajan kokoelman kokeellisesti määritettyjä makromolekyylien 3D-rakenteita. PDB-tietokanta ruokkii tieteellisiä löytöjä, helpottaa lääkkeiden kehitystä ja edistää tutkijoiden yhteistyötä maailmanlaajuisesti runsaan datan ja ristiinviittausominaisuuksiensa ansiosta. Rakennebiologian alan edistyessä PDB-tietokanta säilyy välttämättömänä resurssina, joka paljastaa molekyylirakenteiden salaisuudet ja katalysoi läpimurtoja eri tieteenaloilla.

## Kuinka avata PDB -tiedostot?

PDB-tiedostojen avaamiseen voit käyttää erilaisia ohjelmistotyökaluja ja katseluohjelmia, jotka on erityisesti suunniteltu molekyylien visualisointiin ja analysointiin. Tässä on muutamia yleisesti käytettyjä vaihtoehtoja:

-**PyMOL:**
PyMOL on suosittu molekyylivisualisointiohjelmisto, jonka avulla voit avata ja analysoida PDB-tiedostoja. Se tarjoaa käyttäjäystävällisen käyttöliittymän, jossa on laajoja ominaisuuksia molekyylirakenteiden visualisointiin ja manipulointiin. PyMOL on saatavana sekä avoimen lähdekoodin että kaupallisena versiona.

-**Kimeeri:**
UCSF Chimera on tehokas ohjelmistotyökalu molekyylirakenteiden visualisointiin ja analysointiin. Se tukee laajaa valikoimaa tiedostomuotoja, mukaan lukien PDB-tiedostot. Chimera tarjoaa kattavan joukon työkaluja molekyyligrafiikkaan, mallien rakentamiseen ja makromolekyylien interaktiiviseen tutkimiseen.

- **VMD (Visual Molecular Dynamics):**
VMD on molekyylimallinnus- ja simulointiohjelmisto, joka tukee muun muassa PDB-tiedostoja. Se on erityisen hyödyllinen biomolekyylijärjestelmien tutkimiseen ja molekyylidynamiikan simulaatioiden suorittamiseen. VMD tarjoaa edistyneitä visualisointiominaisuuksia ja analysointityökaluja.

-**Jmol:**
Jmol on avoimen lähdekoodin Java-pohjainen molekyylikatseluohjelma, joka voi avata PDB-tiedostoja. Se mahdollistaa molekyylirakenteiden interaktiivisen visualisoinnin ja tarjoaa ominaisuuksia zoomaukseen, pyörittämiseen ja etäisyyksien mittaamiseen. Jmolia voidaan käyttää erillisenä sovelluksena tai upotettuna verkkosivustoille.

-**UCSF ChimeraX:**
ChimeraX on seuraavan sukupolven molekyylivisualisointiohjelma, jonka on kehittänyt sama Chimeran takana oleva tiimi. Se tarjoaa parannetun käyttöliittymän, parannetut visualisointiominaisuudet ja tuen suurille tietojoukoille. ChimeraX pystyy avaamaan PDB-tiedostoja ja tarjoaa edistyneitä työkaluja rakenneanalyysiin ja visualisointiin.

-**Biovia Discovery Studio:**
Biovia Discovery Studio on kattava mallinnus- ja simulointityökalusarja, jota käytetään laajasti molekyylibiologian tutkimuksessa. Se tukee PDB-tiedostojen avaamista ja analysointia ja tarjoaa joukon molekyylimallinnus- ja analyysiominaisuuksia.

## Johtopäätös:

ATE-tiedostojen monimuotoisuus kokeellisista rakenteista ennustettuihin malleihin tarjoaa laajan kirjon tietoa rakennebiologian tutkijoille. Nämä tiedostot ovat peräisin kokeellisista tekniikoista tai laskennallisista menetelmistä, ne tarjoavat perustan proteiinirakenteiden tutkimiselle, toiminnallisten mekanismien selvittämiselle ja lääkekeksintöjen helpottamiseksi. Erilaisten ATE-tiedostojen saatavuus ja käyttö edistävät rakennebiologian kehitystä ja vaikuttavat syvästi eri tieteenaloihin.

