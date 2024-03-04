{
  "date": "2020-03-16",
  "keywords": [
"DWG",
"Dokumento formatas",
"CAD",
"Atviras",
"Sukurti"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie DWG failo formatą ir API, kurios gali kurti ir atidaryti DWG failus.",
  "title": "DWG failo formatas",
  "linktitle": "DWG",
  "menu": {
    "docs": {
      "parent": "cad",
      "identifier": "cad-dw-ltg"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra DWG failas?

Failai su DWG plėtiniu yra patentuoti dvejetainiai failai, naudojami 2D ir 3D projektavimo duomenims laikyti. Kaip ir DXF, kurie yra ASCII failai, DWG yra dvejetainis failo formatas CAD (kompiuterinio projektavimo) brėžiniams. Jame yra vektorinis vaizdas ir metaduomenys, skirti CAD failų turiniui atvaizduoti. Yra nemokamų peržiūros priemonių, skirtų DWG failams peržiūrėti Windows operacinėje sistemoje, pvz., nemokama Autodesk DWG TrueView. Taip pat yra ir kitų trečiųjų šalių programų, kurios palaiko DWG failų pasiekimą. DWG failuose yra vartotojo sukurta informacija ir apima:

* Dizainai

* Geometriniai duomenys

* Žemėlapiai ir nuotraukos


Šį formatą plačiai naudoja architektai, inžinieriai ir dizaineriai įvairiems projektavimo tikslams.

## Trumpa istorija ##

DWG file format has evolved with the time since its formal introduction in 1982. Toliau pateikiama trumpa praeities įvykių apžvalga iš istorijos perspektyvos.

**1982 m.:** Autodesk licencijavo DWG failo formatą , kurį 1970 m. sukūrė Mike'as Riddle'as, kaip AutoCAD pagrindą.

**1998 m.:** Išleisdama AutoCAD R14.01, Autodesk pridėjo failų patikrinimą naudodama DWGCHECK funkciją, kuri į programos sukurtus DWG failus įdėjo užšifruotą kontrolinę sumą ir produkto kodą, Autodesk vadinamą WaterMark.

**2006 m.:** Autodesk modifikavo AutoCAD 2007, įtraukdama TrustedDWG technologiją, kad į DWG failus būtų įtraukta teksto eilutė Autodesk DWG. Šis failas yra patikimas DWG, kurį paskutinį kartą išsaugojo Autodesk programa arba Autodesk licencijuota programa. To tikslas buvo padėti Autodesk programinės įrangos vartotojams užtikrinti, kad šie failai būtų sukurti naudojant Autodesk arba RealDWG programą, o tai tikrai turėtų padėti sumažinti nesuderinamumo riziką.

## Failo struktūra ##

DWG buvo vienas iš plačiai naudojamų failų formatų įvairiose programose ir turi tvirtą failų struktūrą. Kadangi DWG yra dvejetainis failo formatas, jis nėra skaitomas žmonėms, kaip paprastas ASCII [DXF](/cad/dxf/) failo formatas. DWG failuose paprastai yra informacijos apie vaizdo koordinates ir visus su jais susijusius metaduomenis. OpenDesign gali atsisiųsti visą DWG failo formato [specifications](https://www.opendesign.com/files/guestdownloads/OpenDesign_Specification_for_.dwg_files.pdf). DWG failo formato failų struktūra apibendrinta taip.

**Antraštė**: failo antraštę sudaro DWG antraštės kintamieji ir informacija apie ciklinį atleidimo patikrinimą (CRC), kuris naudojamas klaidai aptikti. Kiekvienas poskyris yra specializuotas vektorius, kuriame skirtingo ilgio bitai naudojami skirtingoms etiketėms pavaizduoti. Pavyzdžiui, pirmieji 6 DWG antraštės kintamojo bitai reiškia versijos eilutę.

**Klasių apibrėžimai:** DWG faile gali būti daug klasių, atsižvelgiant į konkretų .dwg failo tikslą. Informacija, pvz., klasės metaduomenų klasės duomenų srities dydis, klasės numeris ir kontrolinė suma, be kitos.

**Šablonas**: tai neprivaloma, o R15 ir R15 versijoms ši skiltis yra po skyriumi Objekto laisva vieta.

**Padėklas**: metaduomenys pridedami prie galo ir uždedami tam tikru baitų skaičiumi, todėl senesnės AutoCAD programinės įrangos versijos yra suderinamos su naujuoju DWG failo formatu.

**Vaizdo duomenys**: šios skilties metaduomenys priklauso nuo konkretaus .dwg tipo. R14 ir R15 naudotojams šis skyrius yra neprivalomas.

**Objekto duomenys**: objekto duomenis sudaro visas lentelės objektų sąrašas, žodyno įrašai ir tt, atitinkantys esamą objektų sąrašą.

**Objektų žemėlapis**: kiekvieno objekto vieta faile nurodyta šioje failo dalyje. Dauguma šio skyriaus metaduomenų yra failų rankenėlės, kurios atlieka objekto identifikavimo ir atvaizdavimo vaidmenį.

**Laisva objekto vieta**: ši skiltis yra neprivaloma visiems vartotojams

**Antra antraštė**: failo antraštės dalies dublikatas DWG failo pabaigoje

## Nuorodos Nr.

* [DWG failo formato specifikacijos](https://www.opendesign.com/files/guestdownloads/OpenDesign_Specification_for_.dwg_files.pdf)

* [DWG failo specifikacija](https://www.scan2cad.com/blog/dwg/file-spec/)

* [DWG – Vikipedija](https://en.wikipedia.org/wiki/.dwg)


