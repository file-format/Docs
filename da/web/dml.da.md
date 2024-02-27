{
  "date": "2021-05-25",
  "keywords": [
"DML",
"DML fil",
"DML filformat",
"DML filtype",
"fil",
"type",
"hvad er en DML-fil"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DML - DynaScript HTML-fil",
  "description": "Lær om DML-filformat og API'er, der kan oprette og åbne DML-filer.",
  "linktitle": "DML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-dm-dal"
}
},
  "lastmod": "2021-05-25"
}

## Hvad er en DML fil?

En fil med filtypenavnet .dml er en webscriptsidekodefil oprettet med DyanScript. DynaScript er et dynamisk [HTML](/web/html/) scriptsprog, der er kompatibelt med ECMAScript og giver de fleste af de samme funktioner som andre scriptsprog. Det ligner ColdFusion-kode og Microsoft Active Server Pages (ASP)-kode. DML-filer kan åbnes og ses i standard webbrowsere, der ligner andre HTML-sider.

## DML filformat

DML-filer oprettes i almindeligt tekstfilformat og kan åbnes med en teksteditor for at se koden. Kodeskrivning ved hjælp af DML-scriptsprog kan bruges til dynamisk at generere HTML på serverside hostede DML-sider. DynaScripts er bygget ud fra følgende sprogelementer:


 * SCRIPT-tag - Disse er indlejret i dokumenter som HTML-kommentarer. En HTML-kommentar er markeret med en \
 * Bogstaver - Disse er faste værdier i DynaScript-filer. Eksempler på disse omfatter heltal såsom s 123 , 0x3F , 0123, flydende kommatal såsom 456.789 , 3.2e-8, Boolean såsom sand eller falsk og streng såsom Regnen i Spanien
 * Variabler - DynaScript-variabler behøver ikke at defineres eller tildele dem til en fast datatype. En variabel skal have en værdi, før du bruger den i et udtryk; ellers genereres en runtime-advarsel.
 * Udtryk - Disse er kombinationer af variable, bogstavelige værdier, operatorer og andre udtryk. Højre side af en opgaveerklæring er et udtryk.
 * Operatorer - Disse opererer på et eller flere udtryk kaldet operander. Disse kan være enten ternære, binære eller unære: ternære operatorer virker på tre udtryk, binære operatorer virker på to udtryk, og unære operatorer virker på ét.
 * Udsagn - Disse kontrollerer scriptflow, manipulerer objekter og generel programmering. Generelt følger disse udsagn standard C- og Java-syntaks. Eksempler er if-else, do-while loops, switch, break, continue osv. ligesom ethvert andet scriptsprog.
* Funktioner - Funktioner, som ethvert andet scriptsprog, giver dig mulighed for at indkapsle et sæt instruktioner én gang i et dokument som en funktion, og derefter bruge det flere gange gennem hele dokumentet (ved at kalde funktionen). DynaScript understøtter også funktioner.

* Objekter - DynaScript er objektorienteret og understøtter 'objekter' og de grundlæggende objektorienterede begreber indkapsling, polymorfi og arv.


