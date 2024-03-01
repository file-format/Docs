{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "APK - Mikä on APK-tiedosto?",
  "description": "Opi tuntemaan, mikä on APK-tiedosto ja sovellusliittymät, jotka voivat luoda ja avata APK-tiedostoja.",
  "linktitle": "APK",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-ap-fik"
}
},
  "lastmod": "2021-04-27"
}

## Mikä on APK-tiedosto?

Tiedosto, jonka laajennus on .apk, on Googlen Android-sovellustiedosto, jota käytetään sovellusten (sovellusten) asentamiseen Android-laitteisiin. Se luodaan suoritettavana tiedostona virallisella IDE Google Android Studiolla ja ladataan Google Play -kauppaan loppukäyttäjien ladattavaksi ja asennettavaksi. APK-tiedostoja voidaan luoda ja asettaa saataville manuaalista asennusta varten sekä ennen julkaisua Google Play Kaupassa. Tämä auttaa testaamaan luodun APK-pakettitiedoston toimivuutta ja käyttäytymistä. Siksi on varmistettava, että APK-tiedosto on luotettavasta lähteestä eikä sisällä haittaohjelmia.

## APK tiedostomuoto

APK-tiedostot on pakattu pakattuna [ZIP](/compression/zip/)-tiedostomuotoon, joka voidaan avata millä tahansa ZIP-tiedostonavausohjelmistolla. Tällaisen tiedoston .apk-tunniste voidaan nimetä uudelleen muotoon .zip ja avata tiedosto missä tahansa ZIP-sovelluksessa tai purkaa sen sisältö.

## APK-paketin sisältö

Yksi APK-tiedosto sisältää kaikki sen asentamiseen ja suorittamiseen tarvittavat tiedostot. ZIP-sovelluksella purettu APK-tiedosto sisältää seuraavat tiedostot ja kansiot.

 * `META-INF/`: Hakemisto, joka sisältää luettelotiedoston, allekirjoituksen ja luettelon arkiston resursseista
 * `lib/`: Hakemisto, joka sisältää käännetyn koodin, joka liittyy tiettyihin alustoihin, kuten armeabi-v7a, x86, arm64-v8a jne.
 * `res/`: Hakemisto, joka sisältää kääntämättömiä resursseja, kuten kuvia
 * `assets/`: Hakemisto, joka sisältää sovellusomaisuudet, jotka AssetManager voi noutaa.
 * `androidManifest.xml`: Sisältää APK-tiedoston nimen, versiotiedot ja sisällön
 * `classes.dex`: Nämä ovat koottuja Java-luokkia, joita voidaan ajaa Dalvik-virtuaalikoneella ja Android Runtimella
 * `resources.arsc`: Käännetty resurssitiedosto, kuten merkkijonot

## Kuinka avata APK-tiedostoja

APK-tiedostot on tarkoitettu asennettavaksi Android-laitteisiin. Lisäksi Windows 11 on ensimmäinen Windowsin versio, joka tukee virallisesti APK-tiedostojen asennusominaisuutta.

### Kuinka asentaa APK-tiedosto Android-laitteeseen

Voit asentaa APK-tiedoston Android-laitteeseesi seuraavien vaiheiden avulla.

 1. Lataa APK verkkoselaimella
 2. Napauta sitä – sinun pitäisi sitten nähdä sen latautuvan laitteesi yläpalkissa
 3. Kun se on ladattu, avaa Lataukset, napauta APK-tiedostoa ja napauta pyydettäessä Kyllä.

Näiden vaiheiden noudattaminen aloittaa sovelluksen asennuksen laitteellesi.

### APK-tiedoston avaaminen Windowsissa

Voit käyttää Android-emulaattoria Windows PC:ssä APK-tiedoston avaamiseen/käyttämiseen. BlueStacks on yksi tällainen Android-emulaattori, jota voidaan käyttää Android-emulaattorin avaamiseen Windowsissa. Jos käytät Windows 11:tä, olet onnekas, sillä Windows 11 tukee virallisesti mahdollisuutta asentaa APK-tiedostoja.

### Kuinka avata APK-tiedosto Macissa

