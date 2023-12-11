{
"data": "2023-09-27",
  "keywords": [
"cfg",
"fișier cfg",
"fișier de configurare cfg celestia",
"Ce este un fișier cfg",
"cum se deschide fișierul cfg",
"fişier",
"extensie fișier cfg",
"extensie"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Format fișier CFG - Fișier de configurare Celestia",
  "description":"Aflați despre formatul fișierului de configurare CFG Celestia și despre API-urile care pot crea și deschide fișiere CFG.",
  "linktitle": "CFG Celestia",
  "menu": {
    "docs": {
      "identifier": "settings-cfg-celestia",
      "parent": "settings"
}
},
"lastmod": "2023-09-27"
}

## Ce este un fișier CFG?

Un fișier de configurare Celestia este un fișier text simplu utilizat de Celestia, programul de simulare a universului 3D. Aceste fișiere sunt vitale pentru personalizarea modului în care se comportă Celestia, ce obiecte cerești sunt afișate și cum apare programul. Cu toate acestea, editarea acestor fișiere necesită o atenție deosebită, deoarece modificările necorespunzătoare pot perturba procesul de încărcare al Celestia, împiedicându-l să ruleze corect.

## Celestia

Celestia este un software gratuit de simulare a astronomiei 3D, open-source, care permite utilizatorilor să exploreze și să vizualizeze universul într-un mod extrem de realist și interactiv. A fost dezvoltat de Chris Laurel și a fost lansat pentru prima dată la începutul anilor 2000. Celestia este disponibil pentru sistemele de operare Windows, macOS și Linux.

Caracteristicile și aspectele cheie ale Celestia includ:

- **Vizualizare 3D realistă:** Celestia oferă o reprezentare detaliată și precisă a sistemului nostru solar, precum și a stelelor, galaxiilor și a altor obiecte cerești. Utilizează modele și texturi 3D de înaltă calitate pentru a crea o experiență captivantă vizual.

- **Bază de date extinsă cerească:** Software-ul vine cu o bază de date vastă încorporată de obiecte cerești cunoscute, inclusiv stele, planete, luni, asteroizi, comete și nave spațiale. Utilizatorii pot localiza și explora cu ușurință aceste obiecte.

- **Acuratețe științifică:** În timp ce Celestia este un instrument de vizualizare, își propune să reprezinte obiectele și fenomenele cerești cât mai precis posibil, pe baza datelor științifice disponibile.

## Formate de fișiere utilizate de Celestia

Celestia utilizează diverse formate de fișiere pentru diferite aspecte ale simulării sale astronomice 3D. Iată câteva dintre formatele cheie de fișiere folosite de Celestia:

1. **Fișiere de configurare (.cel)**
- *Descriere*: fișiere text simplu care permit utilizatorilor să personalizeze comportamentul, aspectul și conținutul Celestia.
- *Scop*: Personalizarea setărilor, definirea locațiilor și specificarea obiectelor cerești.

2. **Modele și rețele 3D**
- *Formate*: [.3ds](/ro/3d/3ds/), [.obj](/ro/3d/obj/), [.dae](/ro/3d/dae/), .ac
- *Descriere*: Formate de fișiere model 3D acceptate utilizate pentru redarea corpurilor cerești și a navelor spațiale.
- *Scop*: Afișarea obiectelor 3D în Celestia.

3. **Fișiere texturi**
- *Formate*: [.jpg](/ro/image/jpeg/), [.png](/ro/image/png/), [.dds](/ro/image/dds/)
- *Descriere*: Aceste fișiere oferă texturi de suprafață pentru corpurile cerești.
- *Scop*: Maparea texturilor pe modele 3D pentru un aspect realist.

4. **Cataloage cu stea și fișiere de date**
- *Formate*: formate personalizate, [.csv](/ro/spreadsheet/csv/), [.tsv](/ro/spreadsheet/tsv/)
- *Descriere*: Fișiere de date utilizate pentru a reprezenta stelele și alte obiecte cerești, asigurând o simulare precisă.
- *Scop*: Reprezentarea exactă a obiectelor cerești.

5. **Texture Cube Maps**
- *Descriere*: Hărțile cuburilor sunt folosite pentru a simula aspectul obiectelor cerești îndepărtate, cum ar fi galaxiile.
- *Scop*: Redarea obiectelor îndepărtate cu texturi realiste.

6. **Fișiere script**
- *Descriere*: Aceste fișiere conțin scripturi personalizate scrise în limbajul de scripting al Celestia.
- *Scop*: Permite utilizatorilor să creeze evenimente și animații dinamice în universul Celestia.

## Fișierul de configurare Celestia

Iată o prezentare generală a ceea ce puteți face cu fișierul de configurare Celestia:

1. **Setarea locației dvs.**: vă puteți specifica locația pe Pământ folosind parametrii de latitudine, longitudine și altitudine. Acest lucru îi permite Celestia să afișeze cu precizie cerul nocturn din poziția ta.

```
Location "My Location"
{
    Latitude 40.7128
    Longitude -74.0060
    Altitude 0
}
```

2. **Personalizarea opțiunilor de vizualizare:** Puteți ajusta diverse opțiuni de vizualizare, cum ar fi câmpul de vizualizare, setările de timp și preferințele de randare.

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

3. **Încărcarea obiectelor cerești:** Puteți adăuga obiecte cerești, cum ar fi stele, planete, asteroizi, nave spațiale și multe altele la simulare. Fiecare obiect este definit în fișierul de configurare cu proprietățile sale.

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

4. **Definirea navelor spațiale:** Puteți să vă creați propriile nave spațiale fictive sau să le folosiți pe cele reale, specificând parametrii acestora, cum ar fi poziția, orientarea și modelele 3D.

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

5. **Crearea de scripturi:** Puteți scrie scripturi în limbajul de scriptare personalizat al Celestia pentru a crea evenimente și animații dinamice.

## Cum se deschide fișierul CFG?

Programe care deschid sau fac referire la fișiere CFG

- Celestia (gratuit) pentru (Windows, Mac, Linux)

## Alte fișiere CFG

Iată și alte tipuri de fișiere care folosesc extensia de fișier **.cfg**.

**Setari**
- [CFG - Celestia Configuration File](/ro/settings/cfg-celestia/)
- [CFG - Fișier de conexiune la server Citrix](/ro/settings/cfg-citrix/)
- [CFG - Fișier de configurare MAME](/ro/settings/cfg-mame/)
- [CFG - Fișier de configurare LightWave](/ro/settings/cfg-lightwave/)

**Joc**
- [CFG - Wesnoth Markup Language File](/ro/game/cfg-wesnoth/)
- [CFG - Fișier de configurare MUGEN](/ro/game/cfg-mugen/)
- [CFG - Fișier de configurare a motorului sursă](/ro/game/cfg-sourceengine/)

**Sistem și diverse**
- [CFG - Fișier CFG](/ro/system/cfg/)
- [CFG - Fișier de configurare a modelului Cal3D](/ro/misc/cfg-cal3d/)

## Referințe
* [Celestia](https://en.wikipedia.org/wiki/Celestia)

