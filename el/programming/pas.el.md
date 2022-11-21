{
  "date" : "2021-04-22",
  "keywords": [ ".pas file", "pas file format", "extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PAS - Αρχείο προέλευσης μονάδας Δελφών",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου PAS με παράδειγμα PAS και API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία PAS.",
  "linktitle" : "PAS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-22"
}

## Τι είναι ένα αρχείο PAS;
Ένα αρχείο .pas είναι στην πραγματικότητα ένα αρχείο πηγαίου κώδικα που μπορεί να βρεθεί σε ένα πρόγραμμα προγραμματισμού Delphi. Το Delphi είναι μια εφαρμογή ανάπτυξης λογισμικού που χρησιμοποιείται από προγραμματιστές για την κατασκευή λογισμικών που βασίζονται στα Windows. γραμμένο στη γλώσσα των Δελφών. Η γλώσσα Delphi είναι μια παραλλαγή της γλώσσας Object Pascal. Έτσι μπορεί να μεταγλωττιστεί σε εγγενή κώδικα Win32 με τον μεταγλωττιστή Delphi.

## Μορφή αρχείου PAS

Η μορφή αρχείου PAS είναι ένα αρχείο κωδικοποίησης που είναι δεσμευμένο για την πηγή μονάδας Delphi. Οι μονάδες υλοποιούνται ως τα κύρια δομικά στοιχεία των εφαρμογών Delphi. Μπορείτε να δείτε τον πηγαίο κώδικα του τρέχοντος έργου Delphi μέσω του μενού **Έργο > Προβολή πηγής**. Οι προγραμματιστές μπορούν να δημιουργήσουν και να αποθηκεύσουν μια μονάδα ως αυτόνομο αρχείο που μπορεί να χρησιμοποιήσει οποιοδήποτε έργο. Μόλις προστεθεί μια μονάδα στο έργο, η Delphi την καταχωρεί στη ρήτρα χρήσεων του αρχείου έργου .DPR.

## Παράδειγμα αρχείου PAS
Όταν γράφουμε μία γραμμή κώδικα. Οι Δελφοί μας γράφει πολλές γραμμές έξυπνα. Όλος ο πηγαίος κώδικας είναι γραμμένος στο αρχείο PAS. Ακολουθεί ένα βασικό παράδειγμα μονάδας πηγής Delphi ή αρχείου PAS:
```
unit Unit1;
 
 interface
 
 uses
   Windows, Messages, SysUtils, Variants, Classes, Graphics, Controls, Forms,
   Dialogs, StdCtrls;
 
 type
   TForm1 = class(TForm)
     Label1: TLabel;      // The label we have added
     Button1: TButton;    // The button we have added
     procedure Button1Click(Sender: TObject);
   private
     { private declarations }
   public
     { public declarations }
   end;
 
 var
   Form1: TForm1;
 
 implementation
 
 {$R *.dfm}
 
 // The button action we have added
 procedure TForm1.Button1Click(Sender: TObject);
 begin
   Label1.Caption := 'Hello World';    // Label changed when button pressed
 end;
 
 end.
```


## βιβλιογραφικές αναφορές

* [Κατανόηση των Αρχείων Προέλευσης Έργου και Μονάδας των Δελφών](https://www.thoughtco.com/understanding-delphi-project-files-dpr-1057652)
* [Γράφοντας το πρώτο σας πρόγραμμα Delphi](http://www.delphibasics.co.uk/Article.asp?Name=FirstPgm)

