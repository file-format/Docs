{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Μορφή αρχείου PS",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου PS και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία PS.",
  "linktitle" : "PS",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## Τι είναι ένα αρχείο .PS; ##

Το PostScript (PS) είναι μια γλώσσα περιγραφής σελίδας γενικής χρήσης που χρησιμοποιείται στην επιχείρηση επιτραπέζιων και ηλεκτρονικών εκδόσεων. Ο κύριος στόχος του PostScript (PS) είναι να διευκολύνει τη δισδιάστατη σχεδίαση γραφικών. Οι περισσότερες γλώσσες απαιτούν ένα ξεχωριστό στάδιο μεταγλώττισης πριν από την εκτέλεση του κώδικα, ενώ η μορφή Post Script (PS) υποστηρίζει μια άμεση ερμηνεία χρόνου εκτέλεσης. Η πρώιμη έκδοσή του ορίζει τα γραφικά σχήματα, τις διαφορετικές εμφανίσεις κειμένου και τις μοντελοποιημένες εικόνες σε εκτυπωμένες σελίδες ή σελίδες που εμφανίζονται, ακολουθώντας τους κανόνες του μοντέλου απεικόνισης της Adobe. Ένα πρόγραμμα PS είναι σε θέση να επικοινωνεί μια περιγραφή εγγράφου μεταξύ ενός συστήματος σύνθεσης και εκτύπωσης, διατηρώντας τη συσκευή ανεξάρτητη και υψηλού επιπέδου. Επιπλέον, αυτό το πρόγραμμα είναι επίσης ικανό να ρυθμίζει την εμφάνιση κειμένου και γραφικών σε μια οθόνη.

Η περιγραφή της σελίδας PostScript είναι διαθέσιμη για απόδοση, εμφάνιση στον εκτυπωτή και σε άλλη συσκευή εξόδου με τη βοήθεια του διερμηνέα PostScript της συσκευής. Καθώς οι εντολές για την εκτύπωση χαρακτήρων, γραφικών σχημάτων και εικόνων εκτελούνται από διερμηνέα, για τη συγκεκριμένη συσκευή, η περιγραφή PostScript υψηλού επιπέδου μετατρέπεται σε μορφή δεδομένων ράστερ χαμηλού επιπέδου. Γενικά, διαφορετικές εφαρμογές όπως εικονογράφοι, συστήματα σύνθεσης εγγράφων και σχεδιασμός με τη βοήθεια υπολογιστή (CAD) είναι αυτοματοποιημένες για τη δημιουργία περιγραφών σελίδων PostScript. Γενικά οι προγραμματιστές πρέπει να γράφουν προγράμματα PostScript τη στιγμή της δημιουργίας νέων εφαρμογών. Ωστόσο, ένας προγραμματιστής μπορεί να εκμεταλλευτεί τις δυνατότητες της γλώσσας PostScript που δεν είναι προσβάσιμες σε καμία εφαρμογή γράφοντας ένα πρόγραμμα PS για αυτήν την ειδική κατάσταση.

## Σύντομη Ιστορία ##

Η έννοια της γλώσσας PostScript εισήχθη για πρώτη φορά από τον John Warnock. Το 1966 δούλευε σε ένα έργο του λιμανιού της Νέας Υόρκης. Προσπαθούσε να αναπτύξει έναν διερμηνέα για ένα μεγάλο τρισδιάστατο γραφικό για τη βάση δεδομένων αυτού του έργου. Για την επεξεργασία αυτών των γραφικών, ο John Warnock συνέλαβε τη γλώσσα Design System. Εν τω μεταξύ, η Xerox PARC έψαχνε για ένα τυπικό μέσο καθορισμού εικόνων σελίδας για τον πρώτο τους εκτυπωτή λέιζερ. Αν και ο Bob Sproull και ο William Newman το 1975-76 ανέπτυξαν τη μορφή Press (μορφή δεδομένων) για να οδηγούν εκτυπωτές λέιζερ, ωστόσο χρειαζόταν μια γλώσσα για μεγαλύτερη ευελιξία. Το 1978 ο Warnock έγινε μέλος του Martin Newell στο Xerox PARC και ξαναέγραψε την ερμηνευτική γλώσσα, JaM που αργότερα αναπτύχθηκε και επεκτάθηκε στη γλώσσα Interpress. Ο Warnock ίδρυσε την Adobe Systems τον Δεκέμβριο του 1982 με τους Chuck Geschke, Doug Brotz, Ed Taft και Bill Paxton. Άρχισαν να εργάζονται σε μια απλούστερη γλώσσα που ονομάζεται PostScript παρόμοια με την Interpress, η οποία κυκλοφόρησε εμπορικά το 1984. Ο Steve Jobs από την Apple τους επισκέφτηκε και τους συμβούλεψε να προσαρμόσουν το PostScript για να οδηγούν εκτυπωτές λέιζερ.

Τον Μάρτιο του 1985, ο πρώτος εκτυπωτής με ενσωματωμένο διερμηνέα PostScript ήταν ο LaserWriter της Apple, ο οποίος έφερε επανάσταση στην επιτραπέζια δημοσίευση (DTP). Η τεχνική ευρωστία και η ευρεία διαθεσιμότητα έκαναν τη PostScript, μια γλώσσα επιλογής για επιτραπέζιους και ηλεκτρονικές εκδόσεις. Κατά τη διάρκεια του 1990, ένας διερμηνέας για τη γλώσσα PostScript ήταν ένα ουσιαστικό μέρος των εκτυπωτών λέιζερ.

## Κύρια χαρακτηριστικά ##

Οι δυνατότητες της γλώσσας PostScript για αντιμετώπιση διαδραστικών γραφικών και περιγραφής σελίδας διαθέτουν τα ακόλουθα χαρακτηριστικά:

**Σχήματα:** Αυθαίρετη φύση, μπορεί να αποτελούνται από ευθείες γραμμές, καμπύλες, τετράγωνα και κυβικές καμπύλες που μπορεί να είναι και αυτοδιερχόμενες και αποσυνδεδεμένες (σε τμήματα και τρύπες).

**Χειριστές ζωγραφικής:** επιτρέπουν το περίγραμμα σχήματος οποιουδήποτε πάχους, χρώματος, γεμίσματος ή επιτρέπουν στο σχήμα να σχεδιαστεί ως απόκομμα για να επιτρέπεται η περικοπή οποιουδήποτε άλλου γραφικού.

**Τα χρώματα:** έχουν την ποικιλομορφία όπως κλίμακα του γκρι, RGB, CMYK και CIE. Ειδικά είδη χρωμάτων μοντελοποιούνται ως διαφορετικά χαρακτηριστικά: σημαδιακά χρώματα, χρωματική χαρτογράφηση, ακόμη και σκίαση και επανάληψη μοτίβων.

**Κείμενο:** πλήρως ενσωματωμένο με γραφικά. Επιπλέον, το μοντέλο απεικόνισης Adobe επιτρέπει στους χαρακτήρες κειμένου να εμφανίζονται ως γραφικά σχήματα που μπορούν να λειτουργήσουν από οποιονδήποτε κανονικό χειριστή γραφικών.

**Δείγματα εικόνων**: εξάγονται από αρχικές πηγές (σαρωμένες φωτογραφίες) ή μπορούν να παραχθούν συνθετικά. Η γλώσσα PostScript προσφέρει διάφορα μέσα για την αναγέννηση εικόνων σε οποιαδήποτε ανάλυση και σύμφωνα με διαφορετικά μοντέλα χρωμάτων σε μια συσκευή εξόδου.

Μια γλώσσα προγραμματισμού γενικής χρήσης μπορεί να εκμεταλλευτεί τις δυνατότητες γραφικών PostScript γλώσσα ενσωματώνοντας Ps στο πλαίσιό της. Οι πρωτόγονοι τύποι δεδομένων, όπως αριθμοί, χαρακτήρες, πίνακες και συμβολοσειρές. έλεγχος πρωτόγονων, όπως βρόχοι, διαδικασίες και προϋποθέσεις. και ορισμένα μη συμβατικά χαρακτηριστικά, όπως λεξικά, προσδιορίζονται στη γλώσσα. Αυτά τα χαρακτηριστικά διευκολύνουν τους προγραμματιστές να γράφουν εντολές για να επικαλούνται λειτουργίες υψηλότερου επιπέδου. Αυτές οι λειτουργίες υψηλού επιπέδου ικανοποιούν τις ανάγκες μιας πολύπλοκης εφαρμογής. Αυτή η πρακτική είναι πιο συμπαγής και αποτελεσματική αντί να χρησιμοποιεί ένα σταθερό σύνολο βασικών λειτουργιών.

Προγράμματα γραμμένα σε PostScript μπορούν να παραχθούν, να κοινοποιηθούν και να ερμηνευθούν με τη μορφή κειμένου πηγής ASCII. Ολόκληρη η γλώσσα μπορεί να οριστεί με τη μορφή εκτυπώσιμων χαρακτήρων και λευκού χώρου. Αυτή η αναπαράσταση υποστηρίζει τους προγραμματιστές να δημιουργούν, να χειρίζονται και να κατανοούν τη γλώσσα εύκολα. Επιπλέον, η αποθήκευση και η μετάδοση αρχείων μεταξύ διαφορετικών υπολογιστών και λειτουργικών συστημάτων διατηρήθηκε βολική χάρη στην ανεξαρτησία του μηχανήματος.

Οι δυαδικές κωδικοποιημένες μορφές της γλώσσας είναι δυνατές, όταν το πρόγραμμα είναι εγγυημένο σε μια πλήρως διαφανή διαδρομή επικοινωνίας προς τον διερμηνέα PostScript. Η Adobe συνιστά αυστηρή συνοχή στην αναπαράσταση ASCII των προγραμμάτων PS για ανταλλαγή εγγράφων ή αποθήκευση αρχείων.

## Εκδόσεις ##

Το PS(.ps) είναι η επέκταση αρχείου για ένα έγγραφο PostScript. Τα Εθνικά Αρχεία του ΗΒ κατηγοριοποιούν πέντε χρονολογικές εκδόσεις του αρχείου PostScript, που ορίζονται στην έκδοση DSC: εκδόσεις 1.0, 2.0, 2.1, 3.0, 3.1. Κάθε έκδοση ορίζει σημαντικά δομικά σχόλια. Το Encapsulated PostScript File (EPS) είναι ένας ειδικός υποτύπος του αρχείου PostScript που χρησιμοποιεί τη γλώσσα για να καθορίσει ένα ορθογώνιο γραφικό. Το Εγχειρίδιο Αναφοράς Γλώσσας PostScript περιγράφει ένα EPS ως: "Ένα αρχείο PostScript (EPS) σε κάψουλα είναι ένα πρόγραμμα PostScript που περιγράφει το πολύ μία σελίδα σε μορφή που μπορεί να εισαχθεί από άλλες εφαρμογές για ενσωμάτωση σε ένα έγγραφο που περιέχει." Ένα αρχείο εγγράφου PostScript μπορεί να ενσωματώσει ένα αρχείο EPS σε αυτό. Μια πρόσθετη χρήση του PostScript αναφέρεται ως Display PostScript (DPS). Το DPS δημιουργεί γραφικά στην οθόνη μέσω μιας μηχανής γραφικών που χρησιμοποιεί το μοντέλο και τη γλώσσα απεικόνισης PostScript.

## Βιβλιογραφικές αναφορές ##

* [Οικογένεια μορφής PostScript](https://www.loc.gov/preservation/digital/formats/fdd/fdd000029.shtml)

