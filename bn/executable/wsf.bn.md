{
  "date": "2021-06-30",
  "keywords": [
    "wsf file",
    "wsf file format",
    "what is a wsf file",
    "file",
    "wsf example",
    "wsf file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Muhammad Umar"
  },
  "draft": "false",
  "toc": true,
  "description": "WSF ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যেগুলি WSF ফাইল তৈরি এবং খুলতে পারে।",
  "title": "WSF - উইন্ডোজ স্ক্রিপ্ট ফাইল",
  "linktitle": "WSF",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-wsf-bn"
    }
  },
  "lastmod": "2021-06-30"
}

## একটি WSF ফাইল কি?
একটি WSF ফাইল হল একটি স্ক্রিপ্ট যা এক্সিকিউটেবল বিভাগের অধীনে পড়ে এবং সাধারণত মাইক্রোসফ্ট উইন্ডোজে ব্যবহৃত হয়। স্ক্রিপ্টটি একাধিক ভাষার মিশ্রণকে সমর্থন করে, এর অর্থ হল WSF ফাইলে JScript, VBScript এবং ঐচ্ছিকভাবে কিছু XML উপাদান বা অন্যান্য স্ক্রিপ্টিং ভাষা যেমন Python, Object REXX, Perl, Kixtart এর মিশ্রণ অন্তর্ভুক্ত থাকতে পারে যদি ব্যবহারকারী দ্বারা ইনস্টল করা থাকে। WSF ফাইলগুলি WScript বা CScript এর অনুপস্থিতিতে নিজেদেরকে কার্যকর করে। WSF ফাইলগুলি ত্রুটি বিচ্ছিন্নকরণ এবং ধ্রুবক প্রকাশ করার ক্ষেত্রে উপকারী হতে পারে।

## WSF ফাইল বিন্যাস
WSF ফাইল বিন্যাস আপনার পূর্ববর্তী উইন্ডোজ স্ক্রিপ্ট হোস্ট প্রকল্প থেকে JScript এবং VBScript মিশ্রিত করতে পারে, একটি .wsf ফাইল আপনাকে Windows স্ক্রিপ্ট হোস্টের সাথে সেগুলি ব্যবহার করতে দেয়। একটি WSF স্ক্রিপ্ট ফাংশনগুলির একটি লাইব্রেরি এনক্যাপসুলেট করে যা বিভিন্ন WSF ফাইল দ্বারা ব্যবহার করা যেতে পারে। নীচের উদাহরণটি একটি .wsf ফাইল দেখায় যাতে একটি JScript ফাইল (fso.js) অন্তর্ভুক্ত থাকে এবং একটি VBScript ফাংশন যা অন্য ফাংশনকে কল করে।
```
<job id="IncludeExample">
   <script language="JScript" src="FSO.JS"/>
   <script language="VBScript">
      ' Get the free space for drive C.
      s = GetFreeSpace("c:")
      WScript.Echo s
   <script>
</job>
```
WSF বিন্যাস নিম্নলিখিত অতিরিক্ত বৈশিষ্ট্য সমর্থন করে:
- বিবৃতি অন্তর্ভুক্ত
- একাধিক ইঞ্জিন
- লাইব্রেরি টাইপ করুন
- টুলস
- এক ফাইলে একাধিক কাজ

## WSF ফাইলের সুবিধা
WSF ফাইলগুলি নিম্নলিখিত ক্ষেত্রে উপকারী হতে পারে:

