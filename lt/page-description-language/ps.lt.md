{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PS failo formatas",
  "description": "Sužinokite apie PS failo formatą ir API, kurios gali kurti ir atidaryti PS failus.",
  "linktitle": "PS",
  "menu": {
    "docs": {
      "parent": "page-description-language",
      "identifier": "page-description-language-p-lts"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra .PS failas? ##

PostScript (PS) is a general-purpose page description language used in the business of desktop and electronic publishing. The main focus of PostScript (PS) is to facilitate the two-dimensional graphic design. Most languages require a distinct compilation stage before the code execution while Post Script (PS) format support a runtime straight forward interpretation. Its early version defines the graphical shapes, different text appearances and modelled imageries on printed pages or displayed pages, following the rules of Adobe imaging model. A program of PS is able to intercommunicate a document description between a composition and printing system keeping the device independent and high-level. Moreover this program is also capable of governing the appearance of text and graphics on a display.

PostScript page description is available to be rendered, displayed on printer and other output device with the help of the PostScript interpreter of the device. As the commands to print characters, graphical shapes and images are executed by interpreter, for that specific device, the high-level PostScript description converts into the low level raster data format. Generally, different applications such as illustrators, document composition systems and computer-aided design (CAD) are automated to generate PostScript page descriptions. Generally programmers have to write PostScript programs at the time of new applications creation.  However, a programmer can take advantage of the capabilities of the PostScript language that are not accessible in any application by writing a PS a program for that special situation.

## Trumpa istorija ##

The concept of the PostScript language was first introduced by John Warnock. In 1966 he was working on a project of New York Harbor. He was trying to develop an interpreter for a large three-dimensional graphics for the database of that project. For processing these graphics, John Warnock conceived the Design System language. Meanwhile Xerox PARC were looking for a standard means of defining page images for their first laser printer. Though Bob Sproull and William Newman in 1975-76 developed the Press format (data format) to drive laser printers yet a language was needed for more flexibility. In 1978 Warnock joined Martin Newell in Xerox PARC and rewrote the interpretive language, JaM which was later grew and extended into the Interpress language. Warnock founded Adobe Systems in December 1982 with Chuck Geschke, Doug Brotz, Ed Taft and Bill Paxton. They started working on a simpler language called PostScript similar to Interpress, which released commercially in 1984. Steve'as Jobsas iš Apple aplankė juos ir patarė pritaikyti PostScript lazeriniams spausdintuvams.

1985 m. kovo mėn. pirmasis spausdintuvas su įterptu PostScript interpretatoriumi buvo Apple LaserWriter, kuris sukėlė revoliuciją darbalaukio leidyboje (DTP). Dėl techninio patikimumo ir plačiai paplitusio prieinamumo PostScript tapo pasirinkta stalinio ir elektroninio leidybos kalba. 1990 m. PostScript kalbos vertėjas buvo esminė lazerinių spausdintuvų dalis.

## Pagrindinės funkcijos ##

The capabilities of the PostScript language to deal with interactive graphics and page description possess the following features:

**Formos:** savavališkos prigimties, gali būti sudarytos iš tiesių linijų, kreivių, kvadratų ir kubinių kreivių, kurios gali būti ir savaime einančios, ir atsijungusios (atkarpose ir skylėse).

**Dažymo operatoriai:** leidžia bet kokio storio, spalvos, užpildo formos kontūrus arba leisti figūrą nupiešti kaip iškarpą, kad būtų galima apkarpyti bet kokį kitą grafiką.

**Spalvos:** yra įvairios, pavyzdžiui, pilkos spalvos, RGB, CMYK ir CIE. Specialios spalvos modeliuojamos kaip skirtingos savybės: taškinės spalvos, spalvų atvaizdavimas, tolygus šešėliavimas ir pasikartojantys raštai.

**Tekstas:** visiškai integruotas su grafika. Be to, Adobe vaizdo gavimo modelis leidžia teksto simbolius rodyti kaip grafines formas, kurias gali valdyti bet kuris įprastas grafikos operatorius.

**Vaizdų pavyzdžiai**: paimti iš originalių šaltinių (nuskaitytos nuotraukos) arba gali būti pagaminti sintetiniu būdu. PostScript kalba siūlo įvairias priemones atkurti vaizdus bet kokia skiriamąja geba ir pagal skirtingus spalvų modelius išvesties įrenginyje.

Bendrosios paskirties programavimo kalba gali pasinaudoti PostScript kalbos grafinių galimybių pranašumais, įterpdama Ps į savo sistemą. Primityvūs duomenų tipai, tokie kaip skaičiai, simboliai, masyvai ir eilutės; valdyti primityvus, pvz., kilpas, procedūras ir sąlyginius; ir kai kurios netradicinės funkcijos, pvz., žodynai, yra nurodytos kalboje. Šios funkcijos palengvina programuotojams rašyti komandas, kad iškviestų aukštesnio lygio operacijas. Šios aukšto lygio operacijos atitinka sudėtingo taikymo poreikius. Tokia praktika yra kompaktiškesnė ir efektyvesnė, o ne naudojant fiksuotą pagrindinių operacijų rinkinį.

Programos, parašytos PostScript, gali būti kuriamos, perduodamos ir interpretuojamos ASCII šaltinio teksto forma. Visą kalbą galima apibrėžti spausdinamų simbolių ir tarpų pavidalu. Šis vaizdas padeda programuotojams lengvai kurti, valdyti ir suprasti kalbą. Be to, failų saugojimas ir perdavimas tarp įvairių kompiuterių ir operacinių sistemų buvo patogus dėl mašinos nepriklausomybės.

Galimos dvejetainės užkoduotos kalbos formos, kai programai garantuojamas visiškai skaidrus komunikacijos kelias į PostScript vertėją. Adobe rekomenduoja griežtai suderinti PS programų ASCII atvaizdavimą keičiantis dokumentais arba saugoti archyvus.

## Versijos ##

PS(.ps) is the file extension for a PostScript document. UK National Archives categorize five chronological versions of PostScript file, defined in the DSC version: versions 1.0, 2.0, 2.1, 3.0, 3.1. Kiekviena versija apibrėžia svarbius struktūrinius komentarus. Encapsulated PostScript File (EPS) yra specialus PostScript failo potipis, kuriame naudojama kalba nurodyti stačiakampį grafiką. PostScript kalbos informaciniame vadove EPS aprašomas taip: Inkapsuliuotas PostScript (EPS) failas yra PostScript programa, aprašanti ne daugiau kaip vieną puslapį formoje, kurią kitos programos gali importuoti ir įterpti į turintį dokumentą. PostScript dokumento faile gali būti EPS failas. Papildomas PostScript naudojimas minimas kaip Display PostScript (DPS). DPS sukuria grafiką ekrane naudodama grafikos variklį, kuris naudoja PostScript vaizdo gavimo modelį ir kalbą.

## Nuorodos Nr.

* [PostScript formatų šeima](https://www.loc.gov/preservation/digital/formats/fdd/fdd000029.shtml)


