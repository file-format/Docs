{
  "date" : "2021-08-02",
  "keywords" :[ "fișier reg", "format fișier reg", "ce este un fișier reg", "fișier", "exemplu reg", "extensie fișier reg", "extensie", "format"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Aflați despre formatul de fișier REG și despre API-urile care pot crea și deschide fișiere REG.",
  "title" :"REG - Fișier de registru Windows",
  "linktitle" : "REG",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-02"
}

## Ce este un fișier REG?
Un fișier REG este pur și simplu un fișier text cu extensia .reg. Aceste fișiere sunt de obicei create prin exportul cheilor tipice din Registry. Aceste fișiere pot fi folosite și ca o copie de rezervă a registrului (în special acest pas este important înainte de a face modificări!). Puteți vedea că unii le-au făcut disponibile ca fișiere descărcabile pe aceleași site-uri care vă arată cum să efectuați un hack de registry. Un fișier REG este util pentru a face modificări manuale în Registry și pentru a exporta aceste modificări. Doar curățați puțin fișierul și apoi partajați-l altora.

## Format de fișier REG
Formatul de fișier REG a fost conceput pentru exportul și importarea porțiunilor din registry Windows folosind o sintaxă bazată pe INI. Registrul Windows este o bază de date relațională sau ierarhică care păstrează setările de nivel scăzut pentru sistemul de operare Microsoft Windows și alte aplicații care utilizează registrul Windows. Alternativ, putem spune, registry sau Windows Registry constă din informații, opțiuni, setări și alte valori pentru programele și hardware-ul instalat pe toate versiunile sistemelor de operare Microsoft Windows.
### Sintaxa fișierului REG
Iată câteva elemente cheie ca parte a unei sintaxe a fișierului REG:
- **RegistryEditorVersion**: De exemplu, „Windows Registry Editor Version 5.00” pentru Windows 2000, Windows XP și Windows Server 2003.
- **Linie goală**: identifică începutul unei noi căi de registry.
- **RegistryPathx**: Calea subcheii care deține prima valoare pe care o importați.
- **DataItemNamex**: numele elementului de date pe care doriți să îl importați.
- **DataTypex**: tipul de date pentru valoarea de registry.

Cheile sunt stocate în fișiere .reg folosind următoarea sintaxă:
```
[<Hive name>\<Key name>\<Subkey name>]
"Value name"=<Value type>:<Value data>
```
Puteți edita valoarea implicită a unei chei folosind „@” în loc de „Nume valoare”:
```
[<Hive name>\<Key name>\<Subkey name>]
@=<Value type>:<Value data>
```
### Exemplu
Iată un exemplu de fișier REG
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

## Referințe

* [Registrul Windows - de Wikipedia](https://en.wikipedia.org/wiki/Windows_Registry)
* [Cum să adăugați, să modificați sau să ștergeți subchei și valori de registry folosind un fișier .reg](https://support.microsoft.com/en-us/topic/how-to-add-modify-or-delete-registry-subkeys-and-values-by-using-a-reg-file-9c7f37cf-a5e9-e1cd-c4fa-2a26218a1a23)
