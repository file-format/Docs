{
  "date" : "2019-10-11",
  "keywords" :[ "soubor mpx", "formát souboru mpx", "co je soubor mpx", "soubor", "příklad mpx", "přípona souboru mpx", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MPX - Microsoft Project Exchange File Format",
  "description":"Další informace o formátu souboru MPX a rozhraních API, která mohou vytvářet a otevírat soubory MPX.",
  "linktitle" : "MPX",
  "menu" : {
    "docs" : {
      "parent" : "project-management"
}
},
  "lastmod" : "2021-05-07"
}

## Co je soubor MPX? ##

Soubor s příponou .mpx je formát souborů Microsoft Exchange. Formát souboru MPX byl vyvinut společností Microsoft Project (MSP), aby usnadnil výměnu informací o projektu mezi MSP a dalšími aplikacemi podporujícími formát souboru MPX, včetně Primavera Project Planner, Sciforma a Timerline Precision Estimating. Pomocí souborů MPX můžete přenést všechny druhy informací z projektu do jiného systému, jako jsou podrobné informace o přiřazení zdrojů, informace z kalendáře nebo informace z dialogového okna Informace o projektu.

Microsoft Project 4.0 zavedl podporu pro vytváření a čtení formátů souborů MPX, které byly nadále používány prostřednictvím Microsoft Project 98. Podpora pro vytváření souborů MPX však přestala vydávat Microsoft Project 2000 a verze do Microsoft Project 2010 podporují pouze čtení MPX. Formát souboru MPX není podporován ve verzích pozdějších než MSP 2010.

## MPX formát souboru ##

Přehled specifikací souborů MPX je uveden v této části. Kompletní specifikace naleznete v této [Knowledge Base](https://support.microsoft.com/en-us/office/file-formats-supported-by-project-desktop-face808f-77ab-4fce-9353-14144ba1b9ae) článek a lze na něj odkazovat podrobnosti.

### Záznamy ###

Záznam souboru MPX se skládá z informací o projektu. Existují různé typy záznamů, kde každý záznam má své vlastní pořadí. Každý typ záznamu je identifikován svým číslem záznamu. U MPX souboru je nutné obsahovat typ záznamu File Creation. Jiné typy záznamů nejsou povinné. V následující tabulce jsou uvedeny všechny typy záznamů, jejich čísla záznamů a počet záznamů, které může každý typ obsahovat v souboru MPX. Zařazení záznamu do souboru MPX se musí řídit pořadím tabulky, s komentářem vloženým kamkoli.

|Název záznamu|Číslo záznamu|Maximální počet záznamů
---|---|---|
|Vytvoření souboru (vyžadováno)|žádné|1
|Nastavení měny|10|1
|Výchozí nastavení|11|1
|Nastavení data a času|12|1
|Definice základního kalendáře|20|250
|Základní kalendářní hodiny|25| 7 na záznam Definice základního kalendáře
|Výjimka základního kalendáře|26| 250 za záznam Definice základního kalendáře
|Záhlaví projektu|30|1
|Definice textové tabulky zdrojů|140|1- (Nebo můžete použít záznam Definice tabulky numerických zdrojů)
|Definice číselné tabulky zdrojů|41|1
|Zdroj|50|9 999
|Poznámky ke zdrojům|51| 1 na záznam zdroje
|Definice kalendáře zdrojů|55| 1 na záznam zdroje
|Otevírací doba kalendáře zdrojů|56| 7 na kalendář zdrojů
|Výjimka kalendáře zdrojů| 57|250 za kalendář zdrojů
|Textová definice tabulky úloh|60|1 (Nebo můžete použít záznam Definice tabulky číselných úloh)
|Definice číselné tabulky úloh|61|1
|Úkol|70|9
|Poznámky k úkolu|71| 1 na záznam úkolu
|Opakující se úkol|72| 1 na záznam úkolu
|Přiřazení zdrojů|75| 100 za záznam úkolu
|Přiřazení Pole pracovní skupiny|76| 1 na záznam o zadání
|Názvy projektů|80|500
|DDE a propojení klienta OLE|81|500
|Komentáře|0|neomezeno

### Struktura souboru ###

Soubor MPX se skládá z výše uvedených záznamů, které jsou uvnitř souboru uspořádány přednastaveným způsobem. Podrobnosti o těchto typech záznamů jsou diskutovány následovně:

**Záznam o vytvoření souboru (FCR):** Toto je povinný záznam, jehož účelem je identifikovat:

* Formát souboru (MPX)
* Znak oddělovače seznamu použitý v souboru
* Program a číslo verze použité k vytvoření souboru
* Číslo verze formátu souboru MPX použitého v souboru
* Kódová stránka použitá k vytvoření souboru

Toto musí být první záznam v souboru. Při exportu z aplikace Microsoft Project je znak oddělovače seznamu určen v položce Místní nastavení v Ovládacích panelech systému Windows. Záznam FCR obsahuje následující pole:

* MPX následované bezprostředně znakem oddělovače seznamu
* Název/identifikátor programu
* Číslo verze souboru
* Kódová stránka (850, 437, MAC, ANSI)

Záznam může například obsahovat informaci **MPX, Microsoft Project, 3.0**, která určuje, že se v tomto souboru MPX jako oddělovací znak seznamu použije čárka. Verze formátu MPX použitá v souboru je exportována z aplikace Microsoft Project verze 3.0.

**Nastavení měny** Tento záznam, který má číslo záznamu 10, určuje nastavení pro možnosti měny v dialogovém okně Možnosti. Pokud tento záznam není zahrnut, použije se aktuální nastavení v dialogovém okně Možnosti. Oddělovače tisíců a desetinných míst se zadávají v položce Místní nastavení v Ovládacích panelech systému Windows.
Pole zahrnutá v tomto záznamu jsou:

* Symbol měny
* Pozice symbolu (0 # za, 1 # před, 2 # za s mezerou, 3 # před s mezerou)
* Číslice měny (0,1,2)
* Oddělovač tisíců
* Desetinný oddělovač

**Příklad:** 10,$,1,2,",",.
Tento příklad uvádí, že hodnoty měny obsahují před sebou znak dolaru ($), že za desetinnou čárkou jsou zahrnuty dvě číslice, že se k oddělení tisíců používá čárka a jako desetinná čárka se používá tečka. Protože znak oddělovače seznamu je zahrnut v poli Oddělovač tisíců, je pole uzavřeno v uvozovkách.

**Výchozí nastavení:** Tento záznam, který má číslo záznamu 11, určuje nastavení výchozích možností v dialogovém okně Možnosti. Není-li doba trvání specifikována, je třeba nastavit výchozí jednotku trvání pro správné výpočty jednotek doby trvání. Pokud tento záznam není zahrnut, použije se aktuální nastavení v dialogovém okně Možnosti.
Pole zahrnutá v tomto záznamu jsou:

* Výchozí jednotky trvání (0 # minut, 1 # hodin, 2 # dnů, 3 # týdnů)
* Výchozí typ trvání (0 # nepevné, 1 # pevné)
* Výchozí pracovní jednotky (0 # minut, 1 # hodin, 2 # dnů, 3 # týdnů)
* Výchozí hodiny/den
* Výchozí hodiny/týden
* Výchozí standardní sazba
* Výchozí sazba přesčasů
* Aktualizace stavu úlohy Aktualizace stavu zdroje (0 # ne, 1 # ano)
* Rozdělit probíhající úkoly (0 # ne, 1 # ano)

**Nastavení data a času:** Tento záznam, který má číslo záznamu 12, určuje nastavení pro možnosti data a času v dialogovém okně Možnosti a volbu Formát data pruhového textu v dialogovém okně Rozvržení. Pokud tento záznam není zahrnut, použije se aktuální nastavení v dialogovém okně Možnosti.
\\Pole zahrnutá v tomto záznamu jsou:

* Datum objednávky (0 # měsíc/den/rok, 1 # den/měsíc/rok, 2 # rok/měsíc/den)
* Formát času (0 # 12 hodin, 1 # 24 hodin)
* Výchozí čas (počet minut po půlnoci)
* Oddělovač data
* Časový oddělovač
* Text od 0:00 do 11:59
* Text od 12:00 do 23:59
* Formát data (0-14)*
* Formát data pruhového textu (0-194)*

**Definice základního kalendáře:** Tyto záznamy mající číslo záznamu 20 definují základní kalendáře a jejich pracovní a nepracovní dny v týdnu. Výchozí nastavení se použije, pokud pro den není žádný záznam. Výchozí nastavení jsou pondělí až pátek pro pracovní dny a sobota a neděle pro dny pracovního klidu. V tomto záznamu je pole Název povinné. Zadání 0 pro každý den znamená, že daný den je nepracovním dnem, a zadání 1 znamená, že daný den je pracovním dnem.
Pole zahrnutá v tomto záznamu jsou:

* Název
* Neděle
* pondělí
* úterý
* Středa
* Čtvrtek
* pátek
* Sobota

**Základní kalendářní hodiny:** Tyto záznamy se záznamem číslo 25 určují pracovní dobu pro dny v týdnu, pokud se liší od výchozího nastavení. Výchozí pracovní doba je 8:00 až 12:00 a 13:00 až 17:00 Každý záznam Základní kalendářní hodiny odkazuje na předchozí záznam Definice základního kalendáře. Za každým záznamem definice základního kalendáře může následovat až sedm těchto záznamů.

* Den v týdnu (1 - 7, kde 1 # neděle a 7 # sobota)
*Od času 1
*Do času 1
*Od času 2
*Do času 2
*Od času 3
*Do času 3

**Výjimka základního kalendáře:** Tyto záznamy s číslem záznamu 26 definují výjimky pro dny a hodiny specifikované v předchozích dvou typech záznamů. Za každým záznamem definice základního kalendáře může následovat až 250 těchto záznamů. Tyto záznamy musí být uvedeny v chronologickém pořadí. Pokud je výjimka jeden den, můžete pole Do data ponechat prázdné. Pokud nejsou uvedeny žádné časy, použijí se výchozí časy od 8:00 do 12:00 a od 13:00 do 17:00.
Pole zahrnutá v tomto záznamu jsou:

* Od data
* K datu
* Nepracující/pracovní (0 # nepracující, 1 # pracovní)
*Od času 1
*Do času 1
*Od času 2
*Do času 2
*Od času 3
*Do času 3

**Záhlaví projektu:** Tento záznam s hodnotou záznamu 30 nastavuje globální pole projektu, jako je datum zahájení projektu a datum ukončení projektu. Pole v tomto záznamu odpovídají informacím v dialogových oknech Informace o projektu a Statistiky.
Pole a karty zahrnuté v tomto záznamu jsou:

* Záložka Projekt
* Společnost
* Manažer
* Kalendář (standardně se používá, pokud není záznam)
* Datum zahájení (pro importovaný soubor se vypočítává buď toto pole, nebo následující pole, v závislosti na nastavení Plán od)
* Datum dokončení
* Plán od (0 # začátek, 1 # konec)
* Dnešní datum*
* Komentáře
* Náklady
* Základní náklady
* Aktuální cena
* Práce
* Základní práce
* Skutečná práce
* Práce
* Doba trvání*
* Základní trvání*
* Skutečná doba trvání
* Procento dokončeno
* Začátek základní linie
* Dokončení základní linie
* Skutečný začátek
* Skutečné dokončení
* Start Variance
* Dokončit odchylku
* Předmět
* Autor
* Klíčová slova

**Definice tabulky textových zdrojů**: Tento záznam uvádí seznam polí zdrojů v pořadí, která jsou importována nebo exportována. U importovaných souborů se názvy musí shodovat s názvy polí použitými v aplikaci Microsoft Project. U exportovaných souborů tento záznam pochází z tabulky exportu prostředku. Musí být použit buď tento záznam, nebo záznam Numeric Resource Table Definition. Při exportu z aplikace Microsoft Project jsou zahrnuty oba tyto záznamy.

**Definice číselné tabulky zdrojů:** Tento záznam používá čísla místo názvů a uvádí seznam polí zdrojů v pořadí, která jsou importována nebo exportována. Toto je alternativní metoda pro identifikaci polí prostředků obsažených v každém záznamu prostředku a je užitečná při definování souboru MPX vytvořeného cizojazyčným produktem.

**Zdroj:** Tyto záznamy obsahují informace o každém importovaném nebo exportovaném zdroji. Každý záznam zdroje popisuje jeden zdroj. Při importu informací jsou zahrnutá pole definována záznamem Definice tabulky zdrojů textu nebo záznamem Definice tabulky numerických zdrojů. Při exportu informací jsou zahrnuta pole uvedená v tabulce Export zdroje.

**Poznámky ke zdrojům:** Tyto záznamy obsahují poznámky o bezprostředně předcházejícím záznamu o zdroji. Pro nový řádek v poznámce se použije znak ASCII 127. Pokud poznámka obsahuje znak oddělovače seznamu, uzavřete poznámku do uvozovek.

**Definice kalendáře zdrojů:** Tyto záznamy definují pracovní dny pro zdroj uvedený v bezprostředně předcházejícím záznamu zdroje. Pokud pro importované soubory neexistuje žádná položka pro pole Název základního kalendáře, použije se Standardní. Žádný záznam pro konkrétní den znamená, že den je nastaven jako výchozí (2). Pokud neexistují žádné záznamy Definice kalendáře zdrojů, jako základní kalendář pro zdroj se použije Standardní, přičemž pro dny se použije výchozí. Pro každý den hodnota 0 znamená, že den je nepracovním dnem, 1 znamená, že den je pracovním dnem, a 2 určuje, že je použito výchozí nastavení.

**Hodiny kalendáře zdrojů:** Tyto záznamy definují pracovní dobu zdroje, která se liší od základního kalendáře používaného zdrojem. Tyto záznamy platí pro záznam Definice kalendáře zdrojů bezprostředně předcházející tomuto záznamu. Za každým záznamem definice kalendáře zdrojů může následovat až sedm těchto záznamů.

**Výjimka kalendáře zdrojů:** Tyto záznamy definují výjimky pro dny a hodiny specifikované v předchozích dvou typech záznamů. Za každým záznamem definice kalendáře zdrojů může následovat až 250 těchto záznamů. Tyto záznamy musí být uvedeny v chronologickém pořadí. Pokud je výjimka pouze jeden den, můžete pole Do data ponechat prázdné. Pokud nejsou uvedeny žádné časy, použijí se výchozí časy od 8:00 do 12:00 a od 13:00 do 17:00.

**Textová definice tabulky úkolů:** Tento záznam uvádí seznam polí úkolů v pořadí, která se importují nebo exportují. U importovaných souborů se názvy musí shodovat s názvy polí použitými v aplikaci Microsoft Project. Pokud je soubor exportován, pochází tento záznam z tabulky Export úlohy. Při exportu z aplikace Microsoft Project jsou zahrnuty oba tyto záznamy. Pole vypočítaná aplikací Microsoft Project, jako je například Plánované spuštění a Plánované dokončení, jsou při importu ignorována. Pokud máte pevně stanovená data zahájení nebo ukončení úkolu, použijte pole Typ omezení a Datum omezení.

**Definice číselné tabulky úkolů:** Tento záznam používá čísla namísto názvů a uvádí seznam polí úkolů v pořadí, která jsou importována nebo exportována. Jedná se o alternativní metodu identifikace polí úlohy obsažených v každém záznamu úlohy a je užitečná při definování souboru MPX vytvořeného cizojazyčným produktem.

**Úkol:** Tyto záznamy obsahují informace pro každý importovaný nebo exportovaný úkol. Každý záznam úkolu popisuje jeden úkol. Při importu informací jsou zahrnutá pole definována záznamem Definice tabulky textových úloh nebo záznamem Definice tabulky číselných úloh. Při exportu informací jsou zahrnuta pole uvedená v tabulce Export úlohy.

**Poznámky k úkolu:** Tyto záznamy obsahují poznámky k bezprostředně předcházejícímu záznamu úkolu. Použijte znak ASCII 127 k označení nového řádku v poznámce. Pokud poznámka obsahuje znak oddělovače seznamu, uzavřete poznámku do uvozovek.

**Přiřazení zdrojů**: Tyto záznamy obsahují informace o zdrojích přiřazených k úkolu, který byl definován v předchozím záznamu úkolu. Pokud slučujete soubory a chcete zachovat informace o přiřazení prostředků, musíte tyto informace zahrnout do souboru MPX. Pokud sloučíte, všechna existující přiřazení ke sloučeným úkolům budou odstraněna. Pokud slučujete soubory na základě jedinečných ID, prostředky se přiřazují pomocí jedinečných ID prostředků, nikoli pomocí ID.

**Pole pracovní skupiny přiřazení zdrojů:** Tyto záznamy obsahují informace, které jsou uloženy s každým přiřazením pro funkce Workgroup aplikace Microsoft Project 4.0 a 4.1. Pokud používáte funkce Workgroup, musíte tento záznam zahrnout, abyste zajistili, že žádná z informací nebude ztracena.

**Názvy projektů:** Tyto záznamy obsahují seznam všech názvů propojení DDE uložených v projektu.

**DDE a OLE Client Links:** Tyto záznamy obsahují seznam odkazů DDE do projektu.

**Komentáře:** Tyto záznamy lze použít k přidání komentářů k souboru a mohou se objevit na libovolné pozici v souboru. Každý záznam komentářů musí začínat „0“.

## Problémy s otevřením souboru MPX ##

Zde je seznam některých běžných problémů, které mohou nastat a způsobit nesprávné fungování formátu MPX:

* Absence podpůrného softwaru
* Poškozený soubor
* Soubor infikovaný virem
* Žádné přístupové právo v systému k otevření souborů
* Zastaralá jednotka ve vašem systému
* Přípona souboru je přejmenována

## Reference ##

* [MPX – Microsoft Knowledge Base](https://support.microsoft.com/en-us/office/file-formats-supported-by-project-desktop-face808f-77ab-4fce-9353-14144ba1b9ae)

