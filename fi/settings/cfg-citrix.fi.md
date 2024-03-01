{
  "date": "2023-09-27",
  "keywords": [
"cfg",
"cfg-tiedosto",
"cfg Citrix-palvelinyhteystiedosto",
"mikä on cfg-tiedosto",
"kuinka avata cfg-tiedosto",
"tiedosto",
"cfg tiedostopääte",
"laajennus"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "CFG-tiedostomuoto - Citrix-palvelinyhteystiedosto",
  "description": "Opi CFG Citrix Server Connection -tiedostomuodosta ja API:ista, jotka voivat luoda ja avata CFG-tiedostoja.",
  "linktitle": "CFG Citrix",
  "menu": {
    "docs": {
      "identifier": "settings-cfg-citrix-fi",
      "parent": "settings"
}
},
  "lastmod": "2023-09-27"
}

## Mikä on CFG-tiedosto?

CFG-tiedosto tunnetaan myös nimellä **Citrix Server Connection File**. Se on tärkeä komponentti, jota käytetään yhteyden muodostamiseen Citrix-palvelimeen. Tämä tiedosto sisältää tärkeitä tietoja, joita tarvitaan onnistuneeseen yhteyden muodostamiseen asiakaslaitteen ja Citrix-palvelimen välillä. Se sisältää yleensä tietoja, kuten palvelimen isäntänimen tai IP-osoitteen, tietyn käytettävän palvelimen portin ja todentamiseen vaadittavat tunnistetiedot, jotka usein sisältävät käyttäjänimen ja salasanan.

Nämä CFG-tiedostot ovat ratkaisevassa asemassa Citrix-asiakasohjelmiston määrittämisessä, jolloin käyttäjät voivat muodostaa yhteyden eri Citrix-palvelimiin saumattomasti. Ne toimivat määritystiedostoina, jotka virtaviivaistavat yhteysprosessia määrittämällä ennalta olennaiset parametrit, mikä vähentää käyttäjien tarvetta syöttää nämä tiedot manuaalisesti aina, kun he haluavat käyttää Citrix-palvelinta.

## Citrix palvelin

Citrix-palvelin, joka tunnetaan myös nimellä Citrix XenApp tai Citrix XenDesktop -palvelin, on Citrixin virtualisointiratkaisuissa käytettävä erikoispalvelin. Citrix on yritys, joka tarjoaa teknologiaa etäkäyttöön, sovellusten virtualisointiin ja työpöydän virtualisointiin. Citrix-palvelimilla on keskeinen rooli näissä ratkaisuissa helpottamalla sovellusten ja työpöytäympäristöjen toimittamista etäkäyttäjille tai asiakaslaitteille.

Näin Citrix-palvelin tyypillisesti toimii:

1.  **Sovellus- ja työpöytätoimitus**: Citrix-palvelimet isännöivät sovelluksia ja työpöytäympäristöjä. Sen sijaan, että ohjelmisto ajettaisiin suoraan käyttäjän laitteessa, sovellus tai työpöytä toimii Citrix-palvelimella, ja asiakaslaitteeseen siirretään vain käyttöliittymä. Tämän ansiosta käyttäjät voivat käyttää Windows-sovelluksia ja pöytätietokoneita useista eri laitteista, kuten PC-, Mac-, tablet-tietokoneista ja älypuhelimista.
    
2.  **Etäkäyttö**: Citrix-palvelimet mahdollistavat etäkäytön sovelluksiin ja työasemiin, jolloin käyttäjät voivat työskennellä missä tahansa Internet-yhteyden avulla. Tämä on erityisen arvokasta etä- ja hajautetuille ryhmille, koska se tarjoaa johdonmukaisen ja turvallisen tietojenkäsittelykokemuksen.
    
3.  **Kuorman tasapainotus**: Citrix-palvelimet toimivat usein klustereina tasapainottaakseen saapuvien yhteyksien kuormitusta. Kuormituksen tasapainotus varmistaa, että käyttäjien pyynnöt jakautuvat tasaisesti palvelimien kesken, mikä optimoi suorituskyvyn ja saatavuuden.

## Citrix-palvelinyhteystiedosto

Citrix-palvelinyhteystiedosto, jota usein kutsutaan CFG-tiedostoksi, on määritystiedosto, jota käytetään Citrix-ympäristöissä yhteyksien luomiseen asiakaslaitteiden ja Citrix-palvelimien välille. Citrix Server Connection -tiedostoon tyypillisesti sisältyvät keskeiset tiedot voivat sisältää:

1.  **Isäntänimi tai IP-osoite**: Tämä määrittää sen Citrix-palvelimen verkkosijainnin, johon asiakaslaitteen tulee muodostaa yhteys. Se tunnistaa, missä Citrix-resurssit isännöidään.
    
2.  **Palvelinportti**: Portin numero, jota käytetään yhteydenpitoon Citrix-palvelimen kanssa. Tämä varmistaa, että tiedot siirretään oikeaan palveluun palvelimella.
    
3.  **Käyttäjänimi ja salasana**: Käyttäjätunnukset, mukaan lukien käyttäjätunnus ja salasana, voidaan sisällyttää todennustarkoituksiin. Näiden tunnistetietojen avulla käyttäjät voivat todistaa henkilöllisyytensä ja saada pääsyn Citrixin resursseihin.
    
4.  **Yhteysasetukset**: CFG-tiedostot voivat sisältää erilaisia yhteysasetuksia, kuten salausasetuksia, istunnon aikakatkaisuarvoja ja näyttöasetuksia. Nämä asetukset auttavat määrittämään käyttökokemusta ja suojausparametreja.
    
5.  **Resurssien määritys**: Määrityksistä riippuen CFG-tiedosto voi määrittää, mitkä Citrix-resurssit (sovellukset tai työpöydät) käynnistetään, kun yhteys muodostetaan.

## Citrixin käyttämät tiedostomuodot

Citrix-palvelimet ja niihin liittyvät Citrix-tekniikat tukevat useita tiedostomuotoja sovellusten, työasemien ja sisällön toimittamiseksi etäkäyttäjille. Tässä on joitain yleisiä Citrix-palvelinten käyttöönotuksiin liittyviä tiedostomuotoja:

1.  **ICA (Independent Computing Architecture)**:
    
- **.ica**: ICA-tiedosto on Citrixin sovellusten ja työpöytätoimituksen ydinkomponentti. Se sisältää tietoja yhteyden muodostamisesta Citrix-palvelimeen, kuten palvelimen osoite, portti, salausasetukset ja näyttöasetukset. Kun käyttäjä napsauttaa Citrix-resurssia, [.ica](/misc/ica/)-tiedosto luodaan ja Citrix Receiver (tai Citrix Workspace) -asiakasohjelma käyttää sitä yhteyden muodostamiseen.
2.  **Citrix-vastaanotin (tai Citrix Workspace) -paketit**:
    
- **.exe**: Citrix Receiver- tai Citrix Workspace -asennuspaketit tulevat usein suoritettavassa muodossa eri käyttöjärjestelmille (esim. [.exe](/executable/exe/) Windowsille, [.dmg](/compression/dmg/) macOS:lle). Näiden pakettien avulla käyttäjät voivat asentaa asiakasohjelmistoja laitteilleen.
3.  **Citrix Workspace App (aiemmin Citrix Receiver)**:
    
- **.app**: macOS:ssä Citrix Workspace App on pakattu macOS-sovellustiedostoksi [.app](/executable/app/).
4.  **Web-selaimen yhteensopivuus**:
    
- Citrix-ratkaisuja voi käyttää verkkoselaimien kautta, tyypillisesti käyttämällä HTML5:tä verkkopohjaiseen käyttöön. Käyttäjät muodostavat yhteyden Citrixin resursseihin URL-osoitteiden kautta ilman erityisiä tiedostomuotoja.
5.  **Virtuaaliset työpöydän levykuvat**:
    
- **.vhd, .vhdx**: Citrix XenDesktop ja XenApp voivat toimittaa virtuaalisia työpöytiä ja sovelluksia käyttämällä virtuaalisen kiintolevyn [VHD](/disc-and-media/vhd/)- tai [VHDX](/disc-and-media/vhdx/)-tiedostoja.
6.  **Resurssien julkaisun metatiedot**:
    
- **.xml**: Citrixin järjestelmänvalvojat käyttävät usein [XML](/web/xml/)-tiedostoja määrittääkseen resurssien julkaisuasetuksia, mukaan lukien sovelluksen ominaisuudet, käyttöoikeuskäytännöt ja käyttäjämääritykset.
7.  **Tulostinohjaintiedostot**:
    
- Citrix-ympäristöt voivat vaatia tiettyjä tulostinohjaintiedostoja (esim. .inf) oikean tulostustoiminnan varmistamiseksi etäsovelluksia käytettäessä.
8.  **Käyttäjäprofiilin tiedot**:
    
- **.upm**: Citrix Profile Management voi tallentaa käyttäjäprofiilitiedot .upm-tiedostoihin tarjotakseen yhtenäisen käyttökokemuksen eri istunnoissa ja laitteissa.
9.  **Asetustiedostot**:
    
- **.conf**: Erilaisia konfiguraatiotiedostoja, eli niitä voidaan käyttää määrittämään asetuksia Citrixin komponenteille, kuten Citrix License Serverin kokoonpanotiedostot (esim. CtxLicChk.conf).
10.  **Citrix ADC (NetScaler) -kokoonpano**:

- **.nsconfig:** Citrix Application Delivery Controllers (ADC), joka tunnettiin aiemmin nimellä NetScaler, määritystiedostot tallentavat kuormituksen tasapainottamiseen, turvallisuuteen ja liikenteen hallintaan liittyviä asetuksia.

## Kuinka avata CFG -tiedosto?

Ohjelmat, jotka avaavat CFG-tiedostoja tai viittaavat niihin

- Citrix Access Client (Windows, MAC, Linux)

## Muut CFG-tiedostot

Tässä on muita tiedostotyyppejä, jotka käyttävät **.cfg**-tiedostotunnistetta.

**Asetukset**
- {{HYPERLINKKI1}}
- {{HYPERLINKKI1}}
- {{HYPERLINKKI1}}
- {{HYPERLINKKI1}}

**Peli**
- {{HYPERLINKKI1}}
- {{HYPERLINKKI1}}
- {{HYPERLINKKI1}}

**Järjestelmä ja muut**
- {{HYPERLINKKI1}}
- {{HYPERLINKKI1}}

## Viitteet
* [Citrix Virtual Apps](https://en.wikipedia.org/wiki/Citrix_Virtual_Apps)


