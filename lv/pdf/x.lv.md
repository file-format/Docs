{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PDF/X faila formāts",
  "description": "Uzziniet par PDF/X failu formātu un API, kas var izveidot un atvērt PDF/X failus.",
  "linktitle": "PDF/X",
  "menu": {
    "docs": {
      "parent": "pdf",
      "identifier": "pdf--lvx"
}
},
  "lastmod": "2019-09-10"
}

# Kas ir PDF/X fails? #

PDF/X ir ISO 15930 standarts, kas publicēts 2001. gadā ar PDF funkcionalitātes apakškopu. Standarts tika izveidots un publicēts, pamatojoties uz īpašām poligrāfijas un izdevējdarbības nozares prasībām. Visas prasības šim standartam tika izstrādātas atbilstoši dažādajām poligrāfijas un izdevējdarbības nozares vajadzībām. PDF/X prasa, lai atbilstošie faili būtu pilnīgi, ti, atsevišķi. Tas prasa, lai tādi elementi kā lapā izmantotie fonti būtu daļa no dokumenta. Tāds saturs kā 3D vai video nevar būt PDF/X dokumenta daļa. PDF/X dokumentā ietvertajai informācijai ir jābūt precīzai.

## PDF/X standarti un labojumi ##

PDF/X standartu saime sastāv no vairākām versijām, no kurām katra ir paredzēta specializētam rezultātam. Šo standartu izstrādes mērķis bija apmierināt daudzās dažādās poligrāfijas un izdevējdarbības nozares vajadzības.

* `PDF/X-1a` — pazīstams arī kā pirmais PDF/X saimes standarts, lai PDF/X-1a viss saturs būtu daļa no PDF dokumenta, lai to varētu drukāt. Nav atļauti dokumenta elementi, piemēram, fonti, veidlapas, aizsardzība ar paroli un redzamas anotācijas. PDF/X-1a ir savas īpašās prasības, kā arī ir atļautas tādas prasības, kas attiecas uz caurspīdīgumu un slāņiem. Tie arī pieprasa drukas elementiem izmantot tikai CMYK, pelēktoņu vai punktkrāsas, kā rezultātā netiek izmantotas RGB vai no ierīces neatkarīgas krāsu telpas. ir paredzēts apmaiņai, kurā visi faili ir jāpiegādā CMYK (un/vai spot krāsās), bez RGB vai krāsu pārvaldītiem datiem. PDF/X-1a tiek dēvēts arī par pilnīgu apmaiņu, jo ir nepieciešama informācija par pilnīgu

* `PDF/X-3` — tika ieviests 2002. gadā un atcēla daudzus PDF/X-1a ierobežojumus. Tas iespējoja grafiku PDF/X-3, lai izmantotu CMYK, grescale, RGB, Lab un ICC balstītas krāsu telpas. Tas faktiski ir balstīts uz PDF standartiem 1.3 ar [ICC profilu](https://en.wikipedia.org/wiki/ICC_Profile). To dēvē arī par krāsu pārvaldību, pateicoties elastībai un noteikumiem, ko tā ievieš saistībā ar PDF dokumentā iekļautajām krāsām.

* `PDF/X-4` - atbalsta caurspīdīgās plēves, tāpēc PDF-X/4 satur visus izvadei nepieciešamos datus bez saplacināšanas.

* `PDF/X-5` — ir balstīts uz PDF/X-4, pievienojot atbalstu ārējai grafikai, izmantojot atsauces XObjects, kā arī ārējos n-krāsu profilus nolūka atveidošanai. Izmantojiet to daļējai drukāšanas datu apmaiņai, izmantojot PDF versiju 1.6


## Atsauces Nr.

* [PDF/X — Wikipedia](https://en.wikipedia.org/wiki/PDF/X)


