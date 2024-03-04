{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MSG – „Microsoft Outlook“ el. pašto formatas",
  "description": "Sužinokite apie MSG failo formatą ir API, kurios gali kurti ir atidaryti MSG failus.",
  "linktitle": "MSG",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-ms-ltg"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra MSG failas?

MSG is a file format used by [Microsoft Outlook](https://products.office.com/en-us/outlook/email-and-calendar-software-microsoft-outlook?rtc#1) and Exchange to store email messages, contact, appointment, or other tasks. Such messages may contain one or more email fields, with the sender, recipient, subject, date, and message body, or contact information, appointment particulars, and one or more task specifications. The properties that constitute the Message object, including are also a part of the MSG file.  MSG file has headers, main message body, and hyperlinks as plain ASCII text. MSG files are also suitable with the programs that need Microsoft's Messaging Applications Programming Interface (MAPI).

## MSG failo struktūra

CFB_3 formatas yra MSG failo pagrindas. Paradigma pagrįsta saugyklų ir srautų koncepcijomis, gana artimomis katalogams ir failams. Todėl pagrindinis skirtumas tarp pirmųjų yra visa hierarchija, supakuota į atskirą failą, vadinamą sudėtiniu failu. Objektai sudaro pranešimų failus ir susideda iš vienos nuosavybės arba jos rinkinių. Ši galimybė palengvina programoms sudėtingus, struktūrizuotus duomenis saugoti viename faile. Šis formatas taip pat nurodo kelias saugyklas, kiekviena saugykla žymi pranešimo objektą kaip pagrindinį komponentą. Šiose saugyklose yra daug srautų, atspindinčių to komponento savybę. Taip pat galima įdėti saugyklą.

## Mapi ypatybės

Viršutiniame .msg failo lygyje saugyklose yra srautai, kuriuose saugomos ypatybės. Savybės gali būti suskirstytos į šias kategorijas:

* Fiksuoto ilgio savybės

* Kintamo ilgio savybės

* Daugiavertės savybės


Nepriklausomai nuo kategorijos, nuosavybė yra pažymėta arba pavadinta. Tačiau įvardintoms ypatybėms reikalinga tinkama atvaizdavimo informacija, kaip nurodyta jų atvaizdavimo saugykloje.

## Saugyklos

Saugyklos yra pagrindiniai pranešimo objekto komponentai. MSG failo formatas nurodo šias saugyklas:

## Aukščiausio lygio struktūra

Pranešimo objektas yra visas aukščiausias MSG failo formato lygis. Priklausomai nuo tipo, savybių, gavėjų ir priedo objektų skaičiaus, pranešimo objektas gali turėti skirtingas srauto saugyklas atitinkamame .MSG faile.

### Ryšys su kitomis struktūromis

Msg failo formatas turi šiuos ryšius su kitomis struktūromis:

* .msg pagrindas yra sudėtinio failo dvejetainio failo formatas.

* Šiame formate naudojamos ypatybės, kurias naudoja pranešimų ir priedų objektų protokolas.


## Scenarijai, kaip išvengti MSG formatų

Pranešimo objektas gali būti bendrinamas tarp klientų arba pranešimų saugyklų, kurios naudoja .msg failų sistemą. Yra keletas aplinkybių, kai žinutės objekto saugojimas .msg failo formatu būtų netinkamas. Pavyzdžiui:

* Jei palaikomas didelis atskiras archyvas, geriau naudoti visas funkcijas turintį formatą, kuriame rodiniai gali būti pateikiami tiksliau.

* Jei imtuvas nežinomas, gali būti, kad imtuvas nepalaiko formato ir gali būti pristatytas privatus arba nesvarbus.


## MSG failo pavyzdys

To get an idea of how a MSG file looks like, you can download a [sample MSG file](https://products.conholdate.app/viewer/view/mL7cmq6qYbcNG329P/sample-msg-file.msg) and open on your computer to view its contents.

## Nuorodos

* [[MS-OXMSG]: Outlook MSG failo formatas](https://msdn.microsoft.com/en-us/library/cc463912(v#exchg.80).aspx)


