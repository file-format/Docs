{
"datum": "2023-03-07",
  "keywords": [
"reg soubor",
"co je soubor reg",
"soubor",
"přípona souboru reg",
"rozšíření"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formát souboru REG - soubor registru systému Windows",
  "description":"Další informace o formátu REG a rozhraních API, která mohou vytvářet a otevírat soubory REG.",
"linktitle": "REG",
  "menu": {
    "docs": {
      "identifier": "system-reg",
      "parent": "system"
}
},
"lastmod": "2023-03-07"
}

## Co je soubor REG?

Soubor REG je formát souboru používaný k importu nebo exportu dat registru systému Windows. Registr Windows je hierarchická databáze, která ukládá konfigurační nastavení a možnosti pro operační systém Windows a nainstalované aplikace. Registr obsahuje informace, jako jsou uživatelské preference, nastavení aplikací, data konfigurace hardwaru a softwaru a další.

Soubor REG má obvykle příponu souboru „.reg“ a je to soubor ve formátu prostého textu, který obsahuje řadu položek registru a hodnot v určitém formátu. Formát se skládá z části záhlaví, která identifikuje soubor jako soubor registru, za kterým následuje řada párů klíčů a hodnot, které představují položky registru.

## Formát souboru REG – Další informace

Zde je příklad formátu souboru reg:

```
[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Run]
"Example"="C:\\Example.exe"

[HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Explorer\Advanced]
"Hidden"=dword:00000001
```

První řádek souboru určuje verzi editoru registru. Následující řádky obsahují položky registru ve formátu cesty klíče následované názvem hodnoty a daty hodnoty. V tomto příkladu obsahuje soubor reg dvě položky: jednu, která přidá program s názvem "Example.exe" do spouštěcího seznamu Windows, a druhou, která nastaví hodnotu "Hidden" v rozšířeném nastavení Průzkumníka Windows na "true".

Reg soubory lze vytvářet a upravovat pomocí textového editoru, jako je Poznámkový blok. Často se používají pro účely zálohování a obnovy a také pro konfiguraci více počítačů se stejným nastavením registru.

## Import nebo export registru Windows

Soubor REG je typ souboru používaný k importu nebo exportu dat z registru Windows. Registr Windows je hierarchická databáze, která ukládá konfigurační nastavení a možnosti pro operační systém Windows a nainstalované aplikace. Registr obsahuje informace, jako jsou uživatelské preference, nastavení aplikací, data konfigurace hardwaru a softwaru a další.

Soubory Reg lze použít k vytvoření nebo úpravě položek registru a často se používají pro účely zálohování a obnovy a také pro konfiguraci více počítačů se stejným nastavením registru. Zde je návod, jak pomocí souboru reg přidat novou položku registru do registru systému Windows:

1. Vytvořte nový textový soubor pomocí textového editoru, jako je Poznámkový blok.
2. Zadejte položku registru ve správném formátu. Formát se skládá z části záhlaví, která identifikuje soubor jako soubor registru, za kterým následuje řada párů klíčů a hodnot, které představují položky registru. Zde je příklad:

```
Windows Registry Editor Version 5.00

[HKEY_CURRENT_USER\Software\Example]
"Setting1"="Value1"
```

Tím se vytvoří nový klíč s názvem "Příklad" pod klíčem "Software" v podregistru aktuálního uživatele a nastaví se hodnota "Setting1" na "Value1".

3. Uložte soubor s příponou .reg.
4. Poklepáním na soubor .reg přidejte novou položku registru do registru systému Windows.

Budete vyzváni k potvrzení, že chcete přidat položku do registru. Po potvrzení bude nová položka přidána do registru a můžete ji ověřit pomocí nástroje Editor registru.

## Reference
* [Registr Windows](https://en.wikipedia.org/wiki/Windows_Registry)

