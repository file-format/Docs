{
  "date": "2019-10-11",
  "keywords": [
"asmx",
"asmx failą",
"asmx failo formatas",
"asmx failo tipas",
"failą",
"tipo",
"kas yra asmx failas"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ASMX – ASP.NET žiniatinklio tarnybos failas",
  "description": "Sužinokite, kas yra ASMX failas ir API, kurios gali kurti ir atidaryti ASMX failus.",
  "linktitle": "ASMX",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-asm-ltx"
}
},
  "lastmod": "2021-06-10"
}

## Kas yra ASMX failas?

Failas su .asmx plėtiniais yra ASP.NET Web Service failas, užtikrinantis ryšį tarp dviejų objektų internetu naudojant paprastą objektų prieigos protokolą (SOAP). Jis įdiegtas kaip paslauga Windows žiniatinklio serveryje, skirta apdoroti gaunamą užklausą ir grąžinti atsakymą. Skirtingai nuo [ASPX](/web/aspx/) failų, kuriuose yra ASP.NET tinklalapių vizualaus atvaizdavimo kodas, ASMX failai veikia serveryje fone ir atlieka įvairias užduotis, pvz., prisijungia prie duomenų bazės, gauna duomenis ir grąžina juos tokiu formatu, kuriuo buvo pateiktas prašymas. Jie naudojami specialiai XML žiniatinklio paslaugoms.

## ASMX failo formatas

ASMX failai yra paprasto teksto formatu ir gali būti atidaryti arba redaguoti tokiose programose kaip Microsoft Visual Studio arba teksto rengyklės. Tai yra patentuotas Microsoft failo formatas ir turi tiksliai apibrėžtą žiniatinklio paslaugų kūrimo sintaksę. ASMX failo atsakymas SOAP XML forma turi šiuos elementus.

 * Envelop – šakninis elementas, identifikuojantis XML dokumentą kaip SOAP pranešimą.
 * Antraštė – pasirenkamas elementas, kuriame yra konkrečios programos informacijos, pvz., autentifikavimo duomenų. Jei yra antraštės elementas, jis turi būti pirmasis antraštinis elemento Envelope elementas.
 * Turinys – yra SOAP pranešimas, skirtas gavėjui.
 * Gedimas – pasirenkamas elementas, naudojamas klaidų pranešimams nurodyti. Jei yra gedimo elementas, jis turi būti antrinis elemento Body elementas.

ASMX failus galima parašyti .NET kalbomis, tokiomis kaip [C#](/programming/cs/), [Visual Basic](/programming/vb/) arba JScript.

## Kuo ASMX skiriasi nuo ASPX ir ASCX?

ASMX failai skiriasi nuo ASPX ir ASCX failų.

 * ASPX, Active Server Pages, failai yra programavimo failai, generuojami naudojant Microsoft ASP.NET sistemą, veikiančią žiniatinklio serveriuose. Jie pateikiami kliento žiniatinklio naršyklėje, kai vartotojas prašo pasiekti tokį puslapį.
 * ASCX, Active Server User Control, apibrėžia vartotojo valdiklius, kurie naudojami pakartotinai naudojamiems valdikliams apibrėžti ASP.NET tinklalapiuose arba visoje svetainėje.

## Nuorodos

 * [Naudojantis ASMX paslaugą](https://learn.microsoft.com/en-us/xamarin/xamarin-forms/data-cloud/web-services/asmx)
 * [ASCX naudotojo valdymas](https://beansoftware.com/ASP.NET-Tutorials/User-Control.aspx)

