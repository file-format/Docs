{
  "date": "2021-06-24",
  "keywords": [
"OSA",
"osittainen",
"laajennus",
"tiedosto",
"muoto",
"web",
"ladattu"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "OSA - Osittain ladattu tiedosto",
  "description": "Opi PART-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata PART-tiedostoja.",
  "linktitle": "PART",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-par-fit"
}
},
  "lastmod": "2021-06-24"
}

## Mikä on PART-tiedosto? ##

Osatiedosto tai .part-tunniste on osittain ladattu tiedosto. Sitä käytetään, kun lataukset ovat käynnissä tai ovat keskeytyneet minkä tahansa ongelman vuoksi, jolloin latausten hallintaohjelma voi jatkaa latausta aina kun mahdollista.
Tämä tarkoittaa, että selain, kuten Firefox tai tiedostonsiirtoohjelmat, kuten eMule, eMule plus, FlashGet jne. tallentaa osan tiedostosta, nimeltään Osatiedosto, kun lataus tapahtuu laitteessasi. Tämä osatiedosto näyttää, onko lataus käynnissä vai onko se keskeytynyt ennen valmistumista. Ei vain tämä, vaan PART-tiedosto tallentaa kaikki tiedot, kunnes lataus on valmis, minkä vuoksi jotkin niistä voidaan myöhemmin jatkaa, jos haluat aloittaa latauksen uudelleen.

## PART-tiedostomuoto ##

There are few browsers that break large download files into smaller downloads and assign each portion a .part extension. These files can be seen in the “Download” folder. Once the download is finished, the browser will combine all the PART files to give a final downloaded file. For example, while downloading a file from Firefox, the download manager will store the data being downloaded in a PART file and replaces the name with certain characters, and add a .part extension at the end, such as **doodle.or** becomes **JKzMn.or.part**. After completion, Firefox will remove the .part extension and the file will be ready to launch.
