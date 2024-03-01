{
  "date": "2021-06-30",
  "keywords": [
"exe-tiedosto",
"exe-tiedostomuoto",
"mikä on exe-tiedosto",
"tiedosto",
"exe esimerkki",
"exe tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": ".exe-tiedosto on Microsoftin suoritettava tiedosto, joka suoritetaan Windows-käyttöjärjestelmässä. Lisätietoja EXE-tiedostomuodosta.",
  "title": "Mikä on suoritettava EXE-tiedosto?",
  "linktitle": "EXE",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-ex-fie"
}
},
  "lastmod": "2021-06-30"
}

## Mikä on EXE-tiedosto?

Sana EXE on lyhenne sanoista **suoritettava**. .exe-tiedosto on ohjelma, joka voidaan suorittaa Microsoft Windows -käyttöjärjestelmässä. Sovelluskehittäjät julkaisevat enimmäkseen Windows-käyttöjärjestelmän ohjelmansa suoritettavassa muodossa exe-tiedostoina. Se on tavallinen tiedostomuoto sovellusten suorittamiseen Windowsissa. **Setup.exe**, **Install.exe** ja **cmd.exe** ovat joitain yleisiä ja tuttuja EXE-tiedostojen nimiä.

## EXE tiedostomuoto

MS-DOS-kääntäjät esiteltiin muistimalleissa, joissa on 64K muistirajoitus. Yleisenä ideana on asettaa eri segmenttirekisterit x86-suorittimeen (CS, DS, ES, SS) osoittamaan eri tai samoja segmenttejä, mikä mahdollistaa eriasteisen pääsyn muistiin. Jotkut erityiset muistimallit olivat:

- **Pieni**: Kaikki muistin käyttöoikeudet ovat 16-bittisiä (segmenttirekisterit eivät muutu). Tuottaa .COM-tiedoston .EXE-tiedoston sijaan.
- **Pieni**: Kaikki muistikäytöt ovat 16-bittisiä (segmenttirekisterit eivät muutu).
- **Compact**: Data-osoitteet sisältävät sekä segmentin että offsetin, DS- tai ES-rekisterien uudelleenlataamisen käytön yhteydessä ja sallivat jopa 1M dataa. Koodikäytöt eivät muuta CS-rekisteriä, vaan sallivat 64K koodia.
- **Keskitaso**: Koodiosoitteet sisältävät segmentin osoitteen, CS:n uudelleenlatauksen käytön yhteydessä ja jopa 1 miljoonan koodin sallimisen. Tietojen käyttö ei muuta DS- ja ES-rekistereitä, vaan sallii 64K dataa.
- **Suuri**: Sekä koodi- että dataosoitteet ovat (segmentti, offset) pareja, jotka lataavat aina segmentin osoitteet uudelleen. Koko 1M tavun muistitila on käytettävissä sekä koodille että datalle.
- **Huge**: Sama kuin suuressa mallissa, kääntäjä luo lisäaritmetiikkaa, joka mahdollistaa pääsyn yli 64 kt:n taulukoihin.

Kehittäjien on päätettävä, mikä malli valitaan luodessaan exe-tiedostoa.

### Kannettava EXE-tiedostomuoto

Kannettava suoritettava tiedostomuoto (PE) sisältää joukon informatiivisia otsikoita, seuraava on luettelo otsikoista:

- **DOS-otsikko**: MS-DOS-otsikko varmistaa joko taaksepäin yhteensopivuuden tai uusien tiedostotyyppien sulavan vähentämisen.
- **PE-otsikko**: Poikkeama 60 (0x3C) DOS-otsikon alusta on osoitin PE-tiedoston otsikkoon
- **COFF-otsikko**: COFF-otsikossa on tietoja, jotka ovat hyödyllisiä suoritettavalle tiedostolle, ja joitain tietoja, jotka ovat hyödyllisempiä objektitiedostolle.
- **PE valinnainen otsikko**: PE valinnainen otsikko esiintyy heti COFF-otsikon jälkeen, ja jotkut lähteet jopa näyttävät kaksi otsikkoa osana samaa rakennetta.
- **Osataulukko**: Välittömästi PE valinnaisen otsikon jälkeen löydämme osiotaulukon. Osiotaulukko koostuu IMAGE_SECTION_HEADER-rakenteiden joukosta.
- **Yhdistettävät osiot**: Voi säästää muistitilaa yhdistämällä kirjaston koodin useampaan kuin yhteen prosessiin.

## Voitko suorittaa EXE-tiedoston Macissa?

Exe-tiedostoja ei käytetä suoritettavina tiedostoina Mac OS:ssä. Jos kuitenkin haluat suorittaa exe-tiedoston Mac OS:ssä, voit käyttää seuraavia menetelmiä.

 1. **Wine** - Wine on täydellinen ratkaisu ihmisille, jotka haluavat käyttää PC-sovelluksiaan Mac-järjestelmissä. Se on lyhenne sanoista Wine Is Not A Emulator, mikä tarkoittaa. Wine luo saman hakemistoympäristön kuin Microsoft käyttää, jotta voit käyttää Windows-sovellustasi sen avulla.
 2. **Virtuaalikoneet** – Luo Windows-virtuaalikone Parallel Desktopilla tai VM Virtual Boxilla ja suorita sovelluksesi virtuaalikoneen sisällä.
 3. **Boot Camp** - Windows Boot Campin asentaminen ja määrittäminen Mac OS -käyttöjärjestelmään antaa sinun käyttää Windows-käyttöjärjestelmää Mac-koneessa.

## Viitteet

* [.exe- Wikipewdia](https://en.wikipedia.org/wiki/.exe)

* [x86 Disassembly/Windows Executable Files](https://en.wikibooks.org/wiki/X86_Disassembly/Windows_Executable_Files#MS-DOS_EXE_Files)


