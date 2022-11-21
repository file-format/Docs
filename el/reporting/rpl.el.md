{
  "date" : "2021-03-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RPL - Διάταξη σελίδας αναφοράς",
  "keywords" :[ "rpl", "Report Page Layout", "XSD", "SQL Server", "reporting"],
  "description":"Μάθετε σχετικά με τη μορφή ροής RPL, η οποία είναι μια εσωτερική δυαδική μορφή που χρησιμοποιείται από τις υπηρεσίες αναφοράς Microsoft SQL Server κατά την επικοινωνία με τα στοιχεία ελέγχου προβολής.",
  "linktitle" : "RPL",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
}
},
  "lastmod" : "2021-03-02"
}

## Τι είναι ένα αρχείο RPL; ##

Η μορφή ροής RPL (Διάταξη σελίδας αναφοράς) είναι μια εσωτερική δυαδική μορφή που χρησιμοποιείται από τις Υπηρεσίες αναφοράς MS SQL Server κατά την επαφή με τα στοιχεία ελέγχου προβολής για τη μείωση μέρους της εργασίας απόδοσης από το διακομιστή στο στοιχείο ελέγχου προβολής πελάτη. Οι προγραμματιστές μπορούν να δημιουργήσουν προσαρμοσμένους σχεδιαστές αναφορών χρησιμοποιώντας το RPL, το οποίο θα δημιουργήσει RPL καθώς και προσαρμοσμένα προγράμματα απόδοσης αναφορών που επεξεργάζονται και εμφανίζουν το αρχείο RPL για την εμφάνιση αναφορών.

## Δομές RPL

Μια ροή RPL περιλαμβάνει δομή ροής, δομή αναφοράς, ιδιότητες αναφοράς και απαριθμήσεις. Κάθε δομή περιλαμβάνει τα ακόλουθα:

- Ορισμός της δομής.

- Η γραμματική Augmented Backus-Naur Form (ABNF) για τη δομή.

- Ένα μικρό διάγραμμα της δομής.

- Ορισμοί όλων των πεδίων που περιέχονται στη δομή.

Ακολουθούν οι σύντομες σημειώσεις σχετικά με ορισμένες από τις Δομές RPL:

### Δομή ροής
Η δομή ροής αποτελείται από μια σειρά εγγραφών. Μια εγγραφή περιέχει μηδέν ή περισσότερα δομημένα πεδία που περιέχουν τη διάταξη της αναφοράς.

#### RPL Stream
Η ροή RPL πρέπει να έχει μόνο μία εγγραφή αναφοράς και η ροή πρέπει να είναι μια σειρά δυαδικών εγγραφών που διατηρούν την ιεραρχία της αναφοράς.

#### Ρεκόρ
Η εγγραφή είναι ένα βασικό δομικό στοιχείο που χρησιμοποιείται για τη διατήρηση των πληροφοριών σχετικά με μια αναφορά. Μια εγγραφή αποτελείται από μια ακολουθία byte διαφορετικού μήκους. Μια εγγραφή αποτελείται από δύο στοιχεία:
- Τύπος δίσκου
- Τα δεδομένα εγγραφής που είναι ειδικά για αυτόν τον τύπο εγγραφής.
Ο τύπος εγγραφής είναι ένα byte που καθορίζει ποιος τύπος πληροφοριών καθορίζεται από την εγγραφή και πώς ταξινομείται και δομείται η δομή των δεδομένων εγγραφής που αφορούν στην εγγραφή. Η τιμή εγγραφής εξαρτάται από τον τύπο των δεδομένων που είναι ειδικά για αυτήν την εγγραφή.

#### Απλές δομές τύπου δεδομένων

Ο παρακάτω πίνακας ορίζει τους τύπους δεδομένων σε μια ροή RPL.

