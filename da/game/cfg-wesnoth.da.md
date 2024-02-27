{
  "date": "2023-09-27",
  "keywords": [
"cfg",
"cfg fil",
"cfg wesnoth markup sprogfil",
"hvad er en cfg-fil",
"hvordan man åbner cfg fil",
"fil",
"cfg filtypenavn",
"udvidelse"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "CFG-filformat - Wesnoth Markup Language File",
  "description": "Lær om CFG Wesnoth Markup Language File format og API'er, der kan oprette og åbne CFG filer.",
  "linktitle": "CFG Wesnoth",
  "menu": {
    "docs": {
      "identifier": "game-cfg-wesnoth-da",
      "parent": "game"
}
},
  "lastmod": "2023-09-27"
}

## Hvad er en CFG fil?

CFG-filen er også kendt som **Wesnoth Markup Language (WML)**. Det er et brugerdefineret markup-sprog, der primært bruges i spillet Battle for Wesnoth, som er et turbaseret strategispil. WML bruges til at definere og tilpasse forskellige aspekter af spillet, herunder scenarier, kampagner, enheder og mere. Det er en måde for moddere og udviklere at skabe indhold til spillet.

Det er skrevet i et format, der ligner en kombination af XML og simpel scripting. Her er en oversigt over nogle almindelige elementer og strukturer, du kan finde i en WML-fil:

1.  **Tags:** WML bruger tags til at definere forskellige elementer i spillet. Tags er omgivet af vinkelbeslag. For eksempel:

```
[unit]
    type=Elvish Archer
    hitpoints=25
[/unit]
```
    
2.  **Attributter:** Inden for tags kan du definere attributter for at specificere egenskaber eller værdier forbundet med elementet. I eksemplet ovenfor er type og hitpoints attributter.
    
3.  **Arrays og arrays af arrays:** Du kan oprette arrays af data og endda arrays af arrays for at definere lister over enheder, terræntyper eller andre spilelementer.
    
4.  **Betingede erklæringer:** WML understøtter betingede erklæringer til at kontrollere spillets flow. For eksempel:

```
[if]
    condition=have_unit
    variable=x,y
[/if]
```
    
5.  **Sløjfer:** Du kan bruge løkker til at gentage lister over emner eller udføre handlinger gentagne gange.
    
6.  **Inkluderer:** Du kan inkludere andre WML-filer i en WML-hovedfil for at organisere og modularisere dit indhold.
    
7.  **Hændelseshandlere:** Du kan definere hændelseshandlere til at udløse handlinger, når specifikke hændelser opstår i spillet.
    

Her er et forenklet eksempel på en WML-fil, der definerer en brugerdefineret enhed:

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

## Slaget om Wesnoth

The Battle for Wesnoth er et populært og open source turbaseret strategispil. Den er tilgængelig til flere platforme, inklusive Mac, Windows, Linux og mere. Spillet er udviklet af et dedikeret fællesskab af frivillige og er kendt for sit dybe og engagerende gameplay såvel som sin rige fantasiverden.

Nøgletræk ved Kampen om Wesnoth inkluderer:

1.  **Fantasy-indstilling:** Spillet foregår i en fantasiverden med forskellige racer, inklusive mennesker, elvere, dværge, orker og mere. Spillets historie og historiefortælling er en integreret del af dets appel.
    
2.  **Turn-Based Strategy:** Gameplayet er tur-baseret, hvor spillere tager sig tid til at planlægge og udføre deres træk på sekskantede gitter. Den kombinerer taktisk kamp med strategisk beslutningstagning.
    
3.  **Kampagner:** Spillet tilbyder en bred vifte af enkeltspillerkampagner, hver med sin egen historie, karakterer og udfordringer. Spillere kan udforske forskellige fortællinger og scenarier.
    
4.  **Multiplayer:** Wesnoth understøtter online multiplayer, hvilket giver spillerne mulighed for at konkurrere mod hinanden i strategiske kampe. Multiplayer-tilstande inkluderer samarbejdsspil og konkurrerende kampe.

## Hvordan åbner jeg filen CFG?

CFG-filer, som almindeligvis er forbundet med Wesnoth Markup Language (WML), der bruges i The Battle for Wesnoth-spillet, kan nemt redigeres ved hjælp af enhver standard teksteditor. Disse filer indeholder menneskelæselig kode skrevet i WML, som definerer forskellige aspekter af spillet, herunder scenarier, enheder og kampagner.

Mens du kan bruge en hvilken som helst teksteditor til at ændre CFG-filer, har nogle avancerede teksteditorer som Emacs og Vi WML-syntaksfremhævning-plugins tilgængelige. Disse plugins giver nyttig farvekodning og formatering for at gøre det nemmere for brugere at skelne mellem forskellige elementer og strukturer i WML-koden.

Programmer, der åbner eller refererer til CFG filer inkluderer

- The Battle for Wesnoth (gratis) til (Windows, MAC, Linux)
- Microsoft Notesblok

## Andre CFG-filer

Her er andre filtyper, der bruger filtypen **.cfg**.

**Indstillinger**
- [CFG - Celestia Configuration File](/settings/cfg-celestia/)
- [CFG - Citrix Server Connection File](/settings/cfg-citrix/)
- [CFG - MAME Configuration File](/settings/cfg-mame/)
- [CFG - LightWave Configuration File](/settings/cfg-lightwave/)

**Spil**
- [CFG - Wesnoth Markup Language File](/game/cfg-wesnoth/)
- [CFG - M.U.G.E.N Configuration File](/game/cfg-mugen/)
- [CFG - Source Engine Configuration File](/game/cfg-sourceengine/)

**System og diverse**
- [CFG - CFG File](/system/cfg/)
- [CFG - Cal3D Model Configuration File](/misc/cfg-cal3d/)

## Referencer
* [The Battle for Wesnoth](https://en.wikipedia.org/wiki/The_Battle_for_Wesnoth)
