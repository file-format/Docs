{
   "date":"2023-01-04",
   "keywords":[
"UPS",
"ups-tiedosto",
"ups korjaustiedosto",
"kuinka avata ups-tiedosto",
"tiedosto",
"ups tiedostopääte",
"laajennus",
"tiedosto"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"UPS-tiedostomuoto - UPS-korjaustiedosto",
   "description":"Opi UPS Patch File -muodosta ja sovellusliittymistä, jotka voivat luoda ja avata UPS-tiedostoja.",
   "linktitle":"UPS",
   "menu":{
      "docs":{
         "identifier":"game-ups-fi",
         "parent":"game"
}
},
   "lastmod":"2023-01-04"
}

## Mikä on UPS-tiedosto?

UPS-tiedosto, joka tulee sanoista **Universal Patching System**, on korjaustiedostotyyppi, jota käytetään videopelin tai muun ohjelmiston tietojen muokkaamiseen tai muutosten tekemiseen. UPS-tiedostoja käytetään tyypillisesti emulointiyhteisössä korjausten tai muutosten lisäämiseen vanhojen videopelien ROM-levyihin (Read-Only Memory).

## UPS-korjaustiedosto

Näin UPS-korjaustiedosto toimii:

1.  **Alkuperäiset tiedot:** Aloitat alkuperäisellä ROM-tiedostolla videopelistä tai ohjelmistosta, jota haluat muokata. Tämä ROM sisältää pelin koodin ja tiedot.
    
2.  **Korjaustiedosto:** UPS-korjaustiedosto luodaan käyttämällä erityistä korjausohjelmistoa. Tämä korjaustiedosto sisältää muutoksia, jotka haluat soveltaa alkuperäisiin tietoihin. Nämä muutokset voivat sisältää virheenkorjauksia, käännöskorjauksia tai muita muutoksia.
    
3.  **Paikkausprosessi:** Muutosten tekemiseen käytä UPS-korjaustyökalua, joka ottaa syötteenä alkuperäisen ROM- ja UPS-korjaustiedoston. Paikkaustyökalu soveltaa sitten UPS-korjaustiedostossa määritettyjä muutoksia alkuperäiseen ROM-muistiin ja luo muokatun version pelistä tai ohjelmistosta.
    
4.  **Tulos:** Tulos on korjattu tai muokattu ROM, joka sisältää muutoksia UPS-korjaustiedostosta. Tätä korjattua ROM-muistia voidaan sitten toistaa emulaattorilla tai käyttää muilla tavoilla tehdyistä muutoksista riippuen.
    

UPS-korjaustiedostot ovat suosittuja emulointiyhteisössä, koska niiden avulla käyttäjät voivat tehdä parannuksia tai muutoksia vanhoihin peleihin jakamatta koko pelin ROM-muistia, joka saattaa olla tekijänoikeuden alaista. Sen sijaan käyttäjät voivat jakaa vain muutoksia sisältävän UPS-korjaustiedoston, ja käyttäjät voivat ottaa sen käyttöön laillisesti omistamalleen alkuperäiselle ROM-levylleen.

UPS-päivitykset tarjoavat useita etuja verrattuna {{HYPERLINKKI}}:

1.  **Ei kokorajoitusta:** Toisin kuin IPS-korjaukset, jotka on rajoitettu 16 megatavuun, UPS-korjauksia voidaan käyttää minkä tahansa kokoisten tiedostojen kanssa. Tämä joustavuus tekee UPS:stä erityisen hyödyllisen isommille peleille ja ohjelmistoille.
    
2.  **Kaksisuuntainen korjaus:** UPS tukee kaksisuuntaista korjausta, mikä tarkoittaa, että yksi UPS-korjaus voi sekä lisätä että poistaa muutoksia peliin tai ohjelmistoon. Tämä ominaisuus yksinkertaistaa muutosten muokkaamista tai palauttamista, mikä parantaa käyttökokemusta.
    
3.  **CRC32-tarkistussummat:** UPS käyttää CRC32-tarkistussummia sisäänrakennettuna mekanismina varmistaakseen, että korjaukset asennetaan oikeaan peliin tai ohjelmistoon. Tämä tarkistussumman tarkistus auttaa säilyttämään korjattujen tiedostojen eheyden ja estää korjaustiedostojen tahattoman tai virheellisen käytön.

## Kuinka kiinnittää UPS-korjaus?

UPS-korjauksen asentamiseen tarvitset UPS-korjaustyökalun, kuten Lunar IPS (Windows), NUPS (Windows) tai MultiPatch (useita alustoja varten) ja alkuperäisen ROM-muistin pelistä tai ohjelmistoista, jotka haluat korjata.

## Kuinka avata UPS-tiedosto?

UPS-tiedostoja avaavia ohjelmia ovat mm

- **Lunar IPS** (Windows)
- **NUPS** (Windows)
- **MultiPatch** (useita alustoja varten)

## Viitteet
* [Lunar IPS](https://www.romhacking.net/utilities/240/)


