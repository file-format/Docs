{
  "date": "2021-04-23",
  "keywords": [
"RES tiedosto",
"kuinka avata res-tiedosto",
"mikä on res-tiedosto",
"laajennus",
"muoto",
"RES-tiedostomuoto"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "RES - C++ Compiled Resource Script",
  "description": "Opi RES-tiedostomuodosta RES-esimerkillä ja API-liittymillä, jotka voivat luoda ja avata RES-tiedostoja.",
  "linktitle": "RES",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-re-fis"
}
},
  "lastmod": "2021-04-23"
}

## Mikä on RES-tiedosto?
Tiedosto, jonka pääte tai pääte on .res, voi kuulua useisiin tiedostomuotoluokkiin. Tässä keskustelemme RES-tiedostomuodosta, joka on C++ Compiled Resource Script; Microsoft Resource Compiler (rc) -ohjelman luoma binääritiedosto, joka sisältää resurssitietoja; resurssimäärittelytiedoston sisällön perusteella; emoohjelmistoprojektinsa kannalta. .res-tiedosto muotoillaan yleensä uudelleen resurssiobjektitiedostoksi linkittääkseen sen sovelluksen suoritettavaan tiedostoon.

## RES-tiedostomuoto
RES-tiedostomuoto kuuluu Microsoft Resource Compilerille (rc). Resurssien kääntäjä on työkalu, joka kokoaa sovelluksesi käyttämiä resursseja, kuten kohdistimia, kuvakkeita, valikoita ja valintaikkunoita. Resurssitiedostoilla on yleensä .res-tunniste; sisältää resursseja, kuten kohdistimia, kuvia ja versiotietoja. RES-tiedosto voi olla 16- tai 32-bittinen resurssitiedosto.
## Resurssitiedostorakenne
Resurssitiedosto sisältää joukon erilaisia resurssimerkintöjä. Jokainen merkintä sisältää resurssiotsikon ja asiaankuuluvat tiedot. Resurssiotsikko on yleensä DWORD-tasoitettu tiedostossa ja sisältää seuraavat tiedot:

- **DWORD** määrittääksesi resurssin otsikon koon
- **DWORD** määrittääksesi resurssitietojen koon
- Resurssin tyyppi
- Resurssin nimi
- Lisätietoa resursseista

The resource header structure defines the format of the RES file. The data for the resource follows the resource header. Some resources also add a resource-specific group header pattern to provide information about a group of resources. Following are some of the resource entry types and their description:

### Accelerator Table Resources
Kiihdytintaulukko on resurssimerkintä RES-tiedostossa ilman ryhmäotsikkoa. **ACCELTABLEENTRY** -kuvio määrittää kiihdytintaulukon jokaisen merkinnän. RES-tiedostossa voi olla useita kiihdytintaulukoita.

### Kursori- ja kuvakeresurssit
Vaikka järjestelmä pitää jokaista kuvaketta ja kohdistinta yhtenä tiedostona, mutta ne tallennetaan RES-tiedostoihin ryhmänä kuvakeresursseja tai ryhmänä kursoriresursseja. Kuvake- ja kursoriresurssien tiedostomuodot ovat samat. Resurssiryhmän otsikko seuraa kaikkia yksittäisiä kuvakkeita tai kohdistinryhmän osia .res-tiedostossa.

### Valintaikkunan resurssit
Valintaikkuna toteutetaan myös resurssimerkinnäksi RES-tiedostossa. Se sisältää yhden **DLGITEMPLATE**-valintaikkunan otsikkokuvion ja yhden **DLGITEMPLATE**-kuvion kutakin valintaikkunan ohjausobjektia varten. **DLGTEMPLATEEX**- ja **DLGITEMTEMPLATEEX**-mallit selittävät laajennettujen valintaikkunaresurssien muodon.

### Fonttiresurssit
Valikkoresurssi sisältää **MENUHEADER**-kuvion ja sen jälkeen yhden tai useamman **NORMALMENUITEM**- tai **POPUPMENUITEM**-kuvion, yhden kullekin valikkomallin valikkokohdalle. Mallit **MENUEX_TEMPLATE_HEADER** ja **MENUEX_TEMPLATE_ITEM** selittävät laajennettujen valikkoresurssien muodon.

### Viestitaulukon resurssit
Viestitaulukko koostuu muotoillusta tekstistä, joka näytetään virheilmoituksena tai viestilaatikossa. Viestitaulukkoresurssin päämalli on **MESSAGE_RESOURCE_DATA** -rakenne.

### Versioresurssit
Versioresurssin päämalli on **VS_FIXEDFILEINFO**. Muita malleja ovat **VarFileInfo** kielitietoihin liittyvien tietojen tallentamiseen ja **StringFileInfo** mukautettujen merkkijonotietojen tallentamiseen.




## Viitteet

 * [Resource File Formats](https://learn.microsoft.com/en-us/windows/win32/menurc/resource-file-formats)
 
 

