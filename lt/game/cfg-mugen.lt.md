{
  "date": "2023-09-27",
  "keywords": [
"plg",
"cfg failą",
"cfg mugen konfigūracijos failą",
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
  "title": "CFG failo formatas – MUGEN konfigūracijos failas",
  "description": "Sužinokite apie CFG MUGEN konfigūracijos failo formatą ir API, kurios gali kurti ir atidaryti CFG failus.",
  "linktitle": "CFG M.U.G.E.N",
  "menu": {
    "docs": {
      "identifier": "game-cfg-mugen-lt",
      "parent": "game"
}
},
  "lastmod": "2023-09-27"
}

## Kas yra CFG failas?

CFG failas MUGEN kontekste reiškia MUGEN konfigūracijos failą. **MUGEN** yra pritaikomas 2D kovinių žaidimų variklis, sukurtas Elecbyte. Redaguodami įvairius konfigūracijos failus, įskaitant CFG failus, vartotojai gali kurti savo personažus, etapus ir netgi keisti žaidimo elgesį bei taisykles.

Čia yra pagrindinė apžvalga, ką galite rasti MUGEN `.cfg` faile:

1.  **Sistemos konfigūracija**: CFG failuose dažnai yra nustatymų, susijusių su bendru žaidimo variklio veikimu. Tai apima tokius dalykus kaip ekrano skiriamoji geba, garso nustatymai ir įvesties konfigūracija (klaviatūra, vairasvirtė arba valdiklio atvaizdai).
    
2.  **Numatytieji simbolių ir etapų nustatymai**: galite nustatyti numatytuosius simbolių ir etapų nustatymus. Pavyzdžiui, galite nurodyti, kurie simboliai ir etapai įkeliami žaidimui prasidėjus.
    
3.  **Žaidimo parinktys**: MUGEN `.cfg` failai taip pat gali valdyti įvairias žaidimo parinktis, pvz., apvalaus laiko apribojimus, žalos mastelį ir kt.
    
4.  **Derinimas ir kūrimas**: pažengę naudotojai derinimo ir kūrimo tikslais gali naudoti .cfg failus. Šie nustatymai gali valdyti, kaip derinimo informacija bus rodoma ekrane, arba apibrėžti kitus su kūrimu susijusius veiksmus.
    
5.  **Ekrano konfigūracija**: ekrano paketai yra vaizdinės temos, keičiančios žaidimo išvaizdą ir pojūtį. .cfg failai gali nurodyti, kuris ekrano paketas naudojamas, ir sukonfigūruoti įvairius jo elementus.
    
6.  **AI elgesys**: MUGEN leidžia apibrėžti, kaip kompiuteriu valdomi simboliai (AI) elgiasi mūšiuose. .cfg failuose gali būti nustatymų, susijusių su AI sunkumais ir elgesiu.

## MUGEN konfigūracijos failas 

MUGEN CFG (konfigūracijos) failas yra esminis komponentas kūrėjams pritaikytų kovinių žaidimų pasaulyje. Tai įgalina juos formuoti pagrindines savo žaidimo taisykles. Tai apima tokius veiksnius kaip kiekvieno raundo trukmė, kompiuteriu valdomų oponentų iššūkio lygis, žaidimo tempas, derinių daromos žalos mastas ir daug daugiau.

Be to, CFG failas leidžia kūrėjams nustatyti žaidimo rodymo nustatymus, pvz., ekrano skiriamąją gebą, ir nuspręsti, ar žaidimo metu MUGEN turėtų leisti garso efektus ir muziką. Tiems, kurie gerai išmano MUGEN sudėtingumą, šis failas suteikia galimybę pakoreguoti daugybę kitų su žaidimu susijusių nustatymų, kad sukurtų unikalią žaidimų patirtį.

Pagal numatytuosius nustatymus pagrindinis MUGEN CFG failas, žinomas kaip mugen.cfg, yra programos duomenų aplanke. Nors šiame faile galima tiesiogiai redaguoti žaidimo nustatymus, paprastai patartina pirmiausia sukurti atsarginę kopiją. Ši atsargumo priemonė užtikrina, kad prireikus galėsite be vargo grąžinti MUGEN pradinius nustatymus, kad bet kokie nenumatyti pakeitimai nesutrikdytų jūsų žaidimų patirties.

## MUGEN - žaidimų variklis

MUGEN yra universalus ir lengvai pritaikomas 2D kovinių žaidimų variklis, sukurtas Elecbyte. Pavadinimas MUGEN reiškia Mugen Ultimate Game Engine. Iš pradžių jis buvo išleistas 1999 m., o nuo to laiko įgijo specialią vartotojų ir kūrėjų bendruomenę, kuri naudoja variklį savo 2D kovos žaidimams kurti ir kurti.

Štai keletas pagrindinių MUGEN savybių ir aspektų:

1.  **Pritaikomi veikėjai:** MUGEN leidžia vartotojams kurti ir importuoti savo personažus (žinomus kaip kovotojai arba spritai) į žaidimą. Kūrėjai šiems personažams gali sukurti unikalius judesių rinkinius, animacijas ir specialias atakas, kad būtų galima įtraukti praktiškai bet kurį personažą iš įvairių franšizių ar originalių kūrinių.
    
2.  **Etapai:** be veikėjų, naudotojai taip pat gali kurti ir tinkinti etapus, kuriuose vyksta mūšiai. Šiose stadijose gali būti interaktyvių elementų ir unikalių fonų.
      
3.  **Screenpacks:** Screenpacks are visual themes that change overall appearance of game, including menus, character selection screens and life bars. Users can create and share their own screenpacks to give their games unique look and feel.
    
4.  **Garsas ir muzika:** kūrėjai prie savo žaidimų gali pridėti garso efektų ir foninės muzikos, taip pagerindami bendrą žaidimų patirtį.
    
5.  **Scenarijų kūrimas:** pažengę naudotojai gali naudoti integruotą scenarijų kalbą, kad sukurtų sudėtingą veikėjų elgesį, unikalią žaidimo mechaniką ir specialiuosius efektus.

## Kaip atidaryti CFG failą?

MUGEN CFG failai yra paprasto teksto dokumentai, todėl juos galima pasiekti naudojant įvairius teksto redaktorius. Windows sistemoje galite naudoti Microsoft Notepad arba WordPad, o MacOS vartotojai gali naudoti Apple TextEdit šiuo tikslu. Šie redaktoriai leidžia vartotojams lengvai peržiūrėti ir keisti konfigūracijos nustatymus CFG failuose.

Programos, kurios atidaro arba nurodo CFG failus

- Elecbyte MUGEN
- Užrašų knygelė
- Teksto redagavimas

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
* [Mugen (žaidimo variklis)](https://en.wikipedia.org/wiki/Mugen_(game_engine))


