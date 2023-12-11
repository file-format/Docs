{
"dátum":"2023-11-01",
   "keywords":[
"simogatás",
"pat file",
"pat diskstation manager telepítőfájl",
"hogyan lehet megnyitni egy pat fájlt",
"fájl",
"pat fájl kiterjesztése",
"kiterjesztés",
"fájl"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft":"false",
"toc":true,
"title":"PAT fájlformátum - DiskStation Manager telepítőfájl",
   "description":"További információ a PAT DiskStation Manager telepítési fájlformátumáról és az API-król, amelyek PAT fájlokat hozhatnak létre és nyithatnak meg.",
   "linktitle":"PAT",
   "menu":{
      "docs":{
         "identifier":"system-pat-diskstation",
         "parent":"system"
}
},
"lastmod":"2023-11-01"
}

## Mi az a PAT fájl?

A PAT fájlokat általában a **DiskStation Manager (DSM)** operációs rendszerhez társítják, amely a Synology Network-Attached Storage (NAS) eszközök által használt operációs rendszer. A PAT-fájl egy telepítőfájl, amely a DSM-nek a Synology NAS-on történő frissítésére vagy telepítésére szolgál.

## PAT fájl használata

Általában a következőképpen használ PAT fájlt a DSM telepítéséhez vagy frissítéséhez a Synology NAS rendszeren:

1. Töltse le a PAT fájlt: A PAT fájlt a Synology hivatalos webhelyéről vagy más megbízható forrásból szerezheti be.
    







2. Jelentkezzen be a NAS-ba: Nyissa meg Synology NAS-ja webalapú felhasználói felületét az IP-cím webböngészőben történő megadásával. A művelet végrehajtásához rendszergazdai jogosultságra lesz szüksége.
    







3. Lépjen a Csomagközpontba: A webes felületen lépjen a "Csomagközpont" elemre. Itt kezelheti és telepítheti az alkalmazásokat a NAS-on.
    







4. Kézi telepítés: A Package Centerben a „Kézi telepítés” vagy a „Telepítés/Frissítés” opciónak kell lennie a használt DSM verziótól függően. Válassza ezt a lehetőséget.
    







5. Keresse meg a PAT fájlt: A rendszer felkéri, hogy böngésszen a helyi fájlok között, és válassza ki a letöltött PAT fájlt.
    







6. Telepítés vagy frissítés: A PAT fájl kiválasztása után kövesse a képernyőn megjelenő utasításokat a DSM telepítéséhez (ha friss telepítésről van szó), vagy frissítse a DSM-et (ha újabb verzióra frissít).
    







7. Várja meg a befejezést: A telepítési vagy frissítési folyamat eltarthat egy ideig, és a NAS újraindulhat a folyamat részeként. Légy türelmes, és várja meg, amíg véget ér.
    







8. Telepítés utáni konfiguráció: A telepítés vagy frissítés után szükség lehet a NAS-beállítások beállítására.

## DiskStation Manager

A DiskStation Manager, amelyet gyakran DSM-nek is neveznek, a Synology által a hálózathoz csatolt tárolóeszközeihez (NAS) fejlesztett operációs rendszer. Felügyeleti és vezérlőfelületként szolgál a Synology NAS szerverekhez. A DiskStation Manager felhasználóbarát webalapú felületet biztosít, amely lehetővé teszi a felhasználók számára, hogy konfigurálják és kezeljék NAS-juk különféle aspektusait, például adattárolást, fájlmegosztást, biztonsági mentési megoldásokat, multimédiás szolgáltatásokat és még sok mást.

A DSM sokoldalúságáról és kiterjedt csomag-ökoszisztémájáról ismert, amely lehetővé teszi a felhasználók számára, hogy különféle alkalmazásokat és szolgáltatásokat telepítsenek és futtassanak Synology NAS-jukon, így otthoni és üzleti használatra egyaránt alkalmas, többcélú szerverré alakítják. A DiskStation Manager néhány gyakori funkciója közé tartozik a fájlmegosztás, az adatok biztonsági mentése és szinkronizálása, a média streaming, a biztonsági szolgáltatások és a virtualizáció támogatása.

A Synology rendszeresen ad ki frissítéseket és új DSM-verziókat a biztonság, a teljesítmény és a funkciók javítása érdekében. A felhasználók manuálisan frissíthetik a DSM-et PAT-fájlok segítségével, vagy beállíthatják az automatikus frissítéseket, hogy biztosítsák, hogy NAS-juk a DiskStation Manager legújabb és legbiztonságosabb verzióját futtassa.

## PAT fájl megnyitása

A DiskStation Manager kézi frissítéséhez használhat egy PAT-fájlt, amelyet a Synology letöltőközpontból töltött le a következő lépésekkel:

1. Nyissa meg a DiskStation Manager Vezérlőpultját.
2. Navigáljon a „Frissítés és visszaállítás” szakaszhoz, és válassza a „DSM frissítés” lehetőséget.
3. Innen válassza a "Manuális DSM frissítés" lehetőséget.
4. Kattintson a "Tallózás" gombra, majd keresse meg és válassza ki a letöltött PAT fájlt.
5. A DiskStation Manager frissítésének elindításához kattintson az "Alkalmaz" gombra.

## Hivatkozások
* [Synology](https://en.wikipedia.org/wiki/Synology)
