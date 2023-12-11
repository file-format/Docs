{
"datum": "2023-06-08",
  "keywords": [
"soubor crx",
"co je soubor crx",
"jak nainstalovat crx soubor v google chrome",
"jak otevřít soubor crx",
"co obsahuje soubor crx",
"jaký je formát souboru crx",
"soubor",
"přípona souboru crx",
"rozšíření"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formát souboru CRX – rozšíření Google Chrome",
  "description":"Další informace o formátu CRX a rozhraních API, která mohou vytvářet a otevírat soubory CRX.",
  "linktitle": "CRX",
  "menu": {
    "docs": {
      "identifier": "misc-crx",
      "parent": "misc"
}
},
"lastmod": "2023-06-08"
}

## Co je soubor CRX?

Formát souboru CRX je spojen s rozšířeními prohlížeče Google Chrome. Soubor CRX je v podstatě komprimovaný balíček obsahující potřebné soubory a metadata pro rozšíření, které se má nainstalovat a spustit v prohlížeči Google Chrome. Vylepšuje funkčnost nebo vzhled webového prohlížeče tím, že poskytuje další funkci nebo téma.

Když je soubor CRX stažen a nainstalován v prohlížeči Google Chrome, prohlížeč ověří integritu rozšíření pomocí veřejného klíče a podpisu. Pokud je ověření úspěšné, Chrome extrahuje obsah souboru CRX a nainstaluje rozšíření, které jej zpřístupní k použití. Uživatelé mohou svá rozšíření spravovat prostřednictvím stránky Rozšíření Chrome, která umožňuje povolit, zakázat nebo odebrat nainstalovaná rozšíření.

## Jak nainstalovat soubor CRX do Google Chrome?

Chcete-li nainstalovat soubor CRX do prohlížeče Google Chrome, postupujte takto:

1. Otevřete prohlížeč Chrome.
2. Do adresního řádku zadejte `chrome://extensions` a stiskněte Enter.
3. Aktivujte přepínač „Režim vývojáře“ umístěný v pravém horním rohu stránky Rozšíření.
4. Klikněte na tlačítko „Načíst rozbalené“.
5. Vyhledejte a vyberte složku obsahující extrahovaný obsah souboru CRX (nebo jednoduše vyberte samotný soubor CRX).
6. Kliknutím na "Otevřít" nainstalujte rozšíření.

## Co obsahuje soubor CRX?

Soubor CRX obsahuje nezbytné soubory a metadata vyžadovaná pro rozšíření Google Chrome. Zde je rozpis typického obsahu nalezeného v souboru CRX:

- **Soubor manifestu (manifest.json):** Tento soubor je soubor ve formátu JSON, který obsahuje informace o rozšíření, jako je jeho název, verze, popis, oprávnění a skripty na pozadí. Definuje strukturu a chování rozšíření.
- **Soubory JavaScript:** Tyto soubory obsahují kód, který definuje funkčnost rozšíření. Mohou zahrnovat skripty pro zpracování událostí, úpravu webových stránek nebo interakci s rozhraními API prohlížeče Chrome.
- **HTML, CSS a obrázkové soubory:** Rozšíření často obsahují prvky uživatelského rozhraní, jako jsou vyskakovací okna nebo stránky možností. Soubory HTML definují strukturu těchto rozhraní, zatímco soubory CSS řídí jejich vzhled. Soubory obrázků se používají pro ikony nebo jiné grafické prvky.
- **Volitelné zdrojové soubory:** Rozšíření mohou obsahovat další zdroje, jako jsou lokalizační soubory pro podporu více jazyků. Tyto soubory obsahují překlady textu použitého v uživatelském rozhraní rozšíření.
- **Skripty na pozadí:** Pokud má rozšíření procesy na pozadí nebo skripty, které běží nezávisle na aktivní webové stránce, budou tyto skripty zahrnuty do souboru CRX.
- **Skripty obsahu:** Skripty obsahu jsou skripty, které lze vložit do webových stránek za účelem úpravy jejich chování nebo interakce s jejich obsahem. Pokud rozšíření používá skripty obsahu, potřebné soubory pro tyto skripty budou přítomny v souboru CRX.
- **Další položky:** V závislosti na konkrétních požadavcích rozšíření mohou být zahrnuty další soubory, jako jsou audio nebo video soubory, písma nebo datové soubory.

Formát souboru CRX je v podstatě komprimovaný balíček, který obsahuje všechny tyto soubory a složky strukturovaným způsobem. Když je soubor CRX nainstalován v prohlížeči Google Chrome, prohlížeč extrahuje obsah a umístí jej na vhodná místa, což umožní načíst a spustit rozšíření v prohlížeči.

## Jaký je formát souboru CRX?

Formát souboru CRX je specifický formát pro balení a distribuci rozšíření Google Chrome. Je to v podstatě komprimovaný ZIP archiv s jinou příponou souboru. Základní struktura souboru CRX je následující:

- **Podpis souboru:** První 4 bajty souboru obsahují magické číslo "Cr24" (hexadecimálně: 43 72 32 34), které slouží jako podpis k identifikaci souboru jako souboru CRX.
- **Číslo verze:** Další 4 bajty představují číslo verze formátu CRX.
- **Délka veřejného klíče:** Následující 4 bajty označují délku zakódovaného veřejného klíče použitého pro ověření podpisu rozšíření.
- **Délka podpisu:** Následující 4 bajty určují délku podpisu rozšíření.
- **Veřejný klíč:** Tato část obsahuje zakódovaný veřejný klíč používaný k ověření integrity rozšíření.
- **Podpis:** Tato sekce obsahuje podpis rozšíření, který je generován podepsáním obsahu rozšíření pomocí soukromého klíče odpovídajícího výše uvedenému veřejnému klíči.
- **ZIP archiv:** Zbývající bajty souboru CRX tvoří komprimovaný archiv ZIP. Tento archiv obsahuje všechny potřebné soubory a složky rozšíření, včetně souboru manifestu, souborů JavaScript, souborů HTML, souborů CSS, obrázků a jakýchkoli dalších zdrojů.

## Reference
* [Specifikace formátu CRX](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/K3YIsNL_Et4)

