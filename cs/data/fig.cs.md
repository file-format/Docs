{
  "date" : "2024-01-25",
  "author" : {
    "display_name" : "Shakeel Faiz"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "Soubor FIG - MATLAB Soubor obrázku - Co je soubor .fig a jak jej otevřít?",
  "description" : "Přečtěte si o MATLAB Figure File a jak jej otevřít.",
  "linktitle" : "FIG",
  "menu" : {
    "docs" : {
      "identifier" : "data-cs-fig",
      "parent" : "data"
    }
  },
  "lastmod" : "2024-01-25"
}

## Co je soubor FIG?

Soubor FIG je speciální soubor, který obsahuje obrázek nebo graf vytvořený pomocí programu MATLAB, který se používá k provádění matematiky a analýze dat. Tento soubor obsahuje informace o obrázcích nebo grafech, které MATLAB kreslí, aby lidem pomohl lépe vidět a porozumět datům. Je to jako kontejner, který uchovává všechny podrobnosti o grafech.

.FIG je výchozí formát souboru obrázků MATLABu. Ukládá kompletní obrázek, včetně všech os, štítků a nastavení. Chcete-li uložit obrázek v tomto formátu, můžete použít funkci `savefig`:

## O softwaru MATLAB - Pro otevření souboru FIG

MATLAB, zkratka pro „Matrix Laboratory“, je výkonné programovací a numerické výpočetní prostředí vyvinuté společností The MathWorks. Je široce používán pro úlohy, jako je analýza dat, matematické modelování, vývoj algoritmů a vědecké výpočty. MATLAB umožňuje uživatelům manipulovat s maticemi, vykreslovat grafy, implementovat algoritmy a vytvářet uživatelská rozhraní, což z něj činí všestranný nástroj pro inženýry, vědce a výzkumníky napříč různými obory. Jeho intuitivní syntaxe a rozsáhlá knihovna funkcí z něj činí oblíbenou volbu pro řešení složitých matematických problémů a provádění simulací.

## Jak vytvořit soubor FIG v MATLABu?

Chcete-li vytvořit soubor FIG pomocí MATLABu, postupujte takto:

1. **Vyberte data:** Vyberte proměnnou, pro kterou chcete vytvořit graf, z panelu "Pracovní prostor" v MATLABu.

2. **Vyberte typ grafu:** Přejděte na záložku "PLOTY" a klikněte na požadovaný typ pozemku.

3. **Uložte graf jako soubor OBR:**

     - Přejděte do nabídky "Soubor".
     - Zvolte buď "Uložit" nebo "Uložit jako."
     - Zadejte název souboru a rozhodněte se, kam jej chcete uložit.
     - Kliknutím na "Uložit" vytvoříte soubor FIG.

Můžete jej také uložit jako soubor FIG pomocí funkce `savefig`. Vyberte název souboru a zadejte příponu '.fig':

## Jak otevřít soubor FIG?

Chcete-li otevřít soubor FIG v MATLABu, postupujte takto:

1. **Otevřete MATLAB:** Spusťte MATLAB na svém počítači.

2. **Přejděte na záložku "PLOTS":** Klikněte na plot v záložce "PLOTS" a vyberte požadovaný typ grafu.

3. **Otevřete soubor FIG:**

     - Přejděte do nabídky "Soubor".
     - Zvolte "Otevřít."
     - Přejděte do umístění, kde je uložen váš soubor FIG, vyberte jej a klikněte na „Otevřít“.

Případně můžete použít funkci `openfig` v MATLABu:

## Reference
* [MATLAB](https://en.wikipedia.org/wiki/MATLAB)

