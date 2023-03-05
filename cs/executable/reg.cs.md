{
  "date" : "2021-08-02",
  "keywords" :[ "soubor reg", "formát souboru reg", "co je soubor reg", "soubor", "příklad reg", "přípona souboru reg", "přípona", "formát" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Další informace o formátu souboru REG a rozhraních API, která mohou vytvářet a otevírat soubory REG.",
  "title" :"REG - soubor registru systému Windows",
  "linktitle" : "REG",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-02"
}

## Co je soubor REG?
Soubor REG je jednoduše textový soubor s příponou .reg. Tyto soubory se obvykle vytvářejí exportem typických klíčů z registru. Tyto soubory lze také použít jako zálohu registru (Zvláště tento krok je důležitý před provedením změn!). Můžete vidět, že některé je zpřístupnily jako soubory ke stažení na stejných stránkách, které vám ukazují, jak provést hack registru. Soubor REG je užitečný při provádění ručních změn v registru a exportu těchto změn. Stačí soubor trochu vyčistit a poté jej sdílet s ostatními.

## Formát souboru REG
Formát souboru REG byl navržen pro export a import částí registru Windows pomocí syntaxe založené na INI. Registr Windows je relační nebo hierarchická databáze, která uchovává nízkoúrovňová nastavení pro operační systém Microsoft Windows a další aplikace, které používají registr Windows. Alternativa, můžeme říci, registr nebo registr Windows se skládá z informací, možností, nastavení a dalších hodnot pro programy a hardware nainstalovaný na všech verzích operačních systémů Microsoft Windows.
### Syntaxe souboru REG
Zde jsou některé klíčové prvky jako součást syntaxe souboru REG:
- **RegistryEditorVersion**: Např. "Editor registru Windows verze 5.00" pro Windows 2000, Windows XP a Windows Server 2003.
- **Prázdný řádek**: Označuje začátek nové cesty registru.
- **RegistryPathx**: Cesta k podklíči, který obsahuje první hodnotu, kterou importujete.
- **DataItemNamex**: Název datové položky, kterou chcete importovat.
- **DataTypex**: Datový typ pro hodnotu registru.

Klíče jsou uloženy v souborech .reg pomocí následující syntaxe:
```
[<Hive name>\<Key name>\<Subkey name>]
"Value name"=<Value type>:<Value data>
```
Výchozí hodnotu klíče můžete upravit pomocí „@“ namísto „Název hodnoty“:
```
[<Hive name>\<Key name>\<Subkey name>]
@=<Value type>:<Value data>
```
### Příklad
Zde je příklad souboru REG
```
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SOFTWARE\Foobar]
"Value A"="<String value data with escape characters>"
"Value B"=hex:<Binary data (as comma-delimited list of hexadecimal values)>
"Value C"=dword:<DWORD value integer>
"Value D"=hex(0):<REG_NONE (as comma-delimited list of hexadecimal values)>
"Value E"=hex(1):<REG_SZ (as comma-delimited list of hexadecimal values representing a UTF-16LE NUL-terminated string)>
"Value F"=hex(2):<Expandable string value data (as comma-delimited list of hexadecimal values representing a UTF-16LE NUL-terminated string)>
"Value G"=hex(3):<Binary data (as comma-delimited list of hexadecimal values)> ; equal to "Value B"
"Value H"=hex(4):<DWORD value (as comma-delimited list of 4 hexadecimal values, in little endian byte order)>
"Value I"=hex(5):<DWORD value (as comma-delimited list of 4 hexadecimal values, in big endian byte order)>
"Value J"=hex(7):<Multi-string value data (as comma-delimited list of hexadecimal values representing UTF-16LE NUL-terminated strings)>
"Value K"=hex(8):<REG_RESOURCE_LIST (as comma-delimited list of hexadecimal values)>
"Value L"=hex(a):<REG_RESOURCE_REQUIREMENTS_LIST (as comma-delimited list of hexadecimal values)>
"Value M"=hex(b):<QWORD value (as comma-delimited list of 8 hexadecimal values, in little endian byte order)>
```

## Reference

* [Registr Windows – podle Wikipedie](https://en.wikipedia.org/wiki/Windows_Registry)
* [Jak přidat, upravit nebo odstranit podklíče a hodnoty registru pomocí souboru .reg](https://support.microsoft.com/en-us/topic/how-to-add-modify-or-delete-registry-subkeys-and-values-by-using-a-reg-file-9c7f37cf-a5e9-e1cd-c4fa-2a26218a1a23)
