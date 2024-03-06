{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PDF/UA faila formāts",
  "description": "Uzziniet par PDF/UA failu formātu un API, kas var izveidot un atvērt PDF/UA failus.",
  "linktitle": "PDF/UA",
  "menu": {
    "docs": {
      "parent": "pdf",
      "identifier": "pdf-u-lva"
}
},
  "lastmod": "2019-09-10"
}

# Kas ir PDF/UA fails? #

PDF/UA tika publicēts kā [ISO Standard 14289-1](https://en.wikipedia.org/wiki/ISO_14289) 2012. gada augustā, un tā ir pirmā pilnīgā prasību kopas definīcija vispārēji pieejamiem PDF dokumentiem. Termins universāli pieejams attiecas uz izpratni, ka [PDF](/pdf/) dokumentā ietvertajai informācijai jābūt vienlīdz un neatkarīgi pieejamai ikvienam un jo īpaši cilvēkiem ar invaliditāti. PDF/UA standarta ieviešanu var uzskatīt par nozīmīgu soli rīku un lietojumprogrammu izveidē, lai izveidotu un lasītu PDF saturu.

## Prasības faila formātam ##

PDF/UA pamatā ir noteiktas prasības, kas darbojas kā šī standarta būtība. Būtībā tie ir balstīti uz PDF failu marķēšanu, kas nozīmē, ka visiem PDF/UA dokumentiem ir jābūt pareizi marķētiem. Tas arī prasa, lai tagi būtu semantiski atbilstoši un loģiskā secībā. Tas nodrošina, ka gala dokuments, kas izveidots ar PDF/UA specifikācijām, ir uzticamāks un pieejamāks. Tas var likt PDF autoriem apšaubīt, vai viņiem ir jāzina viss par visām šādām prasībām? Par laimi, tas tā nav, jo PDF/UA atbilstības rīki uzņemas atbildību par PDF faila pievienošanu un pieejamības saglabāšanu.

Faila formāta prasības PDF/UA ir šādas.

* Saturs tiek klasificēts vienā no diviem veidiem: jēgpilns saturs un artefakti, piemēram, dekoratīvie lapas elementi. Visam nozīmīgajam saturam jābūt atzīmētam un integrētam visu dokumenta tagu struktūras kokā. Savukārt artefakti ir tikai jāmarķē kā tādi.

* Nozīmīgs saturs ir jāatzīmē ar tagiem un kopā ar pārējiem tagiem dokumentā jāizveido pilnīgs struktūras koks.

* Nozīmīgs saturs ir jāatzīmē ar atbilstošiem semantiskajiem tagiem.

* Dokumenta tagu izveidotajam struktūras kokam jāatspoguļo dokumenta loģiskā lasīšanas secība.

* Drīkst izmantot tikai standarta tagus, kas definēti PDF 1.7; ja tiek izmantoti citi tagi, lomu piešķiršanas ierakstā ir jāreģistrē, kuru standarta tagu katrs pārstāv.

* Informāciju nedrīkst nodot, izmantojot tikai vizuālus līdzekļus (piemēram, kontrastu, krāsu vai pozīciju lapā).

* Nav atļauts mirgojošs, mirgojošs vai mirgojošs saturs ne kā JavaScript kontrolēti efekti, ne kā daļa no jebkādiem PDF failā iegultiem videoklipiem.

* Jānorāda dokumenta nosaukums un dokumentam jābūt iestatītam tā, lai loga nosaukumā būtu redzams nosaukums (nevis faila nosaukums).

* Ir jāatzīmē visa satura valoda, un valodas izmaiņas ir skaidri jāatzīmē kā tādas.


## PDF/UA atbilstība ##

PDF/UA standarts nosaka satura, lasītāju un palīgtehnoloģiju specifikācijas. Šie trīs aspekti ir savstarpēji saistīti, pamatojoties uz dokumenta saturu. Atbilstības prasības katram no tiem ir norādītas tālāk.

## Atbilstoši faili ##

Files conforming to PDF/UA standard should contain features that are valid as per the [PDF 1.7 specifications](https://opensource.adobe.com/dc-acrobat-sdk-docs/standards/pdfstandards/pdf/PDF32000_2008.pdf). However, features that are forbidden by PDF/UA specifically should be excluded.

## Atbilstoši lasītāji ##

Atbilstošam lasītājam ir jāievēro PDF 1.7 specifikāciju noteikumi. Konkrēti, tai jāatbalsta:

* visi tagi, atribūti un atslēgas vērtības, kas norādītas pieejamībai. Tam vajadzētu būt arī iespējai apstrādāt un attēlot ciparparakstus, anotācijas un neobligāto saturu.

* apstrādāt un pārstāvēt ciparparakstus, anotācijas un izvēles saturu

* pārvietoties pa dokumentu, izmantojot dažādus līdzekļus


## Atbilstoša palīgtehnoloģija ##

PDF/UA funkciju atbalstam ir nepieciešama atbilstoša palīgtehnoloģija. Tie ietver, piemēram, satura un lasītāja funkcijas, un tām ir jāļauj pārvietoties pēc lappušu etiķetēm, dokumenta struktūras vai kontūras. Tam vajadzētu arī ļaut lietotājam ignorēt noklusējuma navigācijas tālummaiņu.

## Atsauces Nr.

* [PDF/UA — Wikipedia](https://en.wikipedia.org/wiki/PDF/UA)

* [PDF/UA īsumā](https://pdfa.org/pdfua-in-a-nutshell/)


