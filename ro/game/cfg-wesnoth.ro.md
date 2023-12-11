{
"data": "2023-09-27",
  "keywords": [
"cfg",
"fișier cfg",
"cfg wesnoth markup language file",
"Ce este un fișier cfg",
"cum se deschide fișierul cfg",
"fişier",
"extensie fișier cfg",
"extensie"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "fals",
"toc": true,
"title": "Format de fișier CFG - fișier Wesnoth Markup Language",
  "description":"Aflați despre formatul fișierului CFG Wesnoth Markup Language și despre API-urile care pot crea și deschide fișiere CFG.",
  "linktitle": "CFG Wesnoth",
  "menu": {
    "docs": {
      "identifier": "game-cfg-wesnoth",
      "parent": "game"
}
},
"lastmod": "2023-09-27"
}

## Ce este un fișier CFG?

Fișierul CFG este cunoscut și sub numele de **"Wesnoth Markup Language" (WML)**. Este un limbaj de marcare personalizat folosit în principal în jocul "Battle for Wesnoth", care este un joc de strategie pe rând. WML este folosit pentru a defini și personaliza diverse aspecte ale jocului, inclusiv scenarii, campanii, unități și multe altele. Este o modalitate prin care modderii și dezvoltatorii pot crea conținut pentru joc.

Este scris într-un format care seamănă cu o combinație de XML și scripting simplu. Iată o prezentare generală a unor elemente și structuri comune pe care le puteți găsi într-un fișier WML:

1. **Etichete:** WML folosește etichete pentru a defini diferite elemente din joc. Etichetele sunt incluse în paranteze unghiulare. De exemplu:

```
[unit]
    type=Elvish Archer
    hitpoints=25
[/unit]
```
    










2. **Atribute:** în cadrul etichetelor, puteți defini atribute pentru a specifica proprietăți sau valori asociate elementului. În exemplul de mai sus, "tip" și "hitpoints" sunt atribute.
    










3. **Matrice și matrice de matrice:** Puteți crea matrice de date și chiar matrice de matrice pentru a defini liste de unități, tipuri de teren sau alte elemente de joc.
    










4. **Declarații condiționate:** WML acceptă declarații condiționate pentru a controla fluxul jocului. De exemplu:

```
[if]
    condition=have_unit
    variable=x,y
[/if]
```
    










5. **Bucle:** Puteți utiliza bucle pentru a itera prin liste de articole sau pentru a efectua acțiuni în mod repetat.
    










6. **Include:** Puteți include și alte fișiere WML într-un fișier WML principal pentru a vă organiza și modulariza conținutul.
    










7. **Event Handlers:** Puteți defini event handlers pentru a declanșa acțiuni atunci când anumite evenimente apar în joc.
    











Iată un exemplu simplificat de fișier WML care definește o unitate personalizată:

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

## Bătălia pentru Wesnoth

"The Battle for Wesnoth" este un joc de strategie popular și open-source, bazat pe rând. Este disponibil pentru mai multe platforme, inclusiv Mac, Windows, Linux și multe altele. Dezvoltat de o comunitate dedicată de voluntari, jocul este cunoscut pentru jocul său profund și captivant, precum și pentru lumea sa fantastică bogată.

Caracteristicile cheie ale "Bătăliei pentru Wesnoth" includ:

1. **Setarea fantastică:** Jocul este plasat într-o lume fantastică cu diferite rase, inclusiv oameni, spiriduși, pitici, orci și multe altele. Tradiția și povestirea jocului sunt o parte integrantă a atractivității sale.
    










2. **Strategie pe ture:** Gameplay-ul este pe ture, în care jucătorii își iau timpul pentru a-și planifica și executa mișcările pe grile hexagonale. Combină lupta tactică cu luarea deciziilor strategice.
    










3. **Campanii:** Jocul oferă o gamă largă de campanii pentru un singur jucător, fiecare cu propria poveste, personaje și provocări. Jucătorii pot explora diferite narațiuni și scenarii.
    










4. **Multiplayer:** "Wesnoth" acceptă multiplayer online, permițând jucătorilor să concureze unul împotriva celuilalt în bătălii strategice. Modurile multiplayer includ joc în cooperare și meciuri competitive.

## Cum se deschide fișierul CFG?

Fișierele CFG, care sunt asociate în mod obișnuit cu Wesnoth Markup Language (WML) utilizat în jocul "The Battle for Wesnoth", pot fi editate cu ușurință folosind orice editor de text standard. Aceste fișiere conțin cod care poate fi citit de om, scris în WML, care definește diferite aspecte ale jocului, inclusiv scenarii, unități și campanii.

În timp ce puteți utiliza orice editor de text pentru a modifica fișierele CFG, unele editoare de text avansate precum Emacs și Vi au pluginuri de evidențiere a sintaxei WML disponibile. Aceste plugin-uri oferă codare și formatare utilă pentru a facilita utilizatorilor să distingă diferitele elemente și structuri din codul WML.

Programele care deschid sau fac referire la fișiere CFG includ

- Bătălia pentru Wesnoth (gratuit) pentru (Windows, MAC, Linux)
- Microsoft Notepad

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
* [The Battle for Wesnoth](https://en.wikipedia.org/wiki/The_Battle_for_Wesnoth)
