{
   "date":"2023-10-11",
   "keywords":[
"mtl",
"mtl tiedosto",
"mtl obj materiaalimallin kirjastotiedosto",
"kuinka avata mtl-tiedosto",
"tiedosto",
"mtl tiedostopääte",
"laajennus",
"tiedosto"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"MTL-tiedostomuoto - OBJ-materiaalimallin kirjastotiedosto",
   "description":"Opi MTL OBJ Material Template Library -tiedostomuodosta ja API-liittymistä, jotka voivat luoda ja avata MTL-tiedostoja.",
   "linktitle":"MTL",
   "menu":{
      "docs":{
         "identifier":"3d-mtl-fi",
         "parent":"3d"
}
},
   "lastmod":"2023-10-11"
}

## Mikä on MTL-tiedosto?

MTL-tiedosto, lyhenne sanoista **Material Template Library**, on paritiedostomuoto, jota käytetään 3D-tietokonegrafiikassa ja -mallintamisessa. Se yhdistetään usein **Wavefront OBJ -tiedostomuotoon**, joka on yleinen muoto 3D-mallien ja niihin liittyvien materiaalien ja pintakuvioiden tallentamiseen.

## MTL tiedostomuoto

**MTL-tiedostomuoto** liittyy 3D-tietokonegrafiikkaan, ja sitä käytetään usein yhdessä OBJ-tiedostomuodon (Wavefront .obj) kanssa. OBJ-tiedostot määrittävät 3D-geometrian ja MTL-tiedostot materiaaliominaisuudet niihin liittyville OBJ-tiedostoille.

Tässä on yksinkertainen esimerkki MTL-tiedostosta:

```
newmtl MaterialName
Ka 0.6 0.6 0.6    # Ambient color
Kd 0.8 0.8 0.8    # Diffuse color
Ks 1.0 1.0 1.0    # Specular color
Ns 100            # Shininess
d  1.0            # Dissolve (transparency)
map_Kd texture.jpg  # Diffuse texture map
```

Tässä esimerkissä:

- Ka edustaa ympäristön värejä.
- Kd edustaa hajaväriä.
- Ks edustaa hohtavaa väriä.
- Ns edustaa kiiltoa.
- d tarkoittaa liukenemista (läpinäkyvyyttä).
- `map_Kd` määrittää hajakuviokartan.

Näitä materiaaliominaisuuksia voidaan soveltaa 3D-mallin eri osiin, jotka on määritelty vastaavassa OBJ-tiedostossa.

**MTL-tiedosto on valinnainen ja OBJ-tiedostoja voidaan käyttää ilman siihen liittyviä MTL-tiedostoja**. MTL-tiedostojen käyttö mahdollistaa kuitenkin yksityiskohtaisemman ja realistisemman 3D-mallien renderöinnin määrittämällä pinnan ominaisuuksia ja tekstuureja.

## Materiaalimallikirjasto

Tässä on tärkeää tietoa MTL-tiedostoista:

1.  **Materiaalimääritykset**: .mtl-tiedosto sisältää määritelmät materiaaleille, joita käytetään 3D-objekteihin vastaavassa OBJ-tiedostossa. Jokainen materiaalimääritelmä määrittelee erilaisia ominaisuuksia, kuten värin, kiillon, läpinäkyvyyden ja tekstuurikartat.
    
2.  **Tekstipohjainen muoto**: .mtl-tiedostot ovat yleensä pelkkää tekstiä, mikä tarkoittaa, että niitä voidaan helposti muokata tekstieditorilla. Jokainen materiaalimääritelmä koostuu lauseista, jotka määrittelevät materiaalin attribuutit.
    
3.  **Tektuurikartoitus**: Yksi .mtl-tiedoston olennaisista tehtävistä on määrittää, kuinka pintakuvioita (kuvatiedostoja) kartoitetaan 3D-mallin pinnoille. Se määrittää tekstuuritiedoston polun ja kuinka se kääritään tai sovelletaan malliin.
    
4.  **Esimerkkejä MTL-lausekkeista**: Tässä on joitain esimerkkilauseita, joita saatat löytää .mtl-tiedostosta:
    
- newmtl MaterialName: Tämä määrittää uuden materiaalin nimellä MaterialName.
- `Ka rgb`: Materiaalin ympäristön väri, määritelty RGB-arvoina.
- `Kd rgb`: Materiaalin hajaväri, määritelty RGB-arvoissa.
- Ks rgb: Materiaalin spesifinen väri, määritelty RGB-arvoissa.
- Ns-arvo: materiaalin kiilto tai peilikuvan eksponentti.
- `map_Kd texturefile.jpg`: Määrittää materiaalille hajakuviokartan.
5.  **Useita materiaaleja**: OBJ-tiedosto voi viitata useisiin materiaaleihin, ja jokainen materiaali on määritelty .mtl-tiedostossa. Tämä mahdollistaa monimutkaiset 3D-mallit, joissa on erilaisia materiaaleja eri osiin.
    
6.  **Yhteensopivuus**: 3D-mallinnusohjelmistot ja renderöintikoneet tukevat laajasti .mtl-tiedostoja, mikä mahdollistaa 3D-mallien ja niiden materiaalien siirtämisen eri ohjelmistosovellusten välillä.

## Kuinka avata MTL -tiedosto?

MTL-tiedostot ovat tekstipohjaisia tiedostoja, joten ne voidaan avata millä tahansa tekstieditorilla, mukaan lukien

- Muistio (Windows)
- Notepad++ (Windows)
- Visual Studio Code
- Ylivoimainen teksti
- Atomi
- TextEdit (macOS)

Ohjelmat, jotka avaavat MTL-tiedostoja tai viittaavat niihin, sisältävät

- Adobe Photoshop 2023
- Autodesk Maya 2023
- MeshLab
- Cheetah3D

## Viitteet
* [Wavefront .obj-tiedosto](https://en.wikipedia.org/wiki/Wavefront_.obj_file)


