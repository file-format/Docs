{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "TNEF",
  "description": "Sužinokite apie TNEF failo formatą ir API, kurios gali kurti ir atidaryti TNEF failus.",
  "linktitle": "TNEF",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-tne-ltf"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra TNEF failas?

Neutralus transportavimo įterpimo formatas (TNEF) yra Microsoft patentuotas el. laiškų priedams, pagrįstas pranešimų siuntimo programų programavimo sąsaja (**MAPI**), įterpti. Microsoft Outlook ir Microsoft Exchange Server visiškai palaiko TNEF, o vėliau iššifruoja TNEF į MAPI ir rodo suformatuotus laiškus. El. pašto priedas su TNEF koduote turi MIME tipą MS-TNEF ir saugomas kaip winmail/win.dat. Winmail .dat priede yra ši informacija:


|Pranešimas|OLE objektai|Outlook funkcijos
---|---|---|
|<ul><li> Originalių pranešimų priedai</li><li> Originali formatuota versija</li><li> šriftus, teksto dydžius ir teksto spalvas</li></ul> |<ul><li> įterptos nuotraukos</li><li> įterptieji Office dokumentai</li></ul> |<ul><li> pasirinktines formas</li><li> balsavimo mygtukai</li><li> susitikimo prašymai</li></ul>


Kitos el. pašto paslaugos, kurios nepalaiko TNEF, pateikia paprastą TNEF formato pranešimų tekstą. Outlook įterpia turtingą pranešimo formatą į TNEF failus (OLE) arba tam tikras Outlook funkcijas (formas, apklausos mygtukus ir konferencijų užklausas). Sankcionuoti aiškų TNEF kodavimą Outlook el. pašto kliento programoje neįmanoma, tačiau RTF formato pasirinkimas el. pašto siuntimui netiesiogiai palengvina TNEF kodavimą.

## TNEF failo formatas

TNEF duomenų algoritmas sukuria išlygintą struktūrą iš turtingų hierarchinių pranešimų savybių. Šios išlygintos struktūros tada naudojamos nuosekliam duomenų srautui, sudarytam iš konkrečių savybių, atstovauti.

Kai kuriose situacijose, kai ypatybės pateikiamos grupėse arba turi kelias reikšmes, sraute gali būti skaičiai ir užpildymai, kad būtų užtikrintas konkretus duomenų lygiavimas. Išskirtinė situacija, kai šio algoritmo naudojimas yra naudingas, yra nepalaikomoje pranešimų aplinkoje. Tokiose aplinkose turtingą pranešimo ypatybę į nuoseklųjį duomenų srautą užkoduoja TNEF Writer. Be to, ypatybės, kurios nepriklauso pagrindiniam TNEF, gali būti įdėtos perduodant. Tada šios įdėtos ypatybės tampa prieinamos dekoduojant per TNEF, kad būtų užtikrintas visų pradinio pranešimo ypatybių prieinamumas kliento programai.

TNEF visi skaitmeninių duomenų tipai yra mažo dydžio ir jų dydis yra didesnis nei vienas baitas. Norint apdoroti šias skaitines reikšmes ne mažose platformose, reikia atlikti atitinkamas transformacijas, kad būtų gautos teisingos vertės. Eilučių reikšmės pateikiamos papildytosios Backus-Naur formos (ABNF) formatu pagal [RFC5234] specifikacijas. Kai eilutė baigiasi null simboliu, ji taip pat įtraukiama; pvz., darbininkas@pavyzdys.com %x00.

{{< figure src="../TNEF.png" alt="TNEF failo formatas" >}}

## TNEF atributai ir apdorojimo taisyklės ##

Duomenų srautas TNEF prasideda senos versijos numeriu, parašu, primityviąja rakto reikšme ir atributu, vaizduojančiu kodo puslapį. Šis kodo puslapis sugeneruojamas, kai koduotuvas įrašo ANSI atributus ir ypatybes. Po to srautas tapo atributų serija, kurioje pirmiausia buvo išdėstyti pranešimo atributai, o po to - priedo atributai. Skirtingos pranešimų ir priedų charakteristikos yra specialiuose atributuose, pvz., attMsgProps, attAttachment ir attRecipTable. Atributuose, kurie rodomi TNEF sraute, yra struktūra, pranešimo ypatybės ir konversijos, būtinos, kad juos sudomintų pranešimų ypatybės. Kiekvieną atributą sudaro ID, atributo dydis ir duomenys, kontrolinė suma ir lygis pagal jo taikymą.

## Ryšys su protokolais ir kitais algoritmais ##

Sistemoms, kurios turi prastą mechanizmą, kad būtų rodomas turtingas pranešimų formatas, reikalingas TNEF duomenų perdavimo algoritmas. Naudojant medijos tipą ms-TNEF, algoritmo išvestį sudaro priedo failas (winmail.dat) ir MIME dalis, nurodyta [RFC2045]. Paprasto teksto pranešimo turinys perduodamas naudojant UUENCODE pagal [MSDN-UAF] specifikaciją ir šis pranešimo tekstas arba lygiavertis metodas iššifruojamas gavėjo gale. Be to, TNEF gali perduoti pranešimų duomenis naudodamas įvairius interneto protokolus, tokius kaip SMTP, POP3, IMAP4 ir tuos, kurie integruoja MIME pagal RFC2045 standartą.

## Taikomumo pareiškimas Nr.

Be paprasto pranešimų perdavimo, pradinė TNEF programa turėjo būti sukurta siekiant naudoti pranešimų klases ir palaikyti papildomas funkcijas, kurios neturi originalaus perdavimo protokolo palaikymo. Ši programa buvo dar patobulinta, kad būtų galima perduoti turtingas pranešimų ypatybes ir pavadintas ypatybes, kurias šiuo metu naudoja šiuolaikiniai pranešimų klientai. Kad būtų laikomasi pradinio diegimo, išlaikoma originali atributo sintaksė, o specialus atributas išlaiko naujas pranešimo savybes atskirai.

## Nuorodos

* [Transport Neutral Encapsulation Format](https://en.wikipedia.org/wiki/Transport_Neutral_Encapsulation_Format)

* [El. pašto adresai ir adresų knygos „Exchange Server“](https://learn.microsoft.com/en-us/exchange/email-addresses-and-address-books/email-addresses-and-address-books?view# exchserver-2019)

* [[MS-OXTNEF]: Transporto neutralaus inkapsuliavimo formato (TNEF) duomenų algoritmas](https://msdn.microsoft.com/en-us/library/cc425498(v#exchg.80).aspx)