|Περιγραφή| μορφή|
---|---|
|Char|Αντιπροσωπεύει μια αριθμητική (τακτική) τιμή 16-bit (2-byte).|
|Byte|Αντιπροσωπεύει έναν ακέραιο ανυπόγραφο 8-bit (1-byte).|
|Int16|Αντιπροσωπεύει έναν ακέραιο υπογεγραμμένο 16-bit (2-byte).|
|Single|Αντιπροσωπεύει μια τιμή κινητής υποδιαστολής μονής ακρίβειας 32 bit (4 byte).|
|Decimal|Αντιπροσωπεύει έναν τύπο δεδομένων 128-bit (16-byte).|
|DateTime|Αντιπροσωπεύει μια κωδικοποίηση 64-bit (8-byte) μιας τιμής ημερομηνίας και ώρας.|
|Int64|Αντιπροσωπεύει έναν ακέραιο υπογεγραμμένο 64-bit (8-byte).|
|Int32|Αντιπροσωπεύει έναν ακέραιο υπογεγραμμένο 32-bit (4-byte).|
|Float|Αντιπροσωπεύει μια τιμή κινητής υποδιαστολής μονής ακρίβειας 32 bit (4 byte).|
|Boolean|Αντιπροσωπεύει μια τιμή λογικού τύπου Boolean 8 bit (1 byte). Οι έγκυρες τιμές είναι true (1) και false (0).|
|Long|Αντιπροσωπεύει έναν ακέραιο υπογεγραμμένο 64-bit (8-byte).|
|String|Όλες οι τιμές συμβολοσειράς εντός του πρωτοκόλλου ΠΡΕΠΕΙ να είναι UNICODE UTF-16. Από προεπιλογή, όλες οι τιμές συμβολοσειράς ξεκινούν με έναν ακέραιο που ορίζει το μήκος της συμβολοσειράς. Οι τιμές συμβολοσειράς αντιπροσωπεύονται στο πρωτόκολλο ως πίνακας byte. ο αριθμός των byte ΠΡΕΠΕΙ να είναι ίσος με τον αριθμό των χαρακτήρων στη συμβολοσειρά πολλαπλασιασμένος επί δύο.|

### Δομές αναφοράς
Οι δομές αναφοράς περιλαμβάνουν τους ορισμούς και τα μεγέθη των σχετικών δομών και στοιχείων τους.

Η ακόλουθη λίστα καθορίζει τις δομές της αναφοράς:

- Κανω ΑΝΑΦΟΡΑ
- Εκδοχή
- Ιδιότητες αναφοράς
- Στοιχείο πίνακα μετατόπισης
- Περιεχόμενο σελίδας
- Σελίδα
- Ιδιότητες σελίδας
- Διάταξη σελίδας
- Ενότητα
- Απλό τμήμα
- Μικτό Τμήμα
- Ιδιότητες ενότητας
- Στοιχείο Περιοχής Σώματος
- Στοιχείο κεφαλίδας σελίδας
- Στοιχείο υποσέλιδου σελίδας
- Στοιχείο σώματος
- Ιδιότητες στοιχείων
- Ιδιότητες κοινόχρηστου στοιχείου
- Χρησιμοποιήστε τις ιδιότητες κοινόχρηστου στοιχείου
- Ιδιότητες InlineSharedElement
- Ιδιότητες NonSharedElement
- Στυλ
- SharedStyleProperties
- Ιδιότητες NonSharedStyle
- ActionInfo
- ActionInfoContent
- Δράση
- ActionImageMapAreas
- ActionInfoWithMaps
- DynamicImageData
- ImageConsolidationOffsets
- ReportItem
- Γραμμή
- Εικόνα
- Ιδιότητες ImageData
- ΧρήσηSharedImageDataProperties
- InlineSharedImageDataProperties
- Ιδιότητες NonSharedImageData
- Δεδομένα εικόνας
- ImageMapAreas
- ImageMapArea
- Διάγραμμα
- GaugePanel
- Χάρτης
- Ορθογώνιο
- Υποέκθεση
- RichTextBox
-Περιεχόμενο παραγράφου
- TextRun
- Παράγραφος
- RichTextBoxStructure
- Tablix
- TablixContent
- TablixStructure
- TablixMeasurements
- Πλάτος στηλών
- ColumnInfo
- RowHeights
- RowInfo
- TablixRow
- TablixRowCell
- TablixCorner
- TablixColumnHeader
- TablixRowHeader
- TablixBodyRowCells
- TablixBodyRow
- TablixBodyCell
- TablixRowMembersDef
- TablixColMembersDef
- TablixMemberDef
- Μετρήσεις
- Μέτρηση
- ReportElementEnd

### Ιδιότητες
Ακολουθεί η λίστα των ιδιοτήτων που μπορούν να χρησιμοποιηθούν σε μια ροή RPL:

