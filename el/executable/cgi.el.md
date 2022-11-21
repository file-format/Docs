{
  "date" : "2021-06-28",
  "keywords" :[ "αρχείο cgi", "τι είναι ένα αρχείο cgi", "αρχείο", "παράδειγμα cgi", "επέκταση αρχείου cgi", "επέκταση", "μορφή" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Μάθετε σχετικά με τη μορφή αρχείου CGI και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία CGI.",
  "title" :"CGI - Common Gateway Interface Script File",
  "linktitle" : "CGI",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-28"
}

## Τι είναι ένα αρχείο CGI;
Ένα αρχείο CGI είναι γνωστό ως δέσμη ενεργειών Common Gateway Interface που χρησιμοποιείται από έναν διακομιστή web για την εκτέλεση ενός εξωτερικού προγράμματος για την επεξεργασία των αιτημάτων των χρηστών. Το σενάριο που αποθηκεύτηκε σε ένα αρχείο με επέκταση .cgi είναι συνήθως γραμμένο σε γλώσσες προγραμματισμού C ή Perl. Είχε εισαχθεί από τις πρώτες μέρες του Ιστού, όταν οι προγραμματιστές Ιστού ήθελαν να συνδέσουν βάσεις δεδομένων με τους διακομιστές Ιστού τους. Ένας διακομιστής που υποστήριζε μια κοινή πύλη μεταξύ διακομιστή Ιστού και βάσεων δεδομένων ήταν κατάλληλος για την εκτέλεση του κώδικα CGI.

## Μορφή αρχείου CGI
Τα σενάρια CGI χρησιμοποιούνται από τον διακομιστή Ιστού για να διευκολύνουν τον ιδιοκτήτη να διαμορφώσει τον τρόπο χειρισμού μιας διεύθυνσης URL. Η διαδικασία συνήθως γίνεται με την επισήμανση ενός νέου καταλόγου (όπου βρίσκονται κυρίως τα έγγραφα) ως που περιέχει σενάρια CGI. Το κοινώς γνωστό όνομά του είναι cgi-bin. Για παράδειγμα, το /usr/local/apache/htdocs/cgi-bin θα μπορούσε να επιλεγεί ως κατάλογος CGI στον διακομιστή Web. Όταν ένα πρόγραμμα περιήγησης Ιστού ζητά μια διεύθυνση URL που οδηγεί σε ένα αρχείο εντός του καταλόγου CGI, τότε, αντί απλώς να σταλεί αυτό το αρχείο (/el/usr/local/apache/htdocs/cgi-bin/printenv.pl) στο πρόγραμμα περιήγησης Ιστού, το HTTP ο διακομιστής εκτελεί το καθορισμένο σενάριο και επιστρέφει την έξοδο του σεναρίου στο πρόγραμμα περιήγησης Web. Εν ολίγοις, οτιδήποτε αποστέλλεται η δέσμη ενεργειών CGI σε τυπική έξοδο μεταφέρεται στον πελάτη Web αντί να εμφανίζεται σε ένα τερματικό παραθύρου.

### Παράδειγμα CGI

Ακολουθεί το σενάριο CGI γραμμένο σε Perl, το οποίο εμφανίζει όλες τις μεταβλητές περιβάλλοντος που έχουν περάσει από τον διακομιστή Web:
```
#!/usr/bin/env perl

=head1 DESCRIPTION

printenv — a CGI program that just prints its environment

=cut
print "Content-Type: text/plain\n\n";

for my $var ( sort keys %ENV ) {
    printf "%s=\"%s\"\n", $var, $ENV{$var};
}
```

Η έξοδος θα είναι όπως η παρακάτω:
```
COMSPEC="C:\Windows\system32\cmd.exe"
DOCUMENT_ROOT="C:/Program Files (x86)/Apache Software Foundation/Apache2.4/htdocs"
GATEWAY_INTERFACE="CGI/1.1"
HOME="/home/SYSTEM"
HTTP_ACCEPT="text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8"
HTTP_ACCEPT_CHARSET="ISO-8859-1,utf-8;q=0.7,*;q=0.7"
HTTP_ACCEPT_ENCODING="gzip, deflate, br"
HTTP_ACCEPT_LANGUAGE="en-us,en;q=0.5"
HTTP_CONNECTION="keep-alive"
HTTP_HOST="example.com"
HTTP_USER_AGENT="Mozilla/5.0 (Windows NT 6.1; WOW64; rv:67.0) Gecko/20100101 Firefox/67.0"
PATH="/home/SYSTEM/bin:/bin:/cygdrive/c/progra~2/php:/cygdrive/c/windows/system32:..."
PATHEXT=".COM;.EXE;.BAT;.CMD;.VBS;.VBE;.JS;.JSE;.WSF;.WSH;.MSC"
PATH_INFO="/foo/bar"
PATH_TRANSLATED="C:\Program Files (x86)\Apache Software Foundation\Apache2.4\htdocs\foo\bar"
QUERY_STRING="var1=value1&var2=with%20percent%20encoding"
REMOTE_ADDR="127.0.0.1"
REMOTE_PORT="63555"
REQUEST_METHOD="GET"
REQUEST_URI="/cgi-bin/printenv.pl/foo/bar?var1=value1&var2=with%20percent%20encoding"
SCRIPT_FILENAME="C:/Program Files (x86)/Apache Software Foundation/Apache2.4/cgi-bin/printenv.pl"
SCRIPT_NAME="/cgi-bin/printenv.pl"
SERVER_ADDR="127.0.0.1"
SERVER_ADMIN="(server admin's email address)"
SERVER_NAME="127.0.0.1"
SERVER_PORT="80"
SERVER_PROTOCOL="HTTP/1.1"
SERVER_SIGNATURE=""
SERVER_SOFTWARE="Apache/2.4.39 (Win32) PHP/7.3.7"
SYSTEMROOT="C:\Windows"
TERM="cygwin"
WINDIR="C:\Windows"
```
## Χρήσεις σεναρίων CGI
Τα αρχεία CGI που περιέχουν τα σενάρια CGI χρησιμοποιούνται συνήθως για την επεξεργασία δεδομένων εισόδου από τον χρήστη και την παραγωγή των σχετικών δεδομένων εξόδου. Η υλοποίηση ενός wiki είναι ένα από τα παραδείγματα του προγράμματος CGI. Εάν ο παράγοντας χρήστη στείλει ένα αίτημα για το όνομα μιας καταχώρησης, ο διακομιστής Web εκτελεί το πρόγραμμα CGI. Το πρόγραμμα CGI παίρνει την πηγή της σελίδας αυτής της καταχώρησης, τη μετατρέπει σε HTML και εκτυπώνει το αποτέλεσμα. Ο διακομιστής Web λαμβάνει την έξοδο από το πρόγραμμα CGI και την επιστρέφει στον παράγοντα χρήστη. Στη συνέχεια, εάν ο παράγοντας χρήστη καλέσει τη λειτουργία επεξεργασίας κάνοντας κλικ στο κουμπί "Επεξεργασία σελίδας", το πρόγραμμα CGI εμφανίζει μια περιοχή κειμένου HTML ή άλλο στοιχείο ελέγχου επεξεργασίας με τα περιεχόμενα της σελίδας. Τέλος, εάν ο παράγοντας χρήστη κάνει κλικ στο κουμπί "Δημοσίευση σελίδας", το πρόγραμμα CGI μετατρέπει το ενημερωμένο HTML στην πηγή της σελίδας αυτής της καταχώρισης και το αποθηκεύει.



## βιβλιογραφικές αναφορές

* [Common Gateway Interface - by Wikipewdia](https://en.wikipedia.org/wiki/Common_Gateway_Interface)