Voit myös käyttää BlueStackia macOS:ssä ja avata APK-tiedostoja. Se on ilmainen Android-emulaattori ja tarjoaa sinulle mahdollisuuden käyttää sitä parhaana tapana käyttää vain Android-sovelluksia.

## Kuinka luoda APK-tiedosto

APK-tiedoston luominen edellyttää erikoistyökalujen ja kehitysympäristöjen käyttöä. Android-kehittäjät käyttävät ensisijaisesti Android Studiota, virallista integroitua kehitysympäristöä (IDE) Android-sovellusten kehittämiseen. Tässä on yleiskatsaus APK-tiedoston luomiseen liittyvistä vaiheista:

 1. **Asenna kehitysympäristö:** Asenna ja määritä Android Studio tietokoneellesi. Android Studio tarjoaa kattavan joukon työkaluja Android-sovellusten kehittämiseen, testaamiseen ja pakkaamiseen.
 1. **Kehitä sovelluksesi:** Kirjoita Android-sovelluksesi koodi Java- tai Kotlin-ohjelmointikielillä. Android Studio tarjoaa runsaasti ominaisuuksia ja resursseja, jotka auttavat sinua rakentamaan sovelluksesi, mukaan lukien koodieditorit, emulaattorit ja virheenkorjaustyökalut.
 1. **Rakenna sovellus:** Kun olet kirjoittanut koodin ja suunnitellut käyttöliittymän, käytä Android Studion rakennustyökaluja sovelluksesi kokoamiseen ja pakkaamiseen. Tämä prosessi luo APK-tiedostoa varten tarvittavat tiedostot ja resurssit.
 1. **Allekirjoita APK-tiedosto:** Ennen sovelluksen jakamista on tärkeää allekirjoittaa APK-tiedosto. Sovelluksen allekirjoitus varmistaa sovelluksen eheyden ja aitouden. Android Studion avulla voit luoda allekirjoitusavaimen ja allekirjoittaa APK-tiedostosi tällä avaimella.
 1. **Jaa APK-tiedosto:** Kun olet allekirjoittanut APK-tiedostosi, voit jakaa sitä eri kanavien kautta. Voit ladata sen Google Play Kauppaan jakelua varten laajalle yleisölle tai jakaa sen suoraan käyttäjille sähköpostitse, latauslinkkien tai muiden jakelualustojen kautta.

On syytä huomata, että Android Studiosta luotu APK-tiedosto on yleensä optimoitu tuotantokäyttöön. Kehitysprosessin aikana voit myös luoda virheenkorjaus-APK-tiedostoja, jotka ovat hyödyllisiä testaus- ja virheenkorjaustarkoituksiin, mutta joita ei ole tarkoitettu jakeluun.

## UKK

 * **Voivatko APK-tiedostot vahingoittaa laitettani?** APK-tiedostot voivat muodostaa uhan laitteille. Tämä johtuu mahdollisesta haittaohjelmien esiintymisestä niissä. Siksi on suositeltavaa suorittaa APK-tiedostot online-virustarkistukseen ennen asennuksen jatkamista. Lisäksi Android-virustorjuntasovelluksen käyttäminen on varovainen toimenpide. Vähentääksesi riskiä, että laitteesi joutuu petollisen ohjelman uhriksi, on parasta ladata luotettavista lähteistä, jotka tunnet ja joihin luotat.

 * **Ovatko APK-tiedostot laillisia?** APK-tiedostojen lataaminen ja niiden käyttäminen sovellusten asentamiseen muista lähteistä kuin Google Play Kaupasta on täysin lain rajoissa. APK, joka muistuttaa muotoja, kuten EXE tai ZIP, on tiedostomuoto. Vaikka Google oli tämän muodon edelläkävijä, se on avoin kaikille, jotka voivat luoda ja käyttää APK-tiedostoja.

 * **Kuinka löydän APK-tiedostoja Android-laitteeltani?** APK-tiedostot pysyvät piilossa käyttäjiltä, koska Android hallitsee sovellusten asennuksia taustalla joko Google Playn tai muun sovellusten jakelualustan kautta. Muista lähteistä ladatut APK-tiedostot löytyvät kuitenkin Android-tiedostonhallinnasta.

## Viitteet

* [APK-tiedostomuoto](https://en.wikipedia.org/wiki/Android_application_package)


