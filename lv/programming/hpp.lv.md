{
  "date": "2023-06-08",
  "keywords": [
"hpp failu",
"kas ir hpp fails",
"ko satur hpp fails",
"hpp faila piemērs",
"kāds ir hpp faila formāts",
"failu",
"hpp faila paplašinājums",
"pagarinājumu"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "HPP faila formāts - C++ galvenes fails",
  "description": "Uzziniet par HPP formātu un API, kas var izveidot un atvērt HPP failus.",
  "linktitle": "HPP",
  "menu": {
    "docs": {
      "identifier": "programming-hpp-lv",
      "parent": "programming"
}
},
  "lastmod": "2023-06-08"
}

## Kas ir HPP fails?

.hpp faila formāts parasti tiek izmantots galvenes failiem C++ programmēšanas valodā. Galvenes faili parasti satur deklarācijas un funkciju, klašu, mainīgo un konstantu definīcijas, ko izmanto citi avota koda faili C++ projektā.

Galvenes failu izmantošanas mērķis ir nodrošināt veidu, kā koplietot kopīgu kodu vairākos avota koda failos, nedublējot pašu kodu. Ja C++ avota failam ir jāpiekļūst deklarācijām vai definīcijām no galvenes faila, tas ietver galvenes failu, izmantojot priekšapstrādātāja direktīvu #include.

Faila paplašinājumu .hpp bieži izmanto, lai norādītu, ka fails ir C++ galvenes fails. Galvenes failiem nav obligāti jāizmanto šis konkrētais paplašinājums, un jūs varat saskarties arī ar galvenes failiem ar .h vai citiem paplašinājumiem. Pagarinājuma izvēle lielā mērā ir atkarīga no vienošanās un personīgās izvēles.

Ja C++ avota failā ir iekļauts galvenes fails, izmantojot #include”, kompilators efektīvi apvieno galvenes faila saturu ar avota failu, pirms to kompilē kā vienību. Tas ļauj avota failam piekļūt deklarācijām un definīcijām galvenes failā, nodrošinot kompilatoram nepieciešamo informāciju, lai veiktu tipa pārbaudi un koda ģenerēšanu.

## Ko satur HPP fails?

Šeit ir daži izplatīti saturs, ko varat atrast failā .hpp.

- **Funkciju deklarācijas:** galvenes faili bieži ietver funkciju deklarācijas bez to faktiskās ieviešanas. Šīs deklarācijas sniedz informāciju par funkcijas nosaukumu, atgriešanas veidu un parametriem, ļaujot citiem pirmkoda failiem izmantot funkciju bez nepieciešamības uzzināt ieviešanas detaļas.
- **Klases deklarācijas:** galvenes faili var saturēt klašu deklarācijas, tostarp klases nosaukumu, dalībnieku mainīgos, dalībnieku funkcijas un piekļuves specifikācijas. Iekļaujot klases deklarāciju galvenes failā, citi pirmkoda faili var izveidot šīs klases objektus un piekļūt tās dalībniekiem.
- **Pastāvīgās deklarācijas:** galvenes faili var definēt konstantes, piemēram, globālos mainīgos vai enum vērtības, kas ir paredzētas koplietošanai vairākos avota koda failos. Šīm konstantēm var piekļūt, iekļaujot galvenes failu citos avota failos, ļaujot tiem izmantot noteiktās konstantes.
- **Veidu definīcijas:** galvenes failos var būt tipu definīcijas, izmantojot atslēgvārdu typedef, vai tipa aizstājvārdi, izmantojot atslēgvārdu izmantojot. Šīs definīcijas izveido jaunus nosaukumus esošajiem tipiem, padarot kodu lasāmāku un uzturējamāku.
- **Iekļautās funkciju definīcijas:** dažos gadījumos galvenes failos var būt iekļautas funkciju definīcijas. Iekļautās funkcijas ir mazas funkcijas, kas tiek paplašinātas zvana vietā, nevis tiek izsauktas kā atsevišķa funkcija. Iekļautās funkcijas definīcijas iekļaušana galvenes failā ļauj kompilatoram tieši aizstāt funkcijas izsaukumu ar funkcijas pamattekstu, potenciāli uzlabojot veiktspēju.

## HPP faila piemērs

```
#ifndef PERSON_HPP
#define PERSON_HPP

#include <string>

class Person {
private:
    std::string name;
    int age;

public:
    Person();
    Person(const std::string& name, int age);
    void setName(const std::string& newName);
    void setAge(int newAge);
    std::string getName() const;
    int getAge() const;
    void printInfo() const;
};

#endif

```

## Kāds ir HPP faila formāts?

HPP ir vienkārša teksta fails, taču tas ievēro C++ programmēšanas valodas vispārīgos noteikumus un sintakse. Tālāk ir sniegts .hpp faila vispārējā formāta un struktūras sadalījums:

- **Galvenes aizsargi:** parasti .hpp fails sākas ar galvenes aizsargiem, lai novērstu viena faila vairāku iekļaušanu. Tas tiek panākts, izmantojot priekšapstrādātāja direktīvas, piemēram, #ifndef, #define un #endif. Galvenes aizsargs nodrošina, ka faila saturs tiek iekļauts tikai vienu reizi kompilācijas procesā.
- **Iekļaut paziņojumus:** pēc galvenes aizsargiem varat iekļaut citus nepieciešamos galvenes failus, izmantojot direktīvu #include. Tie var ietvert standarta bibliotēkas galvenes vai citas pielāgotas galvenes, kas nepieciešamas jūsu kodam.
- **Deklarācijas un definīcijas:** .hpp faila primārais saturs ir deklarācijas un dažos gadījumos klašu, funkciju, konstantu, tipa aizstājvārdu un citu elementu definīcijas. Piemēram, varat deklarēt klases, izmantojot atslēgvārdu class”, funkcijas, izmantojot to atgriešanas veidu, nosaukumu un parametru sarakstu, un konstantes, izmantojot atslēgvārdu const”, kam seko to veids un nosaukums.
- **Iekļautās funkciju definīcijas:** noteiktos gadījumos varat iekļaut iekļautās funkciju definīcijas tieši .hpp failā. Iekļautās funkcijas parasti tiek definētas klases pamattekstā, kas nozīmē, ka funkcijas definīcija ir iekļauta līdzās tās deklarācijai. To var izdarīt, pirms funkcijas definīcijas pievienojot atslēgvārdu iekļauts.
- **Nosaukumvietas deklarācijas:** ja kodā izmantojat nosaukumvietas, varat tās deklarēt failā .hpp. Tas tiek darīts, izmantojot atslēgvārdu namespace”, kam seko nosaukumvietas nosaukums un iekļaujot attiecīgo kodu nosaukumvietas blokā.

## Atsauces
* [Galvenes faili (C++)](https://learn.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)