- Ταυτότητα
- ColumnCount
- Διάστημα στηλών
- UniqueName
- Ονομα
- Ετικέτα
- Σελιδοδείκτης
- Συμβουλή εργαλείου
- Εναλλαγή στοιχείου
- Περιγραφή
- Τοποθεσία
- ConsumeContainerWhiteSpace (RPL 10.6)
- Γλώσσα
- Χρόνος εκτέλεσης
- Συγγραφέας
- Αυτόματη ανανέωση
- Όνομα αναφοράς
- Ύψος σελίδας
- Πλάτος σελίδας
- MarginTop
- Περιθώριο Αριστερά
- Περιθώριο Δικαίωμα
- MarginBottom
- Στήλες
- Όνομα σελίδας (RPL 10.6)
- Κλίση
- CanGrow
- CanShrink
- Αξία
- ToggleState
- CanSort
- Κατάσταση ταξινόμησης
- Φόρμουλα
- IsToggleParent
- TypeCode
- Αρχική αξία
- Είναι απλό
- ContentOffset
- StreamName
- Διαστασιολόγηση
- LinkToChild
- PrintOnFirstPage
- PrintBetweenSections (RPL 10.4)
- FormattedValueExpressionBased
- Επεξεργάστηκε με Σφάλμα
- ImageMIMEType
- Όνομα εικόνας
- Πλάτος
- Υψος
- Οριζόντια Ανάλυση
- Κάθετη Ανάλυση
- RawFormat
- Υπερσύνδεσμος
- Σύνδεσμος σελιδοδεικτών
- DrillthroughId
- DrillthroughUrl
- Χρώμα πλαισίου
- BorderColorLeft
- BorderColorRight
- BorderColorTop
- BorderColorBottom
- BorderStyle
- BorderStyleLeft
- BorderStyleRight
- BorderStyleTop
- BorderStyleBottom
- Πλάτος συνόρων
- BorderWidthLeft
- BorderWidthRight
- BorderWidthTop
- BorderWidthBottom
- PaddingLeft
- PaddingRight
- PaddingTop
- PaddingBottom
- Στυλ γραμματοσειράς
- FontFamily
- Μέγεθος γραμματοσειράς
- Βάρος γραμματοσειράς
- Μορφή
- Διακόσμηση κειμένου
- Στοίχιση κειμένου
- Vertical Align
- Χρώμα
- Υψος γραμμής
- Κατεύθυνση
- WritingMode
- UnicodeBiDi
- Εικόνα φόντου
- Χρώμα του φόντου
- BackgroundRepeat
- NumeralLanguage
- NumeralVariant
- Ημερολόγιο
- ColumnHeaderRows
- RowHeaderColumns
- ColsBeforeRowHeader
- LayoutDirection
- DefinitionPath
- Επίπεδο
- MemberCellIndex
- CellItemOffset
- ColSpan
- RowSpan
- DefIndex
- ΣτήληΕυρετήριο
- RowIndex
- Ετικέτα ομάδας
- RecursiveToggleLevel
- Στυλ λίστας
- Επίπεδο λίστας
- Αριθμός παραγράφου
- RightIndent
- LeftIndent
- HangingIndent
- SpaceBefore
- SpaceAfter
- Πρώτη γραμμή
- Σήμανση
- ContentTop
- ContentLeft
- Πλάτος περιεχομένου
- Ύψος περιεχομένου
- Κατάσταση
- CellItemState
- MemberDefState

### Απαριθμήσεις
Η ακόλουθη λίστα δείχνει τις απαριθμήσεις που μπορούν να χρησιμοποιηθούν στη ροή RPL:

- Επιλογές ταξινόμησης
- Μεγέθη
- Τύπος σχήματος
- ImageRawFormat
- FontStyles
- FontWeights
- Διακοσμήσεις κειμένου
- Ευθυγραμμίσεις κειμένου
- Κάθετες Ευθυγραμμίσεις
- Κατευθύνσεις
- Τρόποι γραφής
- UnicodeBiDiTypes
- Ημερολόγια
- BorderStyles
- BackgroundRepeatTypes
- Στυλ λίστας
- MarkupStyles
- TypeCode
- State Values
- TablixMemberStateValues
- TablixMemberDefStateValues
- Μέγεθος RPLS





## Βιβλιογραφικές αναφορές ##

- [Διάταξη σελίδας αναφοράς (RPL) Μορφή δυαδικής ροής](https://docs.microsoft.com/en-us/openspecs/sql_server_protocols/ms-rpl/9c4ff7ba-f6da-4092-9670-aa0e54e73887)

