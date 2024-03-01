{
  "date": "2023-06-12",
  "keywords": [
"bak",
"bak tiedosto",
"BAK Chromium -kirjanmerkit",
"mikä on bak-tiedosto",
"kuinka avata bak-tiedosto",
"tiedosto",
"bak tiedostopääte",
"laajennus"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "BAK-tiedostomuoto - Chromium Bookmarks Backup",
  "description": "Lue lisää BAK Chromium Bookmarks -muodosta ja sovellusliittymistä, jotka voivat luoda ja avata BAK-tiedostoja.",
  "linktitle": "BAK Chromium Bookmarks",
  "menu": {
    "docs": {
      "identifier": "misc-bak-chromium-fi",
      "parent": "misc"
}
},
  "lastmod": "2023-06-12"
}

## Mikä on BAK-tiedosto?

Chromium-pohjaisten verkkoselaimien, kuten Google Chromen ja Microsoft Edgen, yhteydessä .bak-tiedosto on pohjimmiltaan kirjanmerkkisi varmuuskopiotiedosto. Nämä kirjanmerkit tallennetaan pelkkänä tekstiluettelona, ja käytetty tiedostomuoto on JSON. Näiden .bak-tiedostojen tarkoitus on suojata kirjanmerkkejäsi tarjoamalla varmuuskopio, joka voidaan palauttaa, jos ne poistetaan vahingossa tai katoavat.

Chromium-pohjaiset selaimet, kuten Google Chrome, luovat rutiininomaisesti nämä varmuuskopiotiedostot ja antavat niille yleensä nimen Bookmarks.bak. Ne ovat pohjimmiltaan tilannekuva kirjanmerkeistäsi tietyllä hetkellä.

## Kuinka käyttää .bak-tiedostoa kirjanmerkkien palauttamiseen

1. **Etsi varmuuskopiotiedosto:** Se sijaitsee yleensä tietyssä Chromium-profiiliisi liitetyssä kansiossa. Tarkka sijainti voi vaihdella käyttöjärjestelmästäsi riippuen.

Windowsissa: Katso kohdasta `C:\Users\<YourUsername> \AppData\Local\Chromium\User Data\Default\Bookmarks.bak`.

macOS: Hae hakemistosta `~/Library/Application Support/Chromium/Default/Bookmarks.bak`.

Linuxissa: Tarkista `~/.config/chromium/Default/Bookmarks.bak`.

3. Varmista, että Chromium-selain on suljettu.
4. Nimeä Bookmarks.bak-tiedosto uudelleen poistamalla .bak-tunniste, joten sitä kutsutaan yksinkertaisesti Kirjanmerkit.
5. Käynnistä Chromium.

Kun .bak-tiedosto nimetään uudelleen Kirjanmerkit, Chromium käyttää sitä nykyisenä kirjanmerkkitiedostona, ja aiemmat kirjanmerkkisi pitäisi palauttaa.

## Chromium-kirjanmerkkien varmuuskopio

Chromium-kirjanmerkkien varmuuskopiointi on viisas varotoimenpide varmistaaksesi, ettet menetä tärkeitä tallennettuja verkkosivujasi ja URL-osoitteitasi. Chromium on avoimen lähdekoodin selain, joka toimii pohjana muille selaimille, kuten Google Chromelle ja Microsoft Edgelle. Varmuuskopioi Chromium-kirjanmerkkisi seuraavasti:

## Tapa 1: Manuaalinen varmuuskopiointi

1. **Avaa Chromium**: Käynnistä Chromium-selain tietokoneellasi.

2. **Access Bookmarks**: Click on the three vertical dots (menu icon) in the top-right corner of the browser window. From the dropdown menu, hover over "Bookmarks" to reveal the bookmarks submenu.

3. **Export Bookmarks**: In the bookmarks submenu, click on "Bookmark manager." This will open a new tab displaying your bookmarks.

4. **Export Bookmarks**: In the bookmark manager tab, click on the three vertical dots again (usually in the upper-right corner) to open the bookmarks manager menu. From this menu, select "Export bookmarks."

5. **Valitse sijainti**: Valitse, minne haluat tallentaa viedyn kirjanmerkkitiedoston tietokoneellesi. Oletustiedostonimi on bookmarks.html, mutta voit muuttaa sitä, jos haluat. Tallenna se paikkaan, jonka muistat.

6. **Tallenna**: Tallenna kirjanmerkkisi HTML-tiedostona napsauttamalla Tallenna- tai Vie-painiketta.

Kirjanmerkkisi on nyt varmuuskopioitu HTML-tiedostona. Voit kopioida tämän tiedoston ulkoiselle asemalle tai pilvitallennustilaan säilytystä varten.

## Tapa 2: Synkronoi Google-tilin kanssa (jos käytettävissä)

Jos olet kirjautunut sisään Google-tilille Chromiumissa, voit myös käyttää sisäänrakennettua synkronointiominaisuutta pitääksesi kirjanmerkkisi turvassa ja synkronoituna eri laitteiden välillä. Tällä tavalla kirjanmerkkisi varmuuskopioidaan automaattisesti Google-tilillesi.

1. **Avaa Chromium**: Käynnistä Chromium-selain ja varmista, että olet kirjautunut Google-tilillesi.

2. **Enable Sync**: Click on the three vertical dots (menu icon) in the top-right corner of the browser window and go to "Settings."

3. **Synkronointi ja Google-palvelut**: Napsauta Asetukset-välilehden vasemmasta sivupalkista Synkronointi ja Google-palvelut.

4. **Synkronoi tietosi**: Varmista Synkronointi-kohdassa, että Kirjanmerkit on käytössä. Tämä synkronoi kirjanmerkkisi Google-tilisi kanssa.

Kirjanmerkkisi varmuuskopioidaan nyt automaattisesti ja synkronoidaan Google-tilisi kanssa. Voit käyttää niitä kirjautumalla sisään Google-tilillesi millä tahansa laitteella, jossa on Chromium tai jokin muu Google-synkronointia tukeva selain.

Muista varmuuskopioida kirjanmerkkisi ajoittain myös manuaalisesti, varsinkin jos haluat paikallisen kopion, joka ei ole riippuvainen vain Google-tilisi synkronoinnista.

## Kuinka avata BAK-tiedosto

Jos haluat tutkia kirjanmerkkien varmuuskopion raakatietoja, voit avata Bookmarks.bak-tiedoston useilla tekstieditoreilla, kuten Microsoft Visual Studio Code (saatavilla useilla alustoilla), Microsoft Notepad (Windows-käyttäjille), Apple TextEdit. (Mac-käyttäjille) tai mikä tahansa muu valitsemasi tekstieditori. Näin voit tarkastella tiedoston sisältämiä kirjanmerkkejä ja metatietoja.

Voit avata Bookmarks.bak-tiedoston ja tarkastella sen sisältöä erilaisilla tekstinkäsittelyohjelmilla ja koodieditoreilla. Tässä on joitain yleisesti käytettyjä vaihtoehtoja:

1. Visual Studio Code (VS-koodi)
2. Muistio (Windows)
3. TextEdit (Mac)
4. Ylivoimaista tekstiä
5. Muistio++
6. Atomi
7. nano ja Vim (Linux)
8. WordPad (Windows)

## Muut BAK-tiedostot

Tässä on muita tiedostotyyppejä, jotka käyttävät **.bak**-tiedostotunnistetta.

**Tietokanta**
- {{HYPERLINKKI1}}
- {{HYPERLINKKI1}}
- {{HYPERLINKKI}}

**Peli**
- {{HYPERLINKKI1}}

**Sekalaista**
- {{HYPERLINKKI1}}
- {{HYPERLINKKI1}}
- {{HYPERLINKKI1}}
- {{HYPERLINKKI}}

**Asetukset**
- {{HYPERLINKKI1}}

## Viitteet
* [Chromium Bookmarks](https://www.chromium.org/user-experience/bookmarks/)
