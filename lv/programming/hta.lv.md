{
  "date": "2021-09-16",
  "keywords": [
"hta",
"failu",
"pagarinājumu",
"faila formātā",
"hta ieviešana",
"Programmēšanas rokasgrāmata",
"hta piemērs",
"HTML lietojumprogramma",
"Hiperteksta iezīmēšanas valodas lietojumprogramma",
"HTA faili",
"Microsoft HTML lietojumprogramma"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "HTA — HTML lietojumprogrammu faili",
  "description": "Uzziniet par HTA faila formātu un API, kas var izveidot un atvērt HTA failus.",
  "linktitle": "HTA",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-ht-lva"
}
},
  "lastmod": "2021-09-16"
}

## Kas ir HTA fails?

HTMLA apzīmē **Hypertext Markup Language Application** ir programma, kas ir saderīga ar Microsoft Windows. Šīs programmas pirmkods ietver vairāk nekā vienu skriptu valodu, piemēram, [HTML](/web/html/) un [JavaScript](/web/js/). Lietotāja interfeisam priekšroka tiek dota HTML lietojumprogrammai, savukārt, lai izpildītu programmas loģikas prasības, tiek izmantota jebkura cita skriptu valoda.

HTML lietojumprogramma ir neatkarīga no interneta pārlūkprogrammas drošības modeļa un darbojas kā pilnībā uzticama lietojumprogramma. Šo lietojumprogrammu failiem izmantotais paplašinājums ir HTA. Šīs lietojumprogrammas ietver HTML funkcijas, kā arī citu skriptu valodu īpašības.


## Īsa vēsture ##

The HTA was first introduced in 1999 by Microsoft along with the release of Internet Explorer 5. Tas bija saderīgs ar Internet Explorer, un tāpēc to varēja izpildīt tikai operētājsistēmā Windows. Šī tehnoloģija tika patentēta 2003. gadā. HTA faili tiek izpildīti tāpat kā citi .exe faili. HTA faili ir saderīgi arī ar mūsdienu atjaunināto Windows 11 versiju.


## Tehniskā specifikācija Nr.

HTA ir tāds pats formāts kā jebkurai citai HTML lapai, bet daži atribūti tiek izmantoti, lai kontrolētu programmu apmaļu vai ikonu stilus. Turklāt tiek sniegti argumenti HTA uzsākšanai. Šīs lietojumprogrammas var izpildīt, izmantojot programmu mshta.exe. Tam var piekļūt, vienkārši veicot dubultklikšķi uz faila. Šīs programmas automātiski darbojas kopā ar Internet Explorer. Papildus citām specifikācijām tās nav neatkarīgas no Trident dzinēja pārlūkprogrammas, bet ir neatkarīgas no Internet Explorer. Tas nozīmē, ka tos var izpildīt, neizmantojot Internet Explorer.

Atzīmes tiek izmantotas, lai pielāgotu šo lietojumprogrammu izskatu. Pārvēršana no Microsoft HTML lietojumprogrammas uz HTA formātu ir vienkāršāka, ti, jums ir jāmaina tikai paplašinājums. Kā mēs zinām, ka šīs lietojumprogrammas ir pilnībā uzticamas, tāpēc tām ir vairāk funkciju un priekšrocību salīdzinājumā ar vienkāršiem HTML failiem. Lai izveidotu HTA, var izmantot teksta redaktorus. Šos redaktorus var iegādāties Microsoft vai jebkurš cits uzticams avots.


## HTA faila formāta piemērs ##

```
<HTML>
<HEAD>
<HTA:APPLICATION ID="HelloExample" 
   BORDER="bold" 
   BORDERSTYLE="complex"/>
<TITLE>HTA - Hello World</TITLE>
</HEAD>
<BODY>
<H2>HTA - Hello World</H2>
</BODY>
</HTML>

```

## Atsauce Nr.

* [HTA — Wikipedia](https://en.wikipedia.org/wiki/HTML_Application)




