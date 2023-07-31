{
  "date" : "2021-06-21",
  "keywords" :[ "UDL", "extension", "udl file", "udl file format", "Database File Type", "Database File Format", "What is a udl file" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"További információ az UDL fájlformátumról és az API-król, amelyek UDL fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"UDL – Microsoft Universal Data Link File",
  "linktitle" : "UDL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-06-21"
}

## Mi az UDL fájl?
Az .udl kiterjesztésű fájl neve Microsoft Universal Data Link fájl; kapcsolati attribútumok megadása; a Windows-alkalmazások használják az adatbázissal való kapcsolat létrehozására. Az UDL fájl tartalmazza az OLE DB adatforrás kapcsolódási karakterláncát; felhasználónévvel és jelszóval, valamint alapvető kapcsolati karakterlánc-tulajdonságokkal. A tulajdonságok közvetlen kézi megadásának elkerülése érdekében egy kapcsolati karakterláncban, alternatívaként egy Adatkapcsolat tulajdonságai párbeszédpanel használható a kapcsolati információk .udl fájlba történő mentésére.

## UDL fájl formátum
Alapvetően az UDL (Universal Data Link) fájl egy egyszerű szöveges fájl, amely egy adott attribútumokkal vagy tulajdonságokkal rendelkező adatbázis-kapcsolati karakterláncból áll. Az UDL-fájl létrehozása után az SQL Server Management Studio segítségével tesztelhető a kapcsolat ellenőrzésére.

### Csatlakozási karakterlánc tulajdonságai
Az alábbi tulajdonságok állíthatók be az UDL-ben a megfelelő kapcsolat biztosítása érdekében:

- **Szerver neve**: a szerver helye, ahol az elérni kívánt adatbázis található.
- **Hitelesítési lehetőségek**
- **Windows-hitelesítés**: Hitelesítés az SQL Server felé a jelenleg bejelentkezett felhasználó Windows-fiókjának hitelesítő adataival.
- **SQL Server Authentication**: Hitelesítés bejelentkezési azonosítóval és jelszóval.
- **Active Directory – Integrált**: Integrált hitelesítés Azure Active Directory identitással; SQL Server Windows-hitelesítésére is használható.
- **Active Directory - Jelszó**: Felhasználói azonosító és jelszó hitelesítés Azure Active Directory identitással.
- **Active Directory - Univerzális MFA-támogatással**: Interaktív hitelesítés Azure Active Directory identitással.
- **Active Directory – egyszerű szolgáltatás**: Hitelesítés az Azure Active Directory egyszerű szolgáltatásával.
- **Szerver SPN**: Ha megbízható kapcsolatot használ, megadhat egy egyszerű szolgáltatásnevet (SPN) a kiszolgálóhoz.
- **Felhasználónév**: Írja be a hitelesítéshez használandó felhasználói azonosítót, amikor bejelentkezik az adatforrásba.
- **Jelszó**: Írja be a hitelesítéshez használandó jelszót, amikor bejelentkezik az adatforrásba.
- **Üres jelszó**: Ha be van jelölve, lehetővé teszi a megadott szolgáltató számára, hogy üres jelszót használjon a kapcsolati karakterláncban.
- **Jelszó mentésének engedélyezése**: Lehetővé teszi a jelszó mentését a kapcsolati karakterlánccal együtt.
- **Használjon erős titkosítást az adatokhoz**: a kapcsolaton keresztül továbbított adatok titkosítva lesznek.
- **Trust szerver tanúsítvány**: A szerver tanúsítványa érvényesítésre kerül.
- **Adatbázis**: Az elérni kívánt adatbázis neve.
- **Adatbázisfájl csatolása adatbázisnévként**: Megadja a csatolható adatbázis elsődleges fájljának nevét.

## Hivatkozások ##

* [Microsoft Data Access Components](https://en.wikipedia.org/wiki/Microsoft_Data_Access_Components#Universal_data_link)
* [Universal Data Link (UDL) konfiguráció](https://learn.microsoft.com/en-us/sql/connect/oledb/help-topics/data-link-pages?view=sql-server-ver15)

