---
date: 2019-10-11
keywords: toml, .toml, formato file toml, come aprire file toml, estensione .toml, estensione toml
autore:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formato file TOML
linktitle: TOML
description: "Scopri il formato di file TOML e le API che possono creare e aprire file TOML."
menu:
  docs:
    parent: "programming"
lastmod: 2020-12-01
---

## Che cos'è un file TOML? ##

TOML (Tom's Obvious Minimal Language) è un formato di file di configurazione minimo che utilizza l'estensione .toml. TOML mira a essere di facile lettura, a mappare in modo inequivocabile i dizionari e ad essere facile da analizzare in diverse strutture di dati. TOML ha una specifica open source che ha ricevuto contributi dalla comunità. TOML è supportato da molti linguaggi di programmazione come C, C#, Dart, Elixir, Erlang, Go, Java, PHP, Python, Ruby, Swift, ecc. Il tipo MIME per i file TOML è *application/toml*.


## Formato file TOML ##

I file TOML sono costituiti principalmente da coppie chiave/valore, sezioni/tabelle, commenti e devono essere un documento Unicode con codifica UTF-8 valido. TOML supporta i tipi di dati String, Integer, Float, Boolean, Datetime, Array e Table (tabella hash/dizionario). TOML è un linguaggio con distinzione tra maiuscole e minuscole.

### Sintassi ###

- **Coppie chiave-valore**: le coppie chiave-valore sono separate dal segno di uguale (=). Ogni coppia deve trovarsi su una nuova riga.

```toml
primo = "Tom"
last = "Preston-Werner"
```

- **Commenti**: i commenti iniziano con il simbolo cancelletto (#).

```toml
# Questo è un documento TOML.
```

- **Stringhe**: le stringhe sono racchiuse tra virgolette (").

```toml
stringa = "Stringa di esempio"
```

- **Stringhe su più righe**: le stringhe su più righe sono racchiuse tra tre virgolette (""").

```toml
[indirizzo di casa]
strada = """123 Tornado Alley
Suite 16"""
città = "Centro orientale"
stato = "KS"
```

- **Interi/virgola mobile**

```toml
intero = 20
galleggiante = 20,5
```

- **Booleani**: i booleani sono sempre minuscoli.

```toml
bool1 = vero
bool2 = falso
```

- **Date-Time**: per DateTime, puoi utilizzare una data-ora formattata RFC 3339 come mostrato nell'esempio seguente.

```toml
offset_data_ora = 1979-05-27 07:32:00Z
data_ora_locale = 27-05-1979 T07:32:00
data_locale = 27-05-1979
ora_locale = 07:32:00
```

- **Matrici**: le matrici sono racchiuse tra parentesi quadre con elementi separati da virgole (,).

```toml
colori = [ "rosso", "giallo", "verde" ]
```

- **Tabelle**: le tabelle sono raccolte di coppie chiave/valore definite da intestazioni su una nuova riga racchiusa tra parentesi quadre ([]). La tabella termina quando viene fornita una nuova intestazione o quando il file termina.

```toml
[indirizzo di casa]
strada = """123 Tornado Alley
Suite 16"""
città = "Centro orientale"
stato = "KS"

[indirizzo dell'ufficio]
strada = """123 Tornado Alley
Suite 16"""
città = "Centro orientale"
stato = "KS"
```

Le tabelle inline sono racchiuse tra parentesi graffe ({}) con ciascuna coppia chiave/valore separata da virgola (,).

```toml
nome = { primo = "Tom", ultimo = "Pitt" }
```

## Riferimenti ##

- [TOML - Wikipedia](https://en.wikipedia.org/wiki/TOML)
- [TOML](https://toml.io/en/)

