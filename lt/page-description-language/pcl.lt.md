{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PCL",
  "description": "Sužinokite apie PCL failo formatą ir API, kurios gali kurti ir atidaryti PCL failus.",
  "linktitle": "PCL",
  "menu": {
    "docs": {
      "parent": "page-description-language",
      "identifier": "page-description-language-pc-ltl"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra PCL failas? ##

PCL reiškia spausdintuvo komandų kalbą, kuri yra puslapio aprašo kalba, kurią pristatė Hewlett Packard (HP). HP sukūrė PCL, kad būtų veiksmingas būdas valdyti spausdintuvo funkcijas daugelyje skirtingų spausdinimo įrenginių. Formatas iš pradžių buvo sukurtas HP taškiniams ir rašaliniams spausdintuvams, tačiau laikui bėgant buvo įvairių terminių, matricinių ir puslapių spausdintuvų dalis. Formatas buvo keletą kartų peržiūrėtas, todėl buvo sukurtos skirtingos versijos, kuriose kiekviena versija buvo patobulinta, kad atitiktų laiko poreikius, susijusius su spausdintuvo valdymo funkcijomis. Šiandien PCL yra plačiausiai paplitusi spausdintuvų kalba naujausių spausdintuvų rinkoje.

## PCL versijos Nr.

PCL versijos skiriasi funkcionalumu (pvz., šrifto tipo palaikymas: bitmap šriftai, keičiamo dydžio šriftai (Intellifonts, TrueType šriftai), rastrinės grafikos glaudinimo metodai, HP-GL/2 grafinis palaikymas).

**PCL 1:** apie 1980 m. – Spausdinimo ir erdvės funkcija yra pagrindinis funkcijų rinkinys, skirtas paprastam, patogiam vieno vartotojo darbo vietos išvedimui.

**PCL 2:** around 1980 - EDP (Electronic Data Processing)/Transaction functionality is a superset of PCL 1. Pridėtos funkcijos, skirtos bendrosios paskirties, kelių vartotojų sistemos spausdinimui.

**PCL 3**: 1984 - Office Word Processing functionality is a superset of PCL 2. Pridėtos funkcijos, užtikrinančios aukštos kokybės biuro dokumentų gamybą ir padidintą dpi iki 300 dpi. Tai leido naudoti ribotą skaičių taškinių šriftų ir grafikos bei palaiko HP-GL. PCL 3 plačiai mėgdžiojo kiti spausdintuvų gamintojai, o šios bendrovės vadino jį LaserJet Plus emuliacija.
(Spausdintuvai: HP DeskJet šeima, HP LaserJet serijos spausdintuvas, HP LaserJet Plus serijos spausdintuvas)

**PCL3+:** Naudojamas DeskJet ir DesignJet šeimos spausdintuvuose.

**PCL3c:** naudojamas DeskJet ir DesignJet šeimos spausdintuvuose.

**PCL3e**: naudojamas DeskJet ir DesignJet šeimos spausdintuvuose. Dabar taip pat naudojamas PhotoSmart.

**PCL3GUI**: naudoja RTL ir naudoja DeskJet ir DesignJet spausdintuvų šeimos.

**PCLSLEEK**: naudoja RTL ir naudoja DeskJet ir DesignJet spausdintuvų šeimos.

**PCL 4**: 1985 - Page formatting functionality is a superset of PCL 3. Palaikomos makrokomandos, didesni taškiniai šriftai ir grafika. (Spausdintuvai: HP LaserJet II, HP LaserJet IIP (PCL 4.5))

**PCL 5:** 1990 - Office Publishing functionality is a superset of PCL 4. Naujos leidybos galimybės apima šrifto mastelio keitimą ir HP-GL/2 (vektorinę) grafiką. (Spausdintuvai: HP LaserJet III)

**PCL 5e:** 1994 m. – tai didelė peržiūra, apimanti naujas funkcijas, tokias kaip adaptyvioji glaudinimo sistema, 2 baitų simbolių kodavimas, vektorinių šriftų palaikymas ir dvikryptės konfigūracijos komandos. Apima logines operacijas (atitinka GDI ROP), kad pagerintų Windows palaikymą prieš nukirpdami kelius. (Spausdintuvai: HP LaserJet 4)

**PCL 5j:** Naujos funkcijos, pvz., 2 baitų simbolių palaikymas Japonijos nuolatiniams keičiamo dydžio šriftams, vertikalus rašymas, japoniško popieriaus dydžiai ir šrifto eilutės. (Spausdintuvai: HP LaserJet 4PJ)

**PCL 5c:** 1995 - Colour support and Logical Operations was added to PCL5. PCL5c predates PCL5e. Some models also support clipping paths. (Printers: HP Colour LaserJet, HP PaintJet 300 XL (first printer with PCL5c), HP DeskJet 1200C/1600C (these model numbers have been re-used and the newer models are not PCL 5c)

**PCL 5ce:** Palaiko Agfa Microtype keičiamo dydžio šriftus. (Spausdintuvai: HP 2500c Pro spausdintuvas)

**PCL 6 / XL:** 1996 m. – PCL 6 arba PCL XL yra naujas formatas, pristatytas 1995 m., nesuderinamas su jokiomis ankstesnėmis PCL versijomis. (Spausdintuvai: HP LaserJet 5, 5M ir 5N)

## PCL 6 apžvalga ##

HP pristatė PCL 6 1996 m., tai buvo kita PCL kalbos ir susijusių technologijų raida. Jame yra šie komponentai:

**PCL 6 patobulintas:** suteikia optimizuotą versiją, skirtą spausdinti iš grafinių vartotojo sąsajų (GUI), pvz., MS Windows ir OS/2

**PCL 6 standartas:** užtikrina visišką atgalinį suderinamumą su ankstesniais HP LaserJet spausdintuvais

**PCL šriftų sintezė:** suteikia keičiamo dydžio šriftus, šriftų valdymą ir formų bei šriftų saugojimą.

Išplėstinė versija PCL XL yra artimesnė GDI, kurią naudoja daugelis programų. Tai užtikrina, kad būtų atliekama mažiau vertimų, o tai padidintų WYSIWYG galimybes ir pagerintų programų, kurios palaiko patobulintos tvarkyklės įdiegtus pabėgimus, našumą. Patobulintos (PCL XL) tvarkyklės išvestis gali nesutapti su standartinės tvarkyklės išvestimi. Jei išvestis nėra tokia, kokios tikėtasi, vietoj to pasirinkite standartinę (PCL5e) tvarkyklę.

PCL 6 patobulintos komandos sukurtos taip, kad optimaliai atitiktų grafinio spausdinimo reikalavimus, taikomus GUI pagrįstoms programoms. Daugeliu atvejų kiekvienai grafinio spausdinimo komandai, kurią nori atlikti GUI, yra atitinkama komanda PCL 6 Enhanced. Tai sumažina komandų, reikalingų grafiniam puslapiui aprašyti, skaičių. Kiekviena PCL 6 Enhanced komanda sukurta taip, kad iš pagrindinio kompiuterio į spausdintuvą būtų perkeltas minimalus duomenų kiekis. Tai sumažina duomenų, reikalingų puslapiui apibūdinti, kiekį.

Daugumos HP LaserJet spausdintuvų Windows spausdinimo sistemoje yra dvi atskiros tvarkyklės: standartinė ir patobulinta. Standartinė tvarkyklė užtikrina atgalinį suderinamumą, naudodama PCL 6 standarto (PCL5e) komandas, skirtas spausdinti paprastą tekstą arba mišrius teksto ir grafinius puslapius. Patobulinta tvarkyklė naudoja PCL 6 patobulintas komandas, kurios buvo optimizuotos sudėtingiems grafiniams puslapiams spausdinti.

## PCL 6 klasės pataisos Nr.

#### 1.1 klasė ####

**Piešimo įrankiai:** palaiko piešimo linijas, lankus / elipses / akordus, (suapvalintus) stačiakampius, daugiakampius, Bezjė takus, nukirptus takus, rastrinius vaizdus, nuskaitymo linijas, rastrines operacijas.
**Spalvų tvarkymas:** palaiko 1/4/8 bitų paletes, RGB/pilkos spalvų erdvę. Palaikykite pasirinktinius pustonių modelius (maks. 256 raštai).
**Suspaudimas:** Palaiko RLE.
**Matavimo vienetai:** colis, milimetras, dešimtoji milimetro dalis.
**Popieriaus tvarkymas:** palaiko pasirinktinius arba iš anksto nustatytus popieriaus tipų rinkinius, įskaitant įprastus Letter, Legal, A4 ir kt. Galima pasirinkti popierių iš rankinio tiekimo, dėklų, kasečių. Popierius gali būti spausdinamas dvipusiai horizontaliai arba vertikaliai. Popierius gali būti orientuotas vertikaliai, gulsčias arba 180 laipsnių pasukti pirmuosius du.
**Font:** Supports bitmap or TrueType fonts, 8 or 16-bit code points. Choosing character set uses different symbol set code from PCL 5. Kai naudojamas bitmap šriftas, daugelis mastelio keitimo komandų nepasiekiamos. Kai naudojamas TrueType šriftas, kintamo ilgio deskriptoriai, tęsimo blokai nepalaikomi. Kontūro šriftą galima pasukti, keisti mastelį arba nukirpti.

#### 2.0 klasė ####

**Suspaudimas:** Pridėtas patentuotas JPEG glaudinimas, vadinamas JetReady.
**Popieriaus tvarkymas:** spausdinimo medžiaga gali būti nukreipta į skirtingas išvesties dėžes (iki 256). Pridėta A6 ir Japonijos B6 iš anksto nustatyti laikmenos dydžiai. Pridėta trečia iš anksto nustatyta kasetė, 248 išorinio dėklo medijos šaltiniai.
**Šriftas:** Tekstas gali būti rašomas vertikaliai.

#### 2.1 klasė ####

**Spalvų tvarkymas:** Pridėta spalvų derinimo funkcija.
**Suspaudimas:** Pridėta Delta eilutė.
**Popieriaus tvarkymas:** Orientacija, spausdinimo medžiagos dydis yra neprivalomi deklaruojant naują puslapį. Pridėta B5, JIS 8K, JIS 16K, JIS Exec popieriaus rūšys.

#### 3.0 klasė ####

**Spalvų tvarkymas:** leisti naudoti skirtingus pustonių nustatymus vektorinei arba rastrinei grafikai, tekstui. Palaiko adaptyvų pusiau atspalvį.
**Protocol:** Supports PCL passthrough, allowing PCL 5 features to be used by PCL 6 streams. However, some PCL 6 states are not preserved when using this feature.
**Šriftas:** palaiko PCL šriftus.
**Peržiūros priemonė / konverteris:** PCLReader (nemokama programinė įranga) gali peržiūrėti, konvertuoti arba spausdinti bet kokio lygio PCL 6 (įskaitant JetReady) bet kuriame spausdintuve.

## Nuorodos Nr.

* [PCL – Vikipedija](https://en.wikipedia.org/wiki/Printer_Command_Language)


