{
   "date":"2023-10-18",
   "keywords":[
"cpi",
"cpi failu",
"cpi koda lapas informācijas fails",
"kā atvērt cpi failu",
"failu",
"cpi faila paplašinājums",
"pagarinājumu",
"failu"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"CPI faila formāts — koda lapas informācijas fails",
   "description":"Uzziniet par CPI Codepage Information faila formātu un API, kas var izveidot un atvērt CPI failus.",
   "linktitle":"CPI",
   "menu":{
      "docs":{
         "identifier":"system-cpi-lv",
         "parent":"system"
}
},
   "lastmod":"2023-10-18"
}

## Kas ir CPI fails?

.cpi fails Microsoft Windows un DOS operētājsistēmu kontekstā parasti ir **koda lapas informācijas fails.** Šajos failos ir informācija par kodu lapām, kas tiek izmantotas teksta kodēšanai un rakstzīmju kopu kartēšanai. Kodu lapas ir būtiskas teksta attēlošanai un apstrādei dažādās valodās un rakstzīmju kopās.

Operētājsistēmu Windows un DOS kontekstā kodu lapas tiek izmantotas, lai noteiktu, kā rakstzīmes tiek attēlotas un kodētas dažādās valodās un reģionos. Šīs kodu lapas nosaka, kā rakstzīmes tiek saglabātas atmiņā un parādītas ekrānā. Katrai koda lapai ir unikāls identifikators, un .cpi failos tiek glabāta informācija par šīm kodu lapām, tostarp informācija, piemēram, rakstzīmju kartējumi un fontu informācija.

.cpi faili parasti ir atrodami Windows vai DOS sistēmas direktorijos, un tiem ir izšķiroša nozīme, lai operētājsistēma varētu pareizi parādīt tekstu dažādām lokalizācijām un rakstzīmju kopām. Tie palīdz sistēmai saprast, kā interpretēt un renderēt dažādu valodu un kodējumu rakstzīmes.

## Kodu lapas informācijas faili

Sīkāk apskatīsim koda lapas informācijas failus (.cpi) un to darbību MS-DOS un Microsoft Windows iepriekšējo iterāciju ietvaros:

1.  **Rakstzīmju kodējums un kodu lapas**: kodu lapas ir būtiska teksta kodēšanas un parādīšanas sastāvdaļa datorā. Tie nosaka rakstzīmju kodējumu noteiktai valodai vai rakstzīmju kopai. Katra kodu lapa rakstzīmēm piešķir skaitliskas vērtības (koda punktus), ļaujot datoram tās attēlot un attēlot. Piemēram, ASV un Rietumeiropā parasti tiek izmantota koda lapa 437, savukārt koda lapa 850 tiek izmantota latīņu-1 kodēšanai.
    
2.  **Sistēmas inicializācija**: sistēmas inicializēšanas laikā (kad dators tiek palaists), MS-DOS un vecākas Windows versijas nolasa `.cpi` failus, lai noteiktu, kuras kodu lapas atbalstīt. Šī informācija bija ļoti svarīga teksta renderēšanai, tastatūras ievadei un rakstzīmju kopas pārveidošanai.
    
3.  **Displeja un tastatūras atbalsts**: šie faili sniedz informāciju par to, kā rakstzīmes jāparāda ekrānā un kuras rakstzīmju kopas vai kodu lapas jāatbalsta tastatūras ievadei. Dažādas kodu lapas definē dažādas rakstzīmju kopas, tāpēc šie faili palīdz operētājsistēmai zināt, kā pareizi rīkoties ar lietotāja ievadi un parādīt tekstu.
    
4.  **Lokalizācija**: `.cpi` faili ir būtiski operētājsistēmas lokalizācijai. Tie ļauj sistēmai pielāgoties dažādām valodām, reģioniem un rakstzīmju kopām, ļaujot lietotājiem visā pasaulē izmantot MS-DOS vai Windows sev vēlamajās valodās.
    
5.  **Vairāki .cpi faili**: datorā ar daudzvalodu atbalstu varat atrast vairākus .cpi failus, kas atbilst dažādām kodu lapām. Piemēram, sistēmai var būt 437.cpi” Amerikas Savienotajām Valstīm, 850.cpi” Latīņu-1, 852.cpi” Centrāleiropai un tā tālāk. Atbilstošais fails tiek ielādēts, pamatojoties uz lietotāja lokalizāciju vai atlasīto koda lapu.
    
6.  **Fontu informācija**: papildus rakstzīmju kartējumiem šajos failos var būt ietverta informācija par fontu, norādot, kuri fonti jāizmanto katrai kodu lapai. Tas ir svarīgi, lai atveidotu tekstu atbilstošā stilā un izmērā.
    
7.  **Mantotās sistēmas**: `.cpi` faili bija biežāk sastopami vecākās MS-DOS un Windows versijās. Mūsdienu Windows versijās (piemēram, Windows 10 un jaunākās versijās) teksta kodēšanai parasti tiek izmantots Unicode, kas atbalsta plašu rakstzīmju un valodu klāstu. Unicode vienkāršo teksta apstrādi daudzvalodu vidē un ir mūsdienu programmatūras standarts.

## Kā atvērt CPI failu?

.CPI (koda lapas informācijas) faila atvēršana nav tipiska lietotāja darbība, un šie faili parasti nav paredzēti manuālai atvēršanai. Operētājsistēma tos izmanto, lai pārvaldītu teksta kodējumu un rakstzīmju kopas, un sistēma to saturam piekļūst un to izmanto automātiski.

Tomēr, ja vēlaties skatīt .CPI faila saturu informatīvos nolūkos, varat mēģināt to atvērt, izmantojot teksta redaktoru vai heksadecimālo skatītāju. Lūk, kā varat mēģināt atvērt .CPI failu:

1.  **Teksta redaktors**: varat izmantot teksta redaktoru, piemēram, Notepad (operētājsistēmā Windows) vai jebkuru vienkārša teksta redaktoru citās operētājsistēmās, lai atvērtu un skatītu .CPI failu. Ņemiet vērā, ka .CPI failu saturs nav paredzēts cilvēkiem lasāms, un jūs varat redzēt rakstzīmju sērijas, kuras ir grūti interpretēt.
    
2.  **Heksadecimālais skatītājs**: var izmantot heksadecimālo skatītāju vai heksadecimālo redaktoru, lai atvērtu un pārbaudītu .CPI faila saturu tā neapstrādātā binārajā formā. Hex redaktori nodrošina detalizētāku faila datu skatu, kas var būt noderīgi, ja mēģināt izprast tā struktūru. Šādas programmatūras piemēri ir HxD, Hex Fiend (operētājsistēmai macOS) un 010 redaktors.

## Citi CPI faili

Tālāk ir norādīti citi failu tipi, kas izmanto faila paplašinājumu **.cpi**.

**Video un sistēma**
- [CPI - AVCHD Video Clip Information](/video/cpi/)
- [CPI - Codepage Information File](/system/cpi/)

## Atsauces
* [Koda lapa](https://en.wikipedia.org/wiki/Code_page)


