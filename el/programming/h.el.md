{
  "date" : "2019-10-11",
  "keywords" :[ "h", ".h", "τι είναι το αρχείο ah", "πώς να ανοίξετε το αρχείο h", "επέκταση", "αρχείο", "h αρχείο", "h μορφή αρχείου", "h επέκταση αρχείου", "Παράδειγμα αρχείου H"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"H - Μορφή αρχείου κεφαλίδας C/C++",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου H και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχείο H.",
  "linktitle" : "H",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-07"
}

## Τι είναι ένα αρχείο H;

Ένα αρχείο που αποθηκεύεται με **h επέκταση αρχείου** είναι ένα αρχείο κεφαλίδας που χρησιμοποιείται σε αρχεία C/C++ για να περιλαμβάνει τη δήλωση μεταβλητών, σταθερών και συναρτήσεων. Αυτά αναφέρονται από τα αρχεία υλοποίησης [C++](/el/programming/cpp/) που περιέχουν την πραγματική υλοποίηση αυτών των λειτουργιών. Ένα αρχείο κεφαλίδας .h μπορεί επίσης να περιλαμβάνει πρόσθετες πληροφορίες, όπως ορισμούς μακροεντολών. Αυτά τα αρχεία κεφαλίδας αναφέρονται στα αρχεία C/C++ χρησιμοποιώντας την οδηγία «#include».

Ένα νέο έργο C++ περιέχει συνήθως ένα ειδικό αρχείο κεφαλίδας με το όνομα **stdafx.h** αρχείο που είναι το σημείο εκκίνησης για όλες τις αλυσίδες μεταγλώττισης και όλα τα αρχεία κεφαλίδας μπορούν να συμπεριληφθούν σε αυτό το μεμονωμένο αρχείο. Ένα αρχείο .h μπορεί να ανοίξει με οποιοδήποτε πρόγραμμα επεξεργασίας κειμένου, Eclipse IDE, Microsoft Visual Studio IDE, Borland C++ compiler και πολλές άλλες εφαρμογές.

## Μορφή αρχείου .H

Ένα αρχείο .h είναι αρχείο απλού κειμένου που έχει τους δικούς του κανόνες για τον ορισμό της σύνταξης. Τα αρχεία κεφαλίδας μπορούν να περιέχουν τις ακόλουθες πληροφορίες.

**`Μεταβλητές`** - Στην περίπτωση Αντικειμενοστρεφούς Προγραμματισμού (OOP), ένα αρχείο κεφαλίδας κλάσης περιέχει ορισμούς όλων των μεταβλητών επιπέδου κλάσης που είναι προσβάσιμες στα αρχεία πηγαίου κώδικα υλοποίησης
**`Δήλωση μεθόδων`** - Όλες οι δηλώσεις μεθόδων περιλαμβάνονται στα αρχεία κεφαλίδας .h για να είναι προσβάσιμες σε πολλαπλά αρχεία υλοποίησης.
**`Ορισμοί μη ενσωματωμένων συναρτήσεων`** - Τα αρχεία κεφαλίδας μπορούν επίσης να περιέχουν ορισμούς μη ενσωματωμένων μεθόδων.
**`Χάρτες μηνυμάτων`** - Ένα αρχείο κεφαλίδας μπορεί επίσης να περιέχει χάρτες μηνυμάτων σε περίπτωση εφαρμογής πηγαίου κώδικα MFC. Σε αυτήν την περίπτωση, οι χάρτες μηνυμάτων συνδέονται με την υλοποίηση λειτουργικότητας που συνδέεται με στοιχεία διεπαφής χρήστη όπως κουμπί, πλαίσιο ελέγχου, κουμπιά επιλογής κ.λπ.


### Φρουροί κεφαλής

Τα αρχεία κεφαλίδας μπορεί να αυξηθούν σε πολύπλοκα σφάλματα όπου πολλές δηλώσεις περιλαμβάνονται στο ίδιο αρχείο ως αποτέλεσμα της προσθήκης άλλων αρχείων κεφαλίδας. Αυτοί οι διπλοί ορισμοί προκαλούν σφάλματα μεταγλωττιστή. Αυτή η προβληματική κατάσταση μπορεί να αποφευχθεί μέσω ενός μηχανισμού που ονομάζεται προστασία κεφαλίδας που είναι οδηγίες συλλογής υπό όρους όπως φαίνεται παρακάτω.

```
#ifndef ANY_UNIQUE_NAME_HERE
#define ANY_UNIQUE_NAME_HERE

// your declarations (and certain types of definitions) here

#endif
```
Με αυτήν την κεφαλίδα, ο προεπεξεργαστής ελέγχει εάν το "ANY_UNIQUE_NAME_HERE" έχει ήδη οριστεί. Εάν η κεφαλίδα περιλαμβάνεται επανειλημμένα στο ίδιο αρχείο, τα περιεχόμενα της κεφαλίδας θα αγνοηθούν.

## Παράδειγμα αρχείου H

```
// sample.h
#pragma once
#include <vector> // #include directive
#include <string>

namespace N  // namespace declaration
{
    inline namespace P
    {
        //...
}

    enum class colors : short { red, blue, purple, azure };

    const double PI = 3.14;  // const and constexpr definitions
    constexpr int MeaningOfLife{ 42 };
    constexpr int get_meaning()
    {
        static_assert(MeaningOfLife == 42, "unexpected!"); // static_assert
        return MeaningOfLife;
}
    using vstr = std::vector<int>;  // type alias
    extern double d; // extern variable

#define LOG   // macro definition

#ifdef LOG   // conditional compilation directive
    void print_to_log();
#endif

    class my_class   // regular class definition,
    {                // but no non-inline function definitions

        friend class other_class;
    public:
        void do_something();   // definition in my_class.cpp
        inline void put_value(int i) { vals.push_back(i); } // inline OK

    private:
        vstr vals;
        int i;
    };

    struct RGB
    {
        short r{ 0 };  // member initialization
        short g{ 0 };
        short b{ 0 };
    };

    template <typename T>  // template definition
    class value_store
    {
    public:
        value_store<T>() = default;
        void write_value(T val)
        {
            //... function definition OK in template
    }
    private:
        std::vector<T> vals;
    };

    template <typename T>  // template declaration
    class value_widget;
}
```

## βιβλιογραφικές αναφορές

* [Αρχεία κεφαλίδας - Microsoft](https://docs.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)

