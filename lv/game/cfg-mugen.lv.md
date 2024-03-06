{
  "date": "2023-09-27",
  "keywords": [
"sk",
"cfg failu",
"cfg mugen konfigurācijas fails",
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
  "title": "CFG faila formāts — MUGEN konfigurācijas fails",
  "description": "Uzziniet par CFG MUGEN konfigurācijas faila formātu un API, kas var izveidot un atvērt CFG failus.",
  "linktitle": "CFG M.U.G.E.N",
  "menu": {
    "docs": {
      "identifier": "game-cfg-mugen-lv",
      "parent": "game"
}
},
  "lastmod": "2023-09-27"
}

## Kas ir CFG fails?

CFG fails MUGEN kontekstā attiecas uz MUGEN konfigurācijas failu. **MUGEN** ir pielāgojams 2D cīņas spēļu dzinējs, ko izstrādājis Elecbyte. Lietotāji var izveidot savus varoņus, posmus un pat mainīt spēles uzvedību un noteikumus, rediģējot dažādus konfigurācijas failus, tostarp CFG failus.

Šeit ir pamata pārskats par to, ko jūs varētu atrast MUGEN `.cfg' failā:

1.  **Sistēmas konfigurācija**: CFG faili bieži satur iestatījumus, kas saistīti ar spēles dzinēja vispārējo darbību. Tas ietver tādas lietas kā ekrāna izšķirtspēja, skaņas iestatījumi un ievades konfigurācija (tastatūra, kursorsvira vai kontrollera kartējumi).
    
2.  **Rakstzīmju un posmu noklusējuma iestatījumi**: varat definēt rakstzīmju un posmu noklusējuma iestatījumus. Piemēram, varat norādīt, kuras rakstzīmes un posmi tiek ielādēti, kad spēle sākas.
    
3.  **Spēles opcijas**: MUGEN `.cfg` faili var arī kontrolēt dažādas spēles iespējas, piemēram, apaļo laika ierobežojumus, bojājumu mērogošanu un daudz ko citu.
    
4.  **Atkļūdošana un izstrāde**: pieredzējuši lietotāji var izmantot .cfg failus atkļūdošanas un izstrādes nolūkos. Šie iestatījumi var kontrolēt, kā atkļūdošanas informācija tiek parādīta ekrānā, vai definēt citas ar izstrādi saistītas darbības.
    
5.  **Ekrāna pakotnes konfigurācija**: ekrāna pakotnes ir vizuālas tēmas, kas maina spēles izskatu un sajūtu. .cfg faili var norādīt, kurš ekrāna pakotnis tiek izmantots, un konfigurēt dažādus tā elementus.
    
6.  **AI uzvedība**: MUGEN ļauj definēt, kā kaujās uzvedas datora vadītas rakstzīmes (AI). .cfg faili var saturēt iestatījumus, kas saistīti ar AI grūtībām un uzvedību.

## MUGEN konfigurācijas fails 

MUGEN CFG (konfigurācijas) fails ir būtisks komponents veidotājiem pielāgoto cīņas spēļu pasaulē. Tas dod viņiem iespēju veidot savas spēles pamatnoteikumus. Tas ietver tādus faktorus kā katra raunda ilgums, datora vadīto pretinieku izaicinājuma līmenis, spēles temps, kombinācijas, kas ietekmē bojājumus, un daudz ko citu.

Turklāt CFG fails ļauj veidotājiem noteikt spēles displeja iestatījumus, piemēram, ekrāna izšķirtspēju un izlemt, vai MUGEN spēles laikā atskaņot skaņas efektus un mūziku. Tiem, kas labi pārzina MUGEN sarežģījumus, šis fails piedāvā iespēju pielāgot virkni citu ar spēlēm saistītu iestatījumu, lai radītu unikālu spēļu pieredzi.

Pēc noklusējuma MUGEN primārais CFG fails, kas pazīstams kā mugen.cfg, atrodas programmas datu mapē. Lai gan šajā failā ir iespējams tieši rediģēt spēles iestatījumus, parasti ir ieteicams vispirms izveidot rezerves kopiju. Šis piesardzības pasākums nodrošina, ka varat bez piepūles atjaunot MUGEN sākotnējos iestatījumus, ja nepieciešams, lai novērstu neparedzētas izmaiņas, kas traucē jūsu spēļu pieredzi.

## MUGEN — spēļu dzinējs

MUGEN ir daudzpusīgs un ļoti pielāgojams 2D cīņas spēļu dzinējs, ko izstrādājis Elecbyte. Nosaukums MUGEN nozīmē Mugen Ultimate Game Engine. Sākotnēji tas tika izlaists 1999. gadā un kopš tā laika ir ieguvis īpašu lietotāju un veidotāju kopienu, kas izmanto dzinēju, lai izstrādātu un izstrādātu savas 2D cīņas spēles.

Šeit ir dažas galvenās MUGEN funkcijas un aspekti:

1.  **Pielāgojami varoņi:** MUGEN ļauj lietotājiem izveidot un importēt spēlē savus varoņus (pazīstamus kā cīnītājus vai sprites). Veidotāji šiem varoņiem var izstrādāt unikālas kustības, animācijas un īpašus uzbrukumus, ļaujot iekļaut praktiski jebkuru varoni no dažādām franšīzēm vai oriģināliem darbiem.
    
2.  **Posmi:** Papildus varoņiem lietotāji var arī izveidot un pielāgot posmus, kuros notiek cīņas. Šajos posmos var būt interaktīvi elementi un unikāls fons.
      
3.  **Screenpacks:** Screenpacks are visual themes that change overall appearance of game, including menus, character selection screens and life bars. Users can create and share their own screenpacks to give their games unique look and feel.
    
4.  **Skaņa un mūzika:** satura veidotāji savām spēlēm var pievienot skaņas efektus un fona mūziku, uzlabojot kopējo spēļu pieredzi.
    
5.  **Skriptēšana:** pieredzējuši lietotāji var izmantot iebūvēto skriptu valodu, lai izveidotu sarežģītu rakstzīmju uzvedību, unikālu spēļu mehāniku un specefektus.

## Kā atvērt CFG failu?

MUGEN CFG faili ir vienkārša teksta dokumenti, kas padara tos pieejamus ar dažādiem teksta redaktoriem. Operētājsistēmā Windows varat izmantot Microsoft Notepad vai WordPad, savukārt macOS lietotāji šim nolūkam var izmantot Apple TextEdit. Šie redaktori ļauj lietotājiem viegli skatīt un mainīt konfigurācijas iestatījumus CFG failos.

Programmas, kas atver CFG failus vai atsaucas uz tiem

- Elecbyte MUGEN
- Notepad
- Teksta rediģēšana

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
* [Mugen (spēļu dzinējs)](https://en.wikipedia.org/wiki/Mugen_(game_engine))


