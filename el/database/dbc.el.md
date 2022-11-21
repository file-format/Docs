{
  "date" : "2021-06-17",
  "keywords" :[ "DBC", "επέκταση", "αρχείο dbc", "μορφή αρχείου dbc", "Τύπος αρχείου βάσης δεδομένων", "μορφή αρχείου βάσης δεδομένων", "τι είναι αρχείο dbc" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Μάθετε σχετικά με τη μορφή αρχείου DBC και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία DBC.",
  "title" :"DBC - Αρχείο βάσης δεδομένων CAN",
  "linktitle" : "DBC",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-06-17"
}

## Τι είναι ένα αρχείο DBC;
Τα αρχεία με επέκταση .dbc είναι επίσης γνωστά ως αρχεία βάσης δεδομένων CAN. Το αρχείο DBC είναι ένα απλό αρχείο κειμένου που αποτελείται από πληροφορίες για την αποκωδικοποίηση ακατέργαστων δεδομένων διαύλου CAN σε φυσικές τιμές ή σε αναγνώσιμη από τον άνθρωπο μορφή. Παρουσιάζεται το αρχείο DBC, επειδή αυτός είναι ο πολύ συνηθισμένος τρόπος διαχείρισης της αναγνώρισης και της μετάφρασης των δεδομένων. Ο τύπος αρχείου DBC αναπτύχθηκε για να παρέχει τα μέσα τήρησης αρχείων όπως περιγράφεται σε ένα δίκτυο CAN.

## Μορφή αρχείου DBC
Η μορφή αρχείου DBC αντιπροσωπεύει μόνο το αναγνωστικό ή το παθητικό μέρος, δεν παρέχει ένα μέσο για την επεξεργασία των μεταδόσεων. Για την υποστήριξη οχημάτων που δεν έχουν ακόμη συγκεκριμένη εγγενή προσαρμογή. Αυτό γίνεται χρησιμοποιώντας τον γενικό τύπο οχήματος DBC για τη χρήση αρχείων DBC για τη μετάφραση δεδομένων CAN σε μετρήσεις. Κάθε μήνυμα σε ένα DBC γίνεται δομή C με τα σήματα να είναι τα μέλη της δομής C.

### Δομή DBC
Τα δεδομένα DBC αποτελούνται από τα ακόλουθα στοιχεία:

#### Απλό μήνυμα DBC
Ένα απλό μήνυμα DBC αποτελείται από το αναγνωριστικό μηνύματος και τουλάχιστον ένα σήμα. Ακολουθεί μια επίδειξη ενός μηνύματος που αποτελείται από ένα μόνο σήμα 8-bit.

```
BO_ 500 IO_DEBUG: 4 IO
 SG_ IO_DEBUG_test_unsigned : 0|8@1+ (1,0) [0|0] "" DBG
```
#### Υπογεγραμμένα σήματα
Ένα υπογεγραμμένο σήμα μπορεί να σταλεί εφαρμόζοντας αρνητική μετατόπιση σε ένα σήμα. Ακολουθεί ένα παράδειγμα υπογεγραμμένου σήματος στο προηγούμενο μήνυμα.

```
BO_ 500 IO_DEBUG: 4 IO
 SG_ IO_DEBUG_test_unsigned : 0|8@1+ (1,0) [0|0] "" DBG
 SG_ IO_DEBUG_test_signed : 8|8@1- (1,-128) [0|0] "" DBG
```
#### Κλασματικά σήματα
Ένα κλασματικό σήμα μπορεί να σταλεί αποφασίζοντας το εύρος και την ακρίβεια εάν απαιτείται.

```
BO_ 500 IO_DEBUG: 4 IO
 SG_ IO_DEBUG_test_unsigned : 0|8@1+ (1,0) [0|0] "" DBG
 SG_ IO_DEBUG_test_signed : 8|8@1- (1,-128) [0|0] "" DBG
 SG_ IO_DEBUG_test_float1 : 16|8@1+ (0.1,0) [0|0] "" DBG
 SG_ IO_DEBUG_test_float2 : 24|12@1+ (0.01,-20.48) [-20.48|20.47] "" DBG
```
#### Τύποι απαρίθμησης
Ένας τύπος απαρίθμησης χρησιμοποιείται όταν ο χρήστης θέλει να δει ονόματα, αντί για αριθμούς. Δείτε το παρακάτω παράδειγμα.

```
BO_ 500 IO_DEBUG: 4 IO
 SG_ IO_DEBUG_test_enum : 8|8@1+ (1,0) [0|0] "" DBG

BA_ "FieldType" SG_ 500 IO_DEBUG_test_enum "IO_DEBUG_test_enum";

VAL_ 500 IO_DEBUG_test_enum 2 "IO_DEBUG_test2_enum_two" 1 "IO_DEBUG_test2_enum_one" ;
```
#### Πολυπλεξικό μήνυμα
Ο ορισμός πολυπλεξικών μηνυμάτων που χρησιμοποιεί ένα μοναδικό αναγνωριστικό μηνύματος είναι μια επιλογή, ωστόσο, αποκωδικοποιούνται διαφορετικά ανάλογα με την τιμή πολλαπλών σημείων που στάλθηκε. Για να στείλετε ένα πολυπλεξικό μήνυμα παρακάτω, πρέπει να σταλεί ξεχωριστό μήνυμα:

```
BO_ 200 SENSOR_SONARS: 8 SENSOR
 SG_ SENSOR_SONARS_mux M : 0|4@1+ (1,0) [0|0] "" DRIVER,IO
 SG_ SENSOR_SONARS_err_count : 4|12@1+ (1,0) [0|0] "" DRIVER,IO
 SG_ SENSOR_SONARS_left m0 : 16|12@1+ (0.1,0) [0|0] "" DRIVER,IO
 SG_ SENSOR_SONARS_middle m0 : 28|12@1+ (0.1,0) [0|0] "" DRIVER,IO
 SG_ SENSOR_SONARS_right m0 : 40|12@1+ (0.1,0) [0|0] "" DRIVER,IO
 SG_ SENSOR_SONARS_rear m0 : 52|12@1+ (0.1,0) [0|0] "" DRIVER,IO
 SG_ SENSOR_SONARS_no_filt_left m1 : 16|12@1+ (0.1,0) [0|0] "" DBG
 SG_ SENSOR_SONARS_no_filt_middle m1 : 28|12@1+ (0.1,0) [0|0] "" DBG
 SG_ SENSOR_SONARS_no_filt_right m1 : 40|12@1+ (0.1,0) [0|0] "" DBG
 SG_ SENSOR_SONARS_no_filt_rear m1 : 52|12@1+ (0.1,0) [0|0] "" DBG
```

## Παράδειγμα DBC

Ακολουθεί ένα πλήρες παράδειγμα αρχείου dbc:

```
VERSION ""

NS_ :
	BA_
	BA_DEF_
	BA_DEF_DEF_
	BA_DEF_DEF_REL_
	BA_DEF_REL_
	BA_DEF_SGTYPE_
	BA_REL_
	BA_SGTYPE_
	BO_TX_BU_
	BU_BO_REL_
	BU_EV_REL_
	BU_SG_REL_
	CAT_
	CAT_DEF_
	CM_
	ENVVAR_DATA_
	EV_DATA_
	FILTER
	NS_DESC_
	SGTYPE_
	SGTYPE_VAL_
	SG_MUL_VAL_
	SIGTYPE_VALTYPE_
	SIG_GROUP_
	SIG_TYPE_REF_
	SIG_VALTYPE_
	VAL_
	VAL_TABLE_

BS_:

BU_: DBG DRIVER IO MOTOR SENSOR


BO_ 100 DRIVER_HEARTBEAT: 1 DRIVER
 SG_ DRIVER_HEARTBEAT_cmd : 0|8@1+ (1,0) [0|0] "" SENSOR,MOTOR

BO_ 500 IO_DEBUG: 4 IO
 SG_ IO_DEBUG_test_unsigned : 0|8@1+ (1,0) [0|0] "" DBG
 SG_ IO_DEBUG_test_enum : 8|8@1+ (1,0) [0|0] "" DBG
 SG_ IO_DEBUG_test_signed : 16|8@1- (1,0) [0|0] "" DBG
 SG_ IO_DEBUG_test_float : 24|8@1+ (0.5,0) [0|0] "" DBG

BO_ 101 MOTOR_CMD: 1 DRIVER
 SG_ MOTOR_CMD_steer : 0|4@1- (1,-5) [-5|5] "" MOTOR
 SG_ MOTOR_CMD_drive : 4|4@1+ (1,0) [0|9] "" MOTOR

BO_ 400 MOTOR_STATUS: 3 MOTOR
 SG_ MOTOR_STATUS_wheel_error : 0|1@1+ (1,0) [0|0] "" DRIVER,IO
 SG_ MOTOR_STATUS_speed_kph : 8|16@1+ (0.001,0) [0|0] "kph" DRIVER,IO

BO_ 200 SENSOR_SONARS: 8 SENSOR
 SG_ SENSOR_SONARS_mux M : 0|4@1+ (1,0) [0|0] "" DRIVER,IO
 SG_ SENSOR_SONARS_err_count : 4|12@1+ (1,0) [0|0] "" DRIVER,IO
 SG_ SENSOR_SONARS_left m0 : 16|12@1+ (0.1,0) [0|0] "" DRIVER,IO
 SG_ SENSOR_SONARS_middle m0 : 28|12@1+ (0.1,0) [0|0] "" DRIVER,IO
 SG_ SENSOR_SONARS_right m0 : 40|12@1+ (0.1,0) [0|0] "" DRIVER,IO
 SG_ SENSOR_SONARS_rear m0 : 52|12@1+ (0.1,0) [0|0] "" DRIVER,IO
 SG_ SENSOR_SONARS_no_filt_left m1 : 16|12@1+ (0.1,0) [0|0] "" DBG
 SG_ SENSOR_SONARS_no_filt_middle m1 : 28|12@1+ (0.1,0) [0|0] "" DBG
 SG_ SENSOR_SONARS_no_filt_right m1 : 40|12@1+ (0.1,0) [0|0] "" DBG
 SG_ SENSOR_SONARS_no_filt_rear m1 : 52|12@1+ (0.1,0) [0|0] "" DBG




CM_ BU_ DRIVER "The driver controller driving the car";
CM_ BU_ MOTOR "The motor controller of the car";
CM_ BU_ SENSOR "The sensor controller of the car";
CM_ BO_ 100 "Sync message used to synchronize the controllers";

BA_DEF_ "BusType" STRING ;
BA_DEF_ BO_ "GenMsgCycleTime" INT 0 0;
BA_DEF_ SG_ "FieldType" STRING ;

BA_DEF_DEF_ "BusType" "CAN";
BA_DEF_DEF_ "FieldType" "";
BA_DEF_DEF_ "GenMsgCycleTime" 0;

BA_ "GenMsgCycleTime" BO_ 100 1000;
BA_ "GenMsgCycleTime" BO_ 500 100;
BA_ "GenMsgCycleTime" BO_ 101 100;
BA_ "GenMsgCycleTime" BO_ 400 100;
BA_ "GenMsgCycleTime" BO_ 200 100;
BA_ "FieldType" SG_ 100 DRIVER_HEARTBEAT_cmd "DRIVER_HEARTBEAT_cmd";
BA_ "FieldType" SG_ 500 IO_DEBUG_test_enum "IO_DEBUG_test_enum";


VAL_ 100 DRIVER_HEARTBEAT_cmd 2 "DRIVER_HEARTBEAT_cmd_REBOOT" 1 "DRIVER_HEARTBEAT_cmd_SYNC" 0 "DRIVER_HEARTBEAT_cmd_NOOP" ;
VAL_ 500 IO_DEBUG_test_enum 2 "IO_DEBUG_test2_enum_two" 1 "IO_DEBUG_test2_enum_one" ;

```







## Βιβλιογραφικές αναφορές ##

* [Μορφή DBC](http://socialledge.com/sjsu/index.php/DBC_Format)
* [Μια εισαγωγή στα αρχεία J1939 και DBC](https://www.kvaser.com/developer-blog/an-introduction-j1939-and-dbc-files/)

