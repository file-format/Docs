{
"date":"20.07.2023",
   "keywords":[
"ZÁSOBNÍK",
"Soubor BIN",
"soubor",
"Přípona souboru BIN",
"rozšíření",
"soubor"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft":"false",
"toc":true,
"title":"Formát souboru BIN - MacBinary Encoded File",
   "description":"Další informace o formátu BIN a rozhraních API, která mohou vytvářet a otevírat soubory BIN.",
"linktitle":"BIN",
   "menu":{
      "docs":{
         "identifier":"compression-bin",
         "parent":"compression"
}
},
"lastmod":"2023-07-20"
}

## Co je soubor BIN?

Soubor BIN může v kontextu počítačů Macintosh odkazovat na soubor uložený ve formátu MacBinary. MacBinary je formát souborů speciálně navržený pro přenos souborů Macintosh přes internet, e-mail, FTP nebo přenosná média. Účelem MacBinary je zachovat úplnou strukturu souborů a atributy souborů Macintosh, včetně větvení dat a větve prostředků, v rámci jednoho souboru.

Formát MacBinary toho dosahuje zapouzdřením větve prostředků a větve dat systému Macintosh Hierarchical File System (HFS) do komprimovaného souboru. Obsahuje také hlavičku vyhledávače, která obsahuje důležitá metadata o souboru. Spojením všech těchto komponent do jednoho souboru MacBinary zajišťuje, že si soubor zachová svou integritu a lze jej snadno přenášet a sdílet mezi různými platformami.

S pokrokem v souborových systémech a protokolech přenosu souborů společnosti Apple se používání souborů BIN a formátu MacBinary stalo méně běžným. Zavedení formátů souborů, jako je ZIP, a přechod na modernější souborové systémy, jako je HFS+ a APFS, snížily potřebu souborů kódovaných MacBinary. Tyto novější systémy souborů poskytují efektivnější způsoby zpracování atributů souborů, větví prostředků a větví dat, takže formát MacBinary je v dnešním prostředí výpočetní techniky méně potřebný.

## Formát souboru BIN – Další informace

V raných dobách počítačů Macintosh byly soubory kvůli datovým omezením ukládány do dvou samostatných „forků“. „Resource fork“ obsahoval strukturovaná data, zatímco „data fork“ obsahoval nestrukturovaná data. Zatímco klasický Mac OS zacházel s těmito vidlicemi jako s jedním souborem, přenos souborů do systémů jiných než Mac vedl ke ztrátě dat, protože tyto vidlice nerozpoznaly jako jednu entitu. Pro vyřešení tohoto problému vytvořili formát MacBinary jednotlivci jako Dennis Brothers, Harry Chesley a Yves Lempereur. MacBinary komprimoval a zkombinoval větve do jednoho souboru, známého jako soubor BIN, pro přenos do systémů jiných než Mac. Po návratu do Mac OS by se vidlice znovu oddělily. S přechodem od vidlicového HFS v roce 2000 výrazně pokleslo použití formátu MacBinary. Dnes je setkání se souborem BIN s kódováním MacBinary vzácné, pokud nenarazíte na starý soubor na jiném systému než Mac nebo si jej nestáhnete z internetu.

Formát MacBinary prošel postupem času několika verzemi, aby se přizpůsobil změnám v systémech Macintosh a manipulaci se soubory. Zde jsou některé z různých verzí formátu MacBinary:

- **MacBinary I:** Počáteční verze MacBinary, představená na konci 80. let. Kombinoval rozvětvení prostředků a datové rozvětvení do jediného binárního souboru, což umožňuje přenos souborů Macintosh mezi platformami.

- **MacBinary II:** Tato verze, vydaná na počátku 90. let, vylepšila původní formát MacBinary přidáním dalších informací, jako je typ souboru a kódy tvůrců, do záhlaví binárního souboru. Tyto kódy pomohly zachovat integritu a identifikaci souborů Macintosh během přenosu.

- **MacBinary III:** Formát MacBinary III, představený v polovině 90. let, dále vylepšil předchozí verze tím, že do záhlaví binárního souboru zahrnul další metadata, jako je název souboru a data vytvoření a úpravy souboru. To umožnilo komplexnější zachování atributů souborů Macintosh během přenosu.

- **MacBinary IV:** MacBinary IV byl vyvinut, aby řešil problémy s kompatibilitou se vznikajícím operačním systémem Mac OS X na počátku 21. století. Zahrnulo změny, které se přizpůsobily nové struktuře systému souborů a atributům zavedeným v systému Mac OS X.

## Jak otevřít soubor BIN?

Soubory MacBinary Encoded BIN lze otevřít pomocí různých komprimačních nástrojů. Pro uživatele macOS je vhodnou volbou **Apple Archive Utility**. Uživatelé Windows mohou využít software jako **Smith Micro StuffIt Deluxe** k extrahování obsahu souboru MacBinary Encoded BIN. Další možností pro uživatele macOS je **The Unarchiver**, což je všestranný nástroj schopný pracovat s více formáty souborů, včetně MacBinary.

Je důležité si uvědomit, že příponu souboru .bin používají různé formáty souborů, nejen MacBinary. Pokud tedy narazíte na soubor BIN, který nelze otevřít pomocí výše uvedených nástrojů, může být uložen v jiném formátu. V takových případech možná budete muset určit konkrétní formát souboru a použít vhodný software nebo nástroj určený pro tento formát, abyste získali přístup k obsahu souboru.

## Další soubory BIN

Zde jsou další typy souborů, které používají příponu souboru **.bin**.

- [BIN - soubor s obrázkem binárního disku](/cs/disc-and-media/bin/)
- [BIN - Unix Executable File](/cs/executable/bin/)
- [BIN - BlackBerry IT Policy File](/cs/settings/bin/)
- [BIN - Sega Genesis Game ROM](/cs/game/bin/)
- [BIN - Obrázek PSX PlayStation BIOS](/cs/hra/bin-pcsx/)

## Reference

* [MacBinary](https://en.wikipedia.org/wiki/MacBinary)

