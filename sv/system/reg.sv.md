{
"datum": "2023-03-07",
  "keywords": [
"reg fil",
"vad är en reg fil",
"fil",
"reg filtillägg",
"förlängning"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "REG-filformat - Windows-registerfil",
  "description":"Läs mer om REG-format och API:er som kan skapa och öppna REG-filer.",
"linktitle": "REG",
  "menu": {
    "docs": {
      "identifier": "system-reg",
      "parent": "system"
}
},
"lastmod": "2023-03-07"
}

## Vad är REG fil?

En REG-fil är ett filformat som används för att importera eller exportera Windows-registerdata. Windows-registret är en hierarkisk databas som lagrar konfigurationsinställningar och alternativ för Windows-operativsystemet och installerade applikationer. Registret innehåller information som användarinställningar, applikationsinställningar, hårdvaru- och mjukvarukonfigurationsdata med mera.

En REG-fil har vanligtvis filtillägget ".reg" och är en vanlig textfil som innehåller en serie registerposter och värden i ett specifikt format. Formatet består av en rubriksektion som identifierar filen som en registerfil, följt av en serie nyckel- och värdepar som representerar registerposter.

## REG-filformat - Mer information

Här är ett exempel på ett reg filformat:

```
[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Run]
"Example"="C:\\Example.exe"

[HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Explorer\Advanced]
"Hidden"=dword:00000001
```

Den första raden i filen anger versionen av registerredigeraren. Följande rader innehåller registerposterna i formatet en nyckelsökväg följt av ett värdenamn och värdedata. I det här exemplet innehåller reg-filen två poster: en som lägger till ett program som heter "Example.exe" till Windows-startlistan, och en annan som ställer in "Dold"-värdet i Windows Explorers avancerade inställningar till "true".

Reg-filer kan skapas och redigeras med en textredigerare som Anteckningar. De används ofta för säkerhetskopiering och återställning, samt för att konfigurera flera datorer med samma registerinställningar.

## Importera eller exportera Windows-registret

En REG-fil är en typ av fil som används för att importera eller exportera data från Windows-registret. Windows-registret är en hierarkisk databas som lagrar konfigurationsinställningar och alternativ för Windows-operativsystemet och installerade applikationer. Registret innehåller information som användarinställningar, applikationsinställningar, hårdvaru- och mjukvarukonfigurationsdata med mera.

Reg-filer kan användas för att skapa eller ändra registerposter, och de används ofta för säkerhetskopiering och återställning, samt för att konfigurera flera datorer med samma registerinställningar. Så här använder du en reg-fil för att lägga till en ny registerpost i Windows-registret:

1. Skapa en ny textfil med en textredigerare som Anteckningar.
2. Skriv in registerposten i rätt format. Formatet består av en rubriksektion som identifierar filen som en registerfil, följt av en serie nyckel- och värdepar som representerar registerposter. Här är ett exempel:

```
Windows Registry Editor Version 5.00

[HKEY_CURRENT_USER\Software\Example]
"Setting1"="Value1"
```

Detta skapar en ny nyckel som heter "Exempel" under nyckeln "Programvara" i den aktuella användarens registerdatabas och ställer in värdet "Setting1" till "Value1".

3. Spara filen med filtillägget .reg.
4. Dubbelklicka på .reg-filen för att lägga till den nya registerposten i Windows-registret.

Du kommer att bli ombedd att bekräfta att du vill lägga till posten i registret. När du har bekräftat kommer den nya posten att läggas till i registret och du kan verifiera den med hjälp av verktyget Registerredigerare.

## Referenser
* [Windows-registret](https://en.wikipedia.org/wiki/Windows_Registry)

