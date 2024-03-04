{
  "date": "2021-02-15",
  "keywords": [
"asf failą",
"asf failo formatas",
"kas yra asf failas",
"failą",
"asf pavyzdys",
"asf failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ASF – pažangių sistemų failo formatas",
  "description": "Sužinokite apie ASF failo formatą ir API, kurios gali kurti ir atidaryti ASF failus.",
  "linktitle": "ASF",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-as-ltf"
}
},
  "lastmod": "2021-02-16"
}

## Kas yra ASF failas?

Failas su plėtiniu .asf yra daugialypės terpės failo formatas, skirtas skaitmeninės medijos srautams saugoti ir leisti tinkle. Tai konteinerio failo formatas, kuriame gali būti ir vaizdo, ir garso turinio, skirto srautiniam perdavimui internetu. Retai rasite ASF failų ir greičiausiai susidursite su Windows Media Audio ([WMA](/audio/wma/)) ir Windows Media Video ([WMV](/video/wmv/)) failais, kurie abu nurodo ASF failus, kurių turinys užkoduotas atitinkamais kodekais. Windows medijos failus galima kurti ir skaityti naudojant Windows Media Format SDK.

## ASF failo formatas

ASF failą gali sudaryti keli nepriklausomi arba priklausomi srautai. Tai gali apimti kelis garso srautus, skirtus kelių kanalų garsui, arba kelis vaizdo įrašų srautus. Dėl kelių duomenų perdavimo spartų srautai yra tinkami perduoti skirtingu pralaidumu. Be to, ASF failo srautai gali būti suspausto arba nesuspausto formato. Geriausias suspaudimas pasiekiamas naudojant Microsoft Windows Media Audio and Video 9 serijos kodekus. Išsamias ASF failo formato specifikacijas rasite [Microsoft Website](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc).

### ASF aukščiausio lygio failų struktūra

ASF failuose logiškai yra trijų tipų aukščiausio lygio objektai:

* „Antraštės objektas“ – privalomas ir turi būti dedamas kiekvieno ASF failo pradžioje

* „Duomenų objektas“ – privalomas ir turi sekti antraštės objektą

* „Indekso objektas (-ai)“ – neprivaloma, bet naudinga teikiant laiku pagrįstą atsitiktinę prieigą prie ASF failų


Toliau pateiktame paveikslėlyje parodyta aukščiausio lygio ASF failų struktūra.

![ASF File Structure](../asf.png "ASF File Structure")

#### ASF aukščiausio lygio antraštės objektas

Antraštės objektas pateikia gerai žinomą baitų seką ASF failų pradžioje ir pasirinktinai gali turėti metaduomenis, pvz., bibliografinę informaciją. Jame yra visa informacija, kurios reikia norint tinkamai interpretuoti informaciją duomenų objekte. Antraštės objektas gali apimti kelis standartinius objektus, įskaitant, bet tuo neapsiribojant:

 * Failo ypatybių objektas – yra visuotinių failo atributų.
 * Srauto ypatybių objektas – apibrėžia skaitmeninės medijos srautą ir jo charakteristikas.
 * Antraštės plėtinio objektas – leidžia pridėti papildomų funkcijų prie ASF failo, išlaikant atgalinį suderinamumą.
 * Turinys Aprašymas Objektas – yra bibliografinės informacijos.
 * Scenarijaus komandos objektas – yra komandos, kurias galima vykdyti atkūrimo laiko juostoje.
 * Žymeklio objektas – faile pateikia pavadintus perėjimo taškus.

Antraštės objektas vaizduojamas naudojant šią struktūrą:

|Lauko pavadinimas |Lauko tipas |Dydis (bitai)|
---|---|---|
|Objekto ID| GUID| 128|
|Objekto dydis| QWORD| 64|
|Antraštės objektų skaičius| DWORD| 32|
|Rezervuota1| BYTE| 8|
|Rezervuota2| BYTE| 8|

#### ASF aukščiausio lygio duomenų objektas

Visi ASF failo skaitmeninės laikmenos duomenys yra duomenų objekte ir saugomi ASF duomenų paketų pavidalu. Kiekvienas duomenų paketas yra fiksuoto ilgio ir jame yra vieno ar kelių skaitmeninės medijos srautų duomenys.

#### ASF aukščiausio lygio indekso objektai

ASF aukščiausio lygio indekso objektai yra dviejų tipų:

 * Simple Index Object – yra laiko pagrindu ASF failo vaizdo duomenų indeksas. Laiko intervalas tarp indekso įrašų yra pastovus ir saugomas paprastojo indekso objekte.
 * Indekso objektas – nurodo indekso objektą, medijos objekto indekso objektą ir laiko kodo indekso objektą, kurių formatai yra panašūs. Kaip ir paprastas indekso objektas, indekso objektas indeksuojamas pagal laiką su fiksuotu laiko intervalu, bet neapsiriboja vaizdo srautais.

## Nuorodos

* [ASF failo formatas – „Microsoft“](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc)

* [QuickTime failo formatas – Vikipedija](https://en.wikipedia.org/wiki/QuickTime_File_Format)


