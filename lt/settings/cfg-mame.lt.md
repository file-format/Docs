{
  "date": "2023-09-27",
  "keywords": [
"plg",
"cfg failą",
"cfg mame konfigūracijos failą",
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
  "title": "CFG failo formatas – MAME konfigūracijos failas",
  "description": "Sužinokite apie CFG MAME konfigūracijos failo formatą ir API, kurios gali kurti ir atidaryti CFG failus.",
  "linktitle": "CFG MAME",
  "menu": {
    "docs": {
      "identifier": "settings-cfg-mame-lt",
      "parent": "settings"
}
},
  "lastmod": "2023-09-27"
}

## Kas yra CFG failas?

CFG failas yra XML klaviatūros konfigūracijos failas, naudojamas MAME arkadinių vaizdo žaidimų emuliatorių. Tai labai svarbus komponentas, norint pritaikyti klaviatūros valdiklius ir sparčiuosius klavišus, kad jie atitiktų žaidėjo pageidavimus. Šiuose failuose saugomi atvaizdai ir nustatymai, kurie nustato, kaip klaviatūra sąveikauja su emuliatoriumi žaidžiant žaidimą. Redaguodami šį failą vartotojai gali pritaikyti savo žaidimų patirtį, priskirdami tam tikrus klaviatūros klavišus žaidimo veiksmams, pvz., monetos įdėjimui, paleidimui, judėjimui ir įvairioms kitoms funkcijoms.

## MAME konfigūracijos failas

MAME, kuris reiškia **Multiple Arcade Machine Emulator**, yra programinė įranga, leidžianti mėgdžioti ir žaisti arkadinius žaidimus kompiuteryje. MAME naudoja konfigūracijos failus, kad pritaikytų savo elgesį ir nustatymus. Šie konfigūracijos failai paprastai yra cfg aplanke jūsų MAME kataloge.

Čia yra pagrindiniai konfigūracijos failai, su kuriais galite susidurti nustatydami ir konfigūruodami MAME:

1. **mame.ini:** Tai pagrindinis MAME konfigūracijos failas. Jame yra visuotiniai nustatymai, taikomi visiems žaidimams. Šį failą galite rasti MAME diegimo šakniniame kataloge.

1. **default.cfg:** šiame faile saugomi numatytieji visų žaidimų, kurie neturi savo konfigūracijos failų, nustatymai. Jis naudojamas kaip atsarginė konkrečių žaidimų nustatymų dalis.

1. **game-specific.cfg:** šie failai naudojami atskirų žaidimų nustatymams saugoti. Paprastai jie yra pavadinti žaidimo, kurį jie atitinka, ROM failo vardu. Pavyzdžiui, jei turite žaidimą pavadinimu pacman.zip, jo konfigūracijos failas būtų pacman.cfg.

Štai keletas bendrų nustatymų, kuriuos galite rasti MAME konfigūracijos faile.

1. **rompath:** nurodo katalogą, kuriame yra jūsų arkadinių žaidimų ROM.

1. **cfg_directory:** nurodo katalogą, kuriame saugomi žaidimo konfigūracijos failai.

1. **nvram_directory:** nurodo katalogą, kuriame saugomi nepastoviosios RAM (NVRAM) failai. NVRAM saugo geriausius rezultatus ir kitus su žaidimu susijusius duomenis.

1. **artwork_directory:** nurodo katalogą, kuriame saugomi meno kūrinių failai (pvz., rėmeliai, palapinės ir skrajutės).

1. **samplepath:** nurodo katalogą, kuriame yra pavyzdiniai garso failai.

1. **cheatpath:** nurodo katalogą, kuriame yra cheat failai.

Taip pat galite konfigūruoti įvairius kitus nustatymus, pvz., vaizdo ir garso parinktis, valdiklius ir įvesties įrenginius. Norėdami pakeisti šiuos nustatymus, galite atidaryti konfigūracijos failą teksto rengyklėje ir atlikti reikiamus pakeitimus.

## MAME

MAME, kuris reiškia **Multiple Arcade Machine Emulator** yra programinė įranga, skirta senovinių arkadinių mašinų ir arkadinių žaidimų pultų aparatinei įrangai mėgdžioti ir atkartoti. Tai leidžia vartotojams žaisti didžiulę klasikinių arkadinių žaidimų biblioteką šiuolaikiniuose kompiuteriuose ir kituose suderinamuose įrenginiuose. MAME yra atvirojo kodo projektas ir tapo pagrindiniu emuliatoriumi, leidžiančiu išsaugoti ir mėgautis turtinga arkadinių žaidimų istorija.

1. **Emuliacija:** pagrindinis MAME tikslas yra tiksliai mėgdžioti arkadinių mašinų aparatinę įrangą, įskaitant jų centrinius procesorius (CPU), garso lustus, grafikos lustus ir įvesties įrenginius. Šis tikslumo lygis užtikrina, kad žaidimai elgsis kuo panašesni į originalią arkadų patirtį.

1. **Compatibility:** MAME supports wide range of arcade game ROMs, making it one of most comprehensive arcade emulators available. It can run games from various arcade platforms including classic games from '70s, '80s, '90s, and even some more recent arcade titles.

1. **Išsaugojimas:** Viena iš pagrindinių MAME misijų yra išsaugoti arkadinių žaidimų istoriją. Tiksliai imituodama arkadinę aparatinę įrangą, MAME padeda išvengti klasikinių žaidimų praradimo ir užtikrina, kad ateities kartos galėtų juos patirti taip, kaip buvo numatyta iš pradžių.

1. **Priekiniai įrenginiai:** daugelis vartotojų naudoja sąsajas su grafine sąsaja žaidimams tvarkyti ir paleisti per MAME. Šios priekinės dalys leidžia lengviau naršyti plačioje MAME žaidimų bibliotekoje.

## Kaip atidaryti CFG failą?

Programos, kurios atidaro arba nurodo CFG failus

- MAME (nemokama) (Windows)
- ExtraMAME (bandomoji versija)
- MacMAME (MAC)

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
* [MAME](https://en.wikipedia.org/wiki/MAME)


