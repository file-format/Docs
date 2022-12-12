{
  "date" : "2020-11-11",
  "keywords" :[ "DDL", "extensie", "fișier", "format fișier", "Tip fișier bază de date", "Format fișier bază de date", "Fișiere bază de date"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aflați despre formatul de fișier DDL și despre API-urile care pot crea și deschide fișiere DDL.",
  "title" :"Format de fișier DDL - Un fișier de limbă de definire a datelor",
  "linktitle" : "DDL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-11"
}

## Ce este un fișier DDL?

Un fișier cu extensia .ddl este un fișier Data Definition Language care este utilizat pentru a defini schema unei baze de date. Conține instrucțiuni/comenzi pentru lucrul cu structuri de baze de date, cum ar fi tabele, coloane, înregistrări și alte câmpuri. Comenzile dintr-un fișier DDL sunt scrise în [SQL](/ro/database/sql/) și pot efectua operațiuni precum crearea tabelului în baza de date, eliminarea și actualizarea. O schemă de bază de date este deținută de ea creată și toate operațiunile CRUD pot fi efectuate pe ea. Aplicațiile populare care pot crea și deschide fișiere DDL sunt Windows Text Editor, Jetbrains Intellij Idea și EclipseLink.

## comenzi DDL

Un singur fișier DDL poate conține mai multe comenzi care, datorită sintaxei corecte, se vor executa în secvență și vor aduce modificări schemei, cum ar fi crearea de seturi de caractere și tabele, eliminarea tabelelor, redenumirea și modificarea tabelelor. Următoarele comenzi DDL sunt utilizate în mod obișnuit în timpul lucrului cu schema bazei de date.

`CREATE` - Folosit pentru a crea baza de date sau obiectele acesteia (cum ar fi tabelul, indexul, funcția, vizualizările, procedura de stocare și declanșatoarele).

`DROP` – Folosit pentru a șterge obiecte din baza de date.

`ALTER` - Folosit pentru a modifica structura bazei de date.

`TRUNCATE` – Folosit pentru a elimina toate înregistrările dintr-un tabel, inclusiv toate spațiile alocate pentru înregistrările sunt eliminate.

`COMMENT` – Adaugă comentarii la dicționarul de date.

`RENAME` – Redenumește un obiect existent în baza de date.

## Exemplu DDL

Următorul exemplu arată instrucțiunea DDL pentru comanda CREATE care creează un tabel și definește câmpurile acestuia.

```
CREATE TABLE employees (
    id            INTEGER       PRIMARY KEY,
    first_name    VARCHAR(50)   not null,
    last_name     VARCHAR(75)   not null,
    fname         VARCHAR(50)   not null,
    dateofbirth   DATE          not null
);
```

## Referințe ##

* [DDL de Wikipedia](https://en.wikipedia.org/wiki/Data_definition_language)

