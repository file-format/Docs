{
  "date" : "2023-05-17",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aflați despre formatul de fișier NMONEY și despre API-urile care pot crea și deschide fișiere NMONEY.",
  "title" :"Fișier NMONEY - Format fișier contului Denaro",
  "linktitle" : "NMONEY",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2023-05-17"
}

## Ce este un fișier NMONEY?

Un fișier NMONEY este un fișier de bază de date de stocare a datelor financiare care conține istoricul tranzacțiilor financiare. A fost dezvoltat de Nickvision și a fost folosit în software-ul Nickvision Denaro, care este o aplicație software financiară personală. Datele stocate într-un fișier NOMONEY includ informații despre tranzacțiile de credit și debit către un cont.

Fișierele NOMONEY pot fi deschise cu aplicația [Github](https://github.com/NickvisionApps/Denaro).

## Despre Denaro Software

Denaro a fost dezvoltat inițial de [Nickvision](https://nickvision.org/) ca un produs care a fost ulterior convertit într-o aplicație software open-source găzduită pe [Github](https://github.com/NickvisionApps/Denaro) . De atunci, aplicația a fost modificată și actualizată numai pe Github. Aplicația este dezvoltată în C# în Windows UI cu Windows App SDK (WinUI 3 ca în acest moment).

### Caracteristici oferite de Denaro

* Gestionați mai multe conturi simultan cu cea mai populară și familiară interfață cu file
* Filtrați tranzacțiile după tip, grup sau dată
* Tranzacții repetate, cum ar fi facturile care apar în fiecare lună
* Transferați bani dintr-un cont în altul
* Exportați datele dintr-un cont ca fișier CSV și importați un fișier CSV, OFX sau QIF pentru a adăuga tranzacții într-un cont

## Format de fișier Denaro - Mai multe informații

Fișierele Denaro sunt salvate pe disc în format binar. Datele financiare sunt stocate ca fișier de bază de date în format de fișier **.SQLITE3**. SQLITE este un fișier de bază de date SQL ușor creat cu software-ul SQLite. Oferă un motor de bază de date autonom, care este capabil să ofere baze de date cu caracteristici complete și foarte fiabile. Fișierele bazei de date SQLite pot fi utilizate pentru a partaja conținut bogat între sisteme, prin simpla schimbare a acestor fișiere prin rețea. Legăturile SQLite există pentru limbaje de programare precum C, [C#](/ro/programming/cs/), [C++](/ro/programming/cpp/), [Java](/ro/programming/java/), [PHP](/ro/programming/php/), și multe altele.

## Referințe

* [Nickvision](https://nickvision.org/)
* [NIckVision - Github](https://github.com/NickvisionApps/Denaro)

