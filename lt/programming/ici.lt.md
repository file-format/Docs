{
  "date": "2021-09-13",
  "keywords": [
"ici",
"failą",
"pratęsimas",
"Dokumento formatas",
"ICI įgyvendinimas",
"Programavimo vadovas",
"ici pavyzdys",
"ICI programavimo kalba",
"ICI moduliai",
"ICI duomenų modelis",
"ICI dokumentai",
"ICI kalba"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "ICI – programavimo kalbos failas",
  "description": "Sužinokite apie ICI failo formatą ir API, kurios gali kurti ir atidaryti ICI failus.",
  "linktitle": "ICI",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-ic-lti"
}
},
  "lastmod": "2021-09-13"
}

## Kas yra ICI failas?

Bendrosios paskirties programavimo kalba, kuri yra interpretuojama ir kurioje yra keletas funkcijų, tokių kaip dinaminis spausdinimas kartu su lanksčiais duomenų tipais, yra žinoma kaip ICI (ne akronimas) programavimo kalba. Manoma, kad ji panaši į [Perl](/programming/pl/) kalbą. Šią ICI kalbą sudaro srauto valdymo konstrukcijos, taip pat kai kurie C kalbos operatoriai. Tai nėra į objektą orientuota kalba, tačiau kai kurias OOP ypatybes galima pasiekti naudojant specifinį paveldėjimo metodą, vadinamą antstatais. Panašiai kaip [C](/programming/c), ši ICI programavimo kalba turi tą pačią sistemos sąsają ir standartinę integruotų funkcijų biblioteką.


## Trumpa istorija ##

Devintojo dešimtmečio pabaigoje Timas Longas ją sukūrė kaip bendrosios paskirties interpretuojamą programavimo kalbą. Dauguma šios kalbos ypatybių yra panašios į C ir kai kurias funkcijas ji taip pat gali pasiekti taikant specialius metodus. Ši kalba priklauso viešai ir yra prieinama kaip perparduodama kalba, todėl niekas neprivalo paminėti, iš kur jis gavo šaltinio kodą. ICI dokumentacijos autorių teisės priklauso Canon Information System Research Australia.

## Techninė specifikacija Nr.

Šioje kalboje naudojami du skirtingi duomenų tipai. Šie du yra primityviųjų ir bendrųjų duomenų tipai. Abu jie apima skirtingus posakius pagal iš anksto apibrėžtą kalbos sudėtį. Ši kalba palaiko įvairius modulius, tokius kaip įdėtieji ir paprogramės. Kadangi kai kurios jo savybės yra panašios į Perl, ji turi griežtą integraciją su reguliariosiomis išraiškomis.

Rinkiniai gali būti nevienalyčiai ir sudėti. Šie rinkiniai palaiko dažniausiai naudojamas rinkinio operacijas, tokias kaip Union ir Intersection ir tt. Ji dažniausiai naudojama kaip kalba, skirta pagrindiniam daugiašalėms organizacijoms priklausančių programų diegimui.

Beveik visų tipų programas galima parašyti šia kalba, o dažniausiai specifinės programos, kuriose naudojamos sudėtingos duomenų struktūros, yra parašytos ICI programavimo kalba. Programos gali apimti ICI įgyvendinimą taip, kad jos turėtų būti joje įrašytos. Funkcinės programos dalys gali būti įdiegtos ICI moduliais. ICI kalba šiek tiek primena C kalbą, tačiau ICI duomenų modelis yra gana aukštesnio lygio ir skiriasi tokiais tipais kaip žodynai (struct), rinkiniai, dinaminiai masyvai, reguliarios išraiškos ir (realios) eilutės.


## ICI failo formato pavyzdys ##

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

## Nuoroda ##

* [ICI programavimo kalba] (http://atrn.org/ici/doc/ici.html)




