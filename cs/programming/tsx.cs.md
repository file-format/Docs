{
  "date" : "2023-12-28",
  "author" : {
    "display_name" : "Shakeel Faiz"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "Soubor TSX - React TypeScript File - Co je soubor .tsx a jak jej otevřít?",
  "description":"Přečtěte si o souboru TSX React TypeScript a o tom, jak jej otevřít.",
  "linktitle" : "TSX",
  "menu" : {
    "docs" : {
      "identifier": "programming-cs-tsx",
      "parent" : "programming"
    }
  },
  "lastmod" : "2023-12-28"
}

## Co je soubor TSX?

Přípona souboru ".tsx" je běžně spojena se soubory TypeScript, které obsahují kód **React**. **TypeScript je nadmnožina JavaScriptu**, která do jazyka přidává statické psaní, a **React je knihovna JavaScriptu pro vytváření uživatelských rozhraní**. Při společné práci s Reactem a TypeScriptem vývojáři často používají pro své soubory příponu „.tsx“, aby naznačili, že obsahují jak TypeScript, tak JSX (přípona syntaxe Reactu pro JavaScript).

## Příklad souboru TSX

TypeScript vám umožňuje definovat typy pro vaše proměnné, parametry funkcí a další. V souboru „.tsx“ často uvidíte kód TypeScript, který specifikuje typy rekvizit, stavu a dalších proměnných používaných v komponentách React.

```
// Příklad: Kód TypeScript v komponentě React
rozhraní MyComponentProps {
   jméno: řetězec;
   věk: číslo;
}
const MyComponent: React.FC<MyComponentProps> = ({ jméno, věk }) => {
   // Logika komponent zde
   return <div>{name} je {age} let.</div>;
};
```

## JSX (React Syntax Extension)

JSX je rozšíření syntaxe pro JavaScript doporučené Reactem. Vypadá podobně jako XML/HTML a používá se k popisu toho, jak by mělo uživatelské rozhraní vypadat.

```
// Příklad: JSX v komponentě React
const MyComponent: React.FC<MyComponentProps> = ({ jméno, věk }) => {
   return <div>{name} je {age} let.</div>;
};
```

Soubor ".tsx" bude obvykle obsahovat definici komponenty React pomocí funkčních komponent nebo komponent třídy.

```
// Příklad: Definice komponenty React v souboru ".tsx".
const MyComponent: React.FC = () => {
   return <div>Dobrý den, reagujte!</div>;
};
```

Na začátku souboru často uvidíte příkazy importu, které přinášejí potřebné závislosti a moduly.

```
// Příklad: Import příkazů do souboru ".tsx".
import Reagovat z 'reagovat';
```

## Jak otevřít soubor TSX?

Soubory TSX jsou soubory ve formátu prostého textu, takže je můžete otevřít v libovolném textovém editoru, např. Poznámkový blok. Jedná se však o kódující soubory a jsou určeny k otevření pomocí IDE, např. Kód Visual Studio.