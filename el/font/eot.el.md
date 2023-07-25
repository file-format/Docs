{
  "date" : "2020-08-20",
  "keywords" :[ "αρχείο eot", "μορφή αρχείου eot", "τι είναι αρχείο eot", "αρχείο", "παράδειγμα eot", "επέκταση αρχείου eot", "επέκταση", "μορφή" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EOT - Μορφή αρχείου γραμματοσειράς TrueType",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου EOT και τα API για τη δημιουργία και το άνοιγμα αρχείων EOT.",
  "linktitle" : "EOT",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-21"
}

## Τι είναι ένα αρχείο ΕΟΤ;

Ένα αρχείο με επέκταση .eot είναι μια γραμματοσειρά OpenType που είναι ενσωματωμένη σε ένα έγγραφο. Αυτά χρησιμοποιούνται κυρίως σε αρχεία Ιστού, όπως μια ιστοσελίδα. Δημιουργήθηκε από τη Microsoft και υποστηρίζεται από τα Προϊόντα της Microsoft, συμπεριλαμβανομένου του αρχείου παρουσίασης PowerPoint [.pps](/el/presentation/pps). Το αρχείο δεν είναι κύριας χρήσης και είναι ένα είδος συνοδευτικού εγγράφου με το κύριο έγγραφο ή την ιστοσελίδα. Παρόμοια με τις γραμματοσειρές OTF, το EOT υποστηρίζει τόσο Postscript όσο και TrueType περιγράμματα για τα γλυφά. Τα αρχεία EOT είναι μικρότερα σε μέγεθος για το λόγο ότι συμπιέζονται χρησιμοποιώντας συμπίεση LZ. Ο EOT χρησιμοποιεί ένα εργαλείο της Microsoft για να δημιουργήσει μια γραμματοσειρά από υπάρχουσες γραμματοσειρές TTF/OTF.

## Σύντομη Ιστορία

Η γραμματοσειρά EOT υποβλήθηκε στο W3C το 2007 ως μέρος του CSS3 αλλά λόγω των απαιτήσεών της να εγκατασταθεί μόνιμα σε απομακρυσμένο σύστημα έγινε η αιτία της απόρριψής της. Υποβλήθηκε ξανά τον Μάρτιο του 2008, αλλά το W3C επέλεξε τελικά το [Web Font Format](/el/font/woff/) (WOFF) το οποίο τυποποιήθηκε τότε.

## Μορφή αρχείου ΕΟΤ

Μπορείτε να βρείτε λεπτομέρειες για τη μορφή αρχείου EOT στη [σελίδα υποβολής W3](https://www.w3.org/Submission/EOT/#FileFormat) και επεξεργάζεται τη δομή που χρησιμοποιείται από αυτήν τη μορφή γραμματοσειράς. Το EOT αποτελείται από μια ενιαία δομή EMBEDDEDFONT που παρέχει αρκετές βασικές πληροφορίες σχετικά με το όνομα της γραμματοσειράς hte και τους υποστηριζόμενους χαρακτήρες. Η συσκευασία αυτών των πληροφοριών επιτρέπει στους πράκτορες χρήστη να αποφύγουν την αποσυσκευασία, την αποσυμπίεση ή την εγκατάσταση της γραμματοσειράς εάν υπάρχει ήδη στο μηχάνημα.

### EMBEDDEDFONT Δομή
Η δομή EMBEDDEDFONT έχει υποστεί τρεις αναθεωρήσεις, με προσθήκη πρόσθετων δεδομένων στο τέλος της δομής με κάθε αναθεώρηση. Η τελευταία αναθεώρηση της δομής EMBEDDEDFONT είναι όπως απεικονίζεται παρακάτω.

|Τύπος δεδομένων|Όνομα καταχώρισης|Περιγραφή|
---|---|---|
|unsigned long|EOTSize|Συνολικό μήκος δομής σε byte (συμπεριλαμβανομένων δεδομένων συμβολοσειράς και γραμματοσειράς)|
|unsigned long|FontDataSize|Μήκος της γραμματοσειράς OpenType (FontData) σε byte|
|unsigned long|Έκδοση|Αριθμός έκδοσης αυτής της μορφής - 0x00020002|
|ανυπόγραφο μακρύ|Σημαίες|Σημαίες επεξεργασίας|
|byte[10]|FontPANOSE|Η τιμή PANOSE για αυτήν τη γραμματοσειρά - Δείτε http://www.microsoft.com/typography/otspec/os2.htm#pan|
|byte|Charset|Στα Windows αυτό προέρχεται από το TEXTMETRIC.tmCharSet. Αυτή η τιμή καθορίζει το σύνολο χαρακτήρων της γραμματοσειράς. DEFAULT_CHARSET (0x01) υποδηλώνει καμία προτίμηση. - Δείτε https://learn.microsoft.com/en-us/windows/win32/api/wingdi/ns-wingdi-textmetrica|
|byte|Italic|Εάν το bit για το ITALIC έχει οριστεί στο OS/2.fsSelection, η τιμή θα είναι 0x01 - Δείτε http://www.microsoft.com/typography/otspec/os2.htm#fss|
|unsigned long|Weight|Η τιμή βάρους για αυτήν τη γραμματοσειρά - Δείτε http://www.microsoft.com/typography/otspec/os2.htm#wtc|
|unsigned short|fsType|Πληκτρολογήστε σημαίες που παρέχουν πληροφορίες σχετικά με τα δικαιώματα ενσωμάτωσης - Δείτε http://www.microsoft.com/typography/otspec/os2.htm#fst|
|ανυπόγραφο σύντομο|MagicNumber|Μαγικός αριθμός για αρχείο ΕΟΤ - 0x504C. Χρησιμοποιείται για τον έλεγχο για καταστροφή δεδομένων.|
|unsigned long|UnicodeRange1|os/2.UnicodeRange1 (bit 0-31) - Δείτε http://www.microsoft.com/typography/otspec/os2.htm#ur|
|unsigned long|UnicodeRange2|os/2.UnicodeRange2 (bits 32-63) - Δείτε http://www.microsoft.com/typography/otspec/os2.htm#ur|
|unsigned long|UnicodeRange3|os/2.UnicodeRange3 (bit 64-95) - Δείτε http://www.microsoft.com/typography/otspec/os2.htm#ur|
|unsigned long|UnicodeRange4|os/2.UnicodeRange4 (bit 96-127) - Δείτε http://www.microsoft.com/typography/otspec/os2.htm#ur|
|unsigned long|CodePageRange1|CodePageRange1 (bit 0-31) - Δείτε http://www.microsoft.com/typography/otspec/os2.htm#cpr|
|unsigned long|CodePageRange2|CodePageRange2 (bit 32-63) - Δείτε http://www.microsoft.com/typography/otspec/os2.htm#cpr|
|ανυπόγραφο long|CheckSumAdjustment|head.CheckSumAdjustment - Δείτε https://learn.microsoft.com/en-us/typography/opentype/spec/head|
|ανυπόγραφο long|Δέσμευση1|Δεσμευμένο - πρέπει να είναι 0|
|ανυπόγραφο long|Δέσμευση2|Δεσμευμένο - πρέπει να είναι 0|
|ανυπόγραφο long|Δέσμευση3|Δεσμευμένο - πρέπει να είναι 0|
|ανυπόγραφο long|Δέσμευση4|Δεσμευμένο - πρέπει να είναι 0|
|unsigned short|Padding1|Padding για διατήρηση μεγάλης ευθυγράμμισης. Η τιμή πλήρωσης πρέπει πάντα να ορίζεται σε 0x0000.|
|unsigned short|FamilyNameSize|Αριθμός byte που χρησιμοποιούνται από τον πίνακα FamilyName|
|byte|FamilyName[FamilyNameSize]|Πίνακας χαρακτήρων UTF-16 το μήκος των byte FamilyNameSize. Αυτή είναι η συμβολοσειρά της οικογένειας γραμματοσειρών της αγγλικής γλώσσας που βρίσκεται στον πίνακα ονομάτων της γραμματοσειράς (αναγνωριστικό ονόματος = 1) - Δείτε https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding2|Η τιμή padding πρέπει πάντα να ορίζεται σε 0x0000.|
|unsigned short|StyleNameSize|Αριθμός byte που χρησιμοποιούνται από το StyleName|
|byte|StyleName[StyleNameSize]|Πίνακας χαρακτήρων UTF-16 το μήκος των byte StyleNameSize. Αυτή είναι η συμβολοσειρά Font Subfamily της αγγλικής γλώσσας που βρίσκεται στον πίνακα ονομάτων της γραμματοσειράς (όνομα ID = 2) - Δείτε https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding3|Η τιμή padding πρέπει πάντα να ορίζεται σε 0x0000.|
|unsigned short|VersionNameSize|Αριθμός byte που χρησιμοποιούνται από το VersionName|
|bytes|VersionName[VersionNameSize]|Πίνακας χαρακτήρων UTF-16 το μήκος των byte VersionNameSize. Αυτή είναι η συμβολοσειρά της αγγλικής έκδοσης που βρίσκεται στον πίνακα ονομάτων της γραμματοσειράς (όνομα ID = 5) - Δείτε https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding4|Η τιμή padding πρέπει πάντα να ορίζεται σε 0x0000.|
|unsigned short|FullNameSize|Αριθμός byte που χρησιμοποιούνται από το FullName|
|byte|FullName[FullNameSize]|Πίνακας χαρακτήρων UTF-16 το μήκος των byte FullNameSize. Αυτή είναι η συμβολοσειρά πλήρους ονόματος στην αγγλική γλώσσα που βρίσκεται στον πίνακα ονομάτων της γραμματοσειράς (όνομα ID = 4) - Δείτε https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding5|Η τιμή padding πρέπει πάντα να ορίζεται σε 0x0000.|
|unsigned short|RootStringSize|Αριθμός byte που χρησιμοποιούνται από τον πίνακα RootString|
|byte|RootString[RootStringSize]|Πίνακας UTF-16 χαρακτήρων στο μήκος των byte RootStringSize.|
|unsigned long|RootStringCheckSum|RootString CheckSum τιμή. Δείτε παρακάτω τον αλγόριθμο για την επεξεργασία του RootStringChecksum.|
|unsigned long|EUDCCodePage|Απαιτείται τιμή κωδικοσελίδας για υποστήριξη γραμματοσειράς EUDC.|
|unsigned short|Padding6|Η τιμή padding πρέπει πάντα να ορίζεται σε 0x0000.|
|unsigned short|SignatureSize|Αριθμός byte που χρησιμοποιούνται από τον πίνακα Signature. Αυτήν τη στιγμή έχει δεσμευτεί και θα πρέπει να οριστεί σε 0x0000.|
|byte|Υπογραφή[SignatureSize]|Δέσμευση αυτή τη στιγμή. Εάν το SignatureSize είναι 0x0000, δεν υπάρχει μήκος σε αυτόν τον πίνακα.|
|ανυπόγραφο μακρύ|EUDCFlags|Επεξεργασία σημαιών για τη γραμματοσειρά EUDC. Οι τυπικές τιμές μπορεί να είναι TTEMBED_XORENCRYPTDATA και TTEMBED_TTCOMPRESSED.|
|unsigned long|EUDCFontSize|Αριθμός byte που χρησιμοποιούνται από τον πίνακα Signature.|
|byte|EUDCFontData[EUDCFontSize]|Αριθμός byte που χρησιμοποιούνται για τα δεδομένα γραμματοσειράς EUDC. Εάν το EUDCFontSize είναι 0x00000000, δεν υπάρχει μήκος σε αυτόν τον πίνακα.|
|byte|FontData[FontDataSize]|Τα δεδομένα γραμματοσειράς για αυτό το αρχείο EOT. Τα δεδομένα μπορεί να είναι συμπιεσμένα ή κρυπτογραφημένα XOR όπως υποδεικνύεται από τις σημαίες επεξεργασίας.|

## βιβλιογραφικές αναφορές

* [Μορφή αρχείου EOT](https://www.w3.org/Submission/EOT/)
* [Embedded OpenType](https://en.wikipedia.org/wiki/Embedded_OpenType)
* [Ενσωμάτωση γραμματοσειράς](https://en.wikipedia.org/wiki/Font_embedding)

