{
  "date": "2023-05-31",
  "keywords": [
"darbvirsmas fails",
"kas ir darbvirsmas fails",
"ko satur darbvirsmas fails",
"darbvirsmas faila piemērs",
"kā atvērt darbvirsmas failu",
"kāds ir darbvirsmas faila formāts",
"failu",
"darbvirsmas faila paplašinājums",
"pagarinājumu"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "DESKTOP faila formāts — darbvirsmas ievades fails",
  "description": "Uzziniet par DESKTOP formātu un API, kas var izveidot un atvērt DESKTOP failus.",
  "linktitle": "DESKTOP",
  "menu": {
    "docs": {
      "identifier": "settings-desktop-lv",
      "parent": "settings"
}
},
  "lastmod": "2023-05-31"
}

## Kas ir DESKTOP fails?

.desktop fails ir konfigurācijas fails, ko izmanto Linux darbvirsmas vidēs, lai definētu lietojumprogrammu saīsnes un palaišanas programmas. Tas nodrošina metadatus par lietojumprogrammu, piemēram, tās nosaukumu, ikonu, izpildāmo komandu un citus rekvizītus. Šie faili parasti tiek izmantoti, lai izveidotu saīsnes lietojumprogrammu izvēlnēs, darbvirsmas palaišanas programmās vai paneļos Linux sistēmās.

## Ko satur DESKTOP fails?

.desktop failam ir noteikts formāts, un tajā ir vairāki galvenie lauki:

- **[Darbvirsmas ieraksts]:** šī ir .desktop faila galvenā sadaļas galvene.
- **Nosaukums:** norāda lietojumprogrammas nosaukumu.
- **Comment:** Provides brief description or comment about application.
- **Exec:** definē komandu, kas jāizpilda, palaižot lietojumprogrammu.
- **Ikona:** norāda ceļu uz ikonas failu, kas saistīts ar lietojumprogrammu.
- **Termināls:** norāda, vai lietojumprogramma ir jāpalaiž termināļa logā.
- **Veids:** norāda ieraksta veidu, piemēram, Lietojumprogramma vai Saite.
- **Categories:** Specifies categories or groups under which the application should be displayed in the menu.
- **StartupNotify:** norāda, vai darbvirsmas vidē ir jāparāda lietojumprogrammas palaišanas paziņojums.
- **NoDisplay:** Specifies whether application should be hidden from menus.
- **Darbības:** definē papildu darbības, kuras var veikt lietojumprogrammā, piemēram, atvērt konkrētu failu.

## DESKTOP faila piemērs

Šeit ir .desktop faila piemērs fiktīvam teksta redaktoram ar nosaukumu MyTextEditor.

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

Šajā piemērā .desktop fails definē lietojumprogrammu MyTextEditor ar tai saistītajiem rekvizītiem. Tas ietver arī divas papildu darbības Atvērt jaunu logu un Atvērt esošo failu, kurām var piekļūt no lietojumprogrammu palaišanas konteksta izvēlnes.

Ievietojot .desktop failu noteiktos direktorijos, piemēram, `/usr/share/applications' vai `~/.local/share/applications', darbvirsmas vide to atpazīs un attiecīgi parādīs lietojumprogrammu izvēlnēs vai ļaus to palaist no darbvirsma.

## Kā atvērt DESKTOP failu?

Vairākas programmatūras var atvērt un apstrādāt .desktop failus. Šīs programmas parasti ir failu pārvaldnieki vai darbvirsmas vides sistēmās, kuru pamatā ir Linux. Šeit ir daži piemēri:

- **Nautilus (faili):** noklusējuma failu pārvaldnieks GNOME darbvirsmas videi.
- **Nemo:** Cinnamon darbvirsmas vides failu pārvaldnieks.
- **Dolphin:** noklusējuma failu pārvaldnieks KDE Plasma darbvirsmas videi.
- **Thunar:** noklusējuma failu pārvaldnieks Xfce darbvirsmas videi.
- **KDE izvēlnes redaktors:** KDE Plasma darbvirsmas videi raksturīgs rīks, kas ļauj skatīt un rediģēt .desktop failus.

Šie failu pārvaldnieki un darbvirsmas vides nodrošina grafisku saskarni .desktop failu pārvaldībai. Tie ļauj skatīt un rediģēt .desktop failu rekvizītus, izveidot lietojumprogrammu palaišanas programmas un organizēt īsceļus lietojumprogrammu izvēlnēs vai darbvirsmā.

.desktop faili ir vienkārša teksta faili, tāpēc varat tos arī atvērt un rediģēt, izmantojot jūsu izvēlētu teksta redaktoru. Vienkārši ar peles labo pogu noklikšķiniet uz .desktop faila un atlasiet Atvērt ar vai Atvērt ar citu programmu, lai no instalēto programmu saraksta izvēlētos teksta redaktoru.

## Kāds ir DESKTOP faila formāts?

.desktop faila formāts atbilst noteiktai struktūrai un formātam. Tas ir vienkārša teksta fails ar atslēgu un vērtību pāru kopu, kas sakārtots sadaļās. Šeit ir formāta pārskats:

- **Sadaļu galvenes:** katra sadaļa sākas ar galveni, kas ievietota kvadrātiekavās ([]). Primārā sadaļa parasti tiek nosaukta [Desktop Entry], kurā ir ietverti lietojumprogrammas vai palaišanas programmas galvenie metadati.
- **Atslēgas-vērtību pāri:** katrā sadaļā jūs definējat rekvizītus, izmantojot atslēgu un vērtību pārus. Formāts ir Key=Value. Atslēga identificē īpašumu, un vērtība nodrošina atbilstošus datus.
- **Īpašuma sintakse:** rekvizītu vērtības var būt dažāda veida, tostarp virknes, Būla vērtības, failu ceļi vai saraksti. Katras īpašuma vērtības formāts ir atkarīgs no tā veida.
- **Komentāri:** Varat iekļaut komentārus .desktop failā, izmantojot simbolu #. Jebkas, kas tiešsaistē seko simbolam #, tiek uzskatīts par komentāru un tiek ignorēts.

## Atsauces
* [Darbvirsmas ierakstu faili](https://www.baeldung.com/linux/desktop-entry-files)


