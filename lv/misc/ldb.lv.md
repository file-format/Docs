{
  "date": "2023-04-20",
  "keywords": [
"ldb failu",
"kas ir ldb fails",
"kādu informāciju ldb satur",
"kāds ir ldb faila mērķis",
"ldb paplašinājums",
"failu",
"pagarinājumu"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "LDB faila formāts — Microsoft Access bloķēšanas fails",
  "description": "Uzziniet par LDB formātu un kādu informāciju tas satur.",
  "linktitle": "LDB",
  "menu": {
    "docs": {
      "identifier": "misc-ldb-lv",
      "parent": "misc"
}
},
  "lastmod": "2023-04-20"
}

## Kas ir LDB fails?

LDB fails ir bloķēšanas fails, ko Microsoft Access izmanto, lai neļautu vairākiem lietotājiem vienlaikus rediģēt vienu un to pašu datu bāzi. Kad lietotājs atver Access datu bāzi, Access izveido atbilstošu LDB failu tajā pašā direktorijā, kur datu bāze. Šajā failā ir informācija par to, kurš pašlaik izmanto datu bāzi un kādus ierakstus viņi rediģē.

LDB failu automātiski izveido Microsoft Access, kad tiek atvērta datu bāze, un tiek dzēsta, kad datu bāze tiek aizvērta. Ir svarīgi atzīmēt, ka LDB failu nekad nevajadzētu dzēst manuāli, jo tas var radīt problēmas ar datu bāzi.

Ja rodas problēmas ar Microsoft Access datu bāzi, viens no iespējamiem risinājumiem ir mēģināt dzēst ar šo datu bāzi saistīto LDB failu. Tādējādi tiks atbrīvotas visas bloķēšanas, kas var traucēt jums piekļūt datu bāzei. Tomēr, pirms mēģināt veikt šo darbību, noteikti izveidojiet datu bāzes dublējumu, jo LDB faila dzēšana var izraisīt datu zudumu vai sabojāšanu, ja tas tiek darīts nepareizi.

## LDB faila formāts — vairāk informācijas

LDB failā programmā Microsoft Access ir ietverta informācija par lietotājiem, kuri pašlaik piekļūst datu bāzei, piemēram, viņu lietotājvārds, datora nosaukums un pieteikšanās laiks. LDB failā ir arī informācija par jebkādām bloķēšanām, kas ir ievietotas datu bāzē, piemēram, kādus ierakstus kurš lietotājs rediģē.

Šeit ir detalizētāks to informācijas veidu saraksts, ko var atrast LDB failā:

- **Lietotājvārds** - tā lietotāja vārds, kurš pašlaik piekļūst datu bāzei
- **Datora nosaukums** - tā datora nosaukums, no kura lietotājs piekļūst datu bāzei
- **Pieteikšanās laiks** - laiks, kad lietotājs pirmo reizi atvēra datu bāzi
- **Ierakstu bloķētāji** - informācija par to, kurus ierakstus kurš lietotājs pašlaik rediģē
- **Objektu bloķēšanas** - informācija par to, kurus datu bāzes objektus (piemēram, tabulas, veidlapas vai atskaites) kurš lietotājs pašlaik rediģē.
- **Savienojuma informācija** - informācija par to, kā lietotājs ir savienots ar datu bāzi (piemēram, vai viņš izmanto lokālo vai tīkla savienojumu)

LDB failā esošo informāciju izmanto Microsoft Access, lai neļautu vairākiem lietotājiem vienlaikus veikt pretrunīgas izmaiņas vienā datu bāzē. Kad lietotājs mēģina rediģēt ierakstu vai objektu, ko jau ir bloķējis cits lietotājs, Microsoft Access parādīs ziņojumu, kas norāda, ka objekts jau tiek izmantots. LDB fails tiek atjaunināts, kad lietotāji atver un aizver datu bāzi un veic izmaiņas bloķētajos objektos.

## Atsauces
* [What is an LDB File?](https://learn.microsoft.com/en-us/office/troubleshoot/access/ldb-file-description)

