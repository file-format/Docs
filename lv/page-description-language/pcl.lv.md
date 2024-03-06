{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PCL",
  "description": "Uzziniet par PCL failu formātu un API, kas var izveidot un atvērt PCL failus.",
  "linktitle": "PCL",
  "menu": {
    "docs": {
      "parent": "page-description-language",
      "identifier": "page-description-language-pc-lvl"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir PCL fails? ##

PCL apzīmē Printer Command Language, kas ir Hewlett Packard (HP) ieviestā lappuses apraksta valoda. HP izveidoja PCL, lai nodrošinātu efektīvu veidu, kā kontrolēt printera funkcijas daudzās dažādās drukas ierīcēs. Formāts sākotnēji tika izstrādāts HP punktmatricas un tintes printeriem, taču laika gaitā tas ir bijis daļa no dažādiem termiskajiem, matricas un lapu printeriem. Formātam tika veiktas vairākas dažādas pārskatīšanas, kā rezultātā tika izveidotas dažādas versijas, kur katra versija tika uzlabota, lai atbilstu laika prasībām attiecībā uz printera vadības līdzekļiem. Mūsdienās PCL ir visizplatītākā printeru valoda jaunāko printeru tirgū.

## PCL versijas ##

PCL versijas atšķiras pēc funkcionalitātes (piemēram, fontu veidu atbalsts: bitkartes fonti, mērogojami fonti (Intellifonts, TrueType fonti), rastra grafikas saspiešanas metodes, HP-GL/2 grafiskais atbalsts).

**PCL 1:** ap 1980. gadu — Drukas un telpas funkcionalitāte ir pamata funkciju kopums, kas tiek nodrošināts vienkāršai, ērtai viena lietotāja darbstacijas izvadei.

**PCL 2:** around 1980 - EDP (Electronic Data Processing)/Transaction functionality is a superset of PCL 1. Funkcijas tika pievienotas vispārējai, vairāku lietotāju sistēmas drukāšanai.

**PCL 3**: 1984 - Office Word Processing functionality is a superset of PCL 2. Tika pievienotas funkcijas augstas kvalitātes biroja dokumentu izgatavošanai un palielinātai dpi līdz 300 dpi. Tas ļāva izmantot ierobežotu skaitu bitkartes fontu un grafiku, kā arī atbalstīja HP-GL. PCL 3 plaši atdarināja citi printeru ražotāji, un šie uzņēmumi to sauca par LaserJet Plus emulāciju.
(Printeri: HP DeskJet saime, HP LaserJet sērijas printeris, HP LaserJet Plus sērijas printeris)

**PCL3+:** izmanto DeskJet un DesignJet saimes printeri.

**PCL3c:** izmanto DeskJet un DesignJet saimes printeri.

**PCL3e**: izmanto DeskJet un DesignJet saimes printeri. Tagad tiek izmantots arī PhotoSmart.

**PCL3GUI**: izmanto RTL, un to izmanto DeskJet un DesignJet saimes printeri.

**PCLSLEEK**: izmanto RTL, un to izmanto DeskJet un DesignJet saimes printeri.

**PCL 4**: 1985 - Page formatting functionality is a superset of PCL 3. Atbalstītie makro, lielāki bitkartes fonti un grafika. (Printeri: HP LaserJet II, HP LaserJet IIP (PCL 4.5))

**PCL 5:** 1990 - Office Publishing functionality is a superset of PCL 4. Jaunās publicēšanas iespējas ietver fontu mērogošanu un HP-GL/2 (vektoru) grafiku. (Printeri: HP LaserJet III)

**PCL 5e:** 1994. gads — šī ir liela versija, kas ietver jaunas funkcijas, piemēram, adaptīvā saspiešanas sistēmu, 2 baitu rakstzīmju kodējumu, vektora fontu atbalstu un divvirzienu konfigurācijas komandas. Ietver loģiskās operācijas (atbilst GDI ROP), lai uzlabotu Windows atbalstu pirms apgriešanas ceļiem. (Printeri: HP LaserJet 4)

**PCL 5j:** jaunas funkcijas, piemēram, 2 baitu rakstzīmju atbalsts Japānas mērogojamiem fontiem, vertikālā rakstīšana, japāņu papīra izmēri un burtveidolu virknes. (Printeri: HP LaserJet 4PJ)

**PCL 5c:** 1995 - Colour support and Logical Operations was added to PCL5. PCL5c predates PCL5e. Some models also support clipping paths. (Printers: HP Colour LaserJet, HP PaintJet 300 XL (first printer with PCL5c), HP DeskJet 1200C/1600C (these model numbers have been re-used and the newer models are not PCL 5c)

**PCL 5ce:** atbalsta Agfa Microtype mērogojamus burtveidolus. (Printeri: HP 2500c Pro printeris)

**PCL 6 / XL:** 1996. gads — PCL 6 vai PCL XL ir jauns formāts, kas tika ieviests 1995. gadā un nav saderīgs ar iepriekšējām PCL versijām. (Printeri: HP LaserJet 5, 5M un 5N)

## PCL 6 pārskats ##

HP ieviesa PCL 6 1996. gadā, kas bija nākamā PCL valodas un saistīto tehnoloģiju attīstība. Tajā ir šādas sastāvdaļas:

**PCL 6 uzlabots:** nodrošina optimizētu versiju drukāšanai no grafiskām lietotāja saskarnēm (GUI), piemēram, MS Windows un OS/2

**PCL 6 standarts:** nodrošina pilnīgu atpakaļsaderību ar iepriekšējiem HP LaserJet printeriem

**PCL fontu sintēze:** nodrošina mērogojamus fontus, fontu pārvaldību un veidlapu un fontu glabāšanu.

Paplašinātā versija PCL XL ir tuvāka GDI, ko izmanto daudzas lietojumprogrammas. Tas nodrošina, ka tiek veikts mazāk tulkojumu, kā rezultātā tiek palielinātas WYSIWYG iespējas un labāka veiktspēja ar lietojumprogrammām, kas atbalsta uzlabotā draivera ieviestās izejas. Uzlabotā (PCL XL) draivera izvade var nebūt tāda pati kā standarta draivera izvade. Ja izvade nav tāda, kā gaidīts, tā vietā izvēlieties standarta (PCL5e) draiveri.

PCL 6 uzlabotās komandas ir izstrādātas, lai optimāli atbilstu grafikas drukāšanas prasībām lietojumprogrammām, kuru pamatā ir GUI. Vairumā gadījumu katrai grafikas drukāšanas komandai, ko GUI vēlas izpildīt, ir atbilstoša PCL 6 uzlabotā komanda. Tas samazina grafiskās lapas aprakstīšanai nepieciešamo komandu skaitu. Katra komanda programmā PCL 6 Enhanced ir izstrādāta tā, lai būtu nepieciešama minimāla datu pārsūtīšana no resursdatora uz printeri. Tas samazina lapas aprakstīšanai nepieciešamo datu apjomu.

Windows drukas sistēma lielākajai daļai HP LaserJet printeru nodrošina divus atsevišķus draiverus: standarta un uzlaboto. Standarta draiveris nodrošina atpakaļsaderību, izmantojot PCL 6 Standard (PCL5e) komandas, lai drukātu vienkāršu tekstu vai jauktas teksta un grafikas lapas. Uzlabotais draiveris izmanto PCL 6 Enhanced komandas, kas ir optimizētas sarežģītu grafikas lapu drukāšanai.

## PCL 6 klases versijas ##

#### 1.1. klase ####

**Zīmēšanas rīki:** atbalsta līniju, loku/elipšu/akordu, (noapaļotu) taisnstūru, daudzstūru, Bezjē celiņu, apgrieztu celiņu, rastra attēlu, skenēšanas līniju, rastra operāciju zīmēšanu.
**Krāsu apstrāde:** Atbalsta 1/4/8 bitu paletes, RGB/pelēko krāsu telpu. Atbalstiet pielāgotus pustoņu modeļus (ne vairāk kā 256 raksti).
**Saspiešana:** atbalsta RLE.
**Mērvienības:** collas, milimetrs, milimetra desmitā daļa.
**Papīra apstrāde:** atbalsta pielāgotas vai iepriekš noteiktas papīra veidu kopas, tostarp parastās Letter, Legal, A4 utt. Var izvēlēties papīru no manuālās padeves, paplātēm, kasetēm. Papīru var drukāt abpusēji horizontāli vai vertikāli. Papīrs var būt orientēts portretā, ainavā vai 180 grādu pagriešanas režīmā.
**Font:** Supports bitmap or TrueType fonts, 8 or 16-bit code points. Choosing character set uses different symbol set code from PCL 5. Ja tiek izmantots bitkartes fonts, daudzas mērogošanas komandas nav pieejamas. Ja tiek izmantots TrueType fonts, mainīga garuma deskriptori un turpinājuma bloki netiek atbalstīti. Kontūras fontu var pagriezt, mērogot vai nogriezt.

#### 2.0 klase ####

**Saspiešana:** pievienota patentēta JPEG saspiešana ar nosaukumu JetReady.
**Papīra apstrāde:** apdrukājamo materiālu var novirzīt uz dažādām izvades tvertnēm (līdz 256). Pievienoti A6 un japāņu B6 iepriekš iestatītie materiāla izmēri. Pievienots Trešās kasetes priekšiestatījums, 248 ārējās paplātes materiāla avoti.
**Fonts:** tekstu var rakstīt vertikāli.

#### 2.1. klase ####

**Krāsu apstrāde:** Pievienota krāsu saskaņošanas funkcija.
**Saspiešana:** pievienota Delta rinda.
**Papīra apstrāde:** Orientācija, apdrukājamā materiāla izmērs nav obligāti, deklarējot jaunu lapu. Pievienoti B5, JIS 8K, JIS 16K, JIS Exec papīra veidi.

#### 3.0 klase ####

**Krāsu apstrāde:** ļauj izmantot dažādus pustoņu iestatījumus vektoru vai rastra grafikai, tekstam. Atbalsta adaptīvo pustonēšanu.
**Protocol:** Supports PCL passthrough, allowing PCL 5 features to be used by PCL 6 streams. However, some PCL 6 states are not preserved when using this feature.
**Fonts:** atbalsta PCL fontus.
**Skatītājs/pārveidotājs:** PCLReader (bezmaksas programmatūra) var skatīt, pārveidot vai drukāt jebkura līmeņa PCL 6 (tostarp JetReady) jebkurā printerī.

## Atsauces Nr.

* [PCL — Wikipedia](https://en.wikipedia.org/wiki/Printer_Command_Language)


