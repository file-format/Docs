{
  "date" : "2019-10-11",
  "keywords" :[ "aspx", "αρχείο aspx", "μορφή αρχείου aspx", "τύπος αρχείου aspx", "αρχείο", "τύπος", "τι είναι ένα αρχείο aspx" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Μορφή αρχείου ASPX",
  "description" :"Ο οδηγός μορφής αρχείου σας για να μάθετε τι είναι ένα αρχείο ASPX και API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία ASPX.",
  "linktitle" : "ASPX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2020-09-10"
}

## Τι είναι ένα αρχείο ASPX;

Ένα αρχείο με επέκταση .aspx είναι μια ιστοσελίδα που δημιουργείται χρησιμοποιώντας το πλαίσιο Microsoft ASP.NET που εκτελείται σε διακομιστές ιστού. Το ASPX σημαίνει Active Server Pages Extended και αυτές οι σελίδες εμφανίζονται στο πρόγραμμα περιήγησης web στο τέλος του χρήστη όταν γίνεται πρόσβαση στη διεύθυνση URL. Είναι διάδοχος της τεχνολογίας [ASP](/el/web/asp/), η οποία δημιουργείται επίσης στο τέλος του διακομιστή, αλλά δεν χρησιμοποιεί πλαίσιο .NET. Οι σελίδες ASP.NET ενδέχεται να περιέχουν σενάρια [C#](/el/programming/cs/) ή [VB.NET](/el/programming/vb/) που μεταφράζονται σε HTML από τον διακομιστή ιστού για παρουσίαση στον χρήστη στο πρόγραμμα περιήγησης Ιστού. Οι σελίδες ASPX ονομάζονται επίσης Φόρμες Ιστού .NET. Αυτά μπορούν να ανοίξουν και να δημιουργηθούν με εφαρμογές όπως το Microsoft Visual Studio, το Adobe Dreamweaver, το Notepad++ και οποιοδήποτε πρόγραμμα επεξεργασίας κειμένου.

## Μορφή αρχείου ASPX

Οι φόρμες ιστού ASP.NET βασίζονται στο μοντέλο που βασίζεται σε συμβάντα για αλληλεπιδράσεις με την εφαρμογή Ιστού. Το πρόγραμμα περιήγησης, ως τελικός χρήστης, υποβάλλει μια φόρμα Ιστού στον διακομιστή και ο διακομιστής επιστρέφει μια πλήρη σελίδα σήμανσης ή σελίδα HTML ως απόκριση. Το μοντέλο στοιχείου ASP.NET προσφέρει μοντέλο αντικειμένου για σελίδες ASPX. Αυτό το μοντέλο περιγράφει:

* Αντίστοιχα στην πλευρά του διακομιστή σχεδόν όλων των στοιχείων ή ετικετών HTML, όπως \<form> και \<input> .
* Στοιχεία ελέγχου διακομιστή, τα οποία βοηθούν στην ανάπτυξη πολύπλοκης διεπαφής χρήστη. Για παράδειγμα, το στοιχείο ελέγχου Ημερολόγιο ή το στοιχείο ελέγχου Gridview.

Τα αρχεία ASPX χρησιμοποιούν το μοντέλο ASP.NET **Code Behind** για την κατασκευή αυτών των σελίδων.

### Κωδικός σε σειρά

Δείγμα κώδικα που είναι ενσωματωμένο στη σελίδα ASPX και παρέχει όλες τις λειτουργίες για την υλοποίηση του χρήστη. Ο ακόλουθος κώδικας [C#](/el/programming/cs/) αντιπροσωπεύει ένα δείγμα σελίδας ASP.NET που περιλαμβάνει κώδικα εν σειρά:

```
<%@ Language=C# %>
<HTML>
    <script runat="server" language="C#">
        void MyButton_OnClick(Object sender, EventArgs e)
        {
            MyLabel.Text = MyTextbox.Text.ToString();
    }
    </script>
    <body>
        <form id="MyForm" runat="server">
            <asp:textbox id="MyTextbox" text="Hello World" runat="server"></asp:textbox>
            <asp:button id="MyButton" text="Echo Input" OnClick="MyButton_OnClick" runat="server"></asp:button>
            <asp:label id="MyLabel" runat="server"></asp:label>
        </form>
    </body>
</HTML>
```

### Code-Behind

Ο κώδικας μπορεί να γραφτεί και να αποθηκευτεί σε ξεχωριστά αρχεία κλάσης για καθαρό διαχωρισμό της HTML από τη λογική παρουσίασης. Αυτό καθιστά το επίπεδο παρουσίασης ανεξάρτητο από τον εκτελέσιμο κώδικα. Ακολουθεί ο κώδικας πίσω για παρουσίαση στον χρήστη.

```
<%@ Language="C#" Inherits="MyStuff.MyClass" %>
<HTML>
    <body>
        <form id="MyForm" runat="server">
            <asp:textbox id="MyTextBox" text="Hello World" runat="server"></asp:textbox>
            <asp:button id="MyButton" text="Echo Input" Onclick="MyButton_Click" runat="server"></asp:button>
            <asp:label id="MyLabel" runat="server" />
        </form>
    </body>
</HTML>
```

Η εφαρμογή C# της πραγματικής λογικής για το επίπεδο παρουσίασης είναι η εξής.

```
using System;
using System.Web;
using System.Web.UI;
using System.Web.UI.WebControls;

namespace MyStuff
{
    public class MyClass : Page
    {
        protected System.Web.UI.WebControls.Label MyLabel;
        protected System.Web.UI.WebControls.Button MyButton;
        protected System.Web.UI.WebControls.TextBox MyTextBox;

        public void MyButton_Click(Object sender, EventArgs e)
        {
            MyLabel.Text = MyTextBox.Text.ToString();
    }
}
}
```

## βιβλιογραφικές αναφορές

* [ASP.NET WebApps - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/webapps/welcome-webapps)

