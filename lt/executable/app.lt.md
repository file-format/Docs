{
  "date": "2023-02-02",
  "keywords": [
"programos failą",
"kas yra programos failas",
"failą",
"kaip atidaryti programos failą",
"programos failo plėtinys",
"pratęsimas"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie APP failo formatą ir API, kurios gali kurti ir atidaryti APP failus.",
  "title": "APP failo formatas – „macOS“ programų paketas",
  "linktitle": "APP",
  "menu": {
    "docs": {
      "identifier": "executable-app-lt",
      "parent": "executable"
}
},
  "lastmod": "2023-02-02"
}

## Kas yra APP failas?

MacOS .app failas yra specialaus tipo katalogas, kuriame yra visi failai, reikalingi konkrečiai programai paleisti, įskaitant vykdomąjį kodą, išteklius ir metaduomenis. .app plėtinys operacinei sistemai praneša, kad šis katalogas turėtų būti traktuojamas kaip vienas vienetas, o ne kaip atskirų failų rinkinys, ir kad jį galima paleisti tiesiai iš ieškiklio arba doko.

Finder yra numatytoji failų tvarkyklės programa MacOS. Tai leidžia naršyti ir tvarkyti failus bei katalogus kompiuteryje. Dokas yra macOS funkcija, suteikianti greitą prieigą prie dažnai naudojamų programų ir dokumentų. Tiek Finder, tiek Dock leidžia paleisti programas spustelėjus jų .app failus, kurie atidarys atitinkamą programų paketą. Kai paleidžiate programą, paleidžiamas vykdomasis kodas .app pakete, todėl programą galima naudoti. .app failas yra programos atvaizdas failų sistemoje ir suteikia vartotojui būdą pasiekti ir paleisti programą.

Dešiniuoju pelės mygtuku spustelėję .app failą MacOS sistemos Finder programoje ir pasirinkę Rodyti paketo turinį, galėsite matyti vidinę programų paketo struktūrą. Tai naudinga, jei norite pasiekti programos naudojamus išteklius ar failus arba jei norite patikrinti programos turinį trikčių šalinimo tikslais. .app failo paketo turinys paprastai apima išteklių, pvz., vaizdų ir garsų, katalogus, taip pat programos vykdomąjį kodą. Ištyrę .app failo turinį galite gauti gilesnių įžvalgų apie tai, kaip programa sudaroma ir ką ji daro.

## Kaip atidaryti APP failą?

Norėdami atidaryti .app failą MacOS, tiesiog dukart spustelėkite failą Finder. Bus paleista programa, esanti .app pakete. Jei programa yra įdiegta jūsų sistemoje ir buvo susieta su .app failo tipu, dukart spustelėjus failą programa turėtų būti paleista automatiškai. Jei programa nesusieta su .app failo tipu, gali tekti dešiniuoju pelės mygtuku spustelėti failą ir pasirinkti Atidaryti naudojant, kad pasirinktumėte tinkamą programą, su kuria norite ją atidaryti.

MacOS terminale galite atidaryti .app failą naudodami komandą open. Norėdami tai padaryti, eikite į katalogą, kuriame yra .app failas, naudodami komandą cd, tada paleiskite šią komandą:

```
open <AppName>.app 
```

kur<AppName> yra programos, kurią norite paleisti, pavadinimas. Tai paleis programą taip, lyg būtumėte dukart spustelėję ją Finder. Komanda atidaryti yra bendrosios paskirties įrankis, kurį galima naudoti norint atidaryti daugybę skirtingų tipų failų, įskaitant programas, dokumentus ir katalogus. Kai .app faile naudojate komandą open, ji paleidžia pakete esančią programą.

## Nuorodos
* [Bundle (macOS)](https://en.wikipedia.org/wiki/Bundle_(macOS))
