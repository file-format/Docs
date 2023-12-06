{
"datum": "27.09.2023",
  "keywords": [
"cfg",
"cfg soubor",
"soubor připojení k serveru cfg citrix",
"co je soubor cfg",
"jak otevřít soubor cfg",
"soubor",
"přípona souboru cfg",
"rozšíření"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formát souboru CFG - soubor připojení serveru Citrix",
  "description":"Další informace o formátu CFG Citrix Server Connection File a rozhraní API, která mohou vytvářet a otevírat soubory CFG.",
"linktitle": "CFG Citrix",
  "menu": {
    "docs": {
      "identifier": "settings-cfg-citrix",
      "parent": "settings"
}
},
"lastmod": "27.09.2023"
}

## Co je soubor CFG?

Soubor CFG je také známý jako **Citrix Server Connection File**. Je to životně důležitá součást používaná pro navázání spojení se serverem Citrix. Tento soubor obsahuje základní informace nezbytné pro úspěšné spojení mezi klientským zařízením a serverem Citrix. Obvykle obsahuje podrobnosti, jako je název hostitele nebo IP adresa serveru, konkrétní port serveru, který se má použít, a přihlašovací údaje požadované pro ověření, které často zahrnují uživatelské jméno a heslo.

Tyto soubory CFG hrají klíčovou roli při konfiguraci klientského softwaru Citrix a umožňují uživatelům bezproblémové připojení k různým serverům Citrix. Fungují jako konfigurační soubory, které zjednodušují proces připojení předdefinováním základních parametrů, čímž snižují potřebu uživatelů ručně zadávat tyto informace pokaždé, když chtějí získat přístup k serveru Citrix.

## Server Citrix

Server Citrix, známý také jako Citrix XenApp nebo Citrix XenDesktop server, je specializovaný server používaný ve virtualizačních řešeních Citrix. Citrix je společnost, která poskytuje technologii pro vzdálený přístup, virtualizaci aplikací a virtualizaci desktopů. Servery Citrix hrají v těchto řešeních ústřední roli tím, že usnadňují poskytování aplikací a desktopových prostředí vzdáleným uživatelům nebo klientským zařízením.

Takto obvykle funguje server Citrix:

1. **Doručování aplikací a desktopů**: Servery Citrix hostí aplikace a desktopová prostředí. Místo spouštění softwaru přímo na zařízení uživatele běží aplikace nebo desktop na serveru Citrix a do klientského zařízení je přenášeno pouze uživatelské rozhraní. To umožňuje uživatelům přistupovat k aplikacím a desktopům Windows z široké řady zařízení, včetně počítačů PC, Mac, tabletů a chytrých telefonů.
    















2. **Vzdálený přístup**: Servery Citrix umožňují vzdálený přístup k aplikacím a desktopům, což uživatelům umožňuje pracovat odkudkoli s připojením k internetu. To je zvláště cenné pro vzdálené a distribuované týmy, protože poskytuje konzistentní a bezpečný počítačový zážitek.
    















3. **Vyrovnávání zátěže**: Servery Citrix často pracují v klastrech, aby vyrovnaly zatížení příchozích připojení. Vyvažování zátěže zajišťuje, že požadavky uživatelů jsou distribuovány rovnoměrně mezi servery, čímž se optimalizuje výkon a dostupnost.

## Soubor připojení serveru Citrix

Soubor připojení serveru Citrix, často označovaný jako soubor CFG, je konfigurační soubor používaný v prostředích Citrix k navázání spojení mezi klientskými zařízeními a servery Citrix. Klíčové podrobnosti obvykle zahrnuté v souboru připojení serveru Citrix mohou zahrnovat:

1. **Název hostitele nebo IP adresa**: Toto určuje síťové umístění serveru Citrix, ke kterému se má klientské zařízení připojit. Identifikuje, kde jsou zdroje Citrix hostovány.
    















2. **Port serveru**: Číslo portu používaného pro komunikaci se serverem Citrix. Tím je zajištěno, že data jsou přenášena do správné služby na serveru.
    















3. **Uživatelské jméno a heslo**: Pro účely ověření mohou být zahrnuty přihlašovací údaje uživatele, včetně uživatelského jména a hesla. Tyto přihlašovací údaje umožňují uživatelům prokázat svou identitu a získat přístup ke zdrojům Citrix.
    















4. **Nastavení připojení**: Soubory CFG mohou obsahovat různá nastavení připojení, jako je nastavení šifrování, hodnoty časového limitu relace a možnosti zobrazení. Tato nastavení pomáhají konfigurovat uživatelské prostředí a parametry zabezpečení.
    















5. **Konfigurace prostředků**: V závislosti na konfiguraci může soubor CFG specifikovat, které prostředky Citrix (aplikace nebo desktopy) by měly být spuštěny při navázání spojení.

## Formáty souborů používané Citrixem

Servery Citrix a související technologie Citrix podporují několik formátů souborů, které umožňují doručování aplikací, desktopů a obsahu vzdáleným uživatelům. Zde jsou některé běžné formáty souborů spojené s nasazením serveru Citrix:

1. **ICA (Independent Computing Architecture)**:
    















- **.ica**: Soubor ICA je základní součástí aplikace Citrix a poskytování desktopů. Obsahuje informace o připojení k serveru Citrix, jako je adresa serveru, port, nastavení šifrování a předvolby zobrazení. Když uživatel klikne na prostředek Citrix, vygeneruje se soubor [.ica](/cs/misc/ica/), který klient Citrix Receiver (nebo Citrix Workspace) použije k navázání spojení.
2. **Balíčky Citrix Receiver (nebo Citrix Workspace)**:
    















- **.exe**: Instalační balíčky Citrix Receiver nebo Citrix Workspace se často dodávají ve spustitelném formátu pro různé operační systémy (např. [.exe](/cs/executable/exe/) pro Windows, [.dmg](/cs/compression/dmg /) pro macOS). Tyto balíčky umožňují uživatelům instalovat klientský software na jejich zařízení.
3. **Citrix Workspace App (dříve Citrix Receiver)**:
    















- **.app**: V systému macOS je Citrix Workspace App zabalena jako soubor aplikace macOS [.app](/cs/executable/app/).
4. **Kompatibilita webového prohlížeče**:
    















- K řešením Citrix lze přistupovat prostřednictvím webových prohlížečů, obvykle pomocí HTML5 pro webový přístup. Uživatelé se připojují ke zdrojům Citrix prostřednictvím adres URL, aniž by vyžadovali specifické formáty souborů.
5. **Obrázky disku virtuální plochy**:
    















- **.vhd, .vhdx**: Citrix XenDesktop a XenApp mohou poskytovat virtuální desktopy a aplikace pomocí virtuálního pevného disku [VHD](/cs/disc-and-media/vhd/) nebo [VHDX](/cs/disc-and-media /vhdx/) soubory.
6. **Metadata publikování zdrojů**:
    















- **.xml**: Správci Citrixu často používají soubory [XML](/cs/web/xml/) k definování nastavení publikování zdrojů, včetně vlastností aplikací, zásad přístupu a přiřazení uživatelů.
7. **Soubory ovladače tiskárny**:
    















- Prostředí Citrix mohou vyžadovat specifické soubory ovladače tiskárny (např. .inf), aby byla zajištěna správná funkčnost tisku při používání vzdálených aplikací.
8. **Údaje uživatelského profilu**:
    















- **.upm**: Citrix Profile Management může ukládat data uživatelského profilu do souborů .upm, aby poskytoval konzistentní uživatelské zkušenosti napříč relacemi a zařízeními.
9. **Konfigurační soubory**:
    















- **.conf**: Různé konfigurační soubory, tj. mohou být použity k definování nastavení pro komponenty Citrix, jako jsou konfigurační soubory pro Citrix License Server (např. CtxLicChk.conf).
10. **Konfigurace Citrix ADC (NetScaler)**:

- **.nsconfig:** Konfigurační soubory pro Citrix Application Delivery Controllers (ADC), dříve známé jako NetScaler, ukládají nastavení související s vyrovnáváním zátěže, zabezpečením a řízením provozu.

## Jak otevřít soubor CFG?

Programy, které otevírají nebo odkazují na soubory CFG

- Citrix Access Client (Windows, MAC, Linux)

## Jiné soubory CFG

Zde jsou další typy souborů, které používají příponu souboru **.cfg**.

**Nastavení**
- [CFG - Celestia Configuration File](/cs/settings/cfg-celestia/)
- [CFG - Soubor připojení serveru Citrix](/cs/settings/cfg-citrix/)
- [CFG - Konfigurační soubor MAME](/cs/settings/cfg-mame/)
- [CFG - LightWave Configuration File](/cs/settings/cfg-lightwave/)

**Hra**
- [CFG - Wesnoth Markup Language File](/cs/game/cfg-wesnoth/)
- [CFG - Konfigurační soubor MUGEN](/cs/game/cfg-mugen/)
- [CFG - konfigurační soubor zdrojového enginu](/cs/hra/cfg-sourceengine/)

**Systém a různé**
- [CFG - Soubor CFG](/cs/system/cfg/)
– [CFG – konfigurační soubor modelu Cal3D](/cs/misc/cfg-cal3d/)

## Reference
* [Citrix Virtual Apps](https://en.wikipedia.org/wiki/Citrix_Virtual_Apps)

