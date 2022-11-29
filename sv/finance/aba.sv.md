{
  "date" : "2019-10-11",
  "keywords" :[ "aba fil", "aba filformat", "vad är en aba fil", "fil", "aba exempel", "aba filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ABA - CemText File Format",
  "description":"Läs mer om ABA-filformat och API:er som kan skapa och öppna ABA-filer.",
  "linktitle" : "ABA",
  "menu" : {
    "docs" : {
      "identifier":"finance-aba",
      "parent" : "finance"
}
},
  "lastmod" : "2121-03-24"
}

## Vad är ABA fil?

En fil med filtillägget .aba är en Australian Bankers Association (ABA) eller filformatet [Cemtext](https://www.cemtexaba.com/) som används av banker för batchtransaktioner. Det används av de flesta banker för finansiell redovisning. Även känd som en Direct Entry-fil, har ABA-filformatet antagits av de flesta australiska banker som standardformat för batchtransaktioner. Det har fortfarande inte erkänts som standardformat trots att det har använts av Bank of Queensland, NAB och Westpac. ABA-filer kan öppnas med vilken textredigerare som helst som Notepad++.


## ABA filformat

En ABA-fil använder ASCII-formatet för att lagra data för vidarebefordran eller inläsning i banksystem. Formatet har hållits enkelt för att göra det enkelt för integrering i företagens egna ekonomisystem att bearbeta batcher av transaktioner. Till exempel, i ett lönesystem kan ett parti transaktioner laddas upp för att bearbetas i en träff. ABA-filformatsspecifikationerna finns tillgängliga som fullständig transkription på webbplatsen [Cemtext ABA](https://www.cemtexaba.com/aba-format/cemtex-aba-file-format-details) och kan hänvisas till för utvecklarnas referens .

En ABA-fil består av flera rader där varje rad är känd som en "post". Det finns tre huvudposter i en ABA-fil:

* Beskrivande rekord
* Detaljpost
* File Total Record

### Beskrivande post

En "Beskrivande post" innehåller information som rullsekvensnummer, namn på användarens finansiella institut, namn på användningsfil och annan information.

### Detaljpost

Typen "Detaljpost" inkluderar information som bank-/stat-/filialnummer, kontonummer som ska krediteras/debiteras, indikator, transaktionskod, belopp och annan information.

### File Total Record

Typen "File Total Record" inkluderar posttyp 7, BSB Format Filler, Fil (användare) nettototalbelopp, fil (användare) kredit totalt belopp, fil (användare) debiteringssumma och annan information.

### Transaktionskoder

En lista över giltiga transaktionskoder är följande. För det mesta används koden "53 - Pay" i ABA-filer. Dessa transaktionskoder omfattar debeter, krediter och källskatter.

|Kod|Transaktionsbeskrivning|
---|---|
|13|Externt initierade debetposter|
|50|Externt initierade kreditposter med undantag för de som har transaktionskoder|
|51|Australiens regerings säkerhetsintresse|
|52|Familjebidrag|
|53|Betala|
|54|Pension|
|55|Tilldelning|
|56|Utdelning|
|57|Skuldebrev/Noteränta|

## Exempel på ABA-fil

```
0                 01BQL       MY NAME                   1111111004231633  230410
1123-456157108231 530000001234S R SMITH                       TEST BATCH        062-000 12223123MY ACCOUNT      00001200
1123-783 12312312 530000002200J K MATTHEWS                    TEST BATCH        062-000 12223123MY ACCOUNT      00000030
1456-789   125123 530003123513P R JONES                       TEST BATCH        062-000 12223123MY ACCOUNT      00000000
1121-232    11422 530000002300S MASLIN                        TEST BATCH        062-000 12223123MY ACCOUNT      00000000
7999-999            000312924700031292470000000000                        000004
```
## Referenser

* [Cemtext ABA](https://www.cemtexaba.com/)

