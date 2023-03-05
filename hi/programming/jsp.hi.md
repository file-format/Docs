{
  "date" : "2021-04-21",
  "keywords": [ "what is a jsp file", "tutorials on jsp","jsp means","jsp", "jsp files", "extension", "format", "jsp tutorial", ".jsp", "jsp example","jsp file extension" ,"how to open a jsp file"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"जेएसपी - जावा सर्वर पेज फाइल फॉर्मेट",
  "description":"जेएसपी उदाहरण और एपीआई के साथ जेएसपी फ़ाइल प्रारूप के बारे में जानें जो जेएसपी फाइलें बना और खोल सकते हैं।",
  "linktitle" : "JSP",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-07"
}

## जेएसपी फाइल क्या है?
जेएसपी फाइलों को आपके जावा वेब अनुप्रयोगों के लिए गतिशील, डेटा-संचालित पृष्ठों के रूप में महसूस किया जाता है। जेएसपी का मतलब जावा सर्वर पेज है; सर्वलेट के विस्तार के रूप में महसूस किया जा सकता है क्योंकि यह अभिव्यक्ति भाषा जैसे सर्वलेट की तुलना में अधिक कार्यक्षमता को सक्षम बनाता है। जेएसपी और सर्वलेट पुराने जावा वेब अनुप्रयोगों में एक साथ एक ही काम करते हैं। प्रोग्रामिंग परिप्रेक्ष्य से, उनके बीच सबसे स्पष्ट अंतर यह है कि सर्वलेट के साथ आप जावा प्रोग्राम लिखते हैं और फिर उस कोड में स्थिर मार्कअप (जैसे एचटीएमएल) एम्बेड करते हैं, जबकि जेएसपी क्लाइंट-साइड स्क्रिप्ट या मार्कअप से शुरू होता है, फिर जेएसपी टैग को एम्बेड करता है अपने पेज को जावा बैकएंड से कनेक्ट करें।

## जेएसपी फ़ाइल प्रारूप
**Jsp फ़ाइल एक्सटेंशन** के साथ सहेजी गई फ़ाइल में निम्न अनुभाग सूचीबद्ध क्रम में होते हैं:

1. प्रारंभिक टिप्पणियाँ
2. JSP पृष्ठ निर्देश(निर्देशों)
3. वैकल्पिक टैग लाइब्रेरी निर्देश
4. वैकल्पिक जेएसपी घोषणा (ओं)
5. एचटीएमएल और जेएसपी कोड

### प्रारंभिक टिप्पणियाँ
एक JSP फ़ाइल या फ़्रैगमेंट फ़ाइल सर्वर साइड शैली की टिप्पणी से शुरू होती है:

```
<%-- 

  - Author(s):
  - Date:
  - Copyright Notice:
  - @(#)
  - Description: 

  --%>
```
उपरोक्त टिप्पणी केवल सर्वर साइड पर दिखाई देती है क्योंकि ब्राउजर में पेज को रेंडर करते समय इसे हटा दिया जाता है। टिप्पणी में लेखक(कों) के बारे में जानकारी, दिनांक, और संशोधन की कॉपीराइट सूचना, एक पहचानकर्ता और डेवलपर्स के लिए जेएसपी पृष्ठ के बारे में विवरण हो सकता है। वर्णों के संयोजन "@(#)" को कुछ कार्यक्रमों द्वारा एक पहचानकर्ता की शुरुआत के संकेत के रूप में पहचाना जाता है।

### JSP पृष्ठ निर्देश(निर्देशों)
JSP पृष्ठ निर्देश अनुवाद के समय JSPF पृष्ठ से संबद्ध विशेषताओं को परिभाषित करता है। जेएसपी विनिर्देश एक पृष्ठ में कितने जेएसपी पृष्ठ निर्देश लिखे जा सकते हैं, इस पर कोई बाधा नहीं डालता है। निम्न उदाहरण देखें:

```
<%@ page session="false" %>
<%@ page import="java.util.*" %>
<%@ page errorPage="/common/errorPage.jsp" %>
```
यदि कोई पृष्ठ निर्देश, JSP पृष्ठ की सामान्य चौड़ाई से अधिक है, तो निर्देश कई पंक्तियों में टूट जाता है:

```
<%@ page    session="false" 

            import="java.util.*"
            errorPage="/common/errorPage.jsp" 

%>
```
### वैकल्पिक टैग लाइब्रेरी निर्देश
जेएसपी पेज में, एक टैग लाइब्रेरी निर्देश कस्टम टैग लाइब्रेरी घोषित करता है। एक पंक्ति में एक छोटा निर्देश घोषित किया जा सकता है। जेएसपी पेज के शरीर के भीतर एक ही स्थान पर एकाधिक टैग लाइब्रेरी निर्देश एक साथ ढेर किए गए हैं:

```
<%@ taglib uri="URI1" prefix="tagPrefix1" %>
<%@ taglib uri="URI2" prefix="tagPrefix2" %>
...
```
### वैकल्पिक जेएसपी घोषणा (ओं)
  


JSPF फ़ाइल में घोषित विधियाँ और चर JSP घोषणाओं में मौजूद होने चाहिए। ये विधियाँ और चर जावा प्रोग्रामिंग भाषा में घोषणाओं के समान हैं, और इसीलिए प्रासंगिक कोड सम्मेलनों का पालन किया जाना चाहिए। घोषणाएं आमतौर पर एक <%! ... %> जेएसपी घोषणा ब्लॉक, जेएसपी पृष्ठ के शरीर के एक क्षेत्र के भीतर घोषणाओं को केंद्रीकृत करने के लिए। निम्नलिखित उदाहरण देखें:

#### असमान घोषणा ब्लॉक:

```
<%! private int hitCount; %>
    <%! private Date today; %>
    ...
    <%! public int getHitCount() {
            return hitCount;
    }
    %>
```
#### पसंदीदा घोषणा ब्लॉक:
```
<%! 

        private int hitCount;
        private Date today; 

    


        public int getHitCount() {
            return hitCount;
    }
    %>
```
### एचटीएमएल और जेएसपी कोड
JSP पेज के इस सेक्शन में JSP पेज की HTML बॉडी और JSPF कोड, ऐसे JSP एक्सप्रेशंस, स्क्रिप्टलेट्स और JavaBeans निर्देश होते हैं।

## JSP पृष्ठ का जीवनचक्र

चरणवार JSP पृष्ठ प्रवाह यहाँ दिया गया है:

- जेएसपी पेज का अनुवाद
- जेएसपी पेज का संकलन
- क्लासलोडिंग (क्लासलोडर क्लास फ़ाइल लोड करता है)
- तात्कालिकता (उत्पन्न सर्वलेट का ऑब्जेक्ट बनाया गया है)।
- प्रारंभ (कंटेनर jspInit () विधि को आमंत्रित करता है)।
- अनुरोध प्रसंस्करण (कंटेनर _jspService () विधि को आमंत्रित करता है)।
- नष्ट (कंटेनर jspDestroy () विधि को आमंत्रित करता है)।

{{< figure src="../jsp.jpg" alt="जेएसपी फ़ाइल प्रारूप" >}}

## जेएसपी उदाहरण

जेएसपी प्रौद्योगिकियों के बारे में सीखना आजकल बहुत आसान है क्योंकि इंटरनेट पर बहुत सारे जेएसपी ट्यूटोरियल उपलब्ध हैं। निम्न JSP उदाहरण डेटाबेस में उपयुक्त रिकॉर्ड को अपडेट करके ऑर्डर को प्रोसेस करने के लिए है।
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


 


## संदर्भ

* [जावासर्वर पेजों के लिए कोड कन्वेंशन](https://www.oracle.com/technical-resources/articles/javase/code-convention.html)
* [जेएसपी ट्यूटोरियल](https://www.javatpoint.com/jsp-tutorial)

