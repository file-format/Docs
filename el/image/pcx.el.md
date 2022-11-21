{
  "date" : "2022-03-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PCX File Format - Paintbrush Bitmap Image File",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου PCX και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία PCX.",
  "linktitle" : "PCX",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-03-16"
}

## Τι είναι ένα αρχείο PCX;

Ένα αρχείο PCX, το αρχείο Picture Exchange, είναι μια μορφή αρχείου εικόνας ράστερ που χρησιμοποιήθηκε ως εγγενής μορφή αρχείου για την εφαρμογή PC Paintbrush. Αναπτύχθηκε από την ZSoft Corporation, ΗΠΑ για πλατφόρμες DOS και Windows και υιοθετήθηκε ως η κύρια μορφή αρχείου απεικόνισης πριν από την άφιξη των [BMP](/el/image/bmp/), [JPEG](/el/image/jpeg/), και [ PNG](/el/image/png/) μορφές αρχείων. Τα αρχεία PCX είναι μικρότερα σε μέγεθος καθώς συμπιέζονται χρησιμοποιώντας την κωδικοποίηση RLE. Χρησιμοποιείται στο πολυσέλιδο αρχείο [DCX](/el/image/dcx/) που χρησιμοποιείται κυρίως για τη δημιουργία ψηφιακών αρχείων φαξ.

## Μορφή αρχείου PCX

Τα αρχεία PCX αποθηκεύονται σε δίσκο σε δυαδική μορφή αρχείου. Η εσωτερική δομή μορφής αρχείου ακολουθεί μικρή σειρά endian byte και έχει τις ακόλουθες τρεις ενότητες:

**`PCX Header`** - Μια κεφαλίδα PCX έχει μήκος 128 byte. Περιέχει ένα αναγνωριστικό, έναν αριθμό έκδοσης, διαστάσεις εικόνας, 16 χρώματα παλέτας, αριθμητικά επίπεδα χρώματος και βάθος bit κάθε επιπέδου και μια τιμή για τη μέθοδο συμπίεσης.

Το PCX Header είναι όπως φαίνεται παρακάτω με αναφορά από την Εγκυκλοπαίδεια μορφών αρχείων γραφικών (2η έκδοση).
```
typedef struct _PcxHeader
{
  BYTE	Identifier;        /* PCX Id Number (Always 0x0A) */
  BYTE	Version;           /* Version Number */
  BYTE	Encoding;          /* Encoding Format */
  BYTE	BitsPerPixel;      /* Bits per Pixel */
  WORD	XStart;            /* Left of image */
  WORD	YStart;            /* Top of Image */
  WORD	XEnd;              /* Right of Image
  WORD	YEnd;              /* Bottom of image */
  WORD	HorzRes;           /* Horizontal Resolution */
  WORD	VertRes;           /* Vertical Resolution */
  BYTE	Palette[48];       /* 16-Color EGA Palette */
  BYTE	Reserved1;         /* Reserved (Always 0) */
  BYTE	NumBitPlanes;      /* Number of Bit Planes */
  WORD	BytesPerLine;      /* Bytes per Scan-line */
  WORD	PaletteType;       /* Palette Type */
  WORD	HorzScreenSize;    /* Horizontal Screen Size */
  WORD	VertScreenSize;    /* Vertical Screen Size */
  BYTE	Reserved2[54];     /* Reserved (Always 0) */
} PCXHEAD;
```

**`Δεδομένα εικόνας`** - Τα δεδομένα εικόνας PCX ακολουθούν αμέσως μετά την κεφαλίδα. Τα δεδομένα εικόνας μπορεί να συμπιεστούν ανάλογα με τη ρύθμιση πεδίου στην κεφαλίδα. Η αποθήκευση δεδομένων στο αρχείο PCX εξαρτάται από τον αριθμό των καθορισμένων επιπέδων χρώματος. Τα δεδομένα εικόνας είναι οργανωμένα σε σειρές. Σε περίπτωση πολλαπλών επιπέδων, αυτά αποθηκεύονται σε επίπεδο εντός σειράς σε διαδοχική διάταξη κόκκινου, πράσινου και μπλε δεδομένων. Αυτό το μοτίβο επαναλαμβάνεται για κάθε γραμμή στο επίπεδο.

## βιβλιογραφικές αναφορές

* [PCX - By Wikipedia](https://en.wikipedia.org/wiki/PCX)

