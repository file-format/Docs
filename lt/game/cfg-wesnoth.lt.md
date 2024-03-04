{
  "date": "2023-09-27",
  "keywords": [
"plg",
"cfg failą",
"cfg wesnoth žymėjimo kalbos failas",
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
  "title": "CFG failo formatas – Wesnoth žymėjimo kalbos failas",
  "description": "Sužinokite apie CFG Wesnoth Markup Language failo formatą ir API, kurios gali kurti ir atidaryti CFG failus.",
  "linktitle": "CFG Wesnoth",
  "menu": {
    "docs": {
      "identifier": "game-cfg-wesnoth-lt",
      "parent": "game"
}
},
  "lastmod": "2023-09-27"
}

## Kas yra CFG failas?

CFG failas taip pat žinomas kaip **Wesnoth Markup Language (WML)**. Tai yra tinkinta žymėjimo kalba, pirmiausia naudojama žaidime Battle for Wesnoth, kuris yra nuoseklus strateginis žaidimas. WML naudojamas įvairiems žaidimo aspektams apibrėžti ir tinkinti, įskaitant scenarijus, kampanijas, vienetus ir kt. Tai būdas modifikatoriams ir kūrėjams kurti žaidimo turinį.

Jis parašytas tokiu formatu, kuris primena XML ir paprasto scenarijaus derinį. Štai keletas bendrų elementų ir struktūrų, kuriuos galite rasti WML faile, apžvalga:

1.  **Žymos:** WML naudoja žymas skirtingiems žaidimo elementams apibrėžti. Žymos yra įdėtos į kampinius skliaustus. Pavyzdžiui:

```
[unit]
    type=Elvish Archer
    hitpoints=25
[/unit]
```
    
2.  **Atributai:** žymose galite apibrėžti atributus, kad nurodytumėte su elementu susijusias ypatybes arba reikšmes. Aukščiau pateiktame pavyzdyje tipas ir hitpoints yra atributai.
    
3.  **Masyvai ir masyvai:** galite sukurti duomenų masyvus ir net masyvus, kad apibrėžtumėte vienetų, reljefo tipų ar kitų žaidimo elementų sąrašus.
    
4.  **Sąlyginiai teiginiai:** WML palaiko sąlyginius teiginius, kad valdytų žaidimo eigą. Pavyzdžiui:

```
[if]
    condition=have_unit
    variable=x,y
[/if]
```
    
5.  **Cilpos:** galite naudoti kilpas, kad galėtumėte kartoti elementų sąrašus arba pakartotinai atlikti veiksmus.
    
6.  **Apima:** Į pagrindinį WML failą galite įtraukti kitus WML failus, kad galėtumėte tvarkyti ir moduliuoti turinį.
    
7.  **Įvykių tvarkyklės:** galite apibrėžti įvykių tvarkykles, kurios suaktyvintų veiksmus, kai žaidime įvyksta konkretūs įvykiai.
    

Štai supaprastintas WML failo, apibrėžiančio tinkintą vienetą, pavyzdys:

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

## Mūšis dėl Wesnotho

The Battle for Wesnoth yra populiarus atvirojo kodo ruožtu paremtas strateginis žaidimas. Jį galima naudoti kelioms platformoms, įskaitant Mac, Windows, Linux ir kt. Žaidimas, sukurtas atsidavusios savanorių bendruomenės, yra žinomas dėl gilaus ir patrauklaus žaidimo, taip pat turtingo fantazijos pasaulio.

Pagrindinės The Battle for Wesnoth savybės:

1.  **Fantazijos nustatymas:** žaidimas vyksta fantazijų pasaulyje, kuriame yra įvairių rasių, įskaitant žmones, elfus, nykštukus, orkus ir kt. Žaidimo istorija ir pasakojimas yra neatsiejama jo patrauklumo dalis.
    
2.  **Turn-based Strategy:** Žaidimas vyksta eilėmis, kai žaidėjai skiria laiko planuoti ir atlikti savo judesius šešiakampiuose tinkleliuose. Jis sujungia taktinę kovą su strateginių sprendimų priėmimu.
    
3.  **Kampanijos:** žaidimas siūlo platų vieno žaidėjo kampanijų pasirinkimą, kurių kiekviena turi savo siužetą, personažus ir iššūkius. Žaidėjai gali tyrinėti įvairius pasakojimus ir scenarijus.
    
4.  **Kelių žaidėjų:** Wesnoth palaiko internetinį kelių žaidėjų režimą, todėl žaidėjai gali varžytis vieni su kitais strateginėse kovose. Kelių žaidėjų režimai apima bendradarbiavimą ir konkurencines rungtynes.

## Kaip atidaryti CFG failą?

CFG failus, kurie dažniausiai siejami su Wesnoth Markup Language (WML), naudojama žaidime The Battle for Wesnoth, galima lengvai redaguoti naudojant bet kurį standartinį teksto rengyklę. Šiuose failuose yra žmogaus skaitomas kodas, parašytas WML, kuris apibrėžia įvairius žaidimo aspektus, įskaitant scenarijus, vienetus ir kampanijas.

Nors CFG failams modifikuoti galite naudoti bet kurį teksto rengyklę, kai kurie pažangūs teksto redaktoriai, pvz., Emacs ir Vi, turi WML sintaksės paryškinimo papildinius. Šie papildiniai suteikia naudingą spalvų kodavimą ir formatavimą, kad naudotojai galėtų lengviau atskirti skirtingus WML kode elementus ir struktūras.

Programos, kurios atidaro arba nurodo CFG failus, apima

- The Battle for Wesnoth (nemokama) (Windows, MAC, Linux)
- Microsoft Notepad

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
* [The Battle for Wesnoth](https://en.wikipedia.org/wiki/The_Battle_for_Wesnoth)
