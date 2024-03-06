{
  "date": "2023-09-27",
  "keywords": [
"sk",
"cfg failu",
"cfg celestia konfigurācijas fails",
"kas ir cfg fails",
"kā atvērt cfg failu",
"failu",
"cfg faila paplašinājums",
"pagarinājumu"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "CFG faila formāts — Celestia konfigurācijas fails",
  "description": "Uzziniet par CFG Celestia konfigurācijas faila formātu un API, kas var izveidot un atvērt CFG failus.",
  "linktitle": "CFG Celestia",
  "menu": {
    "docs": {
      "identifier": "settings-cfg-celestia-lv",
      "parent": "settings"
}
},
  "lastmod": "2023-09-27"
}

## Kas ir CFG fails?

Celestia konfigurācijas fails ir vienkārša teksta fails, ko izmanto Celestia, 3D Visuma simulācijas programma. Šie faili ir ļoti svarīgi, lai pielāgotu, kā Celestia darbojas, kādi debess objekti tiek parādīti un kā programma parādās. Tomēr šo failu rediģēšana prasa rūpīgu uzmanību, jo nepareizas izmaiņas var traucēt Celestia ielādes procesu, neļaujot tam darboties pareizi.

## Celestia

Celestia ir bezmaksas atvērtā koda 3D astronomijas simulācijas programmatūra, kas lietotājiem ļauj izpētīt un vizualizēt Visumu ļoti reālistiskā un interaktīvā veidā. To izstrādāja Kriss Laurels, un tas pirmo reizi tika izlaists 2000. gadu sākumā. Celestia ir pieejama operētājsistēmām Windows, macOS un Linux.

Celestia galvenās iezīmes un aspekti ir:

- **Reālistiska 3D vizualizācija:** Celestia nodrošina detalizētu un precīzu mūsu Saules sistēmas, kā arī zvaigžņu, galaktiku un citu debess objektu attēlojumu. Tajā tiek izmantoti augstas kvalitātes 3D modeļi un faktūras, lai radītu vizuāli iespaidīgu pieredzi.

- **Plaša debesu datu bāze:** programmatūra ir aprīkota ar plašu iebūvētu datu bāzi ar zināmiem debess objektiem, tostarp zvaigznēm, planētām, pavadoņiem, asteroīdiem, komētām un kosmosa kuģiem. Lietotāji var viegli atrast un izpētīt šos objektus.

- **Zinātniskā precizitāte:** lai gan Celestia ir vizualizācijas rīks, tās mērķis ir pēc iespējas precīzāk attēlot debess objektus un parādības, pamatojoties uz pieejamajiem zinātniskajiem datiem.

## Celestia izmantotie failu formāti

Celestia izmanto dažādus failu formātus dažādiem savas 3D astronomijas simulācijas aspektiem. Šeit ir daži no galvenajiem Celestia izmantotajiem failu formātiem:

1. **Konfigurācijas faili (.cel)**
- *Apraksts*: vienkārša teksta faili, kas ļauj lietotājiem pielāgot Celestia uzvedību, izskatu un saturu.
- *Mērķis*: iestatījumu pielāgošana, atrašanās vietu noteikšana un debess objektu norādīšana.

2. **3D modeļi un tīkli**
- *Formāti*: [.3ds](/3d/3ds/), [.obj](/3d/obj/), [.dae](/3d/dae/), .ac
- *Apraksts*: atbalstītie 3D modeļu failu formāti, ko izmanto debess ķermeņu un kosmosa kuģu renderēšanai.
- *Mērķis*: Celestia 3D objektu attēlošana.

3. **tekstūras faili**
- *Formāti*: [.jpg](/image/jpeg/), [.png](/image/png/), [.dds](/image/dds/)
- *Apraksts*: šie faili nodrošina debess ķermeņu virsmas faktūras.
- *Mērķis*: tekstūru kartēšana 3D modeļos reālistiskam izskatam.

4. **Zvaigžņu katalogi un datu faili**
- *Formāti*: pielāgoti formāti, [.csv](/spreadsheet/csv/), [.tsv](/spreadsheet/tsv/)
- *Apraksts*: datu faili, ko izmanto, lai attēlotu zvaigznes un citus debess objektus, nodrošinot precīzu simulāciju.
- *Mērķis*: precīzs debess objektu attēlojums.

5. **Tektūras kubu kartes**
- *Apraksts*: kubu kartes tiek izmantotas, lai simulētu tālu debess objektu, piemēram, galaktiku, parādīšanos.
- *Mērķis*: attālu objektu renderēšana ar reālistiskām tekstūrām.

6. **Skriptu faili**
- *Apraksts*: šie faili satur pielāgotus skriptus, kas rakstīti Celestia skriptu valodā.
- *Mērķis*: ļauj lietotājiem izveidot dinamiskus notikumus un animācijas Celestia visumā.

## Celestia konfigurācijas fails

Šeit ir pamata pārskats par to, ko varat darīt ar Celestia konfigurācijas failu:

1. **Atrašanās vietas iestatīšana**: varat norādīt savu atrašanās vietu uz Zemes, izmantojot platuma, garuma un augstuma parametrus. Tas ļauj Celestia precīzi attēlot nakts debesis no jūsu atrašanās vietas.

```
Location "My Location"
{
    Latitude 40.7128
    Longitude -74.0060
    Altitude 0
}
```

2. **Skatīšanas opciju pielāgošana:** varat pielāgot dažādas skatīšanās opcijas, piemēram, skata lauku, laika iestatījumus un renderēšanas preferences.

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

3. **Debesu objektu ielāde:** simulācijai varat pievienot tādus debess objektus kā zvaigznes, planētas, asteroīdus, kosmosa kuģus un citus objektus. Katrs objekts ir definēts konfigurācijas failā ar tā īpašībām.

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

4. **Kosmosa kuģu noteikšana:** varat izveidot pats savus izdomātus kosmosa kuģus vai izmantot īstus, norādot to parametrus, piemēram, pozīciju, orientāciju un 3D modeļus.

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

5. **Skriptu izveide:** varat rakstīt skriptus Celestia pielāgotajā skriptu valodā, lai izveidotu dinamiskus notikumus un animācijas.

## Kā atvērt CFG failu?

Programmas, kas atver CFG failus vai atsaucas uz tiem

- Celestia (bezmaksas) operētājsistēmai Windows, Mac, Linux)

## Citi CFG faili

Šeit ir citi failu tipi, kas izmanto faila paplašinājumu **.cfg**.

**Iestatījumi**
- [CFG - Celestia Configuration File](/settings/cfg-celestia/)
- [CFG - Citrix Server Connection File](/settings/cfg-citrix/)
- [CFG - MAME Configuration File](/settings/cfg-mame/)
- [CFG - LightWave Configuration File](/settings/cfg-lightwave/)

**Spēle**
- [CFG - Wesnoth Markup Language File](/game/cfg-wesnoth/)
- [CFG - M.U.G.E.N Configuration File](/game/cfg-mugen/)
- [CFG - Source Engine Configuration File](/game/cfg-sourceengine/)

**Sistēma un citi**
- [CFG - CFG File](/system/cfg/)
- [CFG - Cal3D Model Configuration File](/misc/cfg-cal3d/)

## Atsauces
* [Celestia](https://en.wikipedia.org/wiki/Celestia)


