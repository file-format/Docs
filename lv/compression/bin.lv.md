{
   "date":"2023-07-20",
   "keywords":[
"BIN",
"BIN fails",
"failu",
"BIN faila paplašinājums",
"pagarinājumu",
"failu"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"BIN faila formāts — MacBinary kodēts fails",
   "description":"Uzziniet par BIN formātu un API, kas var izveidot un atvērt BIN failus.",
   "linktitle":"BIN",
   "menu":{
      "docs":{
         "identifier":"compression-bin-lv",
         "parent":"compression"
}
},
   "lastmod":"2023-07-20"
}

## Kas ir BIN fails?

BIN fails Macintosh datoru kontekstā var attiekties uz failu, kas saglabāts MacBinary formātā. MacBinary ir faila formāts, kas īpaši paredzēts Macintosh failu pārsūtīšanai, izmantojot internetu, e-pastu, FTP vai portatīvo datu nesēju. MacBinary mērķis ir vienā failā saglabāt visu Macintosh failu failu struktūru un atribūtus, tostarp gan datu dakšu, gan resursu dakšiņu.

MacBinary formāts to panāk, saspiestā failā iekapsulējot Macintosh hierarhiskās failu sistēmas (HFS) resursu dakšiņu un datu dakšiņu. Tajā ir arī meklētāja galvene, kas satur svarīgus metadatus par failu. Apvienojot visus šos komponentus vienā failā, MacBinary nodrošina, ka fails saglabā savu integritāti un to var viegli pārsūtīt un koplietot dažādās platformās.

Pateicoties Apple failu sistēmu un failu pārsūtīšanas protokolu attīstībai, BIN failu un MacBinary formāta izmantošana ir kļuvusi mazāk izplatīta. Tādu failu formātu kā ZIP ieviešana un pāreja uz modernākām failu sistēmām, piemēram, HFS+ un APFS, ir samazinājusi vajadzību pēc MacBinary kodētiem failiem. Šīs jaunākās failu sistēmas nodrošina efektīvākus veidus, kā rīkoties ar failu atribūtiem, resursu dakšām un datu dakšām, padarot MacBinary formātu mazāk nepieciešamu mūsdienu skaitļošanas vidē.

## BIN faila formāts — vairāk informācijas 

Macintosh datoru pirmsākumos datu ierobežojumu dēļ faili tika glabāti divās atsevišķās dakšās. Resursu dakša saturēja strukturētus datus, savukārt datu dakša glabāja nestrukturētus datus. Lai gan klasiskajā Mac OS versijā šīs dakšas tika uzskatītas par vienu failu, failu pārsūtīšana uz sistēmām, kas nav Mac, izraisīja datu zudumu, jo tās neatzina dakšas kā vienu vienību. Lai to risinātu, MacBinary formātu izveidoja tādi cilvēki kā Deniss Brothers, Harijs Česlijs un Īvs Lemperers. MacBinary saspieda un apvienoja dakšas vienā failā, kas pazīstams kā BIN fails, lai pārsūtītu uz sistēmām, kas nav Mac. Atgriežoties operētājsistēmā Mac OS, dakšas atkal tiks atdalītas. Līdz ar pāreju no uz dakšām balstītā HFS 2000. gados, MacBinary formāta izmantošana ievērojami samazinājās. Mūsdienās MacBinary kodētu BIN failu var atrast reti, ja vien neatrodat vecu failu sistēmā, kas nav Mac, vai lejupielādējat to no interneta.

The MacBinary format has gone through several versions over time to accommodate changes in Macintosh systems and file handling. Here are some of the different versions of the MacBinary format:

- **MacBinary I:** sākotnējā MacBinary versija, kas tika ieviesta 1980. gadu beigās. Tas apvienoja resursu dakšu un datu dakšu vienā binārā failā, ļaujot pārsūtīt Macintosh failus starp platformām.

- **MacBinary II:** šī versija, kas tika izlaista 90. gadu sākumā, uzlaboja sākotnējo MacBinary formātu, binārā faila galvenē pievienojot papildu informāciju, piemēram, faila veidu un veidotāja kodus. Šie kodi palīdzēja saglabāt Macintosh failu integritāti un identifikāciju pārsūtīšanas laikā.

- **MacBinary III:** The MacBinary III format, introduced in the mid-1990s, further enhanced the previous versions by including additional metadata, such as file name and file creation and modification dates, in the binary file's header. This allowed for more comprehensive preservation of Macintosh file attributes during transfer.

- **MacBinary IV:** MacBinary IV tika izstrādāts, lai 2000. gadu sākumā risinātu saderības problēmas ar jauno Mac OS X operētājsistēmu. Tajā tika iekļautas izmaiņas, lai pielāgotos jaunajai failu sistēmas struktūrai un atribūtiem, kas ieviesti operētājsistēmā Mac OS X.

## Kā atvērt BIN failu?

MacBinary Encoded BIN failus var atvērt, izmantojot dažādas saspiešanas utilītas. MacOS lietotājiem piemērota opcija ir **Apple Archive Utility**. Windows lietotāji var izmantot programmatūru, piemēram, **Smith Micro StuffIt Deluxe**, lai izvilktu MacBinary Encoded BIN faila saturu. Vēl viena iespēja MacOS lietotājiem ir **The Unarchiver**, kas ir daudzpusīgs rīks, kas spēj apstrādāt vairākus failu formātus, tostarp MacBinary.

Ir svarīgi atzīmēt, ka .bin faila paplašinājumu izmanto dažādi failu formāti, ne tikai MacBinary. Tāpēc, ja jūs saskaraties ar BIN failu, kuru nevar atvērt ar iepriekšminētajām utilītprogrammām, tas var tikt saglabāts citā formātā. Šādos gadījumos, lai piekļūtu faila saturam, iespējams, būs jānorāda konkrētais faila formāts un jāizmanto šim formātam paredzēta atbilstoša programmatūra vai utilīta.

## Kas ir Macbinary Archive?

MacBinary arhīvs ir faila formāts, kas paredzēts agrīniem Macintosh datoriem, kas attiecas uz Macintosh failu divu dakšu struktūru. Macintosh failu sistēmas sastāv no datu dakšas un resursu dakšas, kas satur datus un metadatus atsevišķi. Lai atvieglotu starpsistēmu savietojamību un tīkla pārsūtīšanu, MacBinary abas dakšas kodē vienā binārā failā. Šis formāts saglabā datu un saistīto resursu integritāti pārsūtīšanas laikā uz sistēmām, kas nav Macintosh sistēmas.

## Vai es varu izdzēst Macbinary arhīvu?

Jā, varat izdzēst MacBinary arhīva failus, ja tie vairs nav nepieciešami vai ja esat izvilcis saturu un saglabājis tos citā formātā. MacBinary arhīvi ir vienkārši Macintosh failu iesaiņošanas metode īpašiem mērķiem, piemēram, pārsūtīšanai starp sistēmām vai uzglabāšanai. Arhīva dzēšana neietekmē tajā esošos failus.

## Kā iPhone tālrunī atvērt Macbinary arhīvu?

MacBinary arhīva atvēršanai iPhone tālrunī, iespējams, būs jāizmanto trešo pušu lietotnes, jo operētājsistēmā iOS nav šī formāta vietējā atbalsta.

## Macbinary Archive Extract — kā izvilkt Macintosh Bin failus?

Lai izvilktu MacBinary (bin) failus modernā datorā, parasti jāizmanto failu ekstrakcijas utilīta vai programmatūra, kas atbalsta šo formātu.

Operētājsistēmā Windows izmantojiet failu arhivēšanas rīku, kas atbalsta MacBinary failus. Populāras iespējas ir WinRAR, 7-Zip vai WinZip.

Operētājsistēmā Mac OS ir iebūvēta arhīva utilīta, kas var apstrādāt dažādus arhīva formātus, tostarp MacBinary. Programmā Finder atrodiet MacBinary failu. Veiciet dubultklikšķi uz MacBinary faila. Arhīva utilītai vajadzētu automātiski palaist un izvilkt saturu. Kad izvilkšana ir pabeigta, varat atrast izvilktos failus tajā pašā vietā, kur oriģinālais MacBinary fails, vai norādītajā galamērķī.

## Citi BIN faili

Šeit ir citi failu tipi, kas izmanto faila paplašinājumu **.bin**.

- [BIN - Binary Disc Image File](/disc-and-media/bin/)
- [BIN - Unix Executable File](/executable/bin/)
- [BIN - BlackBerry IT Policy File](/settings/bin/)
- [BIN - Sega Genesis Game ROM](/game/bin/)
- [BIN - PSX PlayStation BIOS Image](/game/bin-pcsx/)

## Atsauces

* [MacBinary](https://en.wikipedia.org/wiki/MacBinary)


