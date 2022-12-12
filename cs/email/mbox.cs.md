{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MBOX – soubor e-mailové schránky",
  "description":"Další informace o formátu souboru MBOX a rozhraních API, která mohou vytvářet a otevírat soubory MBOX.",
  "linktitle" : "MBOX",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor MBOX?

Formát souboru MBox je obecný termín, který představuje kontejner pro sběr zpráv elektronické pošty. Zprávy jsou uloženy uvnitř kontejneru spolu s jejich přílohami. Zprávy z celé složky se ukládají do jednoho databázového souboru a na konec souboru se připojují nové zprávy. Četné aplikace a API poskytují podporu pro souborový formát MBox, jako je Apple Mail a Mozilla Thunderbird.

## Formát souboru MBOX ##

Formát souboru MBox zůstal poměrně dlouho nestandardizovaný až do roku 2005, kdy byla aplikace/mbox standardizována jako [RFC 4155.](https://tools.ietf.org/rfc/rfc4155.txt) Zprávy ve formátu RFC 2822 , jsou zřetězeny ve formátu souboru MBox jeden po druhém. Každá zpráva začíná oddělovacím řádkem, který identifikuje odesílatele zprávy a také identifikuje datum a čas, kdy byla zpráva přijata konečným příjemcem (buď systémem posledního skoku v přenosové cestě, nebo systémem, který slouží jako příjemce poštovní úložiště). Každá zpráva je obvykle ukončena prázdným řádkem. Konec databáze je obvykle rozpoznán buď podle absence jakýchkoli dalších dat, nebo podle přítomnosti explicitního označení konce souboru.

## Čtení zprávy ze souboru MBox ##

Čtečka prohledává soubor mbox a hledá řádky From_. Libovolný řádek From_ označuje začátek zprávy. Čtenář by se neměl pokoušet využít skutečnosti, že každý řádek From_ (za začátkem souboru) je prázdný. Jakmile čtenář najde zprávu, extrahuje (pravděpodobně poškozenou) obálku odesílatele a datum doručení z řádku From_. Poté čte až do dalšího řádku From_ nebo konce souboru, podle toho, co nastane dříve. Odstraní poslední prázdný řádek a vymaže citace >Od_ řádků a >>Od_ řádků a tak dále. Výsledkem je zpráva RFC 822.

## Úvahy o kódování ##

Obsah souboru MBox se může nevratně promíchat, když přijatý e-mail obsahuje soubor Mbox jako přílohu a je uložen v jiném souboru Mbox. Aby se tomu zabránilo, musí systémy pro zasílání zpráv kódovat databázi mbox pomocí netransparentního kódování přenosu (jako je BASE64 nebo Quoted-Printable), kdykoli je takový objekt přenášen prostřednictvím protokolů pro zasílání zpráv. Implementátoři by také měli být připraveni lokálně zakódovat data mbox, pokud obdrží nevyhovující data.

## Reference ##

* [MBox - RFC4155](https://tools.ietf.org/rfc/rfc4155.txt)
* [Mbox – Wikipedie](https://en.wikipedia.org/wiki/Mbox)

