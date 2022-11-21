{
  "date" : "2019-10-11",
  "keywords" :[ "ashx", "file", "extension", "file format", "ASHX", "ASP.NET Web Handler File" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASHX File Extension - An ASP.NET Web Handler File",
  "description" :"Μάθετε τι είναι ένα αρχείο ASHX και τα API που μπορούν να δημιουργήσουν και να ανοίξουν αρχεία ASHX.",
  "linktitle" : "ASHX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-10"
}

## Τι είναι ένα αρχείο ASHX;

Ένα αρχείο ASHX είναι μια ιστοσελίδα που χρησιμοποιείται από το ASP.NET HTTP Handler για την εξυπηρέτηση του χρήστη με τις σελίδες που αναφέρονται σε αυτό το αρχείο. Το ASP.NET HTTP Handler επεξεργάζεται την εισερχόμενη αίτηση, παραπέμπει στις σελίδες από το αρχείο .ashx και στέλνει πίσω τη μεταγλωττισμένη σελίδα στο πρόγραμμα περιήγησης του χρήστη. Η μέθοδος επεξεργασίας είναι ως επί το πλείστον παρόμοια με αυτή των αρχείων ASPX με τη διαφορά ότι σε αυτήν την περίπτωση, οι αναφερόμενες σελίδες/έγγραφα υποβάλλονται σε επεξεργασία και αποστέλλονται πίσω.

## Μορφή αρχείου ASHX

Τα αρχεία .ashx αποθηκεύονται σε μορφή αρχείου απλού κειμένου και περιέχουν αναφορές σε άλλες σελίδες ή έγγραφα που αποστέλλονται πίσω στο πρόγραμμα περιήγησης του χρήστη κατόπιν αιτήματος. Αυτά μπορούν να ανοίξουν σε οποιοδήποτε πρόγραμμα επεξεργασίας κειμένου και IDE προγραμματιστή όπως το Xamarin Studio, το Microsoft Notepad, το Notepad++ και πολλά άλλα. Τα αρχεία ASHX είναι χρήσιμα σε περίπτωση που έχετε:
* Δυαδικά αρχεία
* Δυναμικές προβολές εικόνων
* Ιστοσελίδες κρίσιμες για την απόδοση
* Αρχεία XML
* Ελάχιστες ιστοσελίδες

## Πώς να μεταγλωττίσετε δυναμικά ένα αρχείο ASHX;

Τα παρακάτω βήματα μπορούν να χρησιμοποιηθούν για την προσθήκη και τη μεταγλώττιση ενός αρχείου ASHX χρησιμοποιώντας το Microsoft Visual Studio.

* προσθέστε ένα Generic handler - Handler1.ashx στο visual studio
* διαγράψτε το αρχείο cs που δημιουργήθηκε αυτόματα.
* ανοίξτε ξανά το ashx,
** αφαιρέστε CodeBehind="Handler1.ashx.cs"
** προσθέστε τον κωδικό c# παρακάτω

```c++
using System;
using System.Collections.Generic;
using System.Linq;
using System.Web;

public class Handler1 : IHttpHandler
{
    public void ProcessRequest(HttpContext context)
    {
        context.Response.ContentType = "text/plain";
        context.Response.Write("Hello World2");
}

    public bool IsReusable
    {
        get
        {
            return false;
    }
}
}
```
### Παράδειγμα ASHX

Ο ακόλουθος κώδικας ASHX επιστρέφει το αρχείο εικόνας κατόπιν αιτήματος του χρήστη όταν το αρχείο ASHX καλείται στο πρόγραμμα περιήγησης Διαδικτύου.


```C++
<%@ WebHandler Language="C#" Class="QueryStringHandler" %>  


using System;  

using System.Web;  


public class QueryStringHandler : IHttpHandler   

{  

    public void ProcessRequest (HttpContext context)   

    {  

        HttpResponse r = context.Response;  

        r.ContentType = "image/png";  

        string file = context.Request.QueryString["file"];  

        if (file == "Arrow")  

        {  

            r.WriteFile("Arrow.gif");  

        }  

        else  

        {  

            r.WriteFile("Image.gif");  

        }  

    }  


    public bool IsReusable   

    {  

        get  

        {  

            return false;  

        }  

    }  

}  

```

## βιβλιογραφικές αναφορές

* [Συμπλήρωση αρχείου ASHX](https://stackoverflow.com/questions/25510189/how-to-dynamically-compile-a-ashx-file)
 


