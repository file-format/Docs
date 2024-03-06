{
  "date": "2023-09-27",
  "keywords": [
"sk",
"cfg failu",
"cfg wesnoth iezīmēšanas valodas fails",
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
  "title": "CFG faila formāts — Vesnota iezīmēšanas valodas fails",
  "description": "Uzziniet par CFG Wesnoth iezīmēšanas valodas faila formātu un API, kas var izveidot un atvērt CFG failus.",
  "linktitle": "CFG Wesnoth",
  "menu": {
    "docs": {
      "identifier": "game-cfg-wesnoth-lv",
      "parent": "game"
}
},
  "lastmod": "2023-09-27"
}

## Kas ir CFG fails?

CFG fails ir pazīstams arī kā **Vesnota iezīmēšanas valoda (WML)**. Tā ir pielāgota iezīmēšanas valoda, ko galvenokārt izmanto spēlē Battle for Wesnoth, kas ir uz gājieniem balstīta stratēģijas spēle. WML tiek izmantots, lai definētu un pielāgotu dažādus spēles aspektus, tostarp scenārijus, kampaņas, vienības un daudz ko citu. Tas ir veids, kā modderi un izstrādātāji var izveidot spēles saturu.

Tas ir uzrakstīts formātā, kas līdzinās XML un vienkāršas skriptēšanas kombinācijai. Tālāk ir sniegts pārskats par dažiem bieži sastopamiem elementiem un struktūrām, ko varat atrast WML failā:

1.  **Tagi:** WML izmanto atzīmes, lai definētu dažādus spēles elementus. Birkas ir ievietotas leņķa iekavās. Piemēram:

```
[unit]
    type=Elvish Archer
    hitpoints=25
[/unit]
```
    
2.  **Atribūti:** tagos varat definēt atribūtus, lai norādītu ar elementu saistītos rekvizītus vai vērtības. Iepriekš minētajā piemērā type un hitpoints ir atribūti.
    
3.  **Masīvi un masīvu masīvi:** varat izveidot datu masīvus un pat masīvu masīvus, lai definētu vienību, reljefa veidu vai citu spēles elementu sarakstus.
    
4.  **Nosacījuma paziņojumi:** WML atbalsta nosacījumu paziņojumus, lai kontrolētu spēles plūsmu. Piemēram:

```
[if]
    condition=have_unit
    variable=x,y
[/if]
```
    
5.  **Cilpas:** varat izmantot cilpas, lai atkārtotu vienumu sarakstus vai veiktu darbības atkārtoti.
    
6.  **Ietver:** Varat iekļaut citus WML failus galvenajā WML failā, lai sakārtotu un modulētu saturu.
    
7.  **Notikumu apstrādātāji:** varat definēt notikumu apdarinātājus, lai aktivizētu darbības, kad spēlē notiek konkrēti notikumi.
    

Šeit ir vienkāršots WML faila piemērs, kas definē pielāgotu vienību:

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

## Cīņa par Vesnotu

The Battle for Wesnoth ir populāra un atvērtā koda uz gājieniem balstīta stratēģijas spēle. Tas ir pieejams vairākām platformām, tostarp Mac, Windows, Linux un citām. Spēle, ko izstrādājusi īpaša brīvprātīgo kopiena, ir pazīstama ar savu dziļo un aizraujošo spēli, kā arī tās bagāto fantāziju pasauli.

Galvenās The Battle for Wesnoth iezīmes ir šādas:

1.  **Fantāzijas iestatījums:** spēle notiek fantāziju pasaulē ar dažādām rasēm, tostarp cilvēkiem, elfiem, rūķiem, orkiem un citiem. Spēles vēsture un stāstu stāstīšana ir tās pievilcības neatņemama sastāvdaļa.
    
2.  **Uz gājieniem balstīta stratēģija:** spēle ir balstīta uz gājieniem, kur spēlētāji velta laiku, lai plānotu un izpildītu kustības uz sešstūra režģiem. Tā apvieno taktisko cīņu ar stratēģisku lēmumu pieņemšanu.
    
3.  **Kampaņas:** spēle piedāvā plašu viena spēlētāja kampaņu klāstu, katrai no kurām ir savs sižets, varoņi un izaicinājumi. Spēlētāji var izpētīt dažādus stāstījumus un scenārijus.
    
4.  **Vairākspēlētāju spēle:** Wesnoth atbalsta tiešsaistes vairāku spēlētāju spēli, ļaujot spēlētājiem sacensties vienam ar otru stratēģiskās cīņās. Vairāku spēlētāju režīmi ietver kooperatīvu spēli un sacensību spēles.

## Kā atvērt CFG failu?

CFG failus, kas parasti tiek saistīti ar Wesnoth iezīmēšanas valodu (WML), ko izmanto spēlē The Battle for Wesnoth, var viegli rediģēt, izmantojot jebkuru standarta teksta redaktoru. Šajos failos ir cilvēkiem lasāms kods, kas rakstīts WML, kas definē dažādus spēles aspektus, tostarp scenārijus, vienības un kampaņas.

Lai gan CFG failu modificēšanai varat izmantot jebkuru teksta redaktoru, dažiem uzlabotajiem teksta redaktoriem, piemēram, Emacs un Vi, ir pieejami WML sintakses izcelšanas spraudņi. Šie spraudņi nodrošina noderīgu krāsu kodēšanu un formatēšanu, lai lietotājiem būtu vieglāk atšķirt dažādus elementus un struktūras WML kodā.

Programmas, kas atver vai atsaucas uz CFG failiem, ietver

- Cīņa par Vesnotu (bezmaksas) operētājsistēmai Windows, MAC, Linux
- Microsoft Notepad

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
* [The Battle for Wesnoth](https://en.wikipedia.org/wiki/The_Battle_for_Wesnoth)
