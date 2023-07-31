{
  "date" : "2019-10-11",
  "keywords" :[ "cshtml", "αρχείο cshtml", "μορφή αρχείου cshtml", "τύπος αρχείου cshtml", "αρχείο", "τύπος", "τι είναι ένα αρχείο cshtml" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CSHTML - Ιστοσελίδα ASP.NET Razor",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου CSHTML και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία CSHTML.",
  "linktitle" : "CSHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-04-29"
}

## Τι είναι ένα αρχείο CSHTML;

Ένα αρχείο με επέκταση .cshtml είναι ένα αρχείο HTML [C#](/el/programming/cs/) που χρησιμοποιείται στον διακομιστή από τη μηχανή Razor Markup για απόδοση των αρχείων ιστοσελίδας στο πρόγραμμα περιήγησης του χρήστη. Αυτή η κωδικοποίηση από την πλευρά του διακομιστή είναι παρόμοια με την τυπική σελίδα ASP.NET που επιτρέπει τη δυναμική δημιουργία περιεχομένου ιστού εν κινήσει καθώς η ιστοσελίδα εγγράφεται στο πρόγραμμα περιήγησης. Ο διακομιστής εκτελεί τον κώδικα από την πλευρά του διακομιστή μέσα στη σελίδα πριν στείλει τη σελίδα που δημιουργήθηκε στο πρόγραμμα περιήγησης. Πολύπλοκες εργασίες όπως η πρόσβαση σε βάσεις δεδομένων και η απόδοση σύνθετων προβολών. Τα αρχεία CSHTML μπορούν να δημιουργηθούν και να προγραμματιστούν χρησιμοποιώντας το Microsoft Visual Studio.

## Μορφή αρχείου CSHTML

Τα αρχεία CSHTML είναι αρχεία κειμένου που ακολουθούν τη σύνταξη που περιγράφεται από τη μηχανή σήμανσης Razor. Το Razor υποστηρίζει και C# και VB.NET και είναι εύκολο στην εκμάθηση και τη χρήση από τα κλασικά ASP και ASP.NET. Το w3schools διαθέτει έναν απλό αλλά αποτελεσματικό οδηγό για την κωδικοποίηση [σύνταξη C# και VB.NET](https://www.w3schools.com/asp/razor_syntax.asp) του Razor.

### Παράδειγμα CSHTML

Ακολουθεί παράδειγμα κώδικα C# που χρησιμοποιείται σε ένα αρχείο CSHTML για το Razor.

```
<!-- Single statement block -->
@{ var myMessage = "Hello World"; }

<!-- Inline expression or variable -->
<p>The value of myMessage is: @myMessage</p>

<!-- Multi-statement block -->
@{
var greeting = "Welcome to our site!";
var weekDay = DateTime.Now.DayOfWeek;
var greetingMessage = greeting + " Here in Huston it is: " + weekDay;
}
<p>The greeting is: @greetingMessage</p>
```

Ο ισοδύναμος κωδικός VB.NET για το Razor είναι ο ακόλουθος.

```
<!-- Single statement block  -->
@Code dim myMessage = "Hello World" End Code

<!-- Inline expression or variable -->
<p>The value of myMessage is: @myMessage</p>

<!-- Multi-statement block -->
@Code
dim greeting = "Welcome to our site!"
dim weekDay = DateTime.Now.DayOfWeek
dim greetingMessage = greeting & " Here in Huston it is: " & weekDay
End Code

<p>The greeting is: @greetingMessage</p>
```

## βιβλιογραφικές αναφορές

* [Razor Syntax Reference - Microsoft](https://learn.microsoft.com/en-us/aspnet/core/mvc/views/razor?view=aspnetcore-5.0)

