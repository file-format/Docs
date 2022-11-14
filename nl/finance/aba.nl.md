{
  "date" : "2019-10-11",
  "keywords" :[ "aba file", "aba file format", "wat is een aba file", "file", "aba example", "aba file extension","extension", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ABA - CemText-bestandsindeling",
  "description":"Meer informatie over ABA-bestandsindeling en API's die ABA-bestanden kunnen maken en openen.",
  "linktitle" : "ABA",
  "menu" : {
    "docs" : {
      "identifier":"finance-aba",
      "parent" : "finance"
}
},
  "lastmod" : "2121-03-24"
}

## Wat is een ABA-bestand?

Een bestand met de extensie .aba is een Australian Bankers Association (ABA) of het [Cemtext](https://www.cemtexaba.com/) bestandsformaat dat door banken wordt gebruikt voor batchtransacties. Het wordt door de meeste banken gebruikt voor het bijhouden van financiële gegevens. Ook bekend als een Direct Entry-bestand, is het ABA-bestandsformaat door de meeste Australische banken overgenomen als standaardformaat voor batchtransacties. Het is nog steeds niet erkend als standaardformaat, ondanks het feit dat het in gebruik is geweest door Bank of Queensland, NAB en Westpac. ABA-bestanden kunnen worden geopend met elke teksteditor zoals Notepad++.


## ABA-bestandsindeling

Een ABA-bestand gebruikt het ASCII-formaat om gegevens op te slaan voor doorsturen of laden in banksystemen. Het formaat is eenvoudig gehouden om het gemakkelijk te maken voor integratie in het eigen financiële systeem van het bedrijf om batches transacties te verwerken. In een salarissysteem kan bijvoorbeeld een batch transacties worden geüpload om in één hit te worden verwerkt. De specificaties van de ABA-bestandsindeling zijn beschikbaar als volledige transcriptie op de website [Cemtext ABA](https://www.cemtexaba.com/aba-format/cemtex-aba-file-format-details) en er kan naar worden verwezen als referentie voor ontwikkelaars .

Een ABA-bestand bestaat uit meerdere regels waarbij elke regel een 'record' wordt genoemd. Er zijn drie hoofdrecords in een ABA-bestand:

* Beschrijvend record
* Detailopname
* Bestand totaal record

### Beschrijvend record

Een 'Beschrijvend record' bevat informatie zoals het spoelvolgnummer, de naam van de financiële instelling van de gebruiker, het aanleverbestand voor de naam van het gebruik en andere informatie.

### Detailopname

Het type 'Detailrecord' omvat informatie zoals bank-/staats-/filiaalnummer, rekeningnummer dat moet worden gecrediteerd/gedebiteerd, indicator, transactiecode, bedrag en andere informatie.

### Bestand Totaal Record

Het type "Bestandstotaalrecord" omvat recordtype 7, BSB-formaatvuller, nettototaalbedrag bestand (gebruiker), totaal kredietbedrag bestand (gebruiker), totaal debetbedrag bestand (gebruiker) en andere informatie.

### Transactiecodes

Een lijst met geldige transactiecodes is als volgt. Meestal wordt de code "53 - Betalen" gebruikt in ABA-bestanden. Deze transactiecodes omvatten debet-, credit- en bronbelastingen.

|Code|Transactiebeschrijving|
---|---|
|13|Extern geïnitieerde debetposten|
|50|Extern geïnitieerde kredietposten met uitzondering van die met transactiecodes|
|51|Veiligheidsbelang van de Australische overheid|
|52|Gezinsbijslag|
|53|Betalen|
|54|Pensioen|
|55|Toewijzing|
|56|Dividend|
|57|Obligatie/Note Rente|

## ABA-bestandsvoorbeeld

```
0                 01BQL       MY NAME                   1111111004231633  230410
1123-456157108231 530000001234S R SMITH                       TEST BATCH        062-000 12223123MY ACCOUNT      00001200
1123-783 12312312 530000002200J K MATTHEWS                    TEST BATCH        062-000 12223123MY ACCOUNT      00000030
1456-789   125123 530003123513P R JONES                       TEST BATCH        062-000 12223123MY ACCOUNT      00000000
1121-232    11422 530000002300S MASLIN                        TEST BATCH        062-000 12223123MY ACCOUNT      00000000
7999-999            000312924700031292470000000000                        000004
```
## Referenties

* [Cemtext ABA](https://www.cemtexaba.com/)

