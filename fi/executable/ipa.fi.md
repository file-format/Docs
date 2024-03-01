{
  "date": "2021-08-30",
  "keywords": [
"ipa tiedosto",
"ipa tiedostomuoto",
"mikä on ipa-tiedosto",
"tiedosto",
"ipa esimerkki",
"ipa tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Opi IPA-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata IPA-tiedostoja.",
  "title": "IPA - iOS-sovelluspakettitiedosto",
  "linktitle": "IPA",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-ip-fia"
}
},
  "lastmod": "2021-08-30"
}

## Mikä on IPA-tiedosto?
Tiedosto, jonka laajennus on .ipa, kuuluu iOS:lle ja tunnetaan sovelluspakettitiedostona. Tämä on arkisto (pakattu [ZIP](/compression/zip/)-pakkauksella) tiedosto, joka tallentaa iOS-sovelluksen, mutta sovellus voidaan asentaa vain iOS- tai ARM-pohjaisiin MacOS-laitteisiin, kuten iPadiin, iPhoneen tai iPod Touchiin. Pääasiassa iTunesia, Apple Configurator 2:ta tai mitä tahansa kolmannen osapuolen ohjelmistoa voidaan käyttää IPA-tiedostojen asentamiseen.

## IPA-tiedostomuoto
IOS-kehittäjät, jotka kehittävät sovelluksia Apple Xcodella, tuntevat IPA-tiedostot hyvin, koska heidän on pakattava kehittämänsä sovellukset IPA-tiedostoiksi joko sovelluskaupan käyttöönottoa varten. Vaikka IPA-tiedostot on asennettu iOS-sovelluksina, voit kuitenkin myös purkaa ne nähdäksesi niiden sisältämät sovellustiedot. Koska IPA-tiedosto sisältää vain yhden binaarin matkapuhelimien ARM-arkkitehtuurille eikä se sisällä binaaria x86-arkkitehtuurille, monia .ipa-tiedostoja ei voi asentaa iPhone Simulatoriin.
### .ipa-tiedoston rakenne
Seuraava esimerkki näyttää IPA:n rakenteen:

```
/Payload/
/Payload/Application.app/
/iTunesArtwork
/iTunesArtwork@2x
/iTunesMetadata.plist
/WatchKitSupport/WK
/META-INF
```
Yllä oleva on sisäänrakennettu rakenne iTunesin ja App Storen tunnistamiseksi. Tämän rakenteen mukaan:
- Payload-hakemisto sisältää kaikki sovellustiedot.
- iTunes Artwork -tiedosto on 512 × 512 pikselin PNG-kuva, joka sisältää sovelluksen kuvakkeen, joka näkyy iTunesissa ja iPadin App Store -sovelluksessa.
- iTunesMetadata.plist sisältää erilaisia tietoja, kuten kehittäjän nimi ja tunnus, tekijänoikeustiedot, paketin tunniste, sovelluksen nimi, genre, julkaisupäivä, ostopäivä jne.
- META-INF-kansio sisältää vain metatiedot siitä, mitä ohjelmaa on käytetty IPA:n luomiseen.


## Viitteet 

* [.ipa - Wikipedia](https://en.wikipedia.org/wiki/.ipa)



