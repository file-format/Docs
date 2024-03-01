{
  "date": "2023-09-27",
  "keywords": [
"cfg",
"cfg-tiedosto",
"cfg wesnoth -kuvauskielitiedosto",
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
  "title": "CFG-tiedostomuoto - Wesnothin merkintäkielitiedosto",
  "description": "Opi CFG Wesnoth Markup Language -tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata CFG-tiedostoja.",
  "linktitle": "CFG Wesnoth",
  "menu": {
    "docs": {
      "identifier": "game-cfg-wesnoth-fi",
      "parent": "game"
}
},
  "lastmod": "2023-09-27"
}

## Mikä on CFG-tiedosto?

CFG-tiedosto tunnetaan myös nimellä **Wesnoth Markup Language (WML)**. Se on mukautettu merkintäkieli, jota käytetään ensisijaisesti Battle for Wesnoth -pelissä, joka on vuoropohjainen strategiapeli. WML:ää käytetään pelin eri osien määrittelyyn ja mukauttamiseen, mukaan lukien skenaariot, kampanjat, yksiköt ja paljon muuta. Se on tapa moddereille ja kehittäjille luoda sisältöä peliin.

Se on kirjoitettu muodossa, joka muistuttaa XML:n ja yksinkertaisen komentosarjan yhdistelmää. Tässä on yleiskatsaus joistakin yleisistä elementeistä ja rakenteista, joita saatat löytää WML-tiedostosta:

1.  **Tagit:** WML käyttää tunnisteita pelin eri elementtien määrittämiseen. Tagit on suljettu kulmasuluissa. Esimerkiksi:

```
[unit]
    type=Elvish Archer
    hitpoints=25
[/unit]
```
    
2.  **Attribuutit:** Tunnisteiden sisällä voit määrittää attribuutteja elementtiin liittyvien ominaisuuksien tai arvojen määrittämiseksi. Yllä olevassa esimerkissä type ja hitpoints ovat attribuutteja.
    
3.  **Matriisit ja Arrays of Arrays:** Voit luoda tietotaulukoita ja jopa matriiseja määrittääksesi luetteloita yksiköistä, maastotyypeistä tai muista pelielementeistä.
    
4.  **Ehdolliset lauseet:** WML tukee ehdollisia lauseita pelin kulun hallitsemiseksi. Esimerkiksi:

```
[if]
    condition=have_unit
    variable=x,y
[/if]
```
    
5.  **Silmukat:** Voit käyttää silmukoita selataksesi kohdeluetteloita tai suorittaaksesi toimintoja toistuvasti.
    
6.  **Sisältää:** Voit sisällyttää muita WML-tiedostoja WML-päätiedostoon sisällön järjestämiseksi ja moduloimiseksi.
    
7.  **Tapahtumakäsittelijät:** Voit määrittää tapahtumakäsittelijöitä käynnistämään toimintoja, kun pelissä tapahtuu tiettyjä tapahtumia.
    

Tässä on yksinkertaistettu esimerkki WML-tiedostosta, joka määrittää mukautetun yksikön:

```
[unit_type]
    id=my_custom_unit
    name="Custom Unit"
    description="A unit created using WML."
    image="units/my_custom_unit.png"
    hitpoints=30
    movement_type=foot
[/unit_type]
```

## Taistelu Wesnothin puolesta

The Battle for Wesnoth on suosittu ja avoimen lähdekoodin vuoropohjainen strategiapeli. Se on saatavana useille alustoille, kuten Macille, Windowsille, Linuxille ja muille. Vapaaehtoisyhteisön kehittämä peli tunnetaan syvästä ja mukaansatempaavasta pelattavuudestaan sekä rikkaasta fantasiamaailmastaan.

The Battle for Wesnothin tärkeimmät ominaisuudet ovat:

1.  **Fantasia-asetukset:** Peli sijoittuu fantasiamaailmaan, jossa on erilaisia rotuja, kuten ihmisiä, tonttuja, kääpiöitä, örkkejä ja paljon muuta. Pelin tarina ja tarinankerronta ovat olennainen osa sen vetovoimaa.
    
2.  **Vuoropohjainen strategia:** Peli on vuoropohjaista, jossa pelaajat suunnittelevat ja toteuttavat liikkeensä kuusikulmaisilla ruudukoilla. Siinä yhdistyvät taktinen taistelu ja strateginen päätöksenteko.
    
3.  **Kampanjat:** Peli tarjoaa laajan valikoiman yksinpelikampanjoita, joista jokaisella on oma tarinansa, hahmonsa ja haasteensa. Pelaajat voivat tutkia erilaisia kertomuksia ja skenaarioita.
    
4.  **Moninpeli:** Wesnoth tukee online-moninpeliä, jolloin pelaajat voivat kilpailla toisiaan vastaan strategisissa taisteluissa. Moninpelitilat sisältävät yhteistyöpelin ja kilpailuottelut.

## Kuinka avata CFG -tiedosto?

CFG-tiedostoja, jotka liittyvät yleisesti The Battle for Wesnoth -pelissä käytettyyn Wesnoth Markup Language (WML) -kieleen, voidaan helposti muokata millä tahansa tavallisella tekstieditorilla. Nämä tiedostot sisältävät WML-kielellä kirjoitettua ihmisen luettavaa koodia, joka määrittelee pelin eri näkökohdat, mukaan lukien skenaariot, yksiköt ja kampanjat.

Vaikka voit käyttää mitä tahansa tekstieditoria CFG-tiedostojen muokkaamiseen, joissakin edistyneissä tekstieditoreissa, kuten Emacsissa ja Vi:ssä, on saatavilla WML-syntaksin korostuslaajennuksia. Nämä laajennukset tarjoavat hyödyllistä värikoodausta ja muotoilua, jotta käyttäjät voivat erottaa WML-koodin eri elementit ja rakenteet helpommin.

Ohjelmat, jotka avaavat tai viittaavat CFG-tiedostoihin, sisältävät

- Battle for Wesnoth (ilmainen) (Windows, MAC, Linux)
- Microsoft Notepad

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
* [The Battle for Wesnoth](https://en.wikipedia.org/wiki/The_Battle_for_Wesnoth)
