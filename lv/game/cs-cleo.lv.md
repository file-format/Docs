{
   "date":"2023-01-04",
   "keywords":[
"cs",
"cs fails",
"cs cleo pielāgotais skripts",
"kā atvērt cs failu",
"failu",
"cs faila paplašinājums",
"pagarinājumu",
"failu"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"CS faila formāts — CLEO pielāgotais skripts",
   "description":"Uzziniet par CS CLEO pielāgotā skripta formātu un API, kas var izveidot un atvērt CS failus.",
   "linktitle":"CS CLEO",
   "menu":{
      "docs":{
         "identifier":"game-cs-cleo-lv",
         "parent":"game"
}
},
   "lastmod":"2023-01-04"
}

## Kas ir CS fails?

.CS fails CLEO kontekstā (saīsinājums no CLEO bibliotēkas) parasti attiecas uz pielāgotu skripta failu, ko izmanto Grand Theft Auto (GTA) videospēļu sērijā. CLEO ir populārs modificēšanas ietvars, kas ļauj spēlētājiem izveidot un pievienot pielāgotus skriptus GTA spēlēm, ļaujot viņiem modificēt spēles gaitu, pievienot jaunas funkcijas un uzlabot kopējo spēļu pieredzi.

## CS faila pārskats

Tālāk ir sniegts pamata pārskats par to, ko var saturēt .cs fails programmā CLEO.

1.  **Skripta kods**: .cs failā ir skripta kods, kas rakstīts CLEO skriptu valodā. Šī skriptu valoda ir raksturīga CLEO un tiek izmantota, lai definētu pielāgoto skriptu uzvedību spēlē. Kodu var rakstīt, izmantojot teksta redaktoru, un tas parasti atbilst noteiktai sintaksei.
    
2.  **Modifications**: CLEO scripts can make various modifications to game such as changing behavior of in-game objects, creating custom missions, adding new vehicles, weapons and more. The possibilities are extensive and depend on creativity and programming skills of script author.
    
3.  **Aktivizatori**: CLEO skripti bieži ietver aktivizētājus, kas nosaka, kad un kā pielāgotajam skriptam jādarbojas. Šie aktivizētāji var būt balstīti uz notikumiem spēlē, spēlētāja darbībām vai īpašiem nosacījumiem.
    
4.  **Mainīgie un funkcijas**: CLEO skripti var izmantot mainīgos, lai uzglabātu un apstrādātu datus, kā arī funkcijas, lai iekapsulētu un atkārtoti izmantotu kodu. Šie mainīgie un funkcijas tiek izmantoti, lai kontrolētu skripta uzvedību.

## CS faila piemērs

Šeit ir vienkāršs CLEO .cs skripta piemērs, kas maina laika apstākļus spēlē:

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

## CLEO bibliotēka

**CLEO bibliotēka**, ko bieži dēvē vienkārši par CLEO, ir populāra un jaudīga modifikācijas sistēma Grand Theft Auto (GTA) videospēļu sērijai. Tas ļauj spēlētājiem un modificētājiem izveidot un pievienot pielāgotus skriptus GTA spēlēm, ļaujot viņiem mainīt spēles gaitu, pievienot jaunas funkcijas un uzlabot kopējo spēļu pieredzi. CLEO ir īpaši labi pazīstams ar savu elastību un ērtu lietošanu GTA modificēšanas kopienā.

Šeit ir dažas galvenās CLEO bibliotēkas funkcijas un aspekti:

1.  **Skriptu valoda**: CLEO ievieš savu skriptu valodu, kas ir raksturīga modificēšanas sistēmai. Skriptu valoda ir izstrādāta tā, lai tā būtu salīdzinoši viegli saprotama un darbotos ar to, padarot to pieejamu gan iesācējiem, gan pieredzējušiem modificētājiem.
    
2.  **Pielāgoti skripti**: izmantojot CLEO, varat izveidot pielāgotus skriptus, kas spēļu pasaulē var veikt plašu funkciju klāstu. Šie skripti var mainīt uzvedību spēlē, pievienot jaunas misijas, ieviest jaunus transportlīdzekļus vai ieročus, mainīt spēles fiziku un daudz ko citu.
    
3.  **Izsaucēji un notikumi**: CLEO skriptus var aktivizēt dažādi spēles notikumi, spēlētāja darbības vai īpaši apstākļi. Tas ļauj modderiem izveidot dinamisku un interaktīvu saturu spēlē.
    
4.  **Support for Multiple GTA Versions**: CLEO has versions tailored to different GTA games, including GTA III, GTA Vice City, GTA San Andreas, GTA IV and others. This means that modders can create and share their custom scripts for different GTA titles.

## CLEO bibliotēkas izmantotie failu formāti

CLEO modifikācijā Grand Theft Auto (GTA) spēlēm moduļu izveidei un instalēšanai parasti tiek izmantoti vairāki failu formāti. Šie failu formāti kalpo dažādiem mērķiem, sākot no faktisku skriptu saturēšanas līdz papildu resursu, piemēram, faktūru, modeļu vai audio, glabāšanai. Šeit ir daži no galvenajiem failu formātiem, kas tiek izmantoti CLEO modifikācijā:

1.  **.cs (pielāgots skripts)**: CLEO .cs faili ir pielāgoti skriptu faili, kas rakstīti CLEO skriptu valodā. Šajos failos ir kods, kas nosaka mod uzvedību un funkcionalitāti. .cs faili ir CLEO modifikācijas pamatā, un tos izpilda spēle, lai ieviestu pielāgotas funkcijas.
    
2.  **.csa (pielāgots skriptu arhīvs)**: .csa faili ir arhīvi, kuros var saglabāt vairākus .cs skripta failus. Tos bieži izmanto, lai kopā iesaiņotu saistītos skriptus, lai atvieglotu instalēšanu un pārvaldību.
    
3.  **.fxt (teksta faili)**: .fxt faili ir teksta faili, kurus var izmantot, lai lokalizētu vai nodrošinātu teksta tulkojumus CLEO modifikācijām. Tie satur teksta virknes, kuras var parādīt spēlē, padarot modifikācijas pieejamas spēlētājiem dažādās valodās.
    
4.  **[.bmp](/image/bmp/), [.png](/image/png/), [.jpg](/image/jpeg/) (attēlu formāti)**: šie attēlu formāti tiek izmantoti, lai saglabātu tekstūras un attēlus modifikācijām. Tos var izmantot pielāgotām ādām, transportlīdzekļu faktūrām, HUD elementiem un citiem. Atkarībā no spēles priekšroka var tikt dota dažādiem attēlu formātiem.

## Kā atvērt CS failu?

Lai atvērtu un skatītu CLEO .cs (Custom Script) faila saturu, varat izmantot teksta redaktoru vai koda redaktoru pēc savas izvēles. Kopējā izvēle ietver:

- **Notepad**: vienkāršs teksta redaktors, kas ir iepriekš instalēts operētājsistēmā Windows.
- **Notepad++**: ar funkcijām bagātāks teksta redaktors, kas paredzēts kodēšanai un skriptu veidošanai.
- **Visual Studio Code**: populārs, bezmaksas un ļoti paplašināms koda redaktors.
- **Sublime Text**: vēl viens koda redaktors, kas pazīstams ar savu ātrumu un daudzpusību.
- **Atom**: atvērtā pirmkoda koda redaktors, ko izstrādājis GitHub.

## Citi CS faili

Tālāk ir norādīti citi failu veidi, kuros tiek izmantots faila paplašinājums **.cs**.

**Datu faili un spēle**
- [CS - ColorSchemer Studio Color Scheme](/data/cs-colorschemer/)
- [CS - CLEO Custom Script](/game/cs-cleo/)

**Programmēšana**
- [CS - CSharp Code File](/programming/cs/)

## Atsauces
* [CLEO bibliotēka](https://cleo.li/)


