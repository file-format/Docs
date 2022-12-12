{
  "date" : "2019-10-11",
  "keywords" :[ "fișier aba", "format fișier aba", "ce este un fișier aba", "fișier", "exemplu aba", "extensie fișier aba", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ABA - CemText File Format",
  "description":"Aflați despre formatul de fișier ABA și despre API-urile care pot crea și deschide fișiere ABA.",
  "linktitle" : "ABA",
  "menu" : {
    "docs" : {
      "identifier":"finance-aba",
      "parent" : "finance"
}
},
  "lastmod" : "2121-03-24"
}

## Ce este un fișier ABA?

Un fișier cu extensia .aba este formatul de fișier al Asociației Bancherilor din Australia (ABA) sau [Cemtext](https://www.cemtexaba.com/), care este folosit de bănci pentru tranzacții în loturi. Este folosit de majoritatea băncilor pentru evidența financiară. Cunoscut și ca fișier de intrare directă, formatul de fișier ABA a fost adoptat de majoritatea băncilor australiene ca format implicit pentru tranzacțiile în lot. Încă nu a fost recunoscut ca format standard, în ciuda faptului că a fost utilizat de Bank of Queensland, NAB și Westpac. Fișierele ABA pot fi deschise cu orice editor de text, cum ar fi Notepad++.


## Format de fișier ABA

Un fișier ABA utilizează formatul ASCII pentru a stoca date pentru redirecționare sau încărcare în sistemele bancare. Formatul a fost păstrat simplu pentru a facilita integrarea în sistemul financiar propriu al companiilor pentru a procesa loturi de tranzacții. De exemplu, într-un sistem de salarizare, un lot de tranzacții poate fi încărcat pentru a fi procesat într-o singură lovitură. Specificațiile de format de fișier ABA sunt disponibile ca transcriere completă pe site-ul web [Cemtext ABA](https://www.cemtexaba.com/aba-format/cemtex-aba-file-format-details) și pot fi consultate pentru referință pentru dezvoltatori .

Un fișier ABA constă din mai multe linii în care fiecare linie este cunoscută ca „înregistrare”. Există trei înregistrări principale într-un fișier ABA:

* Înregistrare descriptivă
* Înregistrare de detaliu
* Înregistrare totală a fișierului

### Înregistrare descriptivă

O „Înregistrare descriptivă” conține informații precum numărul de secvență al rolei, numele instituției financiare a utilizatorului, numele utilizării fișierului care furnizează și alte informații.

### Înregistrare de detaliu

Tipul „Înregistrare detaliată” include informații precum Numărul băncii/statului/sucursalului, numărul contului de creditat/debitat, indicator, codul tranzacției, sumă și alte informații.

### Înregistrare totală fișier

Tipul „Înregistrare totală fișier” include tipul de înregistrare 7, completarea formatului BSB, suma totală netă a fișierului (utilizator), suma totală a creditului fișierului (utilizator), suma totală a debitului fișierului (utilizator) și alte informații.

### Coduri de tranzacție

O listă de coduri de tranzacție valide este următoarea. De cele mai multe ori, codul „53 - Pay” este folosit în fișierele ABA. Aceste coduri de tranzacție includ debite, credite și impozite reținute la sursă.

|Cod|Descrierea tranzacției|
---|---|
|13|Elemente de debit inițiate extern|
|50|Elementele de credit inițiate extern, cu excepția celor care poartă coduri de tranzacție|
|51|Interesul de securitate al guvernului australian|
|52|Alocatie familiala|
|53|Plătește|
|54|Pensiune|
|55|Alocatie|
|56|Dividende|
|57|Dobânzi de obligație/Notă|

## Exemplu de fișier ABA

```
0                 01BQL       MY NAME                   1111111004231633  230410
1123-456157108231 530000001234S R SMITH                       TEST BATCH        062-000 12223123MY ACCOUNT      00001200
1123-783 12312312 530000002200J K MATTHEWS                    TEST BATCH        062-000 12223123MY ACCOUNT      00000030
1456-789   125123 530003123513P R JONES                       TEST BATCH        062-000 12223123MY ACCOUNT      00000000
1121-232    11422 530000002300S MASLIN                        TEST BATCH        062-000 12223123MY ACCOUNT      00000000
7999-999            000312924700031292470000000000                        000004
```
## Referințe

* [Cemtext ABA](https://www.cemtexaba.com/)

