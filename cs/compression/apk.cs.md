{
  "date" : "2019-10-11",
  "keywords" :[ "soubor apk", "formát souboru apk", "co je soubor apk", "soubor", "příklad apk", "přípona souboru apk", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APK - Co je soubor APK?",
  "description":"Naučte se vědět, co je soubor APK a rozhraní API, která mohou vytvářet a otevírat soubory APK.",
  "linktitle" : "APK",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-27"
}

## Co je soubor APK?

Soubor s příponou .apk je soubor aplikace Google Android, který se používá k instalaci aplikací (aplikací) do zařízení Android. Je vytvořen jako spustitelný soubor pomocí oficiálního IDE Google Android Studio a je nahrán do obchodu Google Play, aby si jej mohli stáhnout a nainstalovat koncoví uživatelé. Soubory APK lze vygenerovat a zpřístupnit pro ruční instalaci i před publikováním v obchodě Google Play. To pomáhá při testování funkčnosti a chování vygenerovaného souboru balíčku APK. Proto si musíte být jisti, že soubor APK pochází z důvěryhodného zdroje a neobsahuje žádný malware.

## Formát souboru APK

Soubory APK jsou zabaleny jako komprimované ve formátu souboru [ZIP](/cs/compression/zip/), který lze otevřít pomocí jakéhokoli softwaru pro otevírání souborů ZIP. Příponu .apk takového souboru lze přejmenovat na .zip a otevřít soubor v libovolné aplikaci ZIP nebo extrahovat jeho obsah.

## Obsah balíčku APK

Jediný soubor APK obsahuje všechny potřebné soubory, které jsou nutné pro jeho instalaci a spuštění. Soubor APK, když je extrahován pomocí aplikace ZIP, obsahuje následující soubory a složky.

* `META-INF/`: Adresář, který obsahuje soubor manifestu, podpis a seznam zdrojů v archivu
* `lib/`: Adresář obsahující zkompilovaný kód související se specifickými platformami, jako je armeabi-v7a, x86, arm64-v8a atd.
* `res/`: Adresář obsahující nezkompilované zdroje, jako jsou obrázky
* `assets/`: Adresář obsahující prostředky aplikací, které lze načíst pomocí AssetManager.
* `androidManifest.xml`: Obsahuje název, informace o verzi a obsah souboru APK
* `classes.dex`: Toto jsou zkompilované třídy Java, které lze spustit na virtuálním počítači Dalvik a pomocí běhového prostředí Android
* `resources.arsc`: Kompilovaný soubor zdrojů, jako jsou řetězce

## Jak nainstalovat soubor APK na zařízení Android?

Chcete-li nainstalovat soubor APK do zařízení Android, můžete použít následující kroky.

1. Stáhněte si APK pomocí webového prohlížeče
2. Klepněte na něj – pak byste měli vidět stahování na horní liště vašeho zařízení
3. Po stažení otevřete Stahování, klepněte na soubor APK a po zobrazení výzvy klepněte na Ano.

Podle těchto kroků zahájíte instalaci aplikace na vašem zařízení.

## Reference

* [Formát souboru APK](https://en.wikipedia.org/wiki/Android_application_package)

