{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PCL",
  "description":"Další informace o formátu souborů PCL a rozhraních API, která mohou vytvářet a otevírat soubory PCL.",
  "linktitle" : "PCL",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor PCL? ##

PCL je zkratka pro Printer Command Language, což je jazyk popisu stránky zavedený společností Hewlett Packard (HP). Společnost HP vytvořila jazyk PCL, který poskytuje efektivní způsob ovládání funkcí tiskárny na mnoha různých tiskových zařízeních. Formát byl původně vyvinut pro jehličkové a inkoustové tiskárny HP, ale postupem času se stal součástí různých termálních, matricových a stránkových tiskáren. Formát prošel několika různými revizemi, což vedlo k různým verzím, kde každá verze byla vylepšena tak, aby splňovala požadavky času s ohledem na funkce ovládání tiskárny. Dnes je PCL nejrozšířenějším tiskovým jazykem na trhu nejnovějších tiskáren.

## PCL verze ##

Verze PCL se liší funkčností (např. podpora typů písma: bitmapová písma, škálovatelná písma (fonty Intellifonts, TrueType), metody komprese rastrové grafiky, grafická podpora HP-GL/2).

**PCL 1:** kolem roku 1980 – Funkce Print and Space je základní sadou funkcí poskytovaných pro jednoduchý, pohodlný výstup z pracovní stanice pro jednoho uživatele.

**PCL 2:** kolem roku 1980 – funkce EDP (Electronic Data Processing)/transakce jsou nadmnožinou PCL 1. Byly přidány funkce pro všeobecný tisk v systému pro více uživatelů.

**PCL 3**: 1984 - Funkce Office Word Processing je nadmnožinou PCL 2. Byly přidány funkce pro vysoce kvalitní produkci kancelářských dokumentů a zvýšení dpi až na 300 dpi. Umožňoval použití omezeného počtu bitmapových písem a grafiky a podporoval HP-GL. PCL 3 byl široce napodobován jinými výrobci tiskáren a byl těmito společnostmi označován jako „Emulace LaserJet Plus“.
(Tiskárny: řada HP DeskJet, tiskárna řady HP LaserJet, tiskárna řady HP LaserJet Plus)

**PCL3+:** Používá se u tiskáren řady DeskJet a DesignJet.

**PCL3c:** Používá se u tiskáren řady DeskJet a DesignJet.

**PCL3e**: Používá se u tiskáren řady DeskJet a DesignJet. Nyní se používá také ve PhotoSmart.

**PCL3GUI**: Využívá RTL a je používán řadou tiskáren DeskJet a DesignJet.

**PCLSLEEK**: Používá RTL a je používán řadou tiskáren DeskJet a DesignJet.

**PCL 4**: 1985 - Funkce formátování stránky je nadmnožinou PCL 3. Podporovaná makra, větší bitmapová písma a grafika. (Tiskárny: HP LaserJet II, HP LaserJet IIP (PCL 4.5))

**PCL 5:** 1990 – Funkce Office Publishing je nadmnožinou PCL 4. Nové možnosti publikování zahrnují změnu velikosti písma a HP-GL/2 (vektorovou) grafiku. (Tiskárny: HP LaserJet III)

**PCL 5e:** 1994 – Toto je hlavní revize, která zahrnuje nové funkce, jako je adaptivní kompresní systém, 2bajtové kódování znaků, podpora vektorových písem a obousměrné konfigurační příkazy. Zahrnuje logické operace (odpovídá GDI ROP) pro zlepšení podpory Windows před ořezovými cestami. (Tiskárny: HP LaserJet 4)

**PCL 5j:** Nové funkce, jako je podpora dvoubajtových znaků pro japonská rezidentní škálovatelná písma, vertikální psaní, japonské velikosti papíru a řetězce písem. (Tiskárny: HP LaserJet 4PJ)

**PCL 5c:** 1995 – Do PCL5 byla přidána podpora barev a logické operace. PCL5c předchází PCL5e. Některé modely také podporují ořezové cesty. (Tiskárny: HP Color LaserJet, HP PaintJet 300 XL (první tiskárna s PCL5c), HP DeskJet 1200C/1600C (tato čísla modelů byla znovu použita a novější modely nejsou PCL 5c)

**PCL 5ce:** Podporuje škálovatelné typy písma Agfa Microtype. (Tiskárny: HP 2500c Pro Printer)

**PCL 6 / XL:** 1996 - PCL 6 nebo PCL XL je nový formát představený v roce 1995, který není kompatibilní s žádnou předchozí verzí PCL. (Tiskárny: HP LaserJet 5, 5M a 5N)

## PCL 6 Přehled ##

Společnost HP představila PCL 6 v roce 1996, což byl další vývoj jazyka PCL a souvisejících technologií. Má následující komponenty:

**PCL 6 Enhanced:** poskytuje optimalizovanou verzi pro tisk z grafických uživatelských rozhraní (GUI), jako jsou MS Windows a OS/2

**PCL 6 Standard:** poskytuje úplnou zpětnou kompatibilitu s předchozími tiskárnami HP LaserJet

**Syntéza písem PCL:** poskytuje škálovatelná písma, správu písem a ukládání formulářů a písem.

Rozšířená verze PCL XL je blíže GDI, kterou používá mnoho aplikací. Zajišťuje, že se bude provádět méně překladů, což má za následek zvýšené možnosti WYSIWYG a lepší výkon s aplikacemi, které podporují escape implementované ovladačem Enhanced. Výstup z ovladače Enhanced (PCL XL) nemusí být stejný jako výstup ze standardního ovladače. Pokud výstup neodpovídá očekávání, vyberte místo toho ovladač Standard (PCL5e).

Příkazy PCL 6 Enhanced jsou navrženy tak, aby optimálně odpovídaly požadavkům na tisk grafiky pro aplikace založené na grafickém uživatelském rozhraní. Ve většině případů existuje pro každý příkaz k tisku grafiky, který si GUI přeje provést, odpovídající příkaz PCL 6 Enhanced. To snižuje počet příkazů potřebných k popisu grafické stránky. Každý příkaz v PCL 6 Enhanced je navržen tak, aby vyžadoval minimální přenos dat z hostitelského počítače do tiskárny. To snižuje množství dat potřebných k popisu stránky.

Tiskový systém Windows pro většinu tiskáren HP LaserJet poskytuje dva samostatné ovladače: Standardní a Vylepšený. Ovladač Standard poskytuje zpětnou kompatibilitu pomocí příkazů PCL 6 Standard (PCL5e) pro tisk jednoduchého textu nebo smíšených textových a grafických stránek. Ovladač Enhanced využívá příkazy PCL 6 Enhanced, které byly optimalizovány pro tisk složitých grafických stránek.

## PCL 6 Třída Revize ##

#### Třída 1.1 ####

**Nástroje pro kreslení:** Podpora kreslení čar, oblouků/elips/tetiv, (zaoblených) obdélníků, mnohoúhelníků, Bézierových cest, oříznutých cest, rastrových obrázků, skenovacích čar, rastrových operací.
**Manipulace s barvami:** Podpora 1/4/8bitových palet, barevný prostor RGB/šedá. Podpora vlastních polotónových vzorů (max. 256 vzorů).
**Komprese:** Podporuje RLE.
**Měrné jednotky:** Palce, milimetry, desetiny milimetru.
**Manipulace s papírem:** Podpora vlastních nebo předdefinovaných sad typů papíru, včetně běžných Letter, Legal, A4 atd. Může si vybrat papír z ručního podávání, zásobníků, kazet. Papír lze oboustranně tisknout vodorovně nebo svisle. Papír lze orientovat na výšku, na šířku nebo otočení o 180 stupňů.
**Font:** Podporuje bitmapové nebo TrueType fonty, 8 nebo 16bitové kódové body. Výběr znakové sady používá jiný kód znakové sady než PCL 5. Při použití bitmapového písma není k dispozici mnoho příkazů pro změnu měřítka. Při použití písma TrueType, deskriptorů proměnné délky a bloků pokračování nejsou podporovány. Obrysové písmo lze otáčet, měnit jeho měřítko nebo stříhat.

#### Třída 2.0 ####

**Komprese:** Přidána proprietární komprese JPEG nazvaná JetReady.
**Manipulace s papírem:** Média lze přesměrovat do různých výstupních přihrádek (až 256). Přidány přednastavené formáty médií A6 a Japonec B6. Přidána předvolba třetí kazety, 248 zdrojů médií z externího zásobníku.
**Písmo:** Text lze psát svisle.

#### Třída 2.1 ####

**Manipulace s barvami:** Přidána funkce přizpůsobení barev.
**Komprese:** Přidána řada Delta Row.
**Manipulace s papírem:** Orientace a formát média jsou volitelné při deklarování nové stránky. Přidány typy papíru B5, JIS 8K, JIS 16K, JIS Exec.

#### Třída 3.0 ####

**Manipulace s barvami:** Umožňuje použití různých nastavení polotónů pro vektorovou nebo rastrovou grafiku, text. Podporuje adaptivní polotónování.
**Protokol:** Podporuje PCL passthrough, což umožňuje využití funkcí PCL 5 v tocích PCL 6. Některé stavy PCL 6 se však při použití této funkce nezachovají.
**Font:** Podporuje písma PCL.
**Prohlížeč/převaděč:** PCLReader (freeware) může zobrazit, převést nebo vytisknout jakoukoli úroveň PCL 6 (včetně JetReady) na jakékoli tiskárně.

## Reference ##

* [PCL – z Wikipedie](https://en.wikipedia.org/wiki/Printer_Command_Language)

