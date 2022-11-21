{
  "date" : "2021-07-07",
  "keywords" :[ "DMP", "επέκταση", "αρχείο", "μορφή", "σύστημα", "MemoryDump", "Minidump", "προγράμματα", "υπολογιστής", "εφαρμογή" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DMP - Μορφή αρχείου MemoryDump",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου DMP και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία DMP.",
  "linktitle" : "DMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-07"
}

## Τι είναι ένα αρχείο DMP; ##

Το αρχείο DMP σχετίζεται κυρίως με τη μορφή αρχείου MemoryDump ή Minidump. Χρησιμοποιείται στο λειτουργικό σύστημα Microsoft Windows για την αποθήκευση δεδομένων που έχουν απορριφθεί από το χώρο μνήμης του υπολογιστή. Συνήθως, τα αρχεία DMP δημιουργούνται όταν ένα αρχείο διακόπτεται ή παρουσιάζεται σφάλμα. Κατά καιρούς, τα αρχεία DMP είναι πολύ σημαντικά για τεχνικούς ειδικούς ή προχωρημένους χρήστες υπολογιστών για την αντιμετώπιση προβλημάτων που αντιμετωπίζετε και την επίλυση κάθε είδους ζητήματος εφαρμογής. Τα αρχεία DMP αποθηκεύονται ως ιδιόκτητη μορφή στη Microsoft, η οποία χρησιμοποιείται από το λειτουργικό σύστημα για τον εντοπισμό σφαλμάτων οποιασδήποτε εφαρμογής που είναι εγκατεστημένη στο σύστημα.


## Τεχνική προδιαγραφή Μορφής αρχείου DMP

Στα Windows, το εργαλείο συστήματος "savedump.exe" δημιουργεί αρχεία .dmp τα οποία μπορούν στη συνέχεια να υποβληθούν σε επεξεργασία από διάφορα διαθέσιμα βοηθητικά προγράμματα εντοπισμού σφαλμάτων. Το Mini dump (64/128 Kb) αποθηκεύεται από τα Windows στον κατάλογο '%SystemRoot%\Minidump'. Από την άλλη πλευρά, η μνήμη του πυρήνα και η πλήρης μνήμη αποθηκεύονται στη ρίζα του συστήματος ως αρχεία 'Memory.dmp'. Τα αρχεία ένδειξης σφαλμάτων μνήμης είναι σχετικά μεγάλα αρχεία, επομένως μπορούν να καταλάβουν επαρκή χώρο αποθήκευσης. Επομένως, συνιστάται να διαγράψετε τα άχρηστα αρχεία .dmp που πιστεύετε ότι δεν θα είναι χρήσιμα για την αντιμετώπιση προβλημάτων.

Μπορείτε να διαγράψετε αρχεία .dmp είτε με μη αυτόματο τρόπο είτε χρησιμοποιώντας τον προεπιλεγμένο "Οδηγό καθαρισμού δίσκου" στον υπολογιστή σας. Οι επεκτάσεις DMP χρησιμοποιούνται από τα προϊόντα βάσης δεδομένων Oracle για τη χρήση των αρχείων .dmp σε αρχεία βάσης δεδομένων αντιγράφων ασφαλείας και ανάκτησης που δημιουργούνται και χρησιμοποιούνται. Τα αρχεία DMP που δημιουργούνται από την Oracle είναι αντίγραφα ασφαλείας βάσης δεδομένων που μπορούν να χρησιμοποιηθούν για εισαγωγή ή επαναφορά σε μια παρουσία βάσης δεδομένων που εκτελείται μέσω ενός διακομιστή βάσης δεδομένων. Στις περισσότερες περιπτώσεις, τα αρχεία .dmp έχουν σφραγίδες ώρας και ημερομηνίας ως ονόματα αρχείων.

### Περιεχόμενα αρχείου DMP

Ένα αρχείο ένδειξης σφαλμάτων μνήμης περιέχει:

* Η δήλωση διακοπής και οι παράμετροί της.
* Μια λίστα με φορτωμένα προγράμματα οδήγησης.
* Το πλαίσιο του επεξεργαστή (PRCB) για τις διεργασίες που σταμάτησαν την κανονική λειτουργία των Windows.
* Το πλαίσιο του πυρήνα και οι πληροφορίες του επεξεργαστή (EPROCESSES) για τις διεργασίες που έχουν διακοπεί.
* Το πλαίσιο του πυρήνα και οι πληροφορίες του επεξεργαστή (ETHREAD) για το νήμα που σταμάτησε.
* Η στοίβα κλήσης λειτουργίας πυρήνα για το νήμα που τερμάτισε την εκτέλεση της διαδικασίας.


## Παράδειγμα DMP

Το σφάλμα διακοπής 0XC0000218 (Registry_File_Failure) δημιουργεί ένα αρχείο DMP ως εξής:

```
Symbol search path is: srv*
Executable search path is:
Windows XP Kernel Version 2600 (Service Pack 1) UP Free x86 compatible
Product: WinNt, suite: TerminalServer SingleUserTS
Built by: 2600.xpsp2.030422-1633
Kernel base = 0x804d4000 PsLoadedModuleList = 0x80543530
Debug session time: Fri Jun 11 10:22:46 2004
System Uptime: 0 days 0:00:24.187
Loading Kernel Symbols
.................................................
Loading unloaded module list

Loading User Symbols
*******************************************************************************
* *
* Bugcheck Analysis *
* *
*******************************************************************************

Use !analyze -v to get detailed debugging information.

BugCheck C0000218, {e144c418, 0, 0, 0}

Probably caused by : ntoskrnl.exe ( nt!ExRaiseHardError+13c )

Followup: MachineOwner
---------

kd> !analyze -v
*******************************************************************************
* *
* Bugcheck Analysis *
* *
*******************************************************************************

Unknown bugcheck code (c0000218)
Unknown bugcheck description
Arguments:
Arg1: e144c418
Arg2: 00000000
Arg3: 00000000
Arg4: 00000000

Debugging Details:
------------------


BUGCHECK_STR: 0xc0000218

ERROR_CODE: (NTSTATUS) 0xc0000218 - {Registry File Failure} The registry cannot load the hive (file): %hs or its log or alternate. It is corrupt, absent, or not writable.

DEFAULT_BUCKET_ID: DRIVER_FAULT

LAST_CONTROL_TRANSFER: from 8062be87 to 804f4103

STACK_TEXT:
f96f0870 8062be87 0000004c c0000218 f96f09d4 nt!KeBugCheckEx+0x19
f96f0a20 805e9f96 c0000218 00000001 00000001 nt!ExpSystemErrorHandler+0x44c
f96f0bcc 805ea21c c0000218 00000001 00000001 nt!ExpRaiseHardError+0x9a
f96f0c3c 805fb94c c0000218 00000001 00000001 nt!ExRaiseHardError+0x13c
f96f0dac 805aa2b6 00000000 00000000 00000000 nt!CmpLoadHiveThread+0x16a
f96f0ddc 805319c6 805fb7e2 00000001 00000000 nt!PspSystemThreadStartup+0x34
00000000 00000000 00000000 00000000 00000000 nt!KiThreadStartup+0x16


FOLLOWUP_IP:
nt!ExRaiseHardError+13c
805ea21c 837dfc00 cmp dword ptr [ebp-0x4],0x0

SYMBOL_STACK_INDEX: 3

FOLLOWUP_NAME: MachineOwner

SYMBOL_NAME: nt!ExRaiseHardError+13c

MODULE_NAME: nt

IMAGE_NAME: ntoskrnl.exe

DEBUG_FLR_IMAGE_TIMESTAMP: 3ea80977

STACK_COMMAND: kb

BUCKET_ID: 0xc0000218_nt!ExRaiseHardError+13c

Followup: MachineOwner

```

## Αναφορά ##

* [DMP - Microsoft](https://docs.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

