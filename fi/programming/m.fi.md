{
  "date": "2019-10-11",
  "keywords": [
"M tiedosto",
"M",
"laajennus",
"muoto",
"M-tiedostomuoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "M - Matlabin lähdekooditiedosto",
  "description": "Opi Matlab .m Source Code -tiedostosta ja sovellusliittymistä, jotka voivat luoda ja avata MF-tiedostoja.",
  "linktitle": "M",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming--fim"
}
},
  "lastmod": "2020-09-10"
}

# M - Matlabin lähdekooditiedostot

## Mikä on M (Matlab) -tiedosto?

Tiedosto, jonka pääte on .m, on Matlabin käyttämä lähdekooditiedosto. Se on ohjelmointi- ja numeerinen laskenta-alusta, jota käytetään analysointiin, algoritmien kehittämiseen ja simulointimallinnukseen. Kuten muutkin ohjelmointitiedostomuodot, M-tiedosto sisältää lähdekoodia, joka suorittaa Matlab-komentoja kaavioiden piirtämiseksi, simulaatioiden suorittamiseksi ja muiden matemaattisten toimintojen suorittamiseksi. Yksi Matlab-simulaatio voi kattaa useita tällaisia .m-tiedostoja, jotka voivat luokitella sovelluksen komentosarjoiksi, luokiksi, funktioiksi tai ilmoituksiksi. Matlab M -tiedostot voidaan avata millä tahansa tekstieditorilla.

## Matlab M -tiedostomuoto - lisätietoja

Matlab .m -tiedostot ovat tekstitiedostoja, jotka sisältävät ohjelmointikoodin Matlab-ohjelmointikielellä. Ne voidaan avata ja muokata missä tahansa tekstieditorissa ja tallentaa takaisin suoritettaviksi Matlab-ohjelmistoon. Matlab itsessään sisältää Live Editorin, jota käytetään skriptien luomiseen, jotka ovat koodin, tulosteen ja muotoillun tekstin yhdistelmä.

### Matlab-funktiotiedostot

Kuten muutkin ohjelmointikielet, voit luoda .m-tiedoston, joka sisältää vain määritellyn funktion, joka suorittaa vain tietyn tehtävän. Tällaiset tiedostot tallennetaan myös .m-tunnisteella ja ne toteuttavat vain kyseiseen toimintoon liittyvät toiminnot.

### .M-tiedostoesimerkki

Seuraavassa on esimerkki Matlab-funktiotiedostosta, joka laskee ajan, joka kuluu objektin pudotukseen korkeudesta h.

```C++
function t= TimeToGround(h)  
  t=sqrt(h/4.9);
end
```

Tämän funktion kutsumiseksi Matlab-editorista tai toisesta .m-tiedostosta voidaan käyttää seuraavaa koodia.
```C++
TimeToGround(100)
```

## Viitteet

 * [Matlab – tuetut tiedostomuodot](https://www.mathworks.com/help/matlab/standard-file-formats.html)
 * [Matlabin käyttäminen](https://www.maths.unsw.edu.au/sites/default/files/MatlabSelfPaced/lesson0/MatlabLesson0_Mfiles.html)

# M - Objective-C -toteutustiedosto

## Mikä on M (Objective-C) -tiedosto?

M-tiedostoa kutsutaan myös toteutustiedostoksi, joka sisältää Objective-C-kielellä kirjoitetun luokan lähdekoodin, ohjelmointikielen, jota käytetään ohjelmistosovellusten kirjoittamiseen OS X:lle ja iOS:lle. Objective-C on tärkein ohjelmointikieli, jota Applen tärkeimmät API:t, Cocoa ja Cocoa Touch, käyttävät näille alustoille. Yksi tällä kielellä kehitetty ohjelmistosovellus voi sisältää useita .m-tiedostoja, jotka sisältävät ohjelmaluokkien toteutuksen. Ne voidaan avata Apple XCodella, jEditillä ja muilla yleisillä tekstieditoreilla.

## Objective-C M -tiedostomuoto - lisätietoja

M-tiedostot on kirjoitettu pelkkää tekstiä käyttäen Objective-C:n ohjelmointisyntaksia. Jokainen luokan metodi on määriteltävä kaikella tarvittavalla koodillaan näissä toteutustiedostoissa. Nämä toteutus M-tiedostot voivat tuoda yhden tai useamman .h-otsikkotiedoston vaatimusten mukaisesti. Tuontikäsky kertoo kääntäjälle, mistä tähän toteutustiedostoon kuuluva otsikkotiedosto löytyy. Tuontilausunto kirjoitetaan seuraavasti.

```C++
#import "network.h"
```

Jokainen M-tiedoston toteutus alkaa sitten @implementation-direktiivillä, jota seuraa toteutusluokan tiedostonimi. Tämän jälkeen kaikki menetelmätoteutukset, jotka on ilmoitettu otsikkotiedostossa.

### M-tiedostomuotoesimerkki

```C++
UrlConnection.m

#import "UrlConnection.h"

@implementation UrlConnection

(void)connect {
    // In here would be code to attempt a connection to the
    // specified URL, while possibly handling connection errors.
    //
}

 + (BOOL)canHandleRequest:(NSString \*)type
                   forUrl:(NSString \*)url {
    //And in here would be code to see if the given URL passed
    // in is capable of handling the HTTP request type specified
    // by the "type" parameter. It will return YES or NO.
 }

 @end
```

## Viitteet
 * [Tietoja tavoitteesta C](https://developer.apple.com/library/archive/documentation/Cocoa/Conceptual/ProgrammingWithObjectiveC/Introduction/Introduction.html#//apple_ref/doc/uid/TP40011210-CH1-SW1)
 * [Object-C-opas](https://blog.teamtreehouse.com/beginners-guide-objective-c-classes-objects)

