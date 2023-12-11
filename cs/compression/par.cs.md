{
"date":"2023-07-18",
   "keywords":[
"PAR",
"Soubor PAR",
"jak otevřít soubor par",
"soubor",
"Přípona souboru PAR",
"rozšíření",
"soubor"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft":"false",
"toc":true,
"title":"Formát souboru PAR - soubor indexu archivace",
   "description":"Další informace o formátu PAR a rozhraních API, která mohou vytvářet a otevírat soubory PAR.",
   "linktitle":"PAR",
   "menu":{
      "docs":{
         "identifier":"compression-par",
         "parent":"compression"
}
},
"lastmod":"2023-07-18"
}

## Co je soubor PAR?

V rámci archivů Parchive (PAR) odkazuje soubor .par na soubor indexu, který obsahuje skupinu paritních svazků nebo paritních bloků. Tento indexový soubor se používá pro účely zjišťování chyb a obnovy, když dojde ke ztrátě nebo poškození jednoho nebo více souborů v archivu.

Archiv Parchive se obvykle skládá jak z původních datových souborů, tak z odpovídajících paritních svazků. Paritní svazky jsou vytvářeny pomocí Reed-Solomonových algoritmů pro opravu chyb. Tyto paritní svazky obsahují redundantní informace, které lze použít k obnovení původních datových souborů.

Soubor .par, také známý jako sada paritních svazků, obsahuje informace o struktuře a umístění paritních svazků v archivu. Slouží jako index nebo mapa pro proces obnovy. Pomocí souboru .par může specializovaný software PAR určit, které paritní svazky jsou potřeba a jak by měly být použity k rekonstrukci chybějících nebo poškozených souborů.

Když se jeden nebo více souborů v archivu Parchive stane nedostupným nebo poškozeným, soubor .par lze použít ve spojení s dostupnými paritními svazky k obnovení ztracených dat. Software PAR přečte soubor .par, identifikuje chybějící nebo poškozené soubory a použije paritní svazky k jejich rekonstrukci.

## Jak otevřít soubor PAR?

Chcete-li otevřít a používat soubory .par, budete potřebovat specializovaný software PAR. Zde je několik oblíbených možností softwaru, které zvládnou soubory .par:

- **QuickPar:** QuickPar je široce používaný software PAR pro Windows. Umožňuje vytvářet, ověřovat a opravovat soubory PAR. Soubor .par můžete otevřít v QuickPar a ověřit jeho integritu nebo jej použít k opravě poškozených nebo chybějících souborů v archivu Parchive.

- **MultiPar:** MultiPar je další populární software PAR dostupný pro Windows. Podporuje formáty souborů PAR i PAR2 a poskytuje pokročilé funkce pro vytváření, ověřování a opravy archivů. MultiPar může otevírat soubory .par a provádět operace zjišťování chyb a obnovy na základě poskytnutých paritních svazků.

- **MacPAR deLuxe:** MacPAR deLuxe je software PAR navržený speciálně pro macOS. Podporuje formáty souborů PAR a PAR2 a poskytuje podobné funkce jako QuickPar a MultiPar. MacPAR deLuxe může otevírat soubory .par a pomáhat při ověřování archivů a obnově poškozených nebo chybějících souborů.

## Formát souboru PAR - Další informace

Formát souboru PAR, běžně označovaný jako Parchive, je specifický formát souboru používaný pro vytváření paritních dat a provádění detekce chyb a obnovy v archivech souborů. Formát souboru PAR se obvykle skládá ze tří typů: PAR, PAR2 a PAR3.

- **PAR:** Původní formát souboru PAR, také známý jako PAR1, byl vyvinut projektem Parchive. Zahrnuje paritní data generovaná z původních datových souborů. Soubory PAR poskytují základní úroveň detekce a obnovy chyb, ale mají omezení, pokud jde o možnosti opravy chyb.

- **PAR2:** PAR2 je vylepšená verze formátu souboru PAR. Nabízí pokročilejší možnosti opravy chyb a vylepšené funkce obnovy. Soubory PAR2 se obvykle používají k vytváření paritních dat, která mohou obnovit ztracené nebo poškozené soubory v archivu. Soubory PAR2 poskytují lepší ochranu proti poškození dat a jsou široce používány pro účely archivace souborů.

- **PAR3:** PAR3 je nejnovější verze formátu souboru PAR a poskytuje další vylepšení v opravě chyb a obnově. Ve srovnání s PAR2 nabízí ještě vyšší úroveň redundance a oprav chyb. Soubory PAR3 jsou navrženy tak, aby poskytovaly robustnější možnosti ochrany a obnovy dat uložených v archivech.

Oba formáty souborů PAR2 a PAR3 jsou široce podporovány softwarem PAR a nabízejí možnost ověřit integritu souborů v archivu a obnovit ztracená nebo poškozená data. Soubory PAR a PAR2 se stále běžně používají, zatímco soubory PAR3 si postupně získávají přijetí díky svým rozšířeným možnostem opravy chyb.

## Reference
* [Archiv](https://en.wikipedia.org/wiki/Parchive)

