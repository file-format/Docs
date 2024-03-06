{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PS faila formāts",
  "description": "Uzziniet par PS faila formātu un API, kas var izveidot un atvērt PS failus.",
  "linktitle": "PS",
  "menu": {
    "docs": {
      "parent": "page-description-language",
      "identifier": "page-description-language-p-lvs"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir .PS fails? ##

PostScript (PS) is a general-purpose page description language used in the business of desktop and electronic publishing. The main focus of PostScript (PS) is to facilitate the two-dimensional graphic design. Most languages require a distinct compilation stage before the code execution while Post Script (PS) format support a runtime straight forward interpretation. Its early version defines the graphical shapes, different text appearances and modelled imageries on printed pages or displayed pages, following the rules of Adobe imaging model. A program of PS is able to intercommunicate a document description between a composition and printing system keeping the device independent and high-level. Moreover this program is also capable of governing the appearance of text and graphics on a display.

PostScript page description is available to be rendered, displayed on printer and other output device with the help of the PostScript interpreter of the device. As the commands to print characters, graphical shapes and images are executed by interpreter, for that specific device, the high-level PostScript description converts into the low level raster data format. Generally, different applications such as illustrators, document composition systems and computer-aided design (CAD) are automated to generate PostScript page descriptions. Generally programmers have to write PostScript programs at the time of new applications creation.  However, a programmer can take advantage of the capabilities of the PostScript language that are not accessible in any application by writing a PS a program for that special situation.

## Īsa vēsture ##

The concept of the PostScript language was first introduced by John Warnock. In 1966 he was working on a project of New York Harbor. He was trying to develop an interpreter for a large three-dimensional graphics for the database of that project. For processing these graphics, John Warnock conceived the Design System language. Meanwhile Xerox PARC were looking for a standard means of defining page images for their first laser printer. Though Bob Sproull and William Newman in 1975-76 developed the Press format (data format) to drive laser printers yet a language was needed for more flexibility. In 1978 Warnock joined Martin Newell in Xerox PARC and rewrote the interpretive language, JaM which was later grew and extended into the Interpress language. Warnock founded Adobe Systems in December 1982 with Chuck Geschke, Doug Brotz, Ed Taft and Bill Paxton. They started working on a simpler language called PostScript similar to Interpress, which released commercially in 1984. Stīvs Džobss no Apple viņus apmeklēja un ieteica pielāgot PostScript lāzerprinteru vadīšanai.

1985. gada martā pirmais printeris ar iegulto PostScript tulku bija Apple LaserWriter, kas radīja apvērsumu darbvirsmas publicēšanā (DTP). Tehniskā stabilitāte un plašā pieejamība padarīja PostScript par iecienītāko valodu galddatoriem un elektroniskajai publicēšanai. 1990. gadā PostScript valodas tulks bija būtiska lāzerprinteru sastāvdaļa.

## Galvenās iezīmes ##

The capabilities of the PostScript language to deal with interactive graphics and page description possess the following features:

**Formas:** pēc būtības patvaļīgas, var sastāvēt no taisnām līnijām, līknēm, kvadrātiem un kubiskām līknēm, kas var būt gan paššķērsojošas, gan atvienotas (sekcijās un caurumos).

**Glezniecības operatori:** ļauj veidot jebkura biezuma, krāsas, aizpildījuma formas kontūru vai ļauj zīmēt formu kā izgriezumu, lai varētu apgriezt jebkuru citu grafiku.

**Krāsas:** ir dažādas, piemēram, pelēktoņu, RGB, CMYK un CIE. Īpaši krāsu veidi tiek modelēti kā dažādas iezīmes: punktkrāsas, krāsu kartēšana, vienmērīga ēnošana un atkārtojoši raksti.

**Teksts:** pilnībā integrēts ar grafiku. Turklāt Adobe attēlveidošanas modelis ļauj teksta rakstzīmes attēlot kā grafiskas formas, kuras var darbināt jebkurš parasts grafikas operators.

**Attēlu paraugi**: iegūti no oriģinālajiem avotiem (skenētas fotogrāfijas) vai var tikt izgatavoti sintētiski. PostScript valoda piedāvā dažādus līdzekļus attēlu atjaunošanai jebkurā izšķirtspējā un atbilstoši dažādiem krāsu modeļiem izvades ierīcē.

Universāla programmēšanas valoda var izmantot PostScript valodas grafisko iespēju priekšrocības, savā ietvarā iestrādājot Ps. Primitīvie datu tipi, piemēram, skaitļi, rakstzīmes, masīvi un virknes; kontrolēt primitīvus, piemēram, cilpas, procedūras un nosacījumus; valodā ir norādītas dažas netradicionālas funkcijas, piemēram, vārdnīcas. Šīs funkcijas atvieglo programmētājiem rakstīt komandas, lai izsauktu augstāka līmeņa darbības. Šīs augsta līmeņa darbības atbilst sarežģītas lietojumprogrammas vajadzībām. Šāda prakse ir kompaktāka un efektīvāka, nevis izmantojot fiksētu pamatoperāciju kopu.

Programmas, kas rakstītas PostScript, var izveidot, sazināties un interpretēt ASCII avota teksta veidā. Visu valodu var definēt drukājamu rakstzīmju un atstarpju veidā. Šis attēlojums palīdz programmētājiem viegli izveidot, manipulēt un saprast valodu. Turklāt failu glabāšana un pārsūtīšana starp dažādiem datoriem un operētājsistēmām ir ērta, pateicoties mašīnas neatkarībai.

Bināri kodētas valodas formas ir iespējamas, ja programmai ir garantēts pilnībā caurspīdīgs saziņas ceļš uz PostScript tulku. Adobe iesaka stingru saskaņotību ar PS programmu ASCII attēlojumu dokumentu apmaiņai vai arhīva glabāšanai.

## Versijas ##

PS(.ps) is the file extension for a PostScript document. UK National Archives categorize five chronological versions of PostScript file, defined in the DSC version: versions 1.0, 2.0, 2.1, 3.0, 3.1. Katrā versijā ir noteikti svarīgi strukturēšanas komentāri. Iekapsulētais PostScript fails (EPS) ir īpašs PostScript faila apakštips, kas izmanto valodu, lai norādītu taisnstūrveida grafiku. PostScript valodas uzziņu rokasgrāmatā EPS ir aprakstīts šādi: Ikapsulēts PostScript (EPS) fails ir PostScript programma, kas apraksta ne vairāk kā vienu lappusi formā, ko var importēt citas lietojumprogrammas, lai iegultu saturošā dokumentā. PostScript dokumenta fails tajā var iekapsulēt EPS failu. Papildu PostScript izmantošana ir minēta kā Display PostScript (DPS). DPS ģenerē ekrāna grafiku, izmantojot grafikas dzinēju, kas izmanto PostScript attēlveidošanas modeli un valodu.

## Atsauces Nr.

* [PostScript formātu saime](https://www.loc.gov/preservation/digital/formats/fdd/fdd000029.shtml)


