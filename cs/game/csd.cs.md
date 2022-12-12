{
  "date" : "2022-02-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Další informace o formátu CSD Steam Game Data Backup File a rozhraních API.",
  "title" :"Formát souboru CSD - soubor zálohy dat hry Steam",
  "linktitle" : "CSD",
  "menu" : {
    "docs" : {
      "identifier": "game-csd",
      "parent" : "game"
}
},
  "lastmod" : "2022-02-08"
}

## Co je soubor CSD?

Soubor CSD je soubor zálohy hry generovaný herní službou **Steam**, který uživatelům umožňuje stahovat a spravovat hry **Valve**. Obsahuje záložní data související s hrami, která lze použít k obnovení smazané hry. Steam je schopen obnovit hru ze souboru CSD pouze v případě, že byla hra stažena, nainstalována a opravena prostřednictvím služby Steam. Chcete-li obnovit hru ze souboru CSD, použijte možnost Steam → Zálohovat a obnovit Gamesteam a vyberte soubor.

## Formát souboru CSD – Další informace

Vnitřní struktura formátu souboru CSD není veřejně dostupná a specifikace jeho formátu souboru nejsou k dispozici pro vývojáře. Soubory CSD jsou doprovázeny soubory CSM a ISS, což jsou také formáty souborů her Steam.

### Kde najít záložní soubory Steam?

Celé záložní soubory Steam lze nalézt na následujících umístěních:

* C:\Program Files (x86)\Steam\steamapps\common\<game name> \ :
* \cfg\ - Vlastní konfigurace a konfigurační skripty
* \ke stažení\ - Vlastní obsah pro hry pro více hráčů
* \maps\ - Vlastní mapy, které byly nainstalovány nebo staženy během her pro více hráčů
* \materials\ - Vlastní textury a vzhledy
* \SAVE\ - Uložené hry pro jednoho hráče

Umístění her vytvořených třetí stranou se však může lišit a je určeno vývojářem hry.

### Obnovení ze záložního souboru CSD

Nainstalujte si Steam a přihlaste se ke správnému účtu Steam (další pokyny naleznete v části Instalace Steamu)
* Spusťte Steam
* Klikněte na "Steam" v levém horním rohu aplikace Steam
* Vyberte "Zálohovat a obnovit hry..."
* Vyberte "Obnovit předchozí zálohu"
* Přejděte do umístění záložních souborů hry
* Pokračujte okny Steam a nainstalujte potřebné hry.

## Reference

* [Pomocí funkce Steam Backup](https://help.steampowered.com/en/faqs/view/4593-5CB7-DC3C-64F0)

