{
  "date": "2023-05-16",
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "description": "DXL ফাইল ফরম্যাট এবং API সম্পর্কে জানুন যেগুলি DTSX ফাইল তৈরি এবং খুলতে পারে।",
  "title": "DXL ফাইল ফরম্যাট - Domino XML ভাষা ফাইল ফরম্যাট",
  "linktitle": "DXL",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-dxl-bn"
    }
  },
  "lastmod": "2023-05-16"
}

## একটি DXL ফাইল কি?

একটি DXL ফাইল হল একটি XML ভিত্তিক ডেটা স্টোরেজ ফাইল যা এন্টারপ্রাইজ স্তরের ব্যবসায়িক সহযোগিতা সফ্টওয়্যার, Lotus Domino-এর জন্য তৈরি করা হয়েছে। এটিতে লোটাস ডোমিনো ডাটাবেসের সাথে সম্পর্কিত ডেটা রয়েছে যেমন স্কিমা, ডিজাইন উপাদান, দৃশ্য, ফর্ম, নথি এবং ডাটাবেস ডেটা নিজেই। [XML](/web/xml/) হল একটি সার্বজনীন ফাইল বিন্যাস যা যেকোনো প্রোগ্রামিং ভাষায় লেখা সফ্টওয়্যার অ্যাপ্লিকেশন দ্বারা পড়া যায়। এটি মানুষের পঠনযোগ্য এবং যেকোনো পাঠ্য সম্পাদকের সাথে খোলা যেতে পারে। এজন্য DXL ফাইলগুলি বিনিময়যোগ্য ফাইল বিন্যাসে ডেটা রপ্তানি করার ক্ষমতা প্রদান করে।

## DXL ফাইল ফরম্যাট

DXL ফাইলগুলি XML ফাইল ফরম্যাটে সংরক্ষিত হয় এবং যেকোন প্রোগ্রামিং ভাষায় লিখিত অ্যাপ্লিকেশন দ্বারা সহজেই পাঠযোগ্য। এই ফাইলগুলি XML ট্যাগগুলিতে ডেটা এবং সেটিংস সঞ্চয় করে যা ডেটা শ্রেণীবদ্ধ করার পাশাপাশি এটিকে যথাযথ ক্রমে সাজিয়ে রাখে

### DXL আউটপুট উদাহরণ

নিম্নলিখিত একটি নোট নথির জন্য আউটপুট টেক্সট উদ্ধৃতি আউটপুট.

```
<document form="Customers">
	<noteinfo noteid="942" unid="431A199A6FCC9C0985256A54005041A1" sequence="1">
		<created>
			<datetime dst="true">20010522T103636,81-04</datetime>
		</created>
		<modified>
			<datetime dst="true">20010522T103709,78-04</datetime>
		</modified>
		<revised>
			<datetime dst="true">20010522T103709,77-04</datetime>
		</revised>
		<lastaccessed>
			<datetime dst="true">20010522T103709,77-04</datetime>
		</lastaccessed>
		<addedtofile>
			<datetime dst="true">20010522T103709,77-04</datetime>
		</addedtofile>
	</noteinfo>
	<updatedby>
		<name>CN=Michelle Lally/OU=CAM/O=Acme</name>
	</updatedby>
	<item name="date">
		<datetime>20010601</datetime>
	</item>
	<item name="name">
		<text>Harry Hill</text>
	</item>
	</document>
```

## তথ্যসূত্র

 * [DXL ফরম্যাট - Microsoft](https://help.hcltechsw.com/dom_designer/9.0.1/appdev/H_EXAMPLE_DOCUMENT_NOTEINFO_AND_ITEM_ELEMENTS_XML.html)

