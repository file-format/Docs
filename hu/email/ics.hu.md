{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICS - iCalendar fájlformátum",
  "description":"További információ az ICS-fájlformátumról és az API-król, amelyek ICS-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "ICS",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az ICS fájl?

Az Internet Calendaring and Scheduling Core Object Specification (iCalendar) egy internetes szabvány (RFC 2445) a naptári események és ütemezés cseréjéhez és telepítéséhez. Az iCalendar formátum interoperábilis, így biztosítja a naptárinformációk cseréjét a különböző e-mail alkalmazásokkal rendelkező felhasználók között. Az iCalendar a bemeneti adatokat Multipurpose Internet Mail Extensions-ként (MIME) formázza, és megkönnyíti a különböző szállítási protokollokon keresztüli objektumok cseréjét. Ezek az átviteli protokollok lehetnek SMTP, HTTP, pont-pont aszinkron kommunikáció és fizikai média alapú hálózati szállítás.

Az iCalendar lehetővé teszi a felhasználók számára, hogy e-mailben megosszák az eseményeket, a dátumtól/időtől függő feladatokat és az elfoglaltsági adatokat más felhasználókkal, akik válaszolhatnak. Az iCalendar fájlok ".ics" ".iCalendar" vagy ".ifb" utótagokkal tárolhatók, MIME-típussal "text/calendar". Az iCalendar önállóan működik, minden szállítási protokoll-függőség nélkül. A webszerverek (HTTP protokollal) továbbíthatják az iCalendar-információkat, a weboldalak pedig az iCalendar segítségével beágyazott formában tartalmazhatnak iCalendar-adatokat.

## Az ICS fájlformátum rövid története

1998-ban az Internet Engineering Task Force (IETF) szabványként határozta meg az iCalendart (RFC 2445). A szabványt Frank Dawson (Lotus Notes Corporation) és Derik Stenerson (Microsoft) dokumentálta. 2009-ben a szabványt Bernard Desruisseaux (Oracle) ismét RFC 5545 néven finomította. Ezúttal néhány új funkciót adtunk hozzá, és néhány elavult funkciót elavult. 2016-ban megjelent az RFC 7986, és az eredeti iCalendar RFC-re bővült. Az RFC 7986 új jellemzőkkel bővítette a fő VCALENDAR objektumot, és új támogató funkciókat is bevezettek a konferenciarendszerekhez.

## ICS fájlformátum ##

Az iCalendar adatai által használt MIME típus a „text/calendar”. Az iCalendar alapértelmezett karakterkészlete az UTF-8, azonban a MIME paraméterek megadásával más karakterkészlet is használható. Az iCalendar fájl szakaszokat tartalmaz, ezek között a szakaszok között a „VCALENDAR” az a globális szakasz, amely az összes többi szakaszt magába foglalja. A VEVENT szakasz meghatározza az eseményeket, a VTODO felsorolja az összes teendőt, a VJOURNAL naplóbejegyzéseket tartalmaz, a VTIMEZONE pedig az időzóna információit. több hasonló kategóriájú szakasz megengedett. Számos esemény esetén több VEVENT szekció is jelen lehet egy iCalendar fájlban.

### Tartalomsorok ###

Az iCalendar objektumok különálló szövegsorokba vannak rendezve, „tartalmi sorokba”. Ebben a fájlformátumban a CRLF sorozat egy sort zár le, míg a sor hossza 75 oktettre korlátozódik, a sortörés nélkül. Egy hosszú adatelem több sorra is átterelhető.

### Lista- és mezőelválasztók ###

A tulajdonságok és paraméterek olyan értékek listáját adják meg, amelyeket VESZSŐ karakter választ el. Az idézett karakterláncok az URI-alapú paraméterértékekhez használatosak. A paraméterek listája az ingatlanérték alapján összeállítható. Ebben a listában minden tulajdonságparamétert SEMIKOVESZTŐVEL kell elválasztani.

Egy értéklistában egy SEMIKOSZTÓ választja el a tulajdonságparamétereket, és egy VESZSŐ választja el a tulajdonságértékeket. Példa alább látható:

```
ATTENDEE;RSVP#TRUE;ROLE#REQ- contestant:mailto:
name@example.com
DATE;VALUE#DATE:20170304,20180504,2015704,201270904
```

### Több érték

Egyes tulajdonságoknak több értéke is lehet. A többértékű tulajdonságok alapszabálya egy új tartalomsor egyszerű létrehozása a tulajdonság nevével. Egyetlen, több nyelvi változattal rendelkező érték esetén azonban nem szabad többértékű tulajdonságokat használni.

### Bináris tartalom

Az iCalendar objektumon belül a tulajdonságérték hivatkozhat egy külső MIME-entitásban elhelyezett bináris tartalomadatokra egy URI használatával. A soron belüli bináris tartalom speciális helyzetekben használható "ENCODING" paraméterrel, amikor az alkalmazásnak egyetlen entitásként kell kifejeznie egy iCalendar objektumot. A következő példa egy "ATTACH" tulajdonságot magyaráz meg URI hivatkozással:

CSATLAKOZÁS: https://products.conholdate.app/viewer/view/KDDURXKkLk/fileformat.doc

### Karakterkészlet

Bár az iCalendar alapértelmezett karakterkészlet-sémája UTF-8, nincs megadva tulajdonságparaméter a tulajdonságérték karakterkészletének meghatározásához. a MIME átvitelben a "charset" paramétert KELL használni a meglévő karakterkészlethez.

## Hivatkozások

* [Internet Calendaring and Scheduling Core Object Specification](https://www.ietf.org/rfc/rfc5545.txt)
* [iCalendar (RFC 5545)](https://icalendar.org/RFC-Specifications/iCalendar-RFC-5545/)
* [iCalendar](https://en.wikipedia.org/wiki/ICalendar#History_and_design)

