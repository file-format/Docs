{
  "date" : "2021-06-24",
  "keywords" :[ "bat fájl", "mi a bat fájl", "fájl", "bat fájl példa", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"További információ a BAT fájlformátumról és az API-król, amelyek BAT fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"BAT - Batch File Format",
  "linktitle" : "BAT",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-24"
}

## Mi az a BAT fájl?
A BAT-fájlt kötegelt fájlnak nevezik, amely a DOS-szal és a Windows összes verziójával cmd.exe alatt fut. Ez egyszerű szöveges sorparancsok sorozatából áll, amelyeket a parancssori értelmező hajt végre különböző feladatok végrehajtásához, például karbantartó segédprogramok futtatásához a Windows rendszeren belül vagy tipikus programok indításához. A kötegfájl bármilyen parancsot tartalmazhat, amelyet az értelmező interaktívan el tud fogadni, és olyan kódstruktúrát használhat, amely lehetővé teszi a kötegfájlba írt feltételes elágazást és hurkot.
## BAT fájlformátum
A BAT fájlformátum egyszerűen egy szkript, amely az ismétlődő parancssorozatok automatizálására szolgál. A "kötegelt" kifejezést a kötegelt feldolgozásra használják, ez "nem interaktív végrehajtásnak" tekinthető. Ezért előfordulhat, hogy egy kötegfájl nem dolgoz fel több adatból álló köteget. A régi lemez operációs rendszerben (DOS) a kötegfájl a parancssori felület alatt futott a fájlnév és a .bat kiterjesztéssel. A korábbi Microsoft grafikus interfész alapú operációs rendszer, mint például a Microsoft Windows, DOS-függő volt. A felhasználóknak DOS-t kellett használniuk olyan tipikus műveletek végrehajtásához, mint a Windows javítása, optimalizálása vagy újratelepítése. Később a Microsoft bevezette a Windows NT-t, amely nem függött a DOS operációs rendszertől. Ezért a kötegfájlok futtathatók Command Prompt vagy **cmd.exe** használatával a modern Microsoft operációs rendszerekben.
### Batch fájl paraméterei
A parancssor számos speciális változót támogat, például a **%0, %1-től %9**-ig, hogy hivatkozzon a kötegelt job nevére és elérési útjára, valamint a kötegelt jobon belüli kilenc hívási paraméterre. A nem létező paramétereket nulla hosszúságú karakterlánc helyettesíti. Bár a környezeti változókhoz hasonlóan használhatók, de nincsenek elmentve a környezetben. A Microsoft és az IBM ezeket a változókat helyettesítő paramétereknek nevezi, míg a Novell, a Digital Research és a Caldera bevezette a helyettesítő változók kifejezést rájuk.

Íme néhány hasznos Batch fájl parancs:
| Parancs | Leírás |
------|------------|
| VER | Ez a köteg parancs megmutatja az MS-DOS Ön által használt verzióját. |
|ASSOC| Ez egy kötegelt parancs, amely egy kiterjesztést fájltípushoz (FTYPE) társít, megjeleníti a meglévő társításokat, vagy töröl egy társítást. |
|CD| Ez a köteg parancs segít megváltoztatni egy másik könyvtárat, vagy megjeleníti az aktuális könyvtárat. |
|CLS| Ez a köteg parancs törli a képernyőt. |
|MÁSOLÁS| Ez a köteg parancs a fájlok egyik helyről a másikra másolására szolgál. |
|DEL| Ez a köteg parancs fájlokat és nem könyvtárakat töröl. |
|DIR| Ez a köteg parancs egy könyvtár tartalmát listázza ki. |
|DÁTUM| Ez a köteg parancs segít megtalálni a rendszerdátumot. |
|ECHO| Ez a kötegelt parancs üzeneteket jelenít meg, vagy be- vagy kikapcsolja a parancsvisszhangot. |
|KILÉPÉS| Ez a batch parancs kilép a DOS-konzolból. |
|MD| Ez a köteg parancs egy új könyvtárat hoz létre az aktuális helyen. |
|MOVE| Ez a kötegelt parancs fájlokat vagy könyvtárakat mozgat a könyvtárak között. |
|PATH| Ez a köteg parancs megjeleníti vagy beállítja az elérési út változót. |
|SZÜNET| Ez a kötegelt parancs kéri a felhasználót, és megvárja, amíg a bemeneti sort be kell írni. |
|PROMPT| Ezzel a kötegelt paranccsal módosíthatja vagy visszaállíthatja a cmd.exe parancssort. |
|RD| Ez a kötegelt parancs eltávolítja a könyvtárakat, de a könyvtáraknak üresnek kell lenniük az eltávolításuk előtt. |
|REN| Fájlok és könyvtárak átnevezése |
|REM| Ez a köteg parancs a kötegfájlokban lévő megjegyzésekhez használatos, megakadályozva a megjegyzés tartalmának végrehajtását. |
|START| Ez a kötegelt parancs elindít egy programot új ablakban, vagy megnyit egy dokumentumot. |
|IDŐ| Ez a köteg parancs beállítja vagy megjeleníti az időt. |
|TÍPUS| Ez a köteg parancs egy fájl vagy fájlok tartalmát nyomtatja ki a kimenetre. |
|VOL| Ez a köteg parancs megjeleníti a kötetcímkéket. |
|ATTRIB| Megjeleníti vagy beállítja az aktuális könyvtárban lévő fájlok attribútumait |
|CHKDSK| Ez a batch parancs ellenőrzi a lemezt, hogy nincs-e probléma. |
|VÁLASZTÁS| Ez a batch parancs opciók listáját kínálja a felhasználónak. |
|CMD| Ez a kötegelt parancs a parancssor egy másik példányát hívja meg. |
|COMP| Ez a köteg parancs 2 fájlt hasonlít össze a fájlméret alapján. |
|KONVERTÁLÁS| Ez a kötegelt parancs a kötetet FAT16 vagy FAT32 fájlrendszerről NTFS fájlrendszerre konvertálja. |
|DRIVERQUERY| Ez a kötegelt parancs megjeleníti az összes telepített eszközillesztőt és azok tulajdonságait. |
|BŐVÍTÉS| Ez a kötegelt parancs kicsomagolja a fájlokat a tömörített .cab kabinetfájlokból. |
|KERESÉS| Ez a köteg parancs egy karakterláncot keres a fájlokban vagy a bemenetben, és megfelelő sorokat ad ki. |
|FORMAT| Ez a kötegelt parancs formázza a lemezt a Windows által támogatott fájlrendszer (például FAT, FAT32 vagy NTFS) használatára, ezáltal felülírja a lemez korábbi tartalmát. |
|SEGÍTSÉG| Ez a kötegelt parancs a Windows által biztosított parancsok listáját jeleníti meg. |
|IPCONFIG| Ez a köteg parancs megjeleníti a Windows IP-konfigurációját. Megjeleníti a kapcsolat szerinti konfigurációt és a kapcsolat nevét. |
|LABEL| Ez a kötegelt parancs lemezcímkét ad hozzá, beállít vagy eltávolít. |
|TOVÁBBI| Ez a kötegelt parancs a fájl vagy fájlok tartalmát jeleníti meg, egyenként képernyőnként. |
|NET| Különféle hálózati szolgáltatásokat nyújt a használt parancstól függően. |
|PING| Ez a kötegelt parancs ICMP/IP "visszhang" csomagokat küld a hálózaton keresztül a megadott címre. |
|LEÁLLÍTÁS| Ez a kötegelt parancs leállítja a számítógépet, vagy kijelentkezteti az aktuális felhasználót. |
|RENDEZÉS| Ez a batch parancs átveszi a bemenetet egy forrásfájlból, és ábécé sorrendbe rendezi a tartalmát, A-tól Z-ig vagy Z-től A-ig. A kimenetet a konzolra nyomtatja. |
|SUBST| Ez a kötegelt parancs meghajtóbetűjelet rendel egy helyi mappához, megjeleníti az aktuális hozzárendeléseket, vagy eltávolít egy hozzárendelést. |
|SYSTEMINFO| Ez a kötegelt parancs a számítógép és operációs rendszerének konfigurációját mutatja. |
|TASKKILL| Ez a köteg parancs egy vagy több feladatot lezár. |
|FELADATLISTA| Ez a köteg parancs felsorolja a feladatokat, beleértve a feladat nevét és a folyamatazonosítót (PID). |
|XCOPY| Ez a kötegelt parancs fejlettebb módon másolja a fájlokat és könyvtárakat. |
|FA| Ez a kötegelt parancs megjeleníti az aktuális könyvtár összes alkönyvtárának fát, bármilyen rekurziós vagy mélységű szinten. |
|FC |Ez a köteg parancs felsorolja a tényleges különbségeket két fájl között. |
|DISKPART |Ez a batch parancs megjeleníti és konfigurálja a lemezpartíciók tulajdonságait. |
|TITLE |Ez a köteg parancs beállítja a konzolablakban megjelenő címet. |
|SET | Megjeleníti a környezeti változók listáját az aktuális rendszeren. |

## BAT fájl példa
A kötegelt szkripteket általában egyszerű szövegfájlként menti a rendszer; parancsokat tartalmaz, amelyek sorozatban hajtódnak végre. Ezek a fájlok .bat kiterjesztéssel kerülnek mentésre; felismerése és végrehajtása a **Command Interpreter** szoftverrel. Ez a szoftver natívan elérhető a Microsoft Windows rendszerben **cmd.exe** néven.

Íme egy minta Batch Script, amely törli az összes fájlt az aktuális könyvtárban:
```
:: Deletes All files in the Current Directory With Prompts and Warnings
::(Hidden, System, and Read-Only Files are Not Affected)
:: @ECHO OFF
DEL . DR
```


## Hivatkozások

* [Batch Script – Gyors útmutató](https://www.tutorialspoint.com/batch_script/batch_script_quick_guide.htm)
* [Batch fájl – a Wikipewdia által](https://en.wikipedia.org/wiki/Batch_file)

