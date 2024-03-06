---
date: 2019-10-11
keywords: java, .java, java file format, how to open java files, how to run java files, java file, java sample code
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Java faila veidlapaat
linktitle: Java
description: Lnopelniet par Java faila formātu un API, kas var izveidot un atvērt Java failus.
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-07
---

## Kas ir Java fails? ##
Fails, kas satur Java avota kodu un saglabāts ar .java faila paplašinājumu, ir zināms kā Java fails. Java ir viena no visplašāk izmantotajām tehnoloģijām spēļu, mobilo, tīmekļa un galddatoru lietojumprogrammu izstrādei. Tā kā Java ir neatkarīga no platformas, tā darbojas nevainojami operētājsistēmās Windows, Mac, Linux, Raspberry Pi utt. Java ir ļoti līdzīga C# un C++, tāpēc ir vieglāk pārslēgties starp šīm valodām.

## Īsa vēsture ##

Java projektu 1991. gada jūnijā aizsāka Džeimss Goslings, Maiks Šeridans un Patriks Netons. Java sākotnēji tika nosaukta par Ozolu. Vēlāk to pārdēvēja par Green un beidzot par Java. Džeimss Goslings izstrādāja Java ar sintaksi, kas līdzīga C/C++. Pirmo publisko Java versiju 1996. gadā izlaida Sun Microsystems. Tas varētu darboties visās populārajās sistēmās, kuru dēļ Java ātri kļuva populāra. Līdz ar Java 2 izlaišanu 1998. gada decembrī tika izveidotas vairākas konfigurācijas dažāda veida platformām. Versijas bija šādas

- J2EE (Java EE): uzņēmumu risinājumiem
- J2ME (Java ME): mobilajām lietojumprogrammām
- J2SE (Java SE): darbvirsmas lietojumprogrammām

2006. gada 19. novembrī uzņēmums Sun izlaida Java virtuālo mašīnu (JVM) kā bezmaksas atvērtā pirmkoda programmatūru. Pēc tam, kad Oracle Corporation 2009.–2010. gadā iegādājās Sun Microsystems, Džeimss Goslings 2010. gada 2. aprīlī atkāpās no Oracle.

## Kā palaist/izpildīt Java kodu ##

Lai izpildītu Java kodu, tas vispirms ir jākompilē. Šim nolūkam ir nepieciešams Java SDK. Java SDK apkopo Java kodu baitkoda klases failā. Ir IDE, piemēram, Eclipse un IntelliJ Idea, kas atvieglo darbu ar Java failiem, nodrošinot koda pabeigšanu un viegli lietojamu interfeisu Java koda apkopošanai un izpildei.

## Java faila formāts ##

Java sintaksi ļoti ietekmēja C un C++, taču atšķirībā no C++ Java tika veidota gandrīz tikai kā objektorientēta valoda. Java valodā viss kods ir rakstīts klasēs, un katrs datu vienums ir objekts. Atšķirībā no C++, Java neatbalsta operatora pārslodzi vai vairāku mantojumu.

### Java parauga kods ###

Tālāk ir sniegts Java sintakses piemērs.

```java
/*
The example code prints
Hello World from Java to the console.
*/
    public class ExampleApp {
        public static void main(String[] args) {
            System.out.println("Hello World from Java"); // Prints the string to the console.
        }
    }
```
Iepriekš minētajā kodā atslēgvārds **publisks** apzīmē piekļuves pārveidotāju. Tajā teikts, ka šai klasei var piekļūt klases ārpus klases hierarhijas. Piekļuves modifikators var būt arī **aizsargāts** (var piekļūt tajā pašā pakotnē) vai **privāts** (metodēm var piekļūt tikai viena un tā pati klase). **static** pirms metodes norāda, ka metodi var izsaukt bez konkrēta klases gadījuma. ** Void** norāda, ka metode neko neatgriezīs. Lai izdrukātu virkni konsolē. Tiek izmantota komanda System.out.println. Šajā komandā *System* klasei ir statisks lauks *out*, kas ir *PrintStream* klases gadījums, kurā ir *println* metode.

Java failu faila nosaukumam ir jābūt tādam pašam kā klases nosaukumam. Tātad parauga koda Java faila nosaukums būtu *ExampleApp.java*.

## Atsauces Nr.

- [Java (programming language) - Wikipedia](https://en.wikipedia.org/wiki/Java_(programming_language))