### ত্রুটি বিচ্ছিন্নতা
WSF ফাইলের মডুলার প্রকৃতি একটি স্ক্রিপ্ট রেফারেন্সকে অন্যটির সাথে হস্তক্ষেপ করা থেকে বিরত করতে পারে যা WSF কে ত্রুটিগুলি আলাদা করার জন্য উপযোগী করে তোলে। এখানে একটি মডিউল সহ WSF এর একটি উদাহরণ রয়েছে যা একটি ত্রুটি তৈরি করে এবং একটি করে না:
```
<?xml version="1.0" ?>
 <job id="Partially works">
   <!-- This will not work -->
   <script language="VBScript">
'    <![CDATA[
         WScript.echo 4/0 ' Oh, boy! You cannot divide by zero...
     ]]>
   </script>
   <!-- This will work... definitely... -->
   <script language="VBScript">
     <![CDATA[
         WScript.echo "Hello, Scripters!" & vbNewline & _
                      "Fantastic! It worked!"
'    ]]>
   </script>
 </job>
```
### মিশ্র ভাষা সমর্থন
একটি WSF একাধিক ভাষা সমর্থন করে, আপনার কাছে অন্য স্ক্রিপ্টিং ভাষা থেকে একটি স্ক্রিপ্টিং ভাষা ব্যবহার কোড থাকতে পারে। এটি কীভাবে কাজ করে তার একটি উদাহরণ এখানে রয়েছে:
```
<?xml version="1.0" ?>
<!-- Mixing JScript and VBScript -->
 <job id="SORT-VBScriptWithJScript">
   <script language="JScript">
     function SortVBArray(arrVBArray) {return arrVBArray.toArray().sort();}
   </script>
   <script language="VBScript">
'    <![CDATA[
     '** Fastest sort: call the Jscript sort from VBScript
     myData = "a,b,c,1,2,3,X,Y,Z,p,d,q"
     wscript.echo "Original List of values: " & vbTab & myData
     starttime = timer()
     sortedArray = SortVBArray(split(myData,","))
     endtime=timer()
     jscriptTime = round(endtime-starttime,2)
     wscript.echo "JScript sorted in " & jscriptTime & " seconds: "  & vbTab & sortedArray
'    ]]>
   </script>
 </job>
```
### ধ্রুবক প্রকাশ করা
WSF একটি অবজেক্ট রেফারেন্স বা নিয়ন্ত্রণের সাথে একটি XML র‍্যাপারের বাঁধাইকে সমর্থন করে যাতে আপনি সেগুলি ঘোষণা করার পরিবর্তে সেই বস্তুর ধ্রুবকগুলি ব্যবহার করতে পারেন। নিম্নলিখিত একটি উদাহরণ:
```
<?xml version="1.0" ?>
<!-- WSF Example with Object Reference
Notes for this very formal example:
 CDATA is used to help the XML parser ignore 
 special characters in the content of the script.  
 The CDATA open and close must be masked 
 from VBScript by making them comments.
-->
<package>
 <job id="EnumerateConstantsADO">
  <reference object="ADODB.Recordset" />
  <script language="VBScript">
'  <![CDATA[
    dim title, str, i
    ctecArray = Array("adOpenUnspecified","adOpenForwardOnly", _
                      "adOpenKeyset","adOpenDynamic","adOpenStatic")
    title = "ADO Recordset Values for Constants"
    str = title & vbNewLine & vbNewLine
    str = str & "*CursorTypeEnum Constants*" & vbNewLine
    For i = 0 to ubound(ctecArray)
      str = str & Eval(ctecArray(i)) & vbTab & ctecArray(i) & vbNewLine
    Next
    str = str & vbNewLine
    str = str & "*LockTypeEnum Constants*" & vbNewLine
    ltecArray = Array("adLockUnspecified","adLockReadOnly", _
                      "adLockPessimistic","adLockOptimistic", _
                      "adLockBatchOptimistic")
    For i = 0 to ubound(ltecArray)
      str = str & Eval(ltecArray(i)) & vbTab & ltecArray(i) & vbNewLine
    Next
    MsgBox str, vbInformation, Title
'  ]]>
  </script>
 </job>
</package>
```


## তথ্যসূত্র 

* [উইন্ডোজ ইনস্টলার - উইকিপিডিয়া দ্বারা](https://en.wikipedia.org/wiki/Windows_Installer)



