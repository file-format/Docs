{
  "date" : "2021-08-02",
  "keywords" :[ "αρχείο reg", "μορφή αρχείου reg", "τι είναι ένα αρχείο reg", "αρχείο", "παράδειγμα reg", "επέκταση αρχείου reg", "επέκταση", "μορφή" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Μάθετε σχετικά με τη μορφή αρχείου REG και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία REG.",
  "title" :"REG - Αρχείο μητρώου των Windows",
  "linktitle" : "REG",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-02"
}

## Τι είναι ένα αρχείο REG;
Ένα αρχείο REG είναι απλώς ένα αρχείο κειμένου με την επέκταση .reg. Αυτά τα αρχεία δημιουργούνται συνήθως με εξαγωγή τυπικών κλειδιών από το Μητρώο. Αυτά τα αρχεία μπορούν επίσης να χρησιμοποιηθούν ως αντίγραφο ασφαλείας του μητρώου (Ειδικά αυτό το βήμα είναι σημαντικό πριν κάνετε αλλαγές!). Μπορείτε να δείτε ότι ορισμένοι τα έκαναν διαθέσιμα ως αρχεία με δυνατότητα λήψης στους ίδιους ιστότοπους που σας δείχνουν πώς να εκτελέσετε μια εισβολή στο μητρώο. Ένα αρχείο REG είναι χρήσιμο για την πραγματοποίηση μη αυτόματων αλλαγών στο Μητρώο και την εξαγωγή αυτών των αλλαγών. Απλώς καθαρίστε λίγο το αρχείο και μετά μοιραστείτε το με άλλους.

## Μορφή αρχείου REG
Η μορφή αρχείου REG σχεδιάστηκε για την εξαγωγή και εισαγωγή τμημάτων του μητρώου των Windows χρησιμοποιώντας μια σύνταξη που βασίζεται σε INI. Το μητρώο των Windows είναι μια σχεσιακή ή ιεραρχική βάση δεδομένων που διατηρεί τις ρυθμίσεις χαμηλού επιπέδου για το λειτουργικό σύστημα Microsoft Windows και άλλες εφαρμογές που χρησιμοποιούν το μητρώο των Windows. Εναλλακτικά, μπορούμε να πούμε ότι το μητρώο ή το μητρώο των Windows αποτελείται από πληροφορίες, επιλογές, ρυθμίσεις και άλλες τιμές για προγράμματα και υλικό που είναι εγκατεστημένα σε όλες τις εκδόσεις των λειτουργικών συστημάτων Microsoft Windows.
### Σύνταξη του αρχείου REG
Ακολουθούν ορισμένα βασικά στοιχεία ως μέρος μιας σύνταξης αρχείου REG:
- **RegistryEditorVersion**: Π.χ. "Windows Registry Editor Version 5.00" για Windows 2000, Windows XP και Windows Server 2003.
- **Κενή γραμμή**: Προσδιορίζει την έναρξη μιας νέας διαδρομής μητρώου.
- **RegistryPathx**: Η διαδρομή του δευτερεύοντος κλειδιού που περιέχει την πρώτη τιμή που εισάγετε.
- **DataItemNamex**: Το όνομα του στοιχείου δεδομένων που θέλετε να εισαγάγετε.
- **DataTypex**: Ο τύπος δεδομένων για την τιμή μητρώου.

Τα κλειδιά αποθηκεύονται σε αρχεία .reg χρησιμοποιώντας την ακόλουθη σύνταξη:
```
[<Hive name>\<Key name>\<Subkey name>]
"Value name"=<Value type>:<Value data>
```
Μπορείτε να επεξεργαστείτε την προεπιλεγμένη τιμή ενός κλειδιού χρησιμοποιώντας το "@" αντί για το "Value Name":
```
[<Hive name>\<Key name>\<Subkey name>]
@=<Value type>:<Value data>
```
### Παράδειγμα
Ακολουθεί ένα παράδειγμα αρχείου REG
```
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SOFTWARE\Foobar]
"Value A"="<String value data with escape characters>"
"Value B"=hex:<Binary data (as comma-delimited list of hexadecimal values)>
"Value C"=dword:<DWORD value integer>
"Value D"=hex(0):<REG_NONE (as comma-delimited list of hexadecimal values)>
"Value E"=hex(1):<REG_SZ (as comma-delimited list of hexadecimal values representing a UTF-16LE NUL-terminated string)>
"Value F"=hex(2):<Expandable string value data (as comma-delimited list of hexadecimal values representing a UTF-16LE NUL-terminated string)>
"Value G"=hex(3):<Binary data (as comma-delimited list of hexadecimal values)> ; equal to "Value B"
"Value H"=hex(4):<DWORD value (as comma-delimited list of 4 hexadecimal values, in little endian byte order)>
"Value I"=hex(5):<DWORD value (as comma-delimited list of 4 hexadecimal values, in big endian byte order)>
"Value J"=hex(7):<Multi-string value data (as comma-delimited list of hexadecimal values representing UTF-16LE NUL-terminated strings)>
"Value K"=hex(8):<REG_RESOURCE_LIST (as comma-delimited list of hexadecimal values)>
"Value L"=hex(a):<REG_RESOURCE_REQUIREMENTS_LIST (as comma-delimited list of hexadecimal values)>
"Value M"=hex(b):<QWORD value (as comma-delimited list of 8 hexadecimal values, in little endian byte order)>
```

## βιβλιογραφικές αναφορές

* [Μητρώο Windows- από τη Wikipedia](https://en.wikipedia.org/wiki/Windows_Registry)
* [Πώς να προσθέσετε, να τροποποιήσετε ή να διαγράψετε δευτερεύοντα κλειδιά και τιμές μητρώου χρησιμοποιώντας ένα αρχείο .reg](https://support.microsoft.com/en-us/topic/how-to-add-modify-or-delete-registry-subkeys-and-values-by-using-a-reg-file-9c7f37cf-a5e9-e1cd-c4fa-2a26218a1a23)
