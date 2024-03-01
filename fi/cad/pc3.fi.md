{
  "date": "2023-05-09",
  "keywords": [
"pc3 tiedosto",
"mikä on pc3-tiedosto",
"kuinka luoda pc3-tiedosto AutoCADissa",
"mikä on pc3-tiedoston muoto",
"mitä pc3-tiedosto sisältää",
"tiedosto",
"pc3 tiedostopääte",
"laajennus"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "PC3-tiedostomuoto - AutoCAD Plotterin määritystiedosto",
  "description": "Opi PC3-muodosta ja API:ista, jotka voivat luoda ja avata PC3-tiedostoja.",
  "linktitle": "PC3",
  "menu": {
    "docs": {
      "identifier": "cad-pc3-fi",
      "parent": "cad"
}
},
  "lastmod": "2023-05-09"
}

## Mikä on PC3-tiedosto?

PC3-tiedosto AutoCADissa on piirturiasetustiedosto, joka sisältää tulostin- tai piirturiasetukset ohjelmistossa käytettäväksi.

Kun luot uuden piirturikokoonpanon, AutoCAD tallentaa kaikki tarvittavat tiedot tulostimesta tai piirturista PC3-tiedostoon. Tämä sisältää esimerkiksi paperikoot, marginaalit, resoluutiot ja muut käyttämääsi tulostimeen tai piirturiin liittyvät asetukset.

PC3-tiedoston avulla voit helposti asentaa ja määrittää tulostimen tai piirturin AutoCADissa. Jos haluat käyttää PC3-tiedostoa, valitse se Plot-valintaikkunan käytettävissä olevien plotterikokoonpanojen luettelosta.

Voit myös luoda mukautettuja PC3-tiedostoja muokkaamalla olemassa olevan PC3-tiedoston asetuksia tai luomalla uuden PC3-tiedoston tyhjästä käyttämällä Plotter Manageria AutoCADissa.

## Kuinka luoda PC3-tiedosto AutoCADissa?

Voit luoda piirturin määritystiedoston (PC3) AutoCADissa seuraavasti:

1. **Avaa Plotter Manager:** Kirjoita komentoriville PLOTTERMANAGER tai siirry nauhan Output-välilehdelle ja valitse Plotter Manager Plot-paneelista.
2. **Napsauta Add-A-Plotter Wizard:** Tämä käynnistää ohjatun toiminnon, joka opastaa sinua uuden plotterin määritystiedoston luomisessa.
3. **Valitse piirturin valmistaja ja malli:** Ohjattu toiminto kehottaa sinua valitsemaan tulostimesi tai piirturisi valmistajan ja mallin luettelosta. Jos tulostintasi tai piirturisi ei ole luettelossa, voit valita Oma tietokone ja selata ohjaintiedostoa.
4. **Valitse portti:** Valitse portti, johon tulostin tai plotteri on kytketty. Jos olet epävarma, tarkista tulostimen tai piirturin mukana tulleet asiakirjat.
5. **Määritä piirturiasetukset:** Ohjattu toiminto kehottaa sinua määrittämään piirturillesi erilaisia asetuksia, kuten paperikoon, resoluution ja värisyvyyden. Varmista, että olet määrittänyt nämä asetukset oikein tulostimellesi tai piirturillesi.
6. **Tallenna piirturikokoonpano:** Kun olet määrittänyt kaikki asetukset, ohjattu toiminto pyytää sinua antamaan uudelle piirturikokoonpanollesi nimen. Tämä luo uuden PC3-tiedoston ohjatun toiminnon määrittämään kansioon.
7. **Käytä uutta plotterikokoonpanoa:** Jos haluat käyttää uutta plotterikokoonpanoa AutoCADissa, siirry Plot-valintaikkunaan, valitse uusi plotterikokoonpano käytettävissä olevien plotterikokoonpanojen luettelosta ja määritä sitten piirturi tavalliseen tapaan.

Se siitä! Olet nyt luonut AutoCADiin uuden piirturin konfigurointitiedoston (PC3), jota voit käyttää piirustusten tulostamiseen tai piirtämiseen.

## Mikä on PC3-tiedoston muoto?

PC3-tiedostomuoto on patentoitu tiedostomuoto, jota Autodeskin AutoCAD-ohjelmisto käyttää. Se sisältää tietyn plotterin tai tulostimen kokoonpanoasetukset, mukaan lukien paperin koon, värisyvyyden, resoluution ja muut asetukset.

PC3-tiedosto on yleensä tallennettu Plotter Configuration -kansioon AutoCADin asennushakemistossa, ja se voidaan helposti jakaa käyttäjien tai tietokoneiden välillä yhdenmukaisten tulostus- ja piirtoasetusten varmistamiseksi.

PC3-tiedosto on pohjimmiltaan tekstitiedosto, joka sisältää XML-dataa, joka on koneellisesti luettava muoto tietojen tallentamiseen ja vaihtoon. Voit tarkastella ja muokata PC3-tiedoston sisältöä tekstieditorilla tai XML-editorilla, mutta on suositeltavaa, että käytät AutoCADin Plotter Manageria tehdäksesi muutoksia piirturikokoonpanoon, koska tämä varmistaa, että asetukset ovat oikein muotoiltu ja yhteensopivia ohjelmiston kanssa.

## Mitä PC3-tiedosto sisältää?

PC3-tiedosto AutoCADissa sisältää tulostimen tai piirturin kokoonpanoasetukset, jotka ovat ominaisia tietylle laitteelle tai ohjaimelle. AutoCAD käyttää näitä asetuksia tulostaakseen tai piirtääkseen piirustuksesi tarkasti ja varmistaakseen, että ne näyttävät aiotuiltasi.

Tässä on joitain asetuksia, jotka voidaan tallentaa PC3-tiedostoon:

- **Paperikoko:** Tämä määrittää tulostukseen tai piirtämiseen käytettävän paperin koon, kuten A4, Letter tai Mukautettu.
- **Piirtoalue:** Tämä määrittää piirustuksen osan, joka piirretään, kuten koko asettelu tai vain tietty ikkuna.
- **Pit-mittakaava:** Tämä määrittää mittakaavan, jolla piirustus tulostetaan tai piirretään, kuten 1:100 tai 1/4=1'-0.
- **Viivan paksuus:** Tämä määrittää piirustuksen viivojen paksuuden, mikä vaikuttaa siihen, miltä ne näyttävät tulostettaessa tai piirrettäessä.
- **Värisyvyys:** Tämä määrittää tulostuksessa tai piirtämisessä käytettävien värien määrän, kuten mustavalkoisena tai täysvärisenä.
- **Resoluutio:** Tämä määrittää resoluution, jolla piirustus tulostetaan tai piirretään, mikä vaikuttaa siihen, kuinka terävältä ja yksityiskohtaiselta se näyttää.
- **Muut asetukset:** PC3-tiedostossa voidaan määrittää monia muita asetuksia, kuten tulostuslaatu, suunta, marginaalit, varjostus ja paljon muuta.

Luomalla ja käyttämällä PC3-tiedostoa, joka sisältää oikeat asetukset tulostimellesi tai piirturillesi, voit varmistaa, että piirustuksesi tulostetaan tai piirretään tarkasti ja tasalaatuisina.

## Viitteet
* [PC3 AutoCADissa](https://www.autodesk.com/support/technical/article/caas/sfdcarticles/sfdcarticles/Creating-plotter-configuration-files-PC3.html)


