{
  "date" : "2023-12-28",
  "author" : {
    "display_name" : "Shakeel Faiz"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "Plik TSX - Plik React TypeScript - Co to jest plik .tsx i jak go otworzyć?",
  "description":"Dowiedz się o pliku TypeScript TSX React i jak go otworzyć.",
  "linktitle" : "TSX",
  "menu" : {
    "docs" : {
      "identifier": "programming-pl-tsx",
      "parent" : "programming"
    }
  },
  "lastmod" : "2023-12-28"
}

## Co to jest plik TSX?

Rozszerzenie pliku „.tsx” jest powszechnie kojarzone z plikami TypeScript zawierającymi kod **React**. **TypeScript to nadzbiór JavaScript**, który dodaje do języka statyczne pisanie, oraz **React to biblioteka JavaScript do tworzenia interfejsów użytkownika**. Pracując razem z React i TypeScript, programiści często używają rozszerzenia „.tsx” dla swoich plików, aby wskazać, że zawierają one zarówno TypeScript, jak i JSX (rozszerzenie składni React dla JavaScript).

## Przykład pliku TSX

TypeScript umożliwia definiowanie typów zmiennych, parametrów funkcji i nie tylko. Często zobaczysz kod TypeScript w pliku „.tsx” określającym typy właściwości, stanu i innych zmiennych używanych w komponentach React.

```
// Przykład: kod TypeScript w komponencie React
interfejs MyComponentProps {
   nazwa: ciąg;
   wiek: liczba;
}
const MójKomponent: React.FC<MyComponentProps> = ({imię, wiek }) => {
   // Tutaj logika komponentów
   return <div>{name} ma {age} lat.</div>;
};
```

## JSX (rozszerzenie składni React)

JSX to rozszerzenie składni JavaScript zalecane przez React. Wygląda podobnie do XML/HTML i służy do opisu, jak powinien wyglądać interfejs użytkownika.

```
// Przykład: JSX w komponencie React
const MójKomponent: React.FC<MyComponentProps> = ({imię, wiek }) => {
   return <div>{name} ma {age} lat.</div>;
};
```

Plik „.tsx” będzie zazwyczaj zawierał definicję komponentu React przy użyciu komponentów funkcjonalnych lub komponentów klasowych.

```
// Przykład: definicja komponentu React w pliku „.tsx”.
const MójKomponent: React.FC = () => {
   return <div>Witam, reaguj!</div>;
};
```

Często na początku pliku zobaczysz instrukcje importu, wprowadzające niezbędne zależności i moduły.

```
// Przykład: Importowanie instrukcji z pliku „.tsx”.
import Reaguj z „reaguj”;
```

## Jak otworzyć plik TSX?

Pliki TSX to zwykłe pliki tekstowe, więc można je otworzyć w dowolnym edytorze tekstu, np. Notatnik. Są to jednak pliki kodujące i przeznaczone do otwarcia przez IDE np. Kod Visual Studio.