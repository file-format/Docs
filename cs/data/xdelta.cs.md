{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Soubor XDELTA - xdelta Differential File - Co je soubor .xdelta a jak jej otevřít?",
  "description" : "Přečtěte si o xdelta Differential File a jak jej otevřít.",
  "linktitle" : "XDELTA",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-xdelta-cs",
      "parent" : "data"
}
},
  "lastmod" : "2024-02-08"
}

## Co je soubor XDELTA?

Formát souboru XDELTA obsahuje binární rozdíly mezi dvěma dalšími soubory a je generován nástrojem xdelta, nástrojem příkazového řádku pro delta kódování, který zahrnuje výpočet rozdílů mezi dvěma soubory a kódování těchto rozdílů v kompaktním formátu. Soubory XDELTA ukládají binární data představující změny nebo rozdíly mezi původním souborem a aktualizovaným souborem. Binární data v souboru XDELTA představují změny potřebné k transformaci jednoho souboru (původního) na jiný soubor (aktualizovaná nebo opravená verze).

Soubory XDELTA se v herní komunitě často používají k distribuci modifikací (modů) pro videohry. Tyto mody mohou zahrnovat cokoli od kosmetických změn až po významné změny herních mechanismů. Soubory XDELTA umožňují uživatelům aplikovat tyto úpravy na jejich herní instalace záplatou původních herních souborů se změnami specifikovanými v souboru XDELTA.

## xdelta

`xdelta` je nástroj příkazového řádku používaný pro delta kódování a dekódování; primárně se používá k vytváření a aplikaci binárních záplat, často nazývaných delta záplaty nebo xdelta záplaty, mezi dvěma soubory; tyto opravy představují rozdíly mezi původním souborem a upravenou nebo aktualizovanou verzí, což umožňuje efektivní distribuci aktualizací, zejména ve scénářích, kde je omezená šířka pásma nebo úložný prostor.

Zde je stručný přehled hlavních funkcí `xdelta`:

1.  **Creating patches**: `xdelta` can generate a patch file that contains differences between two files. This patch file, often referred to as an "xdelta patch", is relatively small compared to original and updated files, as it only contains the changes between them.
    
2.  **Applying patches**: Once a patch file is created, `xdelta` can apply it to original file to produce updated file. This process involves taking original file and patch file as input and applying changes specified in patch file to generate updated file.
    
3.  **Applying reverse patches**: `xdelta` can also apply reverse patches, which revert changes made to a file. This is useful for rolling back updates or modifications.
    

`xdelta` se běžně používá v různých scénářích, jako je distribuce aktualizací softwaru, záplatování videoher a aktualizace systémových souborů ve vestavěných zařízeních nebo síťových zařízeních. Poskytuje flexibilní a efektivní způsob správy aktualizací souborů a zároveň minimalizuje využití šířky pásma a požadavky na úložiště.

## xdeltaui

xdeltaui je aplikace s grafickým uživatelským rozhraním (GUI) pro správu a aplikaci oprav XDELTA. xdelta gui poskytuje uživatelsky přívětivé rozhraní pro uživatele, jak pracovat se soubory XDELTA a aplikovat je na odpovídající originální soubory, efektivně je opravovat nebo aktualizovat.

Na rozdíl od verze xdelta s příkazovým řádkem, která pracuje prostřednictvím textových příkazů, nabízí xdeltaui intuitivnější způsob práce se soubory XDELTA, zejména pro uživatele, kteří nejsou obeznámeni s rozhraními příkazového řádku nebo preferují grafické nástroje.

S xdeltaui mohou uživatelé obvykle provádět úkoly, jako je výběr původního souboru, výběr souboru opravy XDELTA a použití opravy pro generování aktualizovaného souboru. To může být užitečné zejména při instalaci modů nebo aktualizací pro videohry nebo jiné softwarové aplikace.

## xdelta ke stažení

Na systémech Linux můžete k instalaci `xdelta` použít správce balíčků jako `apt`, `yum` nebo `dnf`. Například na Ubuntu můžete použít následující příkaz:

```
sudo apt-get install xdelta3
```

## Jak používat xdelta

Chcete-li použít `xdelta`, musíte obvykle provést tyto obecné kroky:

1.  **Stáhnout a nainstalovat**: Nejprve se ujistěte, že máte na svém systému nainstalovaný `xdelta`. Můžete si jej stáhnout z oficiálních webových stránek, správců balíčků nebo jiných důvěryhodných zdrojů.
    
2.  **Prepare Files**: Prepare original file (often called source or base file) and updated file (target file) that you want to create a patch for or apply a patch to.
    
3.  **Vytvoření opravy**:
    
- Otevřete rozhraní příkazového řádku (terminál nebo příkazový řádek).
- Použijte příkaz `xdelta` s příslušnými volbami k vytvoření opravy. Základní syntaxe je:
               
```
xdelta delta<original_file><updated_file><patch_output_file>
```
        
Nahradit `<original_file> ` s cestou k původnímu souboru, `<updated_file> ` s cestou k aktualizovanému souboru a `<patch_output_file> ` s požadovaným názvem souboru opravy.
– Příklad:
               
```
xdelta delta původní_soubor aktualizovaný_soubor patch.xdelta
```
        
4.  **Použití opravy**:
    
- Ujistěte se, že máte k dispozici původní soubor a soubor opravy.
- Otevřete rozhraní příkazového řádku.
- Použijte příkaz `xdelta` s příslušnými volbami k použití opravy. Základní syntaxe je:
        
      
```
xdelta patch<original_file><patch_file><output_file>
```
        
Nahradit `<original_file> ` s cestou k původnímu souboru, `<patch_file> ` s cestou k souboru opravy a `<output_file> ` s požadovaným názvem výstupního souboru.
– Příklad:
                
```
xdelta patch původní_soubor patch.xdelta aktualizovaný_soubor
```
        
5.  **Zobrazení nápovědy**: Pokud potřebujete pomoc s konkrétními volbami nebo příkazy, můžete použít příkaz `xdelta` s volbou `--help` k zobrazení informací o použití a dostupných voleb.
    
## Jak otevřít soubor XDELTA

Soubory XDELTA nejsou určeny k přímému otevírání. Pokud si přejete aplikovat XDELTA patch na hru nebo jiný soubor, máte možnost použít buď xdelta, která je kompatibilní na více platformách, nebo xdelta UI, speciálně navržené pro uživatele Windows.

## Reference
* [xdelta](https://en.wikipedia.org/wiki/Xdelta)


