{
  "date" : "2021-04-21",
  "keywords": [ "what is a jsp file", "tutorials on jsp","jsp means","jsp", "jsp files", "extension", "format", "jsp tutorial", ".jsp", "jsp example","jsp file extension" ,"how to open a jsp file"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JSP - Μορφή αρχείου σελίδων διακομιστή Java",
  "description":"Μάθετε σχετικά με τη μορφή αρχείου JSP με παράδειγμα JSP και API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία JSP.",
  "linktitle" : "JSP",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-07"
}

## Τι είναι ένα αρχείο JSP;
Τα αρχεία JSP υλοποιούνται ως οι δυναμικές σελίδες που βασίζονται σε δεδομένα για τις εφαρμογές web Java σας. Το JSP σημαίνει Σελίδες διακομιστή Java. μπορεί να υλοποιηθεί ως επέκταση του Servlet επειδή επιτρέπει περισσότερη λειτουργικότητα από το servlet όπως η γλώσσα έκφρασης. Το JSP και το Servlet κάνουν την ίδια δουλειά μαζί σε παλαιότερες διαδικτυακές εφαρμογές Java. Από την προοπτική προγραμματισμού, η πιο σαφής διαφορά μεταξύ τους είναι ότι με τους servlet γράφετε πρόγραμμα Java και στη συνέχεια ενσωματώνετε στατική σήμανση (όπως η HTML) σε αυτόν τον κώδικα, ενώ το JSP ξεκινά με το σενάριο ή τη σήμανση από την πλευρά του πελάτη και στη συνέχεια ενσωματώνετε ετικέτες JSP σε συνδέστε τη σελίδα σας στο backend Java.

## Μορφή αρχείου JSP
Ένα αρχείο που είναι αποθηκευμένο με **επέκταση αρχείου jsp** περιέχει τις ακόλουθες ενότητες με τη σειρά που παρατίθενται:

1. Εναρκτήρια σχόλια
2. Οδηγίες σελίδων JSP
3. Προαιρετική(ες) οδηγία(εις) βιβλιοθήκης ετικετών
4. Προαιρετική(εις) δήλωση(εις) JSP
5. Κώδικας HTML και JSP

### Άνοιγμα σχολίων
Ένα αρχείο JSP ή ένα αρχείο θραύσματος ξεκινά με ένα σχόλιο στυλ διακομιστή:

```
<%-- 

  - Author(s):
  - Date:
  - Copyright Notice:
  - @(#)
  - Description: 

  --%>
```
Το παραπάνω σχόλιο εμφανίζεται μόνο στην πλευρά του διακομιστή επειδή αφαιρείται κατά την απόδοση της σελίδας στο πρόγραμμα περιήγησης. Το σχόλιο μπορεί να περιέχει τις πληροφορίες σχετικά με τους δημιουργούς, την ημερομηνία και τη σημείωση πνευματικών δικαιωμάτων της αναθεώρησης, ένα αναγνωριστικό και μια περιγραφή σχετικά με τη σελίδα JSP για προγραμματιστές. Ο συνδυασμός των χαρακτήρων "@(#)" αναγνωρίζεται από ορισμένα προγράμματα ως ένδειξη έναρξης ενός αναγνωριστικού.

### Οδηγία(-ές) Σελίδας JSP
Μια οδηγία σελίδας JSP ορίζει χαρακτηριστικά που σχετίζονται με τη σελίδα JSPF κατά τη στιγμή της μετάφρασης. Η προδιαγραφή JSP δεν επιβάλλει περιορισμούς στο πόσες οδηγίες σελίδων JSP μπορούν να γραφτούν σε μία μόνο σελίδα. Δείτε το παρακάτω παράδειγμα:

```
<%@ page session="false" %>
<%@ page import="java.util.*" %>
<%@ page errorPage="/common/errorPage.jsp" %>
```
Εάν μια οδηγία σελίδας υπερβαίνει το κανονικό πλάτος μιας σελίδας JSP, η οδηγία χωρίζεται σε πολλές γραμμές:

```
<%@ page    session="false" 

            import="java.util.*"
            errorPage="/common/errorPage.jsp" 

%>
```
### Οδηγία(-ές) για τη βιβλιοθήκη προαιρετικών ετικετών
Στη σελίδα JSP, μια οδηγία βιβλιοθήκης ετικετών δηλώνει βιβλιοθήκες προσαρμοσμένων ετικετών. Μια σύντομη οδηγία μπορεί να δηλωθεί σε μία μόνο γραμμή. Πολλαπλές οδηγίες βιβλιοθήκης ετικετών στοιβάζονται μαζί στην ίδια θέση μέσα στο σώμα της σελίδας JSP:

```
<%@ taglib uri="URI1" prefix="tagPrefix1" %>
<%@ taglib uri="URI2" prefix="tagPrefix2" %>
...
```
### Προαιρετική(εις) δήλωση(εις) JSP
  


Οι μέθοδοι και οι μεταβλητές που δηλώνονται σε ένα αρχείο JSPF θα πρέπει να υπάρχουν σε δηλώσεις JSP. Αυτές οι μέθοδοι και μεταβλητές είναι παρόμοιες με τις δηλώσεις στη γλώσσα προγραμματισμού Java, και γι' αυτό θα πρέπει να ακολουθούνται οι σχετικές συμβάσεις κώδικα. Οι δηλώσεις συνήθως γράφονται σε ένα μόνο < %! ... %> Μπλοκ δηλώσεων JSP, για να συγκεντρωθούν οι δηλώσεις σε μία περιοχή του σώματος της σελίδας JSP. δείτε τα ακόλουθα παραδείγματα:

#### Διαφορετικά μπλοκ δηλώσεων:

```
<%! private int hitCount; %>
    <%! private Date today; %>
    ...
    <%! public int getHitCount() {
            return hitCount;
    }
    %>
```
#### Προτιμώμενο μπλοκ δηλώσεων:
```
<%! 

        private int hitCount;
        private Date today; 

    


        public int getHitCount() {
            return hitCount;
    }
    %>
```
### Κώδικας HTML και JSP
Αυτή η ενότητα μιας σελίδας JSP περιέχει το σώμα HTML της σελίδας JSP και τον κώδικα JSPF, όπως εκφράσεις JSP, scriptlet και οδηγίες JavaBeans.

## Κύκλος ζωής μιας Σελίδας JSP

Η ροή σελίδας JSP κατά φάση δίνεται εδώ:

- Μετάφραση της Σελίδας JSP
- Σύνταξη Σελίδας JSP
- Classloading (το classloader φορτώνει το αρχείο κλάσης)
- Instantiation (Δημιουργείται αντικείμενο του Generated Servlet).
- Αρχικοποίηση (το κοντέινερ καλεί τη μέθοδο jspInit()).
- Επεξεργασία αιτήματος (το κοντέινερ καλεί τη μέθοδο _jspService()).
- Destroy ( το κοντέινερ καλεί τη μέθοδο jspDestroy()).

{{< figure src="../jsp.jpg" alt="Μορφή αρχείου JSP" >}}

## Παράδειγμα JSP

Η εκμάθηση για τις τεχνολογίες JSP είναι πολύ εύκολη τώρα στις μέρες μας, επειδή πολλά μαθήματα JSP είναι διαθέσιμα μέσω του Διαδικτύου. Το ακόλουθο παράδειγμα JSP είναι για την επεξεργασία της παραγγελίας, με ενημέρωση των κατάλληλων εγγραφών στη βάση δεδομένων.
```
<html>
<head>
  <title>Order Book</title>
</head>
 

<body>
  <h1>Another E-Bookstore</h1>
  <h2>Thank you for ordering...</h2>
 

  <%
    String[] ids = request.getParameterValues("id");
    if (ids != null) {
  %>
  <%@ page import = "java.sql.*" %>
  <%
      Connection conn = DriverManager.getConnection(
          "jdbc:mysql://localhost:8888/ebookshop", "myuser", "xxxx"); // <== Check!
      // Connection conn =
      //    DriverManager.getConnection("jdbc:odbc:eshopODBC");  // Access
      Statement stmt = conn.createStatement();
      String sqlStr;
      int recordUpdated;
      ResultSet rset;
  %>
      <table border=1 cellpadding=3 cellspacing=0>
        <tr>
          <th>Author</th>
          <th>Title</th>
          <th>Price</th>
          <th>Qty In Stock</th>
        </tr>
  <%
      for (int i = 0; i < ids.length; ++i) {
        // Subtract the QtyAvailable by one
        sqlStr = "UPDATE books SET qty = qty - 1 WHERE id = " + ids[i];
        recordUpdated = stmt.executeUpdate(sqlStr);
        // carry out a query to confirm
        sqlStr = "SELECT * FROM books WHERE id =" + ids[i];
        rset = stmt.executeQuery(sqlStr);
        while (rset.next()) {
  %>
          <tr>
            <td><%= rset.getString("author") %></td>
            <td><%= rset.getString("title") %></td>
            <td>$<%= rset.getInt("price") %></td>
            <td><%= rset.getInt("qty") %></td>
          </tr>
  <%}
        rset.close();
  }
      stmt.close();
      conn.close();
}
  %>
  </table>
  <a href="query.jsp"><h3>BACK</h3></a>
</body>
</html>
```


 


## βιβλιογραφικές αναφορές

* [Συμβάσεις κώδικα για τις σελίδες JavaServer](https://www.oracle.com/technical-resources/articles/javase/code-convention.html)
* [JSP Tutorial](https://www.javatpoint.com/jsp-tutorial)

