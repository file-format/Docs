{
  "date": "2019-10-11",
  "keywords": [
"jhtml",
"jhtml failu",
"jhtml faila formātā",
"jhtml faila tips",
"failu",
"veids",
"kas ir jhtml fails"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "JHTML - Java HTML fails",
  "description": "Uzziniet par JHTML faila formātu un API, kas var izveidot un atvērt JHTML failus.",
  "linktitle": "JHTML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-jhtm-lvl"
}
},
  "lastmod": "2021-06-09"
}

## Kas ir JHTML fails?

Fails ar paplašinājumu .jhtml ir [HTML](/web/html/) fails ar [Java](/programming/java/) kodu, kas tiek izpildīts serverī, kad klients pārlūkprogrammā pieprasa šo lapu. Serveris apstrādā pieprasījumus, izpilda funkcijā ietvertās Java funkcijas un atgriež lapu klienta pārlūkprogrammā. JHTML lapās iegultie Java objekti darbojas serverī, lai apstrādātu šāda veida lapu pieprasījumus. JHTML faili var arī piekļūt informācijai no datu bāzes, izmantojot JDBC (Java [Database](/database/) savienojamība) savienojumu. JHTML failus var atvērt jebkurā teksta redaktorā un skatīt tīmekļa pārlūkprogrammās, piemēram, Google Chrome, Firefox un Safari.

## JHTML faila formāts

JHTML ir ATG patentēta tehnoloģija, un to var izveidot, izmantojot ATG (Art Technology Group) Dynamo dokumentu redaktoru. JHTML faili ir rakstīti vienkārša teksta faila formātā, izmantojot standarta HTML un Java kodu. Tie satur standarta HTML tagus papildus patentētajiem tagiem, kas atsaucas uz Java objektiem. Kad lietotājs pieprasa šādu lapu, HTTP serveris pārsūta pieprasījumu Java lietojumprogrammu serverim. JHTML lapa vispirms tiek pārveidota par .java failu un kompilēta, lai ģenerētu [.class](/programming/class/) failu, kas tiek izpildīts kā servlet. Tas ģenerē standarta HTTP un HTML datu straumi, kas tiek atgriezta atpakaļ pieprasītajā pārlūkprogrammā, lai to parādītu lietotājam. Tas ir noderīgi, lai serverī palaistu ar datu bāzi saistītus vaicājumus un atgrieztu galīgo uzkrāto rezultātu klienta pārlūkprogrammā.

## Atsauces

* [HTML dokumenta globālā struktūra](https://www.w3.org/TR/html401/struct/global.html#h-7.5.4)


