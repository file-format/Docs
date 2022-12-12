{
  "date" : "2021-04-23",
  "keywords": [ "config File", "configuration files", "config File format", "extension", "format","git config file","Configuration files in Linux","what is a config file","Config file php", "ssh config file example", "aws config file example", "python config file example" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CONFIG - konfigurációs fájl",
  "description":"Tudjon meg többet a CONFIG fájlformátumról a CONFIG példával és az API-kkal, amelyek CONFIG fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "CONFIG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-23"
}

## Mi az a CONFIG fájl?
A CONFIG fájlt konfigurációs fájlnak nevezik; számos számítógépes szoftver paramétereinek és elsődleges beállításainak konfigurálására szolgál. Egyes szoftverek csak a **konfigurációs fájljaikat** olvassák be indításkor. Mások rendszeresen ellenőrzik a konfigurációs fájlok változásait.

## CONFIG Fájlformátum
A **CONFIG fájlformátum** kiszolgálói folyamatokhoz, szoftveralkalmazásokhoz és operációs rendszer beállításaihoz használatos. A programozó kódot írhat, hogy utasítsa a szoftvert, hogy bizonyos idő elteltével újra és újra olvassa el a konfigurációs fájlokat, és alkalmazza a változtatásokat az aktuális folyamatra. A CONFIG fájlrendszer-rendszerre vonatkozóan nincsenek határozott szabványok vagy szigorú konvenciók. Például a Microsoft Web.config fájlja a CONFIG fájlformátumhoz tartozik, amely [XML](https://docs.fileformat.com/web/xml/) alapú címkekészletekből áll; szerkeszthető Microsoft Visual Studio vagy bármilyen más szövegszerkesztővel.

## Példák konfigurációs fájlokra:
Mivel a konfigurációs fájlok nem szabályok, szabványok vagy konvenciók betartásával jönnek létre, előfordulhat, hogy ezek a fájlok különböző formátumokkal írhatók. A .config fájl XML, [JSON](https://docs.fileformat.com/web/json/) vagy bármilyen más formátumon alapulhat. A következő példák a jól ismert operációs rendszerek és szoftverek konfigurációs fájljaira:

### Konfigurációs fájlok Linux alatt
Minden Linux-program egy végrehajtható fájl, amely tartalmazza a **opcode-ok** listáját, amelyeket a CPU hajt végre a tipikus műveletek végrehajtása érdekében. Szinte minden program működése az Ön igényei szerint testreszabható a konfigurációs fájlok módosításával. A Linux rendszer számos konfigurációs fájlja az /etc könyvtárban található. A konfigurációs fájlok a következő kategóriákba sorolhatók:
|Kategória|Példa| Megjegyzések|
---|---|---|
|Fájlok elérése|/etc/host.conf|Megmondja a hálózati tartománykiszolgálónak, hogyan keresse ki a gazdagépneveket.|
|Indítás és bejelentkezés/kijelentkezés|/etc/rc.d/rc.local|Nem hivatalos. Meghívható az rc, rc.sysinit vagy /etc/inittab.| fájlokból
|Fájlrendszer|/etc/mtools.conf|Az összes művelet (mkdir, másolás, formátum stb.) beállítása DOS-típusú fájlrendszeren.|
|Rendszeradminisztráció|/etc/shells|Tartja a rendszer számára elérhető lehetséges „shell”-ek listáját.|
|Networking|/etc/gated.conf|A kapuzott konfigurációja. Csak a kapuzott démon használja.|
|Rendszerparancsok|/etc/logrotate.conf|A Dynamic Linker konfigurációja.|
|Daemons|/etc/httpd.conf|Az Apache, a webszerver konfigurációs fájlja. Ez a fájl általában nincs az /etc.| mappában
|Felhasználói programok| /etc/lynx.cfg| Proxy beállítások|
### AWS CONFIG fájl példa
A gyakran használt konfigurációs beállítások és hitelesítő adatok az AWS CLI által karbantartott CONFIG-fájlokba menthetők. A CONFIG fájlnak egyszerű szöveges fájlnak kell lennie, amely a következő formátumot használja:
```
[default]
region = us-west-2
output = json

[profile dev-user]
region = us-east-1
output = text

[profile developers]
role_arn = arn:aws:iam::123456789012:role/developers
source_profile = dev-user
region = us-west-2
output = json
```
### SSH CONFIG fájl példa
Az OpenSSH ügyféloldali konfigurációs fájl neve CONFIG, és az .ssh könyvtárban található. Az SSH CONFIG fájl a következő struktúrából áll:
```
Host hostname1
    SSH_OPTION value
    SSH_OPTION value

Host hostname2
    SSH_OPTION value

Host *
    SSH_OPTION value
```
### Python CONFIG fájl példa
Egy Python CONFIG fájl így nézhet ki:

```
#!/usr/bin/env python
import preprocessing

mysql = {
    "host": "localhost",
    "user": "root",
    "passwd": "my secret password",
    "db": "write-math",
}
preprocessing_queue = [
    preprocessing.scale_and_center,
    preprocessing.dot_reduction,
    preprocessing.connect_lines,
]
use_anonymous = True
```



## Hivatkozások

* [A Linux konfigurációs fájlok ismertetése](https://developer.ibm.com/technologies/linux/articles/l-config/)
* [A konfigurációs és hitelesítési fájl beállításai](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-files.html)
* [Konfigurációs fájlok Pythonban](https://martin-thoma.com/configuration-files-in-python/)

