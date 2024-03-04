{
  "date": "2023-09-27",
  "keywords": [
"plg",
"cfg failą",
"cfg celestia konfigūracijos failą",
"kas yra cfg failas",
"Kaip atidaryti cfg failą",
"failą",
"cfg failo plėtinys",
"pratęsimas"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "CFG failo formatas – Celestia konfigūracijos failas",
  "description": "Sužinokite apie CFG Celestia konfigūracijos failo formatą ir API, kurios gali kurti ir atidaryti CFG failus.",
  "linktitle": "CFG Celestia",
  "menu": {
    "docs": {
      "identifier": "settings-cfg-celestia-lt",
      "parent": "settings"
}
},
  "lastmod": "2023-09-27"
}

## Kas yra CFG failas?

Celestia konfigūracijos failas yra paprasto teksto failas, naudojamas Celestia, 3D visatos modeliavimo programa. Šie failai yra gyvybiškai svarbūs nustatant, kaip Celestia elgiasi, kokie dangaus objektai rodomi ir kaip atrodo programa. Tačiau šių failų redagavimas reikalauja kruopštaus dėmesio, nes netinkami pakeitimai gali sutrikdyti Celestia įkėlimo procesą ir neleisti jam tinkamai veikti.

## Celestija

Celestia yra nemokama atvirojo kodo 3D astronomijos modeliavimo programinė įranga, leidžianti vartotojams tyrinėti ir vizualizuoti visatą itin tikroviškai ir interaktyviai. Jį sukūrė Chrisas Laurelis ir pirmą kartą buvo išleistas 2000-ųjų pradžioje. Celestia galima Windows, MacOS ir Linux operacinėms sistemoms.

Pagrindinės Celestia savybės ir aspektai:

– **Realistiška 3D vizualizacija:** Celestia pateikia išsamų ir tikslų mūsų saulės sistemos, taip pat žvaigždžių, galaktikų ir kitų dangaus objektų vaizdą. Jis naudoja aukštos kokybės 3D modelius ir tekstūras, kad sukurtų vizualiai įtraukiančią patirtį.

- **Išsami dangaus duomenų bazė:** programinėje įrangoje yra didžiulė įmontuota žinomų dangaus objektų, įskaitant žvaigždes, planetas, mėnulius, asteroidus, kometas ir erdvėlaivius, duomenų bazė. Vartotojai gali lengvai rasti ir ištirti šiuos objektus.

– **Mokslinis tikslumas:** nors Celestia yra vizualizacijos įrankis, juo siekiama kuo tiksliau pavaizduoti dangaus objektus ir reiškinius, remiantis turimais moksliniais duomenimis.

## Celestia naudojami failų formatai

Celestia naudoja įvairius failų formatus įvairiems 3D astronomijos modeliavimo aspektams. Štai keletas pagrindinių Celestia naudojamų failų formatų:

1. **Konfigūracijos failai (.cel)**
- *Aprašymas*: paprasto teksto failai, leidžiantys vartotojams tinkinti Celestia elgesį, išvaizdą ir turinį.
- *Paskirtis*: tinkinti nustatymus, nustatyti vietas ir nurodyti dangaus objektus.

2. **3D modeliai ir tinkleliai**
- *Formatai*: [.3ds](/3d/3ds/), [.obj](/3d/obj/), [.dae](/3d/dae/), .ac
- *Aprašymas*: palaikomi 3D modelių failų formatai, naudojami dangaus kūnams ir erdvėlaiviams atvaizduoti.
- *Paskirtis*: 3D objektų rodymas Celestia viduje.

3. **Tekstūros failai**
- *Formatai*: [.jpg](/image/jpeg/), [.png](/image/png/), [.dds](/image/dds/)
- *Aprašymas*: šie failai suteikia dangaus kūnų paviršiaus tekstūras.
- *Paskirtis*: tekstūrų atvaizdavimas 3D modeliuose, kad vaizdas būtų tikroviškas.

4. **Žvaigždučių katalogai ir duomenų failai**
- *Formatai*: pasirinktiniai formatai, [.csv](/spreadsheet/csv/), [.tsv](/spreadsheet/tsv/)
- *Aprašymas*: duomenų failai, naudojami žvaigždėms ir kitiems dangaus objektams pavaizduoti, užtikrinant tikslų modeliavimą.
- *Paskirtis*: tikslus dangaus objektų vaizdavimas.

5. **Tekstūros kubo žemėlapiai**
- *Aprašymas*: kubo žemėlapiai naudojami tolimų dangaus objektų, pvz., galaktikų, atsiradimui imituoti.
- *Paskirtis*: nutolusių objektų atvaizdavimas tikroviškomis tekstūromis.

6. **Scenarijaus failai**
- *Aprašymas*: šiuose failuose yra pasirinktiniai scenarijai, parašyti Celestia scenarijų kalba.
- *Paskirtis*: leidžia vartotojams kurti dinamiškus įvykius ir animacijas Celestia visatoje.

## Celestia konfigūracijos failas

Čia yra pagrindinė apžvalga, ką galite padaryti su Celestia konfigūracijos failu:

1. **Vietos nustatymas**: galite nurodyti savo vietą Žemėje naudodami platumos, ilgumos ir aukščio parametrus. Tai leidžia Celestia tiksliai parodyti naktinį dangų iš jūsų padėties.

```
Location "My Location"
{
    Latitude 40.7128
    Longitude -74.0060
    Altitude 0
}
```

2. **Peržiūros parinkčių tinkinimas:** galite koreguoti įvairias peržiūros parinktis, pvz., matymo lauką, laiko nustatymus ir atvaizdavimo nuostatas.

```
Viewpoint
{
    Location "My Location"
    Follow "Earth"
    Eye [0.0 0.0 0.0]
    Center [0.0 0.0 0.0]
    Up [0.0 1.0 0.0]
    Fov 45
}

Time
{
    Date "2023-09-25T12:00:00.000Z"
    Clock "Now"
}

Rendering
{
    Atmosphere false
    Stars 7
    Planetshine 0.25
}

```

3. **Dangaus objektų įkėlimas:** prie modeliavimo galite pridėti dangaus objektų, pvz., žvaigždžių, planetų, asteroidų, erdvėlaivių ir kt. Kiekvienas objektas yra apibrėžtas konfigūracijos faile su jo savybėmis.

```
Star "Sun"
{
    RA 0
    Dec 0
    Distance 0
    AppMag -26.74
    SpectralType "G2V"
}

Planet "Earth"
{
    Parent "Sol"
    Texture "earth.jpg"
    Radius 6371
    EllipticalOrbit
    {
        Period 365.25
        SemiMajorAxis 149.6e6
        Eccentricity 0.017
        Inclination 0
        AscendingNode 0
        ArgOfPericenter 102.94
        MeanAnomaly 100.464
}
}
```

4. **Erdvėlaivių apibrėžimas:** galite sukurti savo išgalvotus erdvėlaivius arba naudoti tikrus, nurodydami jų parametrus, pvz., padėtį, orientaciją ir 3D modelius.

```
Spacecraft "Voyager 1"
{
    Parent "Sol"
    Class "spacecraft"
    Mesh "voyager.3ds"
    Radius 0.01
    EllipticalOrbit
    {
        Period 30700
        SemiMajorAxis 1.08e11
        Eccentricity 0.044
        Inclination 3.4
        AscendingNode 49.0
        ArgOfPericenter 44.0
        MeanAnomaly 35.0
}
}
```

5. **Scenarijų kūrimas:** galite rašyti scenarijus pasirinkta Celestia scenarijų kalba, kad sukurtumėte dinamiškus įvykius ir animacijas.

## Kaip atidaryti CFG failą?

Programos, kurios atidaro arba nurodo CFG failus

- Celestia (nemokama), skirta (Windows, Mac, Linux)

## Kiti CFG failai

Štai kiti failų tipai, kuriuose naudojamas **.cfg** failo plėtinys.

**Nustatymai**
- [CFG - Celestia Configuration File](/settings/cfg-celestia/)
- [CFG - Citrix Server Connection File](/settings/cfg-citrix/)
- [CFG - MAME Configuration File](/settings/cfg-mame/)
- [CFG - LightWave Configuration File](/settings/cfg-lightwave/)

**Žaidimas**
- [CFG - Wesnoth Markup Language File](/game/cfg-wesnoth/)
- [CFG - M.U.G.E.N Configuration File](/game/cfg-mugen/)
- [CFG - Source Engine Configuration File](/game/cfg-sourceengine/)

**Sistema ir kita**
- [CFG - CFG File](/system/cfg/)
- [CFG - Cal3D Model Configuration File](/misc/cfg-cal3d/)

## Nuorodos
* [Celestia](https://en.wikipedia.org/wiki/Celestia)


