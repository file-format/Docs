{
  "date": "2019-10-11",
  "keywords": [
"dcm failą",
"dcm failo formatas",
"kas yra dcm failas",
"failą",
"dcm pavyzdys",
"dcm failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DCM failo formatas – skaitmeninės medicininės informacijos failas",
  "description": "Sužinokite apie DCM failo formatą ir API, kurios gali kurti ir atidaryti DCM failus.",
  "linktitle": "DCM",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-dc-ltm"
}
},
  "lastmod": "2021-07-03"
}

## Kas yra DCM failas?

Failai su plėtiniu .dcm yra skaitmeninis vaizdas, kuriame saugoma pacientų medicininė informacija, pvz., MRT, kompiuterinės tomografijos ir ultragarso vaizdai. DCM failuose naudojamas [DICOM](/image/dicom/) (Skaitmeninis vaizdas ir ryšiai medicinoje) vaizdo failo formatas ir juose gali būti pateikta paciento informacija. Jį sukūrė [National Electrical Manufacturers Association](https://en.wikipedia.org/wiki/National_Electrical_Manufacturers_Association) (NEMA) ir jis buvo skirtas standartizuoti vaizdo failų formatą, skirtą medicininių vaizdų platinimui ir peržiūrai.

## DCM failo formatas

DCM failai saugo informaciją DICOM vaizdo formatu. Šiuose failuose saugomas duomenų rinkinys, kuris yra realaus pasaulio informacija, atitinkantis SOP egzempliorių, susijusį su DICOM IOD. DICOM failo metainformacija saugoma faile, po kurio seka tikrojo duomenų rinkinio baitų srautas.

### DICOM failo metainformacija ##

Kiekviename DICOM faile yra inkapsuliuoto duomenų rinkinio identifikavimo informacijos antraštė, kurią sudaro:
   * 128 baitų failo preambulė
   * 4 baitų DICOM priešdėlis
   * Failo meta elementai

Ši antraštė yra būtina kiekvienam DICOM failui.

### Failo meta elementai ###
|Atributo pavadinimas|Žyma|Tipas| Atributo aprašymas
---|---|---|---|
|Failo preambulė|Nėra žymos ar ilgio laukų|1|Pasiekiamas fiksuotas 128 baitų laukas programos profiliui arba nurodytam diegimo naudojimui. Jei nenaudojamas programos profilis arba konkretus diegimas, visi baitai turi būti nustatyti į 00H. Failų rinkinio skaitytuvai ar naujintojai negali pasikliauti šios preambulės turiniu, kad nustatytų, ar šis failas yra ar nėra DICOM failas.
|DICOM prefiksas|Nėra žymos arba ilgio laukų|1|Keturi baitai, kuriuose yra simbolių eilutė DICM. Šis priešdėlis skirtas naudoti norint atpažinti, ar šis failas yra ar ne DICOM failas.
|Failo metainformacijos grupės ilgis|(0002,0000)|1|Baitų skaičius po šio failo metaelemento (reikšmės lauko pabaiga) iki paskutinio 2 grupės failo metainformacijos elemento imtinai.
|File Meta Information Version|(0002,0001)|1|This is a two byte field where each bit identifies a version of this File Meta Information header. In version 1 the first byte value is 00H and the second value byte value is 01H.Implementations reading Files with Meta Information where this attribute has bit 0 (lsb) of the second byte set to 1 may interpret the File Meta Information as specified in this version of PS3.10. Visi kiti bitai neturi būti tikrinami.
|Media Storage SOP Class UID|(0002,0002)|1|Unikaliai identifikuoja su duomenų rinkiniu susietą SOP klasę. SOP klasės UID, leidžiami laikmenos saugojimui, nurodyti PS3.4 – medijos saugojimo programų profiliuose.
|Media Storage SOP egzempliorius UID|(0002,0003)|1|Unikaliai identifikuoja SOP egzempliorių, susietą su duomenų rinkiniu, įdėtu į failą ir po failo metainformacijos.
|Perdavimo sintaksė UID|(0002,0010)|1|Unikaliai identifikuoja perdavimo sintaksę, naudojamą šiam duomenų rinkiniui koduoti. Ši perkėlimo sintaksė netaikoma failo metainformacijai.
|Įgyvendinimo klasė UID|(0002,0012)|1|Unikaliai identifikuoja diegimą, kuris parašė šį failą, ir jo turinį. Iškilus keitimosi problemoms, ji suteikia nedviprasmišką diegimo, kuris paskutinį kartą parašė failą, tipą.
|Įdiegimo versijos pavadinimas|(0002,0013)|3|Nurodo diegimo klasės UID (0002,0012) versiją naudojant iki 16 repertuaro simbolių.
|Šaltinio taikomosios programos objekto pavadinimas|(0002,0016)|3|DICOM taikomosios programos objekto (AE) pavadinimas AE, kuris parašė šio failo turinį (arba paskutinį kartą jį atnaujino). Jei naudojamas, jis leidžia atsekti klaidų šaltinį iškilus medijų mainų problemoms.
|Privačios informacijos kūrėjo UID|(0002,0100)|3|Privačios informacijos kūrėjo UID (0002,0102).
|Privati informacija|(0002,0102)|1C|Yra privati informacija, patalpinta failo metainformacijoje. Kūrėjas nurodomas (0002,0100). Reikalingas, jei yra privačios informacijos kūrėjo UID (0002,0100).

### Duomenų rinkinio inkapsuliacija ###

DICOM faile yra vienas duomenų rinkinys, kuris atspindi vieną SOP egzempliorių, susijusį su viena SOP klase. DICOM failo metainformacijos perdavimo sintaksės UID turi apibrėžti perdavimo sintaksę, naudojamą duomenų rinkiniui koduoti.

### Failų valdymo informacijos palaikymas ###

Medijos formato sluoksnis pateikia šią failų valdymo informaciją, jei reikia tam tikram DICOM programos profiliui.

  * Failo turinio savininko identifikavimas

  * Prieigos prie failų statistika (pvz., sukūrimo data ir laikas)

  * Programos failų prieigos valdymas

  * Fizinės medijos prieigos kontrolė (pvz., apsauga nuo rašymo)

## Nuorodos Nr.
  * [DICOM standartas](https://www.dicomstandard.org/current/)
  * [DICOM failo formatas](https://dicom.nema.org/dicom/2013/output/chtml/part10/chapter_7.html)

