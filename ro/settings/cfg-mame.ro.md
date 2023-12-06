{
"data": "2023-09-27",
  "keywords": [
"cfg",
"fișier cfg",
"fișier de configurare cfg mame",
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
"title": "Format fișier CFG - fișier de configurare MAME",
  "description":"Aflați despre formatul fișierului de configurare CFG MAME și despre API-urile care pot crea și deschide fișiere CFG.",
"linktitle": "CFG MAME",
  "menu": {
    "docs": {
      "identifier": "settings-cfg-mame",
      "parent": "settings"
}
},
"lastmod": "2023-09-27"
}

## Ce este un fișier CFG?

Fișierul CFG este un fișier XML de configurare a tastaturii utilizat de emulatorii de jocuri video arcade MAME. Este o componentă crucială pentru personalizarea comenzilor de la tastatură și a tastelor rapide pentru a se potrivi preferințelor jucătorului. Aceste fișiere stochează mapări și setări care determină modul în care tastatura interacționează cu emulatorul în timpul jocului. Editând acest fișier, utilizatorii își pot personaliza experiența de joc prin atribuirea tastelor specifice de la tastatură unor acțiuni din joc, cum ar fi inserarea monedelor, pornirea, mișcarea și diverse alte funcții.

## Fișierul de configurare MAME

MAME, care înseamnă **Multiple Arcade Machine Emulator**, este o aplicație software care vă permite să emulați și să jucați jocuri arcade pe computer. MAME folosește fișiere de configurare pentru a-și personaliza comportamentul și setările. Aceste fișiere de configurare sunt de obicei localizate în folderul `cfg` din directorul dvs. MAME.

Iată principalele fișiere de configurare pe care le puteți întâlni la configurarea și configurarea MAME:

1. **mame.ini:** Acesta este fișierul principal de configurare pentru MAME. Conține setări globale care se aplică tuturor jocurilor. Puteți găsi acest fișier în directorul rădăcină al instalării dvs. MAME.

1. **default.cfg:** Acest fișier stochează setările implicite pentru toate jocurile care nu au propriile fișiere de configurare. Este folosit ca alternativă pentru setările specifice jocului.

1. **game-specific.cfg:** Aceste fișiere sunt folosite pentru a stoca setările pentru jocuri individuale. Ele sunt de obicei denumite după fișierul ROM pentru jocul căruia îi corespund. De exemplu, dacă aveți un joc numit "pacman.zip", fișierul de configurare pentru acesta ar fi "pacman.cfg".

Iată câteva setări comune pe care le puteți găsi în fișierul de configurare MAME.

1. **rompath:** Specifică directorul în care se află ROM-urile jocurilor arcade.

1. **cfg_directory:** Specifică directorul în care sunt stocate fișierele de configurare specifice jocului.

1. **nvram_directory:** Specifică directorul în care sunt stocate fișierele RAM nevolatile (NVRAM). NVRAM stochează scoruri mari și alte date specifice jocului.

1. **artwork_directory:** Specifică directorul în care sunt stocate fișierele de artă (cum ar fi rame, marcaje și fluturași).

1. **samplepath:** Specifică directorul în care se află fișierele de sunet eșantion.

1. **cheatpath:** Specifică directorul în care se află fișierele cheat.

De asemenea, puteți configura diverse alte setări, cum ar fi opțiuni video și audio, comenzi și dispozitive de intrare. Pentru a modifica aceste setări, puteți deschide fișierul de configurare în editorul de text și puteți face modificările necesare.

## MAME

MAME, care înseamnă **"Multiple Arcade Machine Emulator",** este o aplicație software concepută pentru a emula și replica hardware-ul mașinilor arcade de epocă și consolelor de jocuri arcade. Le permite utilizatorilor să joace o bibliotecă vastă de jocuri arcade clasice pe computere moderne și alte dispozitive compatibile. MAME este un proiect open-source și a devenit un emulator de preferat pentru păstrarea și bucurarea istoriei bogate a jocurilor arcade.

1. **Emulare:** Scopul principal al MAME este de a emula cu acuratețe hardware-ul mașinilor arcade, inclusiv unitățile lor centrale de procesare (CPU), cipurile de sunet, cipurile grafice și dispozitivele de intrare. Acest nivel de acuratețe asigură că jocurile se comportă cât mai aproape de experiența arcade originală.

1. **Compatibilitate:** MAME acceptă o gamă largă de ROM-uri de jocuri arcade, făcându-l unul dintre cei mai cuprinzătoare emulatoare arcade disponibile. Poate rula jocuri de pe diverse platforme arcade, inclusiv jocuri clasice din anii '70, '80, '90 şi chiar unele titluri arcade mai recente.

1. **Conservare:** Una dintre misiunile principale ale MAME este de a păstra istoria jocurilor arcade. Prin emularea cu acuratețe a hardware-ului arcade, MAME ajută la prevenirea pierderii jocurilor clasice și se asigură că generațiile viitoare le pot experimenta așa cum au fost inițial.

1. **Front-End-uri:** Mulți utilizatori folosesc aplicații front-end care oferă interfață grafică pentru a gestiona și lansa jocuri prin MAME. Aceste front-end-uri facilitează navigarea în biblioteca extinsă de jocuri MAME.

## Cum se deschide fișierul CFG?

Programe care deschid sau fac referire la fișiere CFG

- MAME (gratuit) (Windows)
- ExtraMAME (probă)
- MacMAME (MAC)

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
* [MAME](https://en.wikipedia.org/wiki/MAME)

