{
   "date":"2023-10-11",
   "keywords":[
"chr",
"chr-tiedosto",
"chr cryengine -merkkitiedosto",
"kuinka avata chr-tiedosto",
"tiedosto",
"chr tiedostopääte",
"laajennus",
"tiedosto"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"CHR-tiedostomuoto - CryENGINE-merkkitiedosto",
   "description":"Opi CHR CryENGINE Character -tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata CHR-tiedostoja.",
   "linktitle":"CHR CryENGINE",
   "menu":{
      "docs":{
         "identifier":"3d-chr-cryengine-fi",
         "parent":"3d"
}
},
   "lastmod":"2023-10-11"
}

## Mikä on CHR-tiedosto?

CHR-tiedosto viittaa CryENGINEn yhteydessä **CryENGINE-merkkitiedostoon**. CryENGINE on Crytekin kehittämä pelimoottori, ja näitä tiedostoja käytetään hahmomallien ja niihin liittyvien tietojen tallentamiseen käytettäväksi videopeleissä ja muissa reaaliaikaisissa sovelluksissa.

## CryENGINE-merkkitiedosto

CryENGINE-merkkitiedosto sisältää tyypillisesti seuraavat osat:

1.  **Hahmomalli**: Tämä on hahmon 3D-malli, mukaan lukien sen geometria, tekstuurit ja animaatiot. Nämä mallit luodaan usein ohjelmistoilla, kuten Autodesk Maya tai Blender, ja tuodaan sitten CryENGINEen.
    
2.  **Animaatiotiedot**: CryENGINE tukee monimutkaisia animaatioita hahmoille, joten .chr-tiedosto voi sisältää erilaisia animaatioita, kuten kävelyä, juoksua, hyppäämistä ja paljon muuta. Nämä animaatiot tallennetaan yleensä avainkehystietoina.
    
3.  **Takilatiedot**: Takila viittaa prosessiin, jossa luodaan luuranko hahmomallille, mikä mahdollistaa animaatioiden soveltamisen malliin. .chr-tiedosto voi sisältää tietoa luuhierarkiasta ja siitä, kuinka hahmon verkko on liitetty tähän luurankoon.
    
4.  **Materiaali- ja pintakuviotiedot**: Tietoja merkkimallissa käytetyistä materiaaleista ja niihin liittyvistä pintakuviokartoista voidaan sisällyttää .chr-tiedostoon. CryENGINE tukee fyysisesti perustuvaa renderöintiä, joten nämä materiaalit voivat olla melko yksityiskohtaisia.
    
5.  **Fysiikkatiedot**: Jos hahmon on tarkoitus olla vuorovaikutuksessa pelimaailman kanssa, .chr-tiedosto saattaa sisältää fysiikan tietoja, kuten törmäysmuotoja tai ragdoll-fysiikan rajoituksia.
    
6.  **Määritysasetukset**: Useita hahmojen käyttäytymiseen pelimaailmassa liittyviä konfiguraatioasetuksia, kuten tekoälykäyttäytyminen tai käsikirjoitetut tapahtumat, voivat myös olla osa .chr-tiedostoa.

## CryENGINE

CryENGINE on tehokas pelimoottori, jonka on kehittänyt saksalainen videopeliyhtiö Crytek. Se tunnetaan huippuluokan grafiikkaominaisuuksistaan, ja sitä on käytetty visuaalisesti upeiden ja teknisesti edistyneiden videopelien luomiseen. Tässä on joitain keskeisiä ominaisuuksia ja tietoja CryENGINEsta:

1.  **Grafiikka ja renderöinti**: CryENGINE on tunnettu edistyneistä grafiikkaominaisuuksistaan. Se tukee ominaisuuksia, kuten reaaliaikainen globaali valaistus, korkealaatuinen dynaaminen valaistus ja varjot, fyysisesti perustuva renderöinti (PBR) ja korkearesoluutioiset pintakuviot. Nämä ominaisuudet auttavat luomaan visuaalisesti upeita ja realistisia pelimaailmoja.
    
2.  **Fysiikkamoottori**: CryENGINE sisältää sisäänrakennetun fysiikkamoottorin, joka mahdollistaa realistisen vuorovaikutuksen pelimaailman objektien välillä. Se tukee ominaisuuksia, kuten jäykän kehon fysiikkaa, pehmeän kehon fysiikkaa ja ragdoll-fysiikkaa, mikä tekee siitä sopivan dynaamisten ja mukaansatempaavien ympäristöjen luomiseen.
    
3.  **Maasto ja kasvillisuus**: CryENGINE tarjoaa työkaluja laajojen ja yksityiskohtaisten ulkoympäristöjen luomiseen. Se tukee maaston muokkausta, kasvillisuuden sijoittamista ja dynaamisia sääjärjestelmiä, jolloin kehittäjät voivat luoda laajoja ja realistisia ulkoiluasetuksia.
    
4.  **Hahmoanimaatio**: CryENGINE sisältää vankat työkalut hahmoanimaatioon. Se tukee monimutkaisia hahmolaitteita, kasvojen animaatioita ja sekoituspuujärjestelmää, jonka avulla kehittäjät voivat luoda todentuntuisia hahmoliikkeitä ja animaatioita.
    
5.  **AI-järjestelmä**: Moottorissa on tekoälyjärjestelmä, joka mahdollistaa älykkäiden NPC:iden (ei-pelaajahahmojen) ja vihollisen tekoälyn luomisen. Kehittäjät voivat ohjelmoida tekoälykäyttäytymistä ja vuorovaikutuksia luodakseen haastavia ja mukaansatempaavia pelikokemuksia.
       
6.  **Komentosarjat**: CryENGINE käyttää Schematyc-nimistä komentosarjakieltä, jonka avulla kehittäjät voivat luoda pelilogiikkaa ja vuorovaikutuksia. Lisäksi se tukee C++:aa edistyneempiin ohjelmointitarpeisiin.

## CryENGINE:n käyttämät tiedostomuodot

Tässä on joitain yleisimpiä CryENGINEen liittyviä tiedostotyyppejä:

1.  **cryproj**: CryENGINE-projektitiedostot. Nämä tiedostot tallentavat tietyn peliprojektin projektikohtaiset asetukset ja määritykset.
    
2.  **.level**: Tasotiedostot sisältävät 3D-pelimaailman tietoja, mukaan lukien maaston, kohteet, valaistuksen ja muut tasokohtaiset asetukset. Tasot ovat pelisuunnittelun peruskomponentti CryENGINEssä.
    
3.  **.cgf**: merkkigeometrian muoto. Nämä tiedostot sisältävät 3D-mallitietoja hahmoista, esineistä ja muista pelien resursseista. CGF-tiedostot voivat sisältää geometriaa, pintakuvioita ja animaatiotietoja.
    
4.  **.chrparams**: Merkkiparametritiedostot. Nämä tiedostot tallentavat hahmomallien ja niiden animaatioiden asetukset ja määritykset.
    
5.  **.dds**: DirectX-tekstuurimuoto. CryENGINE käyttää yleisesti DDS-tiedostoja pintakuvioiden tallentamiseen, mukaan lukien hajakartat, normaalit kartat ja muut pintakuviointityypit.
    
6.  **.cryshader**: CryENGINE Shader -tiedostot. Nämä tiedostot määrittelevät, kuinka materiaalit ja esineet renderöidään pelimaailmassa, ja määrittävät varjostimet, materiaalin ominaisuudet ja paljon muuta.
    
7.  **.crytif**: Tekstuuritietotiedosto. Nämä tiedostot tallentavat pintakuvioita koskevia lisätietoja, kuten pakkausasetuksia, mipmapsia ja muita pintakuvioihin liittyviä yksityiskohtia.
    
8.  **.cdf**: merkin määritystiedosto. CDF-tiedostoja käytetään määrittämään merkkiresurssit ja niiden ominaisuudet, mukaan lukien liitteet, animaatiotilat ja hahmoihin liittyvät asetukset.
    
9.  **.dds**: CryENGINE käyttää myös DDS (DirectDraw Surface) -tiedostoja erilaisiin pintakuviokarttoihin, kuten normaaleihin karttoihin, peilikartoihin ja hajakarttoihin.
    
10.  **.anim**: Animaatiotiedostot. Nämä tiedostot tallentavat animaatiotietoja hahmoista ja objekteista, mukaan lukien avainkehykset, luun sijainnit ja animaatiosekvenssit.
    
11.  **.xml**: XML-tiedostoja voidaan käyttää erilaisiin CryENGINE-kokoonpanoihin ja tietojen määrittelyihin, kuten pelilogiikkaan, tekoälykäyttäytymiseen ja muihin.
    
12.  **.pak**: [PAK files](/game/pak/) ovat arkistotiedostoja, joita käytetään pelien resurssien ja resurssien pakkaamiseen, mikä tekee niistä tehokkaampia pelien jakelussa ja lataamisessa.

## Kuinka avata CHR -tiedosto?

Ohjelmat, jotka avaavat CHR-tiedostoja, sisältävät

- **Crytek CryENGINE SDK** (ilmainen kokeiluversio) Windowsille

## Muut CHR-tiedostot

Tässä on muita tiedostotyyppejä, jotka käyttävät **.chr**-tiedostotunnistetta.

**3D**
- {{HYPERLINKKI1}}
- {{HYPERLINKKI}}

**Fontti ja peli**
- {{HYPERLINKKI}}
- {{HYPERLINKKI1}}

## Viitteet
- {{HYPERLINKKI1}}

