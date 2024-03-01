{
  "date": "2021-09-13",
  "keywords": [
"ici",
"tiedosto",
"laajennus",
"tiedosto muoto",
"ICI:n käyttöönotto",
"Ohjelmointiopas",
"ici esimerkki",
"ICI ohjelmointikieli",
"ICI:n moduulit",
"ICI:n tietomalli",
"ICI:n asiakirjat",
"ICI kieli"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "ICI - ohjelmointikielitiedosto",
  "description": "Opi ICI-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata ICI-tiedostoja.",
  "linktitle": "ICI",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-ic-fii"
}
},
  "lastmod": "2021-09-13"
}

## Mikä on ICI-tiedosto?

Yleiskäyttöinen ohjelmointikieli, jota tulkitaan ja joka sisältää useita ominaisuuksia, kuten dynaamisen kirjoittamisen sekä joustavia tietotyyppejä, tunnetaan nimellä ICI (ei lyhenne) -ohjelmointikieli. Sen katsotaan olevan samanlainen kuin {{HYPERLINKKI}}-kieli. Tämä ICI-kieli sisältää vuonohjauskonstrukteja ja sisältää myös joitain C-kielen operaattoreita. Se ei ole oliokieli, mutta jotkin OOP:n ominaisuudet voidaan saavuttaa tietyllä periytymismenetelmällä, joka tunnetaan superrakenteina. Kuten [C](/programming/c), tällä ICI-ohjelmointikielellä on sama järjestelmäliittymä ja vakiokirjasto sisäänrakennetuille toiminnoille.


## Lyhyt historia ##

Tim Long kehitti sen 1980-luvun lopulla yleiskäyttöiseksi tulkituksi ohjelmointikieleksi. Suurin osa tämän kielen ominaisuuksista on samankaltainen kuin C, ja se voi myös saavuttaa joitain ominaisuuksia käyttämällä joitain erikoismenetelmiä. Tämä kieli on omistettu julkisesti ja se on saatavilla jälleenmyyntikielenä, eikä kenenkään ole pakko mainita, mistä hän sai lähdekoodin. ICI:n dokumentaatio on Canon Information System Research Australian tekijänoikeuden alainen.

## Tekniset tiedot ##

Tällä kielellä käytetään kahta eri tietotyyppiä. Nämä kaksi ovat primitiivi- ja koostetietotyyppejä. Molemmat sisältävät erilaisia ilmaisuja niiden ennalta määritetyn kielen koostumuksen mukaan. Tämä kieli tukee erilaisia moduuleja, kuten sisäkkäisiä ja alirutiineja. Koska jotkut sen ominaisuuksista ovat samankaltaisia kuin Perl, se on tiukka integraatio säännöllisten lausekkeiden kanssa.

Joukot on rajoitettu heterogeenisiksi ja sisäkkäisiksi. Nämä joukot tukevat yleisesti käytettyjä joukkotoimintoja, kuten Union ja Intersection jne. Sitä käytetään useimmiten kielenä monikansallisten organisaatioiden omistamien sovellusten ydintoteutuksen vuoksi.

Lähes kaiken tyyppisiä ohjelmia voidaan kirjoittaa tällä kielellä, ja useimmiten erityisohjelmat, jotka sisältävät monimutkaisia tietorakenteita, kirjoitetaan ICI-ohjelmointikielellä. Sovellukset voivat sisältää ICI-toteutuksen siten, että ne pitäisi kirjoittaa siihen. Sovelluksen toiminnalliset osat voidaan toteuttaa ICI:n moduuleilla. ICI:n kieli muistuttaa jonkin verran C-kieltä, mutta ICI:n tietomalli on melko korkeatasoinen ja erilainen tyypeillä, kuten sanakirjat (struct), joukot, dynaamiset taulukot, säännölliset lausekkeet ja (todelliset) merkkijonot.


## ICI-tiedostomuodon esimerkki ##

```

printf("Hello world.\n");

```

```
s = [set 200, 300, "a string"];
if (s[200])
	printf("200 is in the set\n");
if (s[400])
	printf("400 is in the set\n");
if (s["a string"])
	printf("\"a string\" is in the set\n");
s[200] = 0;
if (s[200])
	printf("200 is in the set\n");

```

```

forall (colour in [array "red", "green", "blue"])
	printf("%s\n", colour);

```

## Viite ##

* [ICI-ohjelmointikieli](http://atrn.org/ici/doc/ici.html)




