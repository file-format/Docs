{
   "date":"2023-01-04",
   "keywords":[
"cs",
"cs failą",
"cs cleo pasirinktinį scenarijų",
"kaip atidaryti cs failą",
"failą",
"cs failo plėtinys",
"pratęsimas",
"failą"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"CS failo formatas – CLEO pasirinktinis scenarijus",
   "description":"Sužinokite apie CS CLEO pasirinktinio scenarijaus formatą ir API, kurios gali kurti ir atidaryti CS failus.",
   "linktitle":"CS CLEO",
   "menu":{
      "docs":{
         "identifier":"game-cs-cleo-lt",
         "parent":"game"
}
},
   "lastmod":"2023-01-04"
}

## Kas yra CS failas?

.CS failas CLEO kontekste (CLEO Library santrumpa) paprastai reiškia pasirinktinį scenarijaus failą, naudojamą Grand Theft Auto (GTA) vaizdo žaidimų serijoje. CLEO yra populiari modifikavimo sistema, leidžianti žaidėjams kurti ir pridėti prie GTA žaidimų pasirinktinius scenarijus, leidžiančius keisti žaidimo eigą, pridėti naujų funkcijų ir pagerinti bendrą žaidimų patirtį.

## CS failo apžvalga

Čia pateikiama pagrindinė apžvalga, kas gali būti .cs faile CLEO:

1.  **Scenarijaus kodas**: .cs faile yra scenarijaus kodas, parašytas CLEO scenarijų kalba. Ši scenarijų kalba yra būdinga CLEO ir naudojama apibrėžti tinkintų scenarijų elgseną žaidime. Kodą galima parašyti naudojant teksto rengyklę ir paprastai jis atitinka tam tikrą sintaksę.
    
2.  **Modifications**: CLEO scripts can make various modifications to game such as changing behavior of in-game objects, creating custom missions, adding new vehicles, weapons and more. The possibilities are extensive and depend on creativity and programming skills of script author.
    
3.  **Suaktyvikliai**: CLEO scenarijai dažnai apima aktyviklius, kurie nustato, kada ir kaip pasirinktinis scenarijus turi būti paleistas. Šie paleidikliai gali būti pagrįsti žaidimo įvykiais, žaidėjo veiksmais arba konkrečiomis sąlygomis.
    
4.  **Kintamieji ir funkcijos**: CLEO scenarijai gali naudoti kintamuosius duomenims saugoti ir manipuliuoti, taip pat funkcijas, skirtas kodui įterpti ir pakartotinai naudoti. Šie kintamieji ir funkcijos naudojami scenarijaus elgsenai valdyti.

## CS failo pavyzdys

Štai paprastas CLEO .cs scenarijaus, kuris keičia orą žaidime, pavyzdys:

```
{$CLEO .cs}

03A4: name_thread 'WEATHER'

:WEATHER_LOOP
    // Change the weather to sunny
    0085: 0@ = 11 // Weather ID for sunny weather
    00D8: mission_cleanup
    0051: return 0@ // Exit the script

// Add more code and conditions as needed
```

## CLEO biblioteka

**CLEO biblioteka**, dažnai vadinama tiesiog CLEO, yra populiari ir galinga Grand Theft Auto (GTA) vaizdo žaidimų serijos modifikavimo sistema. Tai leidžia žaidėjams ir modifikuotojams kurti ir pridėti prie GTA žaidimų pasirinktinius scenarijus, leidžiančius keisti žaidimo eigą, pridėti naujų funkcijų ir pagerinti bendrą žaidimų patirtį. CLEO yra ypač gerai žinomas dėl savo lankstumo ir lengvo naudojimo GTA modifikavimo bendruomenėje.

Štai keletas pagrindinių CLEO bibliotekos funkcijų ir aspektų:

1.  **Scenarijų kalba**: CLEO pristato savo scenarijų kalbą, kuri yra būdinga modifikavimo sistemai. Scenarijų kalba sukurta taip, kad būtų gana lengva suprasti ir dirbti su ja, kad ji būtų prieinama tiek pradedantiesiems, tiek patyrusiems modifikuotojams.
    
2.  **Custom Scripts**: Naudodami CLEO galite kurti pasirinktinius scenarijus, kurie žaidimų pasaulyje gali atlikti daugybę funkcijų. Šie scenarijai gali pakeisti elgesį žaidime, pridėti naujų misijų, pristatyti naujas transporto priemones ar ginklus, pakeisti žaidimo fiziką ir dar daugiau.
    
3.  **Suaktyvikliai ir įvykiai**: CLEO scenarijus gali suaktyvinti įvairūs žaidimo įvykiai, žaidėjo veiksmai arba konkrečios sąlygos. Tai leidžia modifikatoriams žaidime kurti dinamišką ir interaktyvų turinį.
    
4.  **Support for Multiple GTA Versions**: CLEO has versions tailored to different GTA games, including GTA III, GTA Vice City, GTA San Andreas, GTA IV and others. This means that modders can create and share their custom scripts for different GTA titles.

## CLEO bibliotekos naudojami failų formatai

Naudojant CLEO modifikavimą, skirtą Grand Theft Auto (GTA) žaidimams, modifikacijoms kurti ir įdiegti dažniausiai naudojami keli failų formatai. Šie failų formatai naudojami įvairiems tikslams – nuo faktinių scenarijų talpinimo iki papildomų išteklių, tokių kaip tekstūros, modeliai ar garso įrašai, saugojimo. Štai keletas pagrindinių failų formatų, naudojamų CLEO modifikavimui:

1.  **.cs (Custom Script)**: CLEO .cs failai yra pasirinktiniai scenarijaus failai, parašyti CLEO scenarijų kalba. Šiuose failuose yra kodas, apibrėžiantis mod elgseną ir funkcionalumą. .cs failai yra CLEO modifikavimo pagrindas ir yra vykdomi žaidime, kad įdiegtų pasirinktines funkcijas.
    
2.  **.csa (Custom Script Archive)**: .csa failai yra archyvai, kuriuose galima saugoti kelis .cs scenarijaus failus. Jie dažnai naudojami susijusiems scenarijams supakuoti, kad būtų lengviau įdiegti ir valdyti.
    
3.  **.fxt (teksto failai)**: .fxt failai yra tekstiniai failai, kurie gali būti naudojami lokalizuoti arba pateikti teksto vertimus CLEO modifikacijoms. Juose yra teksto eilutės, kurios gali būti rodomos žaidime, todėl modifikacijos yra prieinamos žaidėjams skirtingomis kalbomis.
    
4.  **[.bmp](/image/bmp/), [.png](/image/png/), [.jpg](/image/jpeg/) (vaizdo formatai)**: šie vaizdo formatai naudojami modifikacijų tekstūroms ir vaizdams saugoti. Jie gali būti naudojami tinkintoms odoms, transporto priemonių tekstūroms, HUD elementams ir kt. Priklausomai nuo žaidimo, pirmenybė gali būti teikiama skirtingiems vaizdo formatams.

## Kaip atidaryti CS failą?

Norėdami atidaryti ir peržiūrėti CLEO .cs (Custom Script) failo turinį, galite naudoti pasirinktą teksto rengyklę arba kodo rengyklę. Įprasti pasirinkimai apima:

– **Notepad**: paprasta teksto rengyklė, kuri iš anksto įdiegta sistemoje Windows.
- **Notepad++**: daug funkcijų turinti teksto rengyklė, skirta kodavimui ir scenarijų rašymui.
- **Visual Studio Code**: populiarus, nemokamas ir labai išplečiamas kodo rengyklė.
- **Sublime Text**: dar vienas kodo rengyklė, žinoma dėl savo greičio ir universalumo.
– **Atom**: atvirojo kodo redaktorius, kurį sukūrė GitHub.

## Kiti CS failai

Štai kiti failų tipai, kuriuose naudojamas **.cs** failo plėtinys.

**Duomenų failai ir žaidimas**
- [CS - ColorSchemer Studio Color Scheme](/data/cs-colorschemer/)
- [CS - CLEO Custom Script](/game/cs-cleo/)

**Programavimas**
- [CS - CSharp Code File](/programming/cs/)

## Nuorodos
* [CLEO biblioteka](https://cleo.li/)


