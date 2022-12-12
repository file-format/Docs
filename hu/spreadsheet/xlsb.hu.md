{
  "date" : "2019-12-10",
  "keywords" :[ "XLSB", "file", "extension", "file format", "Excel Binary Spreadsheet File" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"A fájlformátum útmutatója, hogy megtudja, mi az XLSB fájl és API-k, amelyek létrehozhatják és megnyithatják azokat.",
  "title" :"What is an XLSB file?",
  "linktitle" : "XLSB",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Mi az XLSB fájl?

Az XLSB fájlformátum az Excel bináris fájlformátumát határozza meg, amely az Excel-munkafüzet tartalmát meghatározó rekordok és struktúrák gyűjteménye. A tartalom tartalmazhat strukturálatlan vagy félig strukturált számtáblázatokat, szöveget, vagy számokat és szöveget egyaránt, képleteket, külső adatkapcsolatokat, diagramokat és képeket. Az [XLSX](/hu/spreadsheet/xlsx/)-től eltérően (amely Open XML fájlformátumon alapul), az XLSB bináris Excel-munkafüzetfájlt képvisel. Az XLSB fájlok gyorsabban olvashatók és írhatók, ami hasznossá teszi őket a nagy fájlokkal való munkavégzéshez. Az XLSB-t ritkán használják munkafüzetek tárolására, mivel az XLSX (és korábban az [XLS](/hu/spreadsheet/xls/)) volt a felhasználók által leggyakrabban kiválasztott fájlformátum a munkafüzetek mentésére. Megnyitható a Microsoft Office 2007 és újabb verzióival.

## XLSB fájlformátum specifikációi ##

Az XLSB fájlformátum fájlformátum-specifikációi 2008-ban 1.0-s verzióként kerültek nyilvánosságra. Azóta a specifikációkat többször felülvizsgálták, és a specifikációk legújabb verzióját (10.0-s verzió) 2018 áprilisában tették közzé. A specifikációkat a Microsoft nyilvánosan [[MS-XLSB] - Excel Binary File Format specifikációk] (https:/ /msdn.microsoft.com/en-us/library/cc313133(v#office.12).aspx), és bárkinek konzultálnia kell vele, ha XLSB fájlformátumú fájlokat olvas vagy ír.

## XLSB fájlstruktúra ##

Az XLSB fájl egy olyan csomag, amely részek gyűjteményéből áll. Ezek a részek információkat tartalmaznak a munkafüzet tartalmáról, beleértve a munkafüzet adatait és a csomag szerkezetét. Egyes részek bináris rekordok használatával tárolt információkat tartalmaznak, mások XML-ként, míg mások bájtok bináris adatfolyamaként tárolják az információkat. Minden bináris rekord nulla vagy több strukturált mezőt tartalmaz, amelyek a munkafüzet adatait tartalmazzák.

#### Csomag ####

Az XLSB-csomag egy [ZIP](/hu/compression/zip/) archívum, amelynek pontosan egy munkafüzetrészt kell tartalmaznia. Ennek a résznek egy kapcsolat célpontja kell, hogy legyen ebben a csomagkapcsolati részben. A munkafüzet rész az XLSB dokumentum kezdő része.

#### Rész ####

A rész egy bájtok folyama, amelyhez hozzárendelt tartalomtípus tartozik, amely meghatározza az alkatrészben tárolt tartalom jellegét és típusát. Egyes részek bináris formátumban, míg mások XML-ben tárolják az információkat. A specifikációs dokumentum [alkatrészek felsorolása](https://msdn.microsoft.com/en-us/library/dd924091(v#office.12).aspx) szakasza felsorolja az érvényes részeket, tartalomtípusokat és kötelező/opcionális kapcsolatokat minden alkatrész egy csomagban.

#### Kapcsolat ####

A forrást és a célerőforrást kapcsolat köti össze. A kapcsolatok lehetnek:

**Csomagkapcsolat:** ahol a cél egy rész, a forrás pedig a csomag mint egész

**Rész-alkatrész kapcsolat:** ahol a cél egy része, a forrás pedig egy része a csomagban

**Explicit kapcsolat:** ahol egy erőforrás a forrásrész tartalmából hivatkozik egy kapcsolatelem ID attribútumértékére hivatkozva

Az **implicit kapcsolat** olyan kapcsolat, amely nem explicit

**Belső kapcsolat:** ahol a cél a csomag része

**Külső kapcsolat:** ahol a cél a csomagban nem szereplő külső erőforrás

#### Rekord ####

A rekord az alapvető építőelem, amely a munkafüzet jellemzőivel kapcsolatos információk tárolására szolgál. Minden bináris rekord egy változó hosszúságú bájtsorozat. A bináris rekord három összetevőből áll:

* egy rekordtípus
* rekordméretű, és
* az adott rekordtípusra jellemző rekordadatok.

**Rekordtípus:** A rekordtípus a rekord által megadott rekordtípust mutatja. Meghatározza továbbá az erre a rekordra jellemző rekordadatok szerkezetét. Az érvényes rekordtípusok a specifikációs dokumentum [Record Enumeration](https://msdn.microsoft.com/en-us/library/dd953057(v#office.12).aspx) szakaszában találhatók. A rekordtípusnak egy vagy két bájtosnak kell lennie, és 128-nál nagyobb vagy egyenlőnek, és 16384-nél kisebbnek kell lennie.

**Rekordméret:** A rekordméret a bájtok számát adja meg, amely a rekordadatok teljes méretét határozza meg. Ennek az értéknek egytől négy bájtig KELL lennie. Ennek az értéknek egy bájtnak KELL lennie, ha az alacsony bájt magas bitje 0; ellenkező esetben ennek az értéknek egy bájtnál nagyobbnak KELL lennie. Ha a bájtok száma nagyobb, mint egy bájt, az egyes egymást követő bájtok magas bitje határozza meg, hogy használ-e további bájtot. Ha a második bájt felső bitje 1, akkor ennek az értéknek egy további harmadik bájtot KELL használni. Ha a harmadik bájt felső bitje 1, akkor ennek az értéknek egy további negyedik bájtot KELL használni. A negyedik bájt magas bitjét figyelmen kívül kell hagyni. Az érték az egyes bájtok hét alacsony bitjéből áll össze. Az alacsony, legkisebb jelentőségű bitek az első bájton belül vannak, és minden egymást követő bájt magasabb rendű biteket tartalmaz, mint az előző bájt.

**Rekordadatok:** A rekord adatkomponens olyan mezőket tartalmaz, amelyek egy adott rekordtípusnak felelnek meg, és a rekord többi részét alkotják. Az adott rekordtípus mezőinek sorrendje és szerkezete, amely a Rekordfelsorolásban szerepel, az adott rekordtípus megfelelő szakaszában van megadva a Rekordok alkalmazásban. A rekord adatösszetevő teljes méretének meg kell egyeznie a rekord méretével. A rekord adatkomponens mezői tartalmazhatnak egyszerű értékeket, értéktömböket, több mező struktúráit, mezőtömböket és struktúratömböket.

#### XLSB rekordpélda ####

A következő rekordtípus és rekordméret ad meg egy **BrtCommentText** rekordot, amelynek mérete 200 bájt:

11111101 00000100 11001000 00000001 [Record Fields]

Az első bájt 11111101, amely alacsony értéket ad meg, 125, és a rekordtípushoz egy második bájt szükséges. A második bájt a 00000100, amely 4 * 128 magas értéket ad meg, ami 512-nek felel meg. A rekordtípus értéke 125 + 512 vagy 637, ami egy **BrtCommentText** rekordtípusnak felel meg. A következő bájt az 11001000, ami 72-es alacsony értéket ad meg, és a rekordmérethez egy második bájt szükséges. A második bájt a 00000001, amely magasabb értéket ad meg, 1 * 128, és hogy a rekordméret nem igényel további bájtot. A rekord mérete 72 + 128 vagy 200, amely a rekord adatkomponensének teljes méretét adja meg bájtban. A rekord adatkomponens mezőit a **BrtCommentText** határozza meg.

## Hivatkozások ##

* [[MS-XLSB] – Excel (.xlsb) bináris fájlformátum](https://msdn.microsoft.com/en-us/library/cc313133(v#office.12).aspx)

