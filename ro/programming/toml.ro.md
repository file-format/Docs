---
date: 2019-10-11
keywords: toml, .toml, format de fișier toml, cum se deschide fișierele toml, extensia .toml, extensia toml
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format de fișier TOML
linktitle: TOML
description: "Aflați despre formatul de fișier TOML și despre API-urile care pot crea și deschide fișiere TOML."
menu:
  docs:
    parent: "programming"
lastmod: 2020-12-01
---

## Ce este un fișier TOML? ##

TOML (Tom's Obvious Minimal Language) este un format de fișier de configurare minim care utilizează extensia .toml. TOML își propune să fie ușor de citit, să mapați fără ambiguitate la dicționare și să fie ușor de analizat în diferite structuri de date. TOML are o specificație open-source care a primit contribuții ale comunității. TOML este acceptat de multe limbaje de programare precum C, C#, Dart, Elixir, Erlang, Go, Java, PHP, Python, Ruby, Swift etc. Tipul MIME pentru fișierele TOML este *application/toml*.


## Format de fișier TOML ##

Fișierele TOML constau în principal din perechi cheie/valoare, secțiuni/tabele, comentarii și trebuie să fie un document Unicode codificat UTF-8 valid. TOML acceptă tipurile de date String, Integer, Float, Boolean, Datetime, Array și Table (tabel hash/dicționar). TOML este un limbaj sensibil la majuscule.

### Sintaxă ###

- **Perechi cheie-valoare**: perechile cheie-valoare sunt separate prin semnul egal (=). Fiecare pereche trebuie să fie pe o linie nouă.

```toml
primul = "Tom"
ultimul = "Preston-Werner"
```

- **Comentarii**: Comentariile încep cu simbolul hash (#).

```toml
# Acesta este un document TOML.
```

- **Șiruri**: Șirurile sunt înconjurate de ghilimele (").

```toml
șir = „Exemplu șir”
```

- **Șiruri cu mai multe linii**: Șirurile cu mai multe linii sunt înconjurate de trei ghilimele ("").

```toml
[adresa de acasa]
strada = """123 Tornado Alley
Suită 16"""
oraș = „East Centerville”
stare = "KS"
```

- **Numerele întregi/flotante**

```toml
întreg = 20
plutitor = 20,5
```

- **Booleans**: Booleans sunt întotdeauna litere mici.

```toml
bool1 = adevărat
bool2 = fals
```

- **Date-Ora**: pentru DateTime, puteți utiliza un format RFC 3339 data-ora, așa cum se arată în exemplul de mai jos.

```toml
offset_date_time = 1979-05-27 07:32:00Z
local_date_time = 1979-05-27T07:32:00
data_locală = 1979-05-27
ora_locală = 07:32:00
```

- **Matrice**: Matricele sunt înconjurate de paranteze drepte cu elemente separate prin virgulă (,).

```toml
culori = [ „rosu”, „galben”, „verde”]
```

- **Tabelele**: Tabelele sunt colecții de perechi cheie/valoare care sunt definite de anteturi pe o nouă linie înconjurată de paranteze drepte ([]). Tabelul se termină când este furnizat un nou antet sau când fișierul se termină.

```toml
[adresa de acasa]
strada = """123 Tornado Alley
Suită 16"""
oraș = „East Centerville”
stare = "KS"

[adresa biroului]
strada = """123 Tornado Alley
Suită 16"""
oraș = „East Centerville”
stare = "KS"
```

Tabelele în linie sunt înconjurate de acolade ({}), fiecare pereche cheie/valoare separată prin virgulă (,).

```toml
nume = { primul = "Tom", ultimul = "Pitt" }
```

## Referințe ##

- [TOML - Wikipedia](https://en.wikipedia.org/wiki/TOML)
- [TOML](https://toml.io/en/)

