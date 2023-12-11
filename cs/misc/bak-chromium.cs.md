{
"datum": "2023-06-12",
  "keywords": [
"bak",
"soubor bak",
"Záložky BAK Chromium",
"co je soubor bak",
"jak otevřít soubor bak",
"soubor",
"přípona souboru bak",
"rozšíření"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formát souboru BAK - Záloha záložek Chromium",
  "description":"Další informace o formátu záložek BAK Chromium a rozhraních API, která mohou vytvářet a otevírat soubory BAK.",
  "linktitle": "BAK Chromium Bookmarks",
  "menu": {
    "docs": {
      "identifier": "misc-bak-chromium",
      "parent": "misc"
}
},
"lastmod": "2023-06-12"
}

## Co je soubor BAK?

Soubor .bak v kontextu webových prohlížečů založených na Chromiu, jako je Google Chrome a Microsoft Edge, je v podstatě záložní soubor vašich záložek. Tyto záložky jsou uloženy jako prostý textový seznam a použitý formát souboru je JSON. Účelem těchto souborů .bak je chránit vaše záložky poskytnutím zálohy, kterou lze obnovit v případě náhodného smazání nebo ztráty.

Prohlížeče založené na Chromu, včetně Google Chrome, tyto záložní soubory běžně vytvářejí a obvykle jim dávají název „Bookmarks.bak“. Jsou to v podstatě snímky vašich záložek v konkrétním okamžiku.

## Jak používat soubor .bak k obnovení záložek

1. **Najděte záložní soubor:** Obvykle se nachází v konkrétní složce spojené s vaším profilem Chromium. Přesné umístění se může lišit v závislosti na vašem operačním systému.

V systému Windows: Podívejte se do `C:\Users\<YourUsername> \AppData\Local\Chromium\User Data\Default\Bookmarks.bak`.

V systému macOS: Hledejte v `~/Library/Application Support/Chromium/Default/Bookmarks.bak`.

V systému Linux: Zkontrolujte `~/.config/chromium/Default/Bookmarks.bak`.

3. Ujistěte se, že máte zavřený prohlížeč Chromium.
4. Přejmenujte soubor „Bookmarks.bak“ odstraněním přípony „.bak“, takže se bude nazývat jednoduše „Záložky“.
5. Spusťte Chromium.

Přejmenováním souboru .bak na „Záložky“ jej Chromium použije jako aktuální soubor záložek a vaše předchozí záložky by měly být obnoveny.

## Zálohování záložek Chromium

Zálohování záložek prohlížeče Chromium je rozumné opatření, které zajistí, že neztratíte své důležité uložené webové stránky a adresy URL. Chromium je prohlížeč s otevřeným zdrojovým kódem, který slouží jako základ pro další prohlížeče, jako je Google Chrome a Microsoft Edge. Chcete-li zálohovat záložky prohlížeče Chromium, postupujte takto:

## Metoda 1: Ruční zálohování

1. **Otevřít Chromium**: Spusťte prohlížeč Chromium v počítači.

2. **Přístup k záložkám**: Klikněte na tři svislé tečky (ikona nabídky) v pravém horním rohu okna prohlížeče. V rozbalovací nabídce umístěte ukazatel myši na položku Záložky a zobrazí se podnabídka záložek.

3. **Exportovat záložky**: V podnabídce záložek klikněte na „Správce záložek“. Otevře se nová karta s vašimi záložkami.

4. **Exportovat záložky**: Na kartě správce záložek znovu klikněte na tři svislé tečky (obvykle v pravém horním rohu), čímž otevřete nabídku správce záložek. Z této nabídky vyberte „Exportovat záložky“.

5. **Vyberte umístění**: Vyberte, kam chcete uložit exportovaný soubor záložek v počítači. Výchozí název souboru je „bookmarks.html“, ale pokud chcete, můžete jej změnit. Uložte jej na místo, které si budete pamatovat.

6. **Uložit**: Kliknutím na tlačítko „Uložit“ nebo „Exportovat“ uložíte záložky jako soubor HTML.

Vaše záložky byly nyní zálohovány jako soubor HTML. Tento soubor můžete zkopírovat na externí disk nebo cloudové úložiště pro úschovu.

## Metoda 2: Synchronizace s účtem Google (pokud existuje)

Pokud jste v prohlížeči Chromium přihlášeni k účtu Google, můžete také použít vestavěnou funkci synchronizace, aby byly vaše záložky v bezpečí a synchronizované mezi zařízeními. Tímto způsobem budou vaše záložky automaticky zálohovány na váš účet Google.

1. **Otevřít Chromium**: Spusťte prohlížeč Chromium a ujistěte se, že jste přihlášeni ke svému účtu Google.

2. **Povolit synchronizaci**: Klikněte na tři svislé tečky (ikona nabídky) v pravém horním rohu okna prohlížeče a přejděte na „Nastavení“.

3. **Synchronizace a služby Google**: Na kartě Nastavení klikněte na levém postranním panelu na „Synchronizace a služby Google“.

4. **Synchronizujte svá data**: V části „Synchronizace“ se ujistěte, že je zapnuta možnost „Záložky“. Tím se synchronizují vaše záložky s vaším účtem Google.

Vaše záložky budou nyní automaticky zálohovány a synchronizovány s vaším účtem Google. Můžete k nim přistupovat po přihlášení ke svému účtu Google na jakémkoli zařízení s prohlížečem Chromium nebo jiným prohlížečem, který podporuje synchronizaci Google.

Nezapomeňte pravidelně zálohovat své záložky také ručně, zvláště pokud chcete místní kopii, která není závislá pouze na synchronizaci vašeho účtu Google.

## Jak otevřít soubor BAK

Pokud chcete prozkoumat nezpracovaná data zálohy záložek, můžete otevřít soubor „Bookmarks.bak“ pomocí různých textových editorů, jako je Microsoft Visual Studio Code (dostupný na více platformách), Microsoft Notepad (pro uživatele Windows), Apple TextEdit (pro uživatele Mac) nebo jakýkoli jiný textový editor podle vašeho výběru. To vám umožní zobrazit záložky a metadata obsažená v souboru.

Můžete otevřít soubor "Bookmarks.bak" a zobrazit jeho obsah pomocí různých textových editorů a editorů kódu. Zde jsou některé běžně používané možnosti:

1. Kód Visual Studio (VS Code)
2. Poznámkový blok (Windows)
3. TextEdit (Mac)
4. Vznešený text
5. Poznámkový blok++
6. Atom
7. nano a Vim (Linux)
8. WordPad (Windows)

## Další soubory BAK

Zde jsou další typy souborů, které používají příponu **.bak**.

**Databáze**
- [BAK - Soubor zálohy databáze](/cs/database/bak/)
- [BAK - Swiftpage Act! Záloha databáze](/cs/databáze/bak-act/)
- [BAK - Záloha databáze Microsoft SQL Server](/cs/database/bak-sqlserver/)

**Hra**
- [BAK - Terraria World or Player Backup](/cs/game/bak-terraria/)

**Různé**
- [BAK - Backup File](/cs/misc/bak-backup/)
- [BAK - Záloha skóre finále 2012](/cs/misc/bak-finale/)
- [BAK - MobileTrans Backup](/cs/misc/bak-mobiletrans/)
- [BAK - Záloha video projektu VEGAS](/cs/misc/bak-vegas/)

**Nastavení**
- [BAK - Holo Launcher Backup](/cs/settings/bak-holo/)

## Reference
* [Chromium Bookmarks](https://www.chromium.org/user-experience/bookmarks/)
