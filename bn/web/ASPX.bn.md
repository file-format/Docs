{
  "date": "2019-10-11",
  "keywords": [
    "aspx",
    "aspx file",
    "aspx file format",
    "aspx file type",
    "file",
    "type",
    "what is an aspx file"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "ASPX ফাইল ফরম্যাট",
  "description": "একটি ASPX ফাইল এবং API যা ASPX ফাইল তৈরি এবং খুলতে পারে তা জানতে আপনার ফাইল বিন্যাস নির্দেশিকা।",
  "linktitle": "ASPX",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-ASPX-bn"
    }
  },
  "lastmod": "2020-09-10"
}

## একটি ASPX ফাইল কি?

.aspx এক্সটেনশন সহ একটি ফাইল হল একটি ওয়েবপেজ যা ওয়েব সার্ভারে চলমান Microsoft ASP.NET ফ্রেমওয়ার্ক ব্যবহার করে তৈরি করা হয়। ASPX এর পূর্ণরূপ হল Active Server Pages Extended এবং এই পেজগুলো ওয়েব ব্রাউজারে ব্যবহারকারীর শেষে প্রদর্শিত হয় যখন URL অ্যাক্সেস করা হয়। এটি [ASP](/web/asp/) প্রযুক্তির উত্তরসূরি যা সার্ভারের শেষে তৈরি হয় কিন্তু .NET ফ্রেমওয়ার্ক ব্যবহার করে না। ASP.NET পৃষ্ঠাগুলিতে [C#](/programming/cs/) বা [VB.NET](/programming/vb/) স্ক্রিপ্ট থাকতে পারে যা ওয়েব সার্ভার দ্বারা ওয়েব ব্রাউজারে ব্যবহারকারীর কাছে উপস্থাপনের জন্য HTML-এ অনুবাদ করা হয়। ASPX পৃষ্ঠাগুলিকে .NET ওয়েব ফর্মও বলা হয়। এগুলি মাইক্রোসফ্ট ভিজ্যুয়াল স্টুডিও, অ্যাডোব ড্রিমওয়েভার, নোটপ্যাড++ এবং যে কোনও পাঠ্য সম্পাদকের মতো অ্যাপ্লিকেশনগুলির সাথে খোলা এবং তৈরি করা যেতে পারে।

## ASPX ফাইল ফরম্যাট

ASP.NET ওয়েব ফর্মগুলি ওয়েব অ্যাপ্লিকেশনের সাথে ইন্টারঅ্যাকশনের জন্য ইভেন্ট-চালিত মডেলের উপর ভিত্তি করে। ব্রাউজার, একটি শেষ ব্যবহারকারী, সার্ভারে একটি ওয়েব ফর্ম জমা দেয় এবং সার্ভার প্রতিক্রিয়া হিসাবে একটি সম্পূর্ণ মার্কআপ পৃষ্ঠা বা HTML পৃষ্ঠা ফেরত দেয়। ASP.NET কম্পোনেন্ট মডেল ASPX পৃষ্ঠাগুলির জন্য অবজেক্ট মডেল অফার করে। এই মডেল বর্ণনা করে:

 * প্রায় সমস্ত HTML উপাদান বা ট্যাগের সার্ভার সাইড কাউন্টারপার্টস, যেমন \<form> এবং \<input> .
 * সার্ভার নিয়ন্ত্রণ, যা জটিল ব্যবহারকারী-ইন্টারফেস বিকাশে সহায়তা করে। উদাহরণস্বরূপ, ক্যালেন্ডার নিয়ন্ত্রণ বা গ্রিডভিউ নিয়ন্ত্রণ।

ASPX ফাইলগুলি এই পৃষ্ঠাগুলি নির্মাণের জন্য ASP.NET **কোড বিহাইন্ড মডেল** ব্যবহার করে।

### ইন-লাইন কোড

নমুনা কোড যা ASPX পৃষ্ঠায় ইনলাইনে এম্বেড করা আছে এবং ব্যবহারকারীর বাস্তবায়নের জন্য সমস্ত কার্যকারিতা প্রদান করে৷ নিম্নলিখিত [C#](/programming/cs/) কোডটি একটি নমুনা ASP.NET পৃষ্ঠার প্রতিনিধিত্ব করে যাতে ইন-লাইন কোড রয়েছে:

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

### কোড-বিহাইন্ড

প্রেজেন্টেশন লজিক থেকে এইচটিএমএল পরিষ্কার আলাদা করার জন্য কোড আলাদা ক্লাস ফাইলে লেখা এবং সংরক্ষণ করা যেতে পারে। এটি উপস্থাপনা স্তরটিকে এক্সিকিউটেবল কোড থেকে স্বাধীন করে তোলে। ব্যবহারকারীর কাছে উপস্থাপনার জন্য নিচের কোড-পিছনে রয়েছে।

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

উপস্থাপনা স্তরের জন্য প্রকৃত যুক্তির C# বাস্তবায়ন নিম্নরূপ।

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

## তথ্যসূত্র

 * [ASP.NET WebApps - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/webapps/welcome-webapps)

