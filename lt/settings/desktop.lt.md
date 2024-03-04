{
  "date": "2023-05-31",
  "keywords": [
"darbalaukio failą",
"kas yra darbalaukio failas",
"kas yra darbalaukio faile",
"darbalaukio failo pavyzdys",
"kaip atidaryti darbalaukio failą",
"koks yra darbalaukio failo formatas",
"failą",
"darbalaukio failo plėtinys",
"pratęsimas"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "DESKTOP failo formatas – darbalaukio įvesties failas",
  "description": "Sužinokite apie DESKTOP formatą ir API, kurios gali kurti ir atidaryti DESKTOP failus.",
  "linktitle": "DESKTOP",
  "menu": {
    "docs": {
      "identifier": "settings-desktop-lt",
      "parent": "settings"
}
},
  "lastmod": "2023-05-31"
}

## Kas yra DESKTOP failas?

.desktop failas yra konfigūracijos failas, naudojamas Linux darbalaukio aplinkose, kad nustatytų programų sparčiuosius klavišus ir paleidimo priemones. Jame pateikiami metaduomenys apie programą, pvz., jos pavadinimas, piktograma, vykdoma komanda ir kitos savybės. Šie failai paprastai naudojami kuriant nuorodas programų meniu, darbalaukio paleidimo priemonėse arba Linux pagrįstų sistemų skydeliuose.

## Kas yra DESKTOP faile?

.desktop failas yra tam tikro formato ir jame yra keli pagrindiniai laukai:

- **[Desktop Entry]:** Tai pagrindinė .desktop failo skyriaus antraštė.
- **Pavadinimas:** Nurodo programos pavadinimą.
- **Comment:** Provides brief description or comment about application.
- **Exec:** apibrėžia komandą, kuri turi būti vykdoma paleidžiant programą.
- **Piktograma:** nurodo kelią į piktogramos failą, susietą su programa.
- **Terminalas:** nurodo, ar programa turi būti paleista terminalo lange.
– **Tipas:** nurodo įrašo tipą, pvz., Programa arba Nuoroda.
- **Categories:** Specifies categories or groups under which the application should be displayed in the menu.
– **StartupNotify:** nurodo, ar darbalaukio aplinka turi rodyti programos paleidimo pranešimą.
- **NoDisplay:** Specifies whether application should be hidden from menus.
– **Veiksmai:** apibrėžiami papildomi veiksmai, kuriuos galima atlikti naudojant programą, pvz., atidaryti konkretų failą.

## DESKTOP failo pavyzdys

Čia yra .desktop failo, skirto fiktyviai teksto rengyklei MyTextEditor, pavyzdys:

```
[Desktop Entry]
Name=MyTextEditor
Comment=A simple text editor
Exec=mytexteditor %F
Icon=/path/to/icon.png
Terminal=false
Type=Application
Categories=TextEditor;Utility;
StartupNotify=true
NoDisplay=false
Actions=OpenNewWindow;OpenExistingFile;

[Desktop Action OpenNewWindow]
Name=Open New Window
Exec=mytexteditor

[Desktop Action OpenExistingFile]
Name=Open Existing File
Exec=mytexteditor %U
```

Šiame pavyzdyje .desktop failas apibrėžia programą MyTextEditor su ja susijusiomis ypatybėmis. Jame taip pat yra du papildomi veiksmai: Atidaryti naują langą ir Atidaryti esamą failą, kuriuos galima pasiekti iš programų paleidimo priemonės kontekstinio meniu.

Įdėjus .desktop failą į konkrečius katalogus, pvz., /usr/share/applications arba ~/.local/share/applications, darbalaukio aplinka jį atpažins ir atitinkamai parodys programą meniu arba leis paleisti iš darbalaukis.

## Kaip atidaryti DESKTOP failą?

Kelios programinės įrangos programos gali atidaryti ir tvarkyti .desktop failus. Šios programos paprastai yra failų tvarkyklės arba darbalaukio aplinkos Linux pagrindu veikiančiose sistemose. Štai keletas pavyzdžių:

- **Nautilus (failai):** numatytoji failų tvarkyklė GNOME darbalaukio aplinkai.
- **Nemo:** Cinnamon darbalaukio aplinkos failų tvarkyklė.
- **Dolphin:** numatytoji failų tvarkyklė KDE Plasma darbalaukio aplinkai.
- **Thunar:** numatytoji failų tvarkyklė, skirta Xfce darbalaukio aplinkai.
- **KDE meniu redaktorius:** įrankis, skirtas KDE Plasma darbalaukio aplinkai, leidžiantis peržiūrėti ir redaguoti .desktop failus.

Šios failų tvarkyklės ir darbalaukio aplinkos suteikia grafinę sąsają .desktop failams valdyti. Jie leidžia peržiūrėti ir redaguoti .desktop failų ypatybes, kurti programų paleidimo priemones ir tvarkyti sparčiuosius klavišus programų meniu arba darbalaukyje.

.desktop failai yra paprasto teksto failai, todėl juos taip pat galite atidaryti ir redaguoti naudodami pasirinktą teksto rengyklę. Tiesiog dešiniuoju pelės mygtuku spustelėkite .desktop failą ir pasirinkite Atidaryti naudojant arba Atidaryti naudojant kitą programą, kad pasirinktumėte teksto rengyklę iš įdiegtų programų sąrašo.

## Koks yra DESKTOP failo formatas?

.desktop failo formatas atitinka tam tikrą struktūrą ir formatą. Tai paprasto teksto failas su raktų ir reikšmių porų rinkiniu, suskirstytų į skyrius. Čia yra formato apžvalga:

- **Skyrių antraštės:** kiekviena sekcija prasideda laužtiniuose skliaustuose ([]) esančia antrašte. Pirminė skiltis paprastai vadinama [Desktop Entry], kurioje yra pagrindiniai programos arba paleidimo priemonės metaduomenys.
– **Raktų ir verčių poros:** kiekvienoje skiltyje ypatybes apibrėžiate naudodami rakto ir reikšmių poras. Formatas yra Key=Value. Raktas identifikuoja savybę, o vertė pateikia atitinkamus duomenis.
– **Ypatybės sintaksė:** ypatybių reikšmės gali būti įvairių tipų, įskaitant eilutes, logines reikšmes, failų kelius arba sąrašus. Kiekvienos nuosavybės vertės formatas priklauso nuo jos tipo.
- **Komentarai:** Galite įtraukti komentarus į .desktop failą naudodami simbolį #. Viskas po # eilutėje yra laikoma komentaru ir yra ignoruojama.

## Nuorodos
* [Desktop Entry-files](https://www.baeldung.com/linux/desktop-entry-files)


