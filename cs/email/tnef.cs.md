{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TNEF",
  "description":"Další informace o formátu souboru TNEF a rozhraních API, která mohou vytvářet a otevírat soubory TNEF.",
  "linktitle" : "TNEF",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor TNEF?

Transport Neutral Encapsulation Format (TNEF) je patentem společnosti Microsoft pro zapouzdření e-mailových příloh na základě rozhraní Messaging Application Programming Interface (**MAPI**). Microsoft Outlook a Microsoft Exchange Server plně podporují TNEF, zatímco později dekódují TNEF do MAPI a zobrazují naformátované e-maily. Příloha e-mailu s kódováním TNEF má typ MIME MS-TNEF a ukládá se jako winmail/win.dat. Příloha ve winmail .dat obsahuje následující informace:


|Zpráva|Objekty OLE|Funkce aplikace Outlook
---|---|---|
|<ul><li> Původní přílohy zpráv</li><li> Původní formátovaná verze</li><li> písma, velikosti textu a barvy textu</li></ul> |<ul><li> vložené obrázky</li><li> vestavěné dokumenty Office</li></ul> |<ul><li> vlastní formuláře</li><li> hlasovací tlačítka</li><li> žádosti o schůzku</li></ul>


Jiné e-mailové služby, které nepodporují TNEF, prezentují prostý text pro zprávy ve formátu TNEF. Aplikace Outlook vloží bohatý formát zprávy do souborů TNEF (OLE) nebo konkrétních funkcí aplikace Outlook (formuláře, tlačítka pro dotazování a požadavky na konference). Schvalování explicitního kódování TNEF v rámci e-mailového klienta Outlook není možné, avšak volba formátu RTF pro odesílání e-mailu implicitně usnadňuje kódování TNEF.

## Formát souboru TNEF

Algoritmus dat TNEF vytváří zploštělou strukturu z bohatých hierarchických vlastností zpráv. Tyto zploštělé struktury pak reprezentují sériový datový tok složený z konkrétních vlastností.

V některých situacích, kdy se vlastnosti vyskytují ve skupinách nebo mají více hodnot, může stream obsahovat počty a výplně, aby bylo možné vynutit konkrétní zarovnání dat. Charakteristická situace, kdy je použití tohoto algoritmu výhodné, je v nepodporujícím prostředí zasílání zpráv. V takových prostředích je vlastnost bohaté zprávy zakódována do sériového datového proudu pomocí TNEF Writer. Dále, vlastnosti, které nepatří k základnímu TNEF, mohou být zapouzdřeny během přenosu. Tyto zapouzdřené vlastnosti se poté zpřístupní dekódováním prostřednictvím TNEF, aby byla zajištěna dostupnost všech vlastností původní zprávy pro klientskou aplikaci.

V TNEF jsou všechny číselné datové typy typu little-endian a jejich velikost je větší než jeden bajt. Zpracování těchto číselných hodnot na platformách, které nejsou Little-endian, vyžaduje provedení příslušných transformací pro získání správných hodnot. Hodnoty řetězce jsou reprezentovány ve formátu Augmented Backus-Naur Form (ABNF) podle specifikací [RFC5234]. Když řetězec končí znakem null, je také zahrnut; například "worker@specimen.com" %x00.

{{< figure src="../TNEF.png" alt="Formát souboru TNEF" >}}

## Atributy TNEF a pravidla zpracování ##

Datový tok v TNEF začíná číslem starší verze, podpisem, hodnotou primitivního klíče a atributem představujícím kódovou stránku. Tato kódová stránka se generuje, když kodér zaznamená atributy a vlastnosti ANSI. Poté se datový proud stal sérií atributů, ve kterých se nejprve řadily atributy zprávy a poté následovaly atributy přílohy. Různé charakteristiky zpráv a příloh jsou obsaženy ve speciálních atributech, jako je attMsgProps, attAttachment a attRecipTable. Atributy, které se objevují v proudu TNEF, obsahují strukturu, vlastnosti zprávy a převody potřebné k jejich zapojení do vlastností zprávy. Každý atribut se skládá z ID, velikosti a dat atributu, kontrolního součtu a úrovně podle jeho použití.

## Vztah k protokolům a jiným algoritmům ##

Systémy, které mají špatný mechanismus pro zobrazení bohatého formátu zpráv, nativně potřebují pro přenos datový algoritmus TNEF. Při použití typu média ms-TNEF se výstup algoritmu skládá z přiloženého souboru (winmail.dat) a části těla MIME specifikované v [RFC2045]. Tělo zprávy ve formátu prostého textu je přenášeno pomocí UUENCODE podle specifikace [MSDN-UAF] a toto tělo zprávy nebo ekvivalentní metoda je dekódována na straně příjemce. Kromě toho může TNEF přenášet data zpráv pomocí různých internetových protokolů, jako jsou SMTP, POP3, IMAP4 a ty, které integrují MIME podle standardu RFC2045.

## Prohlášení o použitelnosti ##

Kromě jednoduchého přenosu zpráv měla být původní aplikace TNEF vytvořena tak, aby používala třídy zpráv a podporovala další funkce, které nemají žádnou původní podporu v transportním protokolu. Tato aplikace byla dále vylepšena pro přenos vlastností bohatých zpráv a pojmenovaných vlastností, které moderní klienti pro zasílání zpráv dnes používají. Pro soulad s původní implementací je zachována původní syntaxe atributu a speciální atribut uchovává vlastnosti nové zprávy samostatně.

## Reference

* [Transport Neutral Encapsulation Format](https://en.wikipedia.org/wiki/Transport_Neutral_Encapsulation_Format)
* [E-mailové adresy a adresáře na Exchange Server](https://learn.microsoft.com/en-us/exchange/email-addresses-and-address-books/email-addresses-and-address-books?view# exchserver-2019)
* [[MS-OXTNEF]: Datový algoritmus TNEF (Transport Neutral Encapsulation Format)](https://msdn.microsoft.com/en-us/library/cc425498(v#exchg.80).aspx)

