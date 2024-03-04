{
  "date": "2019-12-12",
  "keywords": [
"JT",
"failą",
"pratęsimas",
"formatu",
"3D fbx",
""
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie JT failo formatą ir API, kurios gali kurti ir atidaryti JT failus.",
  "title": "JT – Jupiterio teselliacijos failo formatas",
  "linktitle": "JT",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-j-ltt"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra JT failas?

**JT** (Jupiter Tessellation) yra efektyvus, į pramonę orientuotas ir lankstus ISO standartizuotas 3D duomenų formatas, sukurtas Siemens PLM Software. Aviacijos ir kosmoso, automobilių pramonės ir sunkiosios įrangos mechaninės CAD srityse JT naudojamas kaip pirmaujantis 3D vizualizacijos formatas.

JT formatas yra scenos grafikas, palaikantis specifinius CAD atributus ir mazgus. Fasetinių duomenų (trikampių) saugojimui naudojami sudėtingi suspaudimo būdai. Šis formatas sukurtas taip, kad palaikytų vaizdinius atributus, produkto ir gamybos informaciją (PMI) ir metaduomenis. Yra geras asinchroninio turinio srautinio perdavimo palaikymas. Sunkiosios mechanikos pramonėje profesionalai naudoja JT failą savo CAD sprendimuose ir produkto gyvavimo ciklo valdymo (PLM) programinės įrangos programose, norėdami ištirti sudėtingų prekių geometriją.

As JT supports nearly all important 3D CAD formats its assembly can deal with a variety of combination which is known as "multi-CAD". This multi-CAD assembly is always well managed and up-to-date because synchronization among native CAD product description files with their associated JT files takes place automatically. JT files are originally lightweight, so considered to be suitable for internet collaborations. Companies Collaborate through sending 3D visualizations over the media much more easily as compared to “heavy" original CAD files. In addition, JT files ensures many security feature that make intellectual property sharing more secure.

## Trumpa JT failo formato istorija

Engineering Animation, Inc. ir Hewlett Packard buvo pirmieji JT dizaineriai, kurie sukūrė šį formatą kaip tiesioginio modelio įrankių rinkinį. UGS Corp įsigijus EAI, JT tapo UGS rinkinio dalimi. 2007 m. pradžioje UGS paskelbė JT kaip pagrindinį 3D formatą. Tais pačiais metais Siemens AG įsigijo UGS ir pasirodė esanti Siemens PLM programinė įranga. Siemens naudoja JT kaip bendrą sąveikos formatą ir duomenų archyvo formatą. 2009 m. ISO priėmė JT specifikaciją skelbti kaip ISO viešai prieinamą specifikaciją (PAS). 2010 m. viduryje ProSTEP iViP paskelbė, kad pramoniniu lygiu JT ir STEP AP 242 XML galima naudoti kartu, kad būtų pasiektas didžiausias duomenų pranašumas. keistis scenarijais. 2012 metais JT oficialiai paskelbtas kaip ISO standartizuotas (ISO 14306:2012 (ISO JT V1)) 3D vizualizacijos formatas.

## JT failo formatas ##

Visi JT formato objektai yra vaizduojami naudojant objekto identifikatorių, o nuorodos tarp objektų tvarkomos per nurodyto objekto identifikatorių. Šių objektų nuorodų vientisumas gali būti palaikomas išjungiant / susukant rodykles.

JT failas yra išdėstytas kaip blokų serija, o antraštės blokas visada yra pirmasis duomenų blokas faile. Duomenų segmento serija ir TOC segmentas iškart po antraštės bloko. Vienas duomenų segmentas (6 LSG segmentas) turi su nuoroda suderinamą JT failą, visada egzistuoja. TOC segmente yra visų kitų to failo duomenų segmentų vietos informacija.

{{< figure src="../JT-1.png" alt="JT failo formatas" >}}

### Failo antraštė ###

Failo antraštė yra pirmasis JT failo duomenų hierarchijos blokas. Versijų informacija ir TOC vietos informacija yra įtraukta į antraštę, kuri palengvina įkroviklius skaitant failus. Failo antraštės turinys išdėstytas taip.

### TOC segmentas ###

TOC segmentas turi egzistuoti faile ir jame turi būti visų kitų duomenų segmentų identifikavimo ir vietos informacija. Faktinė TOC segmento vieta nurodoma failo antraštės lauke TOC poslinkis. Kiekvienas individualiai adresuojamas duomenų segmentas yra vaizduojamas TOC įrašu TOC segmente.

### Duomenų segmentas ###

JT failas apibrėžia visus saugomus duomenis duomenų segmente. Kai kurie duomenų segmentai gali suspausti visus segmente likusius informacijos baitus. Duomenų segmentų struktūra yra tokia:

![alt text](../JT-2.png "JT Data Segment")

Šioje lentelėje aprašomi skirtingi duomenų segmentų tipai:

|Vardas|Aprašymas
---|---|
|LSG segmentas|Apima objektų rinkinį, susietą per nukreiptas nuorodas, kad sudarytų LSG (nukreiptą aciklinę grafiko struktūrą)
|Shape LOD segmentas|yra geometrinių figūrų (pvz., viršūnių, normaliųjų, daugiakampių ir kt.) apibrėžiančių duomenų.
|JT B-Rep segmentas|Turinti elementą duomenims, kurie atspindi tikslią geometrinę atskiros dalies JT B-Rep formatu ribą.
|XT B-Rep segmentas|Duomenų elementas, skirtas tiksliai geometrinei atskiros dalies ribai pateikti ribų vaizdavimo formatu
|Wireframe segmentas|Duomenys atspindi tikslų 3D vielos rėmelį tam tikrai daliai, apibrėžiamą elementu, esančiu šiame segmente.
|Meta duomenų segmentas | Leidžia saugoti metaduomenis skirtinguose adresuojamuose segmentuose.
|JT ULP segmentas|Turinti elementą duomenims, kurie atspindi pusiau tikslią geometrinę atskiros dalies JT ULP formato ribą.
|JT LWPA segmentas|Yra elementas, apibrėžiantis tam tikros dalies analitinius duomenis. LWPA įtraukia analitinių paviršių rinkinį į dalies b-rep apibrėžimą.

## Suspaudimas ##

3D modelių perdavimo ir saugojimo reikalavimai yra griežtesni, todėl JT failai gali pasinaudoti glaudinimo pranašumais. JT duomenų modelis gali būti sudarytas iš skirtingų failų, naudojant skirtingą glaudinimo techniką, tačiau glaudinimo procesas yra skaidrus JT duomenų vartotojui.

Iki šiol JT Open Toolkit (kaip standartas) ir išplėstinis glaudinimas yra du JT failų naudojami glaudinimo būdai. JT Open Toolkit naudoja lengvą, be nuostolių glaudinimo algoritmą, o išplėstinis glaudinimas naudoja patobulintą, konkrečiai domenui būdingą glaudinimo techniką, todėl geometrijos glaudinimas yra nuostolingas. Klientų programos teikia pirmenybę išplėstiniam glaudinimui, o ne standartiniam glaudinimui, nes išplėstinis glaudinimas duoda gana aukštus glaudinimo koeficientus. Atgalinis suderinamumas su įprastomis JT failų peržiūros programomis palaikomas naudojant standartinį glaudinimą. Suspaudimo forma turi būti suderinama su JT failo formato versija, kurią galima pamatyti, kai JT failas atidaromas naudojant teksto rengyklę ir įtrauktas į ASCII antraštės informaciją.

## Nuorodos Nr.

* [JT failo formato nuoroda](https://www.plm.automation.siemens.com/en_us/Images/JT-v10-file-format-reference-rev-B_tcm1023-233786.pdf)

* [JT (vizualizacijos formatas)](https://en.wikipedia.org/wiki/JT_(visualization_format)#Data_model)


