{
  "date" : "2021-04-20",
  "keywords": [ "JSPF file", "jspf", "JSPF example", "extension", "format", "jspf tutorial", "jsp fragment", "JSPF file format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"JSPF - تنسيق ملف جزء JSP" ,
  "description":"تعرف على تنسيق ملف JSPF وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات JSPF وفتحها." ,
  "linktitle" : "JSPF",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
} ,
  "lastmod" : "2021-04-21"
}

## ما هو ملف JSPF؟
يسمى الملف بامتداد .jspf جزء JSP ؛ ملف ثابت مضمن في ملف JSP آخر. لا يتم تجميع ملفات JSPF من تلقاء نفسها ، ومع ذلك ، يتم تجميعها جنبًا إلى جنب مع الصفحة التي تم تضمينها فيها. بناء الجملة الخاص به مشابه لرمز Java Server Pages (JSP). يحتوي فقط على جزء من JSP ؛ لم يتم تضمين كل مستند JSP بأكمله.

## تنسيق ملف JSPF
يتم استخدام مصطلح "جزء JSP" بدلاً من ذلك حيث تم تحميل مصطلح "جزء JSP" بشكل زائد في مواصفات JSP 2.0. يمكن لأجزاء JSP استخدام امتدادات .jsp أو .jspf ويجب وضعها إما في ** / WEB-INF / jspf ** أو مع باقي الملفات الثابتة. يجب أن تستخدم أجزاء JSP التي ليست صفحات كاملة الامتداد .jspf ويجب وضعها في ** / WEB-INF / jspf **

### JSP أو JSP Fragment File Organization
يحتوي ملف JSP على الأقسام التالية بالترتيب المذكور:

1. افتتاحيات التعليقات
2. توجيه (تعليمات) صفحة JSP
3. توجيه (توجيهات) اختيارية لمكتبة العلامات
4. إعلان (إعلانات) JSP الاختياري
5. كود HTML و JSP

يبدأ كل من ملف JSP أو JSPF بتعليق على نمط جانب الخادم يسمى ** فتح التعليق **:

```
<%-- 
  - Author(s):
  - Date:
  - Copyright Notice:
  - @(#)
  - Description: 
  --%>
```
يمكن أن يكون هذا التعليق مرئيًا فقط على جانب الخادم لأنه تمت إزالته أثناء عرض صفحة JSP.

## متى يتم استخدام ملف JSP Fragment؟
عندما تتطلب صفحة JSP بنية معينة ولكنها معقدة والتي قد يتم إعادة استخدامها أيضًا في صفحات JSP الأخرى ، فإن إحدى طرق التعامل مع ذلك هي تقسيمها إلى أجزاء ، باستخدام نمط العرض المركب (قسم الأنماط في Java Blueprints). على سبيل المثال ، تحتوي صفحة JSP أحيانًا على التخطيط المنطقي التالي في هيكل العرض الخاص بها:

{{< figure src="../jspf.png" alt="تنسيق ملف JSPF" >}}

في هذه الحالة ، يمكن تحويل صفحة JSP المركبة هذه إلى وحدات نمطية مختلفة ، سيُطلق على كل منها جزء JSP منفصل. يمكن بعد ذلك وضع أجزاء JSP في الأماكن المناسبة في صفحة JSP المركبة. ومن ثم ، يتم استخدام ملف JSPF عند استخدام توجيهات التضمين الثابت لتضمين صفحة لا يتم استدعاؤها من تلقاء نفسها ، يجب وضع الملفات ذات الامتداد .jspf في الدليل / WEB-INF / jspf / لأرشيف تطبيق الويب ( حرب).

## مثال JSPF
```
<%@ include file="/WEB-INF/jspf/header.jspf" %>
...
<%@ include file="/WEB-INF/jspf/menuBar.jspf" %>
...
<jsp:include page="<%= currentBody %>" />
...
<%@ include file="/WEB-INF/jspf/footnote.jspf" %>
...
<%@ include file="/WEB-INF/jspf/footer.jspf" %>
...
```

## مراجع

* [اصطلاحات التعليمات البرمجية لصفحات JavaServer](https://www.oracle.com/technical-resources/articles/javase/code-convention.html)

